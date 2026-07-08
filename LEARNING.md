# xtquant 源码学习指南

> 本文件记录 xtquant 项目的学习路径与阅读建议。  
> 学习目标：**先建立整体认知，再按数据流深入核心模块，全程以只读方式理解源码，不修改项目文件。**

---

## 项目定位

xtquant 是**迅投 MiniQMT 量化接口的 Python 封装**，核心提供两条主线：

- **行情数据（xtdata）**：历史/实时 K 线、分时、L2 行情、财务数据等。
- **实盘交易（xttrader）**：报单、撤单、改单、资产/持仓/成交查询等。

核心底层依赖迅投提供的闭源 C++ 扩展 `datacenter.*.pyd`，Python 层负责连接管理、参数封装、类型定义和回调分发。

---

## 第一阶段：建立整体认知（1–2 小时）

### 1. 阅读入口文档

| 文件 | 重点 |
|------|------|
| `README.md` | 项目定位、版权说明、Python 版本兼容、依赖 |
| `doc/xtdata.md` | 行情数据接口的使用方式、函数列表、参数说明 |
| `doc/xttrader.md` | 交易接口的使用方式、回调机制、下单/撤单/查持仓 |

读完应熟悉用户侧 API，例如 `xtdata.get_market_data()`、`xttrader.order_stock()` 等。

### 2. 梳理目录结构

```
xtquant/
├── xtdata.py          ← 行情数据主入口
├── xttrader.py        ← 交易主入口
├── xtconn.py          ← 网络连接管理
├── xtdatacenter.py    ← 数据中心客户端工厂
├── xtconstant.py      ← 常量枚举
├── xttype.py          ← 数据结构定义
├── xtstocktype.py     ← 股票类型常量
├── xttools.py         ← 通用工具函数
├── xtutil.py          ← 辅助工具
├── xtextend.py        ← 扩展功能
├── qmttools/          ← QMT 策略框架相关
├── metatable/         ← 元数据/表结构
├── xtbson/            ← BSON 序列化（兼容多 Python 版本）
├── config/            ← 配置文件、Lua 脚本
└── datacenter.*.pyd   ← 闭源 C++ 核心扩展
```

---

## 第二阶段：按数据流学习核心模块（3–5 小时）

### 1. 连接层：`xtconn.py` + `xtdatacenter.py`

这是整个项目的基础设施，所有行情和交易都依赖它创建的 `client`。

- `xtconn.py`：扫描可用服务地址、创建连接、`connect_any()`。
- `xtdatacenter.py`：调用 `datacenter.IPythonApiClient` 创建 RPC 客户端。

**学习目标**：理解 `client` 对象从何而来，为什么 `xtdata.py` 里大量出现 `client = get_client()`。

### 2. 行情数据：`xtdata.py`

这是项目最大的文件，建议分段阅读：

| 段落 | 内容 |
|------|------|
| 开头常量与配置 | 数据目录、默认参数、连接设置 |
| `connect()` / `get_client()` | 连接管理 |
| `get_market_data()` / `get_market_data_ex()` / `get_market_data3()` | K 线、分时等历史行情 |
| L2 行情函数 | `get_l2_quote()`、`get_l2_order()`、`get_l2_transaction()` |
| 订阅/全推相关 | `subscribe_quote()`、`run()` 回调机制 |
| 财务数据 | `get_financial_data()` 等 |
| 板块/成分股 | `get_stock_list_in_sector()` 等 |

**学习技巧**：
- 从熟悉的函数入手，例如 `get_market_data()`，观察它如何将 Python 参数传给 `client.get_market_data3()`。
- 关注 `_get_market_data_ex_221207` 这类版本适配函数，了解项目如何兼容不同 MiniQMT 版本。

### 3. 交易：`xttrader.py`

重点理解：

- `XtQuantTrader` 类的初始化与连接。
- 回调机制：`set_callback()`、`on_stock_trade()`、`on_order_response()` 等。
- 下单/撤单/改单：`order_stock()`、`cancel_order_stock()`、`withdraw_order_stock()`。
- 查询账户/持仓/资产。

**学习目标**：理解事件驱动模型，交易是异步回调的。

---

## 第三阶段：辅助模块与工具（2–3 小时）

### 1. 类型与常量

| 文件 | 内容 |
|------|------|
| `xtconstant.py` | 委托类型、市场代码、价格类型等枚举 |
| `xttype.py` | `StockAccount`、`XtTrade` 等数据类 |
| `xtstocktype.py` | 股票分类常量 |

这些文件较薄，但对理解接口参数很有帮助。

### 2. 工具函数

- `xttools.py`：通用转换工具。
- `xtutil.py`：辅助函数。
- `xtextend.py`：扩展功能。

### 3. 子模块

- `xtbson/`：BSON 编解码，是与服务端通信的序列化格式。注意按 Python 版本分为 `bson36/` 和 `bson37/` 两套实现。
- `metatable/`：元数据表处理，主要与财务数据、指标字段相关。
- `qmttools/`：QMT 策略框架相关，含 `contextinfo.py`、`stgentry.py` 等。若不做策略框架开发可稍后阅读。

---

## 第四阶段：实践验证（不动源代码）

### 1. Python 内省

查看 `datacenter.IPythonApiClient` 暴露的方法：

```python
import xtquant.datacenter as dc
print(dir(dc.IPythonApiClient))
```

### 2. 打印调用链

写临时脚本调用 `xtdata.get_market_data()`，观察：
- 是否成功连接 MiniQMT。
- 返回的数据结构。
- 日志输出位置与内容。

### 3. 阅读日志配置

- `xtdata.log4cxx`：日志配置文件。
- 运行时日志：通常在当前目录或 `%USERPROFILE%/.xtquant/` 下。

---

## 第五阶段：深入闭源核心（可选）

若前面都已掌握，还想深入：

1. **查看导出符号**：用 `dumpbin /exports` 或 CFF Explorer 查看 `datacenter.*.pyd` 的导出函数。
2. **动态调试**：配合 MiniQMT 运行时，用 x64dbg 或 Visual Studio 附加进程观察调用。
3. **反编译关键函数**：用 Ghidra / IDA 反编译 `get_market_data3` 等函数，但需较强逆向基础。

---

## 推荐学习路线图

```
第1天：README.md + doc/xtdata.md + doc/xttrader.md
        ↓
第2天：xtconn.py → xtdatacenter.py → xtdata.py 前半段
        ↓
第3天：xtdata.py 后半段 + xttrader.py
        ↓
第4天：xtconstant.py + xttype.py + xttools.py + xtutil.py
        ↓
第5天：xtbson/ + metatable/ + qmttools/
        ↓
后续：  跑示例 + 内省 + 按需深入 C 扩展
```

---

## 高效学习技巧

建议边读边画两张图：

1. **行情数据调用链图**  
   `用户调用 xtdata.get_market_data()` → `xtdata.py 封装层` → `client.get_market_data3()` → `datacenter.IPythonApiClient` → `MiniQMT 服务`

2. **交易事件流图**  
   `用户调用 xttrader.order_stock()` → `XtQuantTrader` → `client` → `MiniQMT` → `回调函数 on_xxx()` → `用户策略`

这两张图能帮助你快速建立对整个项目骨架的清晰认知。
