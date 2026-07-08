# xtdata.py 函数调用关系梳理

> 本报告由 AST 静态分析生成，只读不修改源码。

## 一、总体统计

- 顶层函数数量：**138**
- 类方法数量：**9**
- 定义总数：**147**

## 二、直接调用 `client.get_market_data3()` 的函数/方法

| 类型 | 函数/方法 | 行号 |
|------|----------|------|
| func | `get_market_data_ori` | 425 |
| func | `get_market_data_ex_ori` | 517 |
| func | `_get_market_data_ex_ori_221207` | 601 |
| func | `_get_market_data_ex_250414` | 668 |
| func | `get_l2_quote` | 913 |
| func | `get_l2_order` | 931 |
| func | `get_l2_transaction` | 948 |

## 三、全部函数与方法清单

| 类型 | 名称 | 起始行 |
|------|------|--------|
| func | `try_except` | 54 |
| func | `connect` | 94 |
| func | `reconnect` | 160 |
| func | `disconnect` | 172 |
| func | `get_client` | 183 |
| func | `hello` | 195 |
| func | `get_data_dir` | 225 |
| func | `get_field_list` | 239 |
| func | `create_array` | 262 |
| func | `_BSON_call_common` | 282 |
| func | `get_stock_list_in_sector` | 288 |
| func | `get_index_weight` | 308 |
| func | `get_financial_data` | 318 |
| func | `get_financial_data_ori` | 391 |
| func | `get_market_data_ori` | 425 |
| func | `get_market_data` | 447 |
| func | `get_market_data_ex_ori` | 517 |
| func | `get_market_data_ex` | 539 |
| func | `_get_market_data_ex_ori_221207` | 601 |
| func | `_get_market_data_ex_221207` | 631 |
| func | `_get_market_data_ex_250414` | 668 |
| func | `_get_data_file_path` | 703 |
| func | `_needconvert_period` | 766 |
| func | `_validate_period` | 773 |
| func | `_get_market_data_ex_tuple_period_ori` | 802 |
| func | `_convert_component_info` | 831 |
| func | `_get_market_data_ex_tuple_period` | 847 |
| func | `get_local_data` | 875 |
| func | `get_l2_quote` | 913 |
| func | `get_l2_order` | 931 |
| func | `get_l2_transaction` | 948 |
| func | `get_divid_factors` | 965 |
| func | `getDividFactors` | 980 |
| func | `get_main_contract` | 992 |
| func | `get_sec_main_contract` | 1045 |
| func | `datetime_to_timetag` | 1100 |
| func | `timetag_to_datetime` | 1106 |
| func | `timetagToDateTime` | 1117 |
| func | `get_trading_dates` | 1124 |
| func | `get_full_tick` | 1138 |
| func | `subscribe_callback_wrapper` | 1152 |
| func | `subscribe_callback_wrapper_1820` | 1165 |
| func | `subscribe_callback_wrapper_convert` | 1181 |
| func | `subscribe_quote` | 1204 |
| func | `subscribe_quote2` | 1222 |
| func | `subscribe_l2thousand` | 1264 |
| func | `subscribe_l2thousand_queue` | 1300 |
| func | `get_l2thousand_queue` | 1373 |
| func | `_get_index_mirror_data` | 1415 |
| func | `get_transactioncount` | 1442 |
| func | `get_fullspeed_orderbook` | 1455 |
| func | `subscribe_whole_quote` | 1468 |
| func | `unsubscribe_quote` | 1501 |
| func | `run` | 1510 |
| func | `create_sector_folder` | 1521 |
| func | `create_sector` | 1537 |
| func | `get_sector_list` | 1553 |
| func | `get_sector_info` | 1561 |
| func | `add_sector` | 1606 |
| func | `remove_stock_from_sector` | 1620 |
| func | `remove_sector` | 1634 |
| func | `reset_sector` | 1646 |
| func | `_get_instrument_detail` | 1660 |
| func | `get_instrument_detail` | 1714 |
| func | `get_instrument_detail_list` | 1835 |
| func | `download_index_weight` | 1852 |
| func | `download_history_contracts` | 1860 |
| func | `_download_history_data_by_metaid` | 1869 |
| func | `_download_history_data` | 1886 |
| func | `download_history_data` | 1892 |
| func | `download_history_data2` | 1933 |
| func | `download_financial_data` | 2022 |
| func | `download_financial_data2` | 2041 |
| func | `get_instrument_type` | 2081 |
| func | `download_sector_data` | 2104 |
| func | `download_holiday_data` | 2111 |
| func | `get_holidays` | 2123 |
| func | `get_market_last_trade_date` | 2132 |
| func | `get_trading_calendar` | 2136 |
| func | `is_stock_type` | 2193 |
| func | `download_cb_data` | 2197 |
| func | `get_cb_info` | 2201 |
| func | `get_option_detail_data` | 2206 |
| func | `get_option_undl_data` | 2301 |
| func | `get_option_list` | 2365 |
| func | `get_his_option_list` | 2442 |
| func | `get_his_option_list_batch` | 2456 |
| func | `get_ipo_info` | 2547 |
| func | `get_markets` | 2579 |
| func | `get_wp_market_list` | 2604 |
| func | `get_his_st_data` | 2612 |
| func | `subscribe_formula` | 2659 |
| func | `get_formula_result` | 2683 |
| func | `bind_formula` | 2733 |
| func | `unsubscribe_formula` | 2743 |
| func | `call_formula` | 2749 |
| func | `reset_market_trading_day_list` | 2778 |
| func | `reset_market_stock_list` | 2809 |
| func | `push_custom_data` | 2840 |
| func | `get_period_list` | 2864 |
| func | `gen_factor_index` | 2884 |
| func | `create_formula` | 2941 |
| func | `import_formula` | 2968 |
| func | `del_formula` | 2982 |
| func | `get_formulas` | 2994 |
| func | `read_feather` | 3001 |
| func | `write_feather` | 3027 |
| method | `QuoteServer.__init__` | 3050 |
| method | `QuoteServer._BSON_call_common` | 3068 |
| method | `QuoteServer.__str__` | 3071 |
| method | `QuoteServer.connect` | 3074 |
| method | `QuoteServer.disconnect` | 3090 |
| method | `QuoteServer.set_key` | 3107 |
| method | `QuoteServer.test_load` | 3133 |
| method | `QuoteServer.get_available_quote_key` | 3149 |
| method | `QuoteServer.get_server_list` | 3167 |
| func | `get_quote_server_config` | 3188 |
| func | `get_quote_server_status` | 3205 |
| func | `show_quote_server_status` | 3229 |
| func | `watch_quote_server_status` | 3249 |
| func | `fetch_quote_server_from_config` | 3267 |
| func | `get_etf_info` | 3324 |
| func | `download_etf_info` | 3380 |
| func | `download_his_st_data` | 3387 |
| func | `get_hk_broker_dict` | 3399 |
| func | `_covert_hk_broke_data` | 3414 |
| func | `get_broker_queue_data` | 3438 |
| func | `watch_xtquant_status` | 3446 |
| func | `get_full_kline` | 3463 |
| func | `generate_index_data` | 3497 |
| func | `download_tabular_data` | 3593 |
| func | `get_trading_contract_list` | 3693 |
| func | `get_trading_period` | 3750 |
| func | `get_kline_trading_period` | 3818 |
| func | `get_all_trading_periods` | 3899 |
| func | `get_all_kline_trading_periods` | 3915 |
| func | `get_authorized_market_list` | 3931 |
| func | `compute_coming_trading_calendar` | 3939 |
| func | `get_tabular_formula` | 3966 |
| func | `bnd_get_conversion_price` | 4039 |
| func | `bnd_get_call_info` | 4049 |
| func | `bnd_get_put_info` | 4059 |
| func | `bnd_get_amount_change` | 4069 |
| func | `get_tabular_data` | 4079 |
| func | `get_order_rank` | 4116 |
| func | `get_current_connect_sub_info` | 4151 |
| func | `get_all_sub_info` | 4160 |

## 四、函数内部调用关系（本模块内）

> 仅列出每个函数/方法体内直接调用的函数名（包括内置函数和本模块函数）。

### `try_except`

**外部/内置调用：**
- `_TRACEBACK_.format_tb`
- `format`
- `func`
- `join`
- `sys.exc_info`

### `connect`

**内部/客户端调用：**
- `_BSON_call_common`
- `hello`

**外部/内置调用：**
- `Exception`
- `_OS_.path.abspath`
- `_OS_.path.join`
- `__client.get_app_dir`
- `__client.get_data_dir`
- `__client.is_connected`
- `__client.shutdown`
- `get`
- `isinstance`
- `server_list.append`
- `xtconn.connect_any`
- `xtconn.scan_available_server_addr`

### `reconnect`

**内部/客户端调用：**
- `connect`

**外部/内置调用：**
- `__client.shutdown`

### `disconnect`

**外部/内置调用：**
- `__client.shutdown`

### `get_client`

**内部/客户端调用：**
- `connect`

**外部/内置调用：**
- `__client.is_connected`

### `hello`

**内部/客户端调用：**
- `client.get_data_dir`
- `client.get_peer_addr`
- `client.get_server_tag`
- `get_client`

**外部/内置调用：**
- `_BSON_.BSON.decode`
- `dt.datetime.now`
- `print`
- `strftime`

### `get_data_dir`

**内部/客户端调用：**
- `get_client`

### `get_field_list`

**外部/内置调用：**
- `_OS_.path.dirname`
- `_OS_.path.join`
- `__meta_field_list.get`
- `eval`
- `get`
- `metadetail.get`
- `metainfo.get`
- `open`
- `read`
- `str`

### `create_array`

**外部/内置调用：**
- `ctypes.POINTER`
- `ctypes.cast`
- `ctypes.pythonapi.PyCapsule_GetPointer`
- `np.dtype`
- `np.ndarray`

### `_BSON_call_common`

**外部/内置调用：**
- `_BSON_.BSON.decode`
- `_BSON_.BSON.encode`
- `interface`

### `get_stock_list_in_sector`

**内部/客户端调用：**
- `client.get_stock_list_in_sector`
- `get_client`

**外部/内置调用：**
- `_TIME_.mktime`
- `_TIME_.strptime`
- `int`
- `isinstance`
- `sector_name.replace`

### `get_index_weight`

**内部/客户端调用：**
- `client.get_weight_in_index`
- `get_client`

### `get_financial_data`

**内部/客户端调用：**
- `client.get_financial_data`
- `get_client`

**外部/内置调用：**
- `_TIME_.localtime`
- `_TIME_.strftime`
- `all_table.keys`
- `all_table_upper.get`
- `conv_date`
- `len`
- `list`
- `math.isnan`
- `names.get`
- `pd.DataFrame`
- `range`
- `req_list.append`
- `table.upper`

### `get_financial_data_ori`

**内部/客户端调用：**
- `client.get_financial_data`
- `get_client`

**外部/内置调用：**
- `all_table.keys`
- `all_table_upper.get`
- `len`
- `list`
- `range`
- `req_list.append`
- `table.upper`

### `get_market_data_ori`

**内部/客户端调用：**
- `client.get_market_data3`
- `get_client`
- `get_data_dir`

**外部/内置调用：**
- `end_time.timestamp`
- `int`
- `isinstance`
- `start_time.timestamp`

### `get_market_data`

**内部/客户端调用：**
- `get_market_data_ori`

**外部/内置调用：**
- `pd.DataFrame`

### `get_market_data_ex_ori`

**内部/客户端调用：**
- `client.get_market_data3`
- `get_client`
- `get_data_dir`

**外部/内置调用：**
- `end_time.timestamp`
- `int`
- `isinstance`
- `start_time.timestamp`

### `get_market_data_ex`

**内部/客户端调用：**
- `_convert_component_info`
- `_get_market_data_ex_ori_221207`
- `_get_market_data_ex_tuple_period`
- `_needconvert_period`
- `_validate_period`
- `get_broker_queue_data`
- `get_field_list`
- `get_market_data_ex_ori`
- `timetag_to_datetime`

**外部/内置调用：**
- `convert_data_list.append`
- `pd.DataFrame`

### `_get_market_data_ex_ori_221207`

**内部/客户端调用：**
- `client.get_market_data3`
- `get_client`
- `get_data_dir`

**外部/内置调用：**
- `end_time.timestamp`
- `int`
- `isinstance`
- `np.frombuffer`
- `pd.DataFrame`
- `start_time.timestamp`

### `_get_market_data_ex_221207`

**内部/客户端调用：**
- `_get_market_data_ex_ori_221207`
- `get_market_data_ex_ori`

**外部/内置调用：**
- `pd.DataFrame`
- `pd.to_datetime`

### `_get_market_data_ex_250414`

**内部/客户端调用：**
- `client.get_market_data3`
- `get_client`
- `get_data_dir`

**外部/内置调用：**
- `pa.ipc.open_stream`
- `pd.to_datetime`
- `read_all`
- `to_pandas`

### `_get_data_file_path`

**内部/客户端调用：**
- `_BSON_call_common`
- `get_client`

**外部/内置调用：**
- `isinstance`
- `path_result.get`

### `_needconvert_period`

**外部/内置调用：**
- `datas.get`

### `_validate_period`

**外部/内置调用：**
- `__STR_PERIODS.get`
- `__TUPLE_PERIODS.get`
- `isinstance`

### `_get_market_data_ex_tuple_period_ori`

**内部/客户端调用：**
- `_get_data_file_path`
- `client.read_local_data`
- `get_client`

**外部/内置调用：**
- `_BSON_.BSON.decode`
- `cdata_list.append`
- `end_time.timestamp`
- `int`
- `isinstance`
- `start_time.timestamp`

### `_convert_component_info`

**内部/客户端调用：**
- `_convert_component_info`

**外部/内置调用：**
- `convert_field_list.get`
- `data.items`
- `isinstance`

### `_get_market_data_ex_tuple_period`

**内部/客户端调用：**
- `_convert_component_info`
- `_get_market_data_ex_tuple_period_ori`
- `get_field_list`

**外部/内置调用：**
- `all_data.items`
- `convert_data_list.append`
- `isinstance`
- `pd.DataFrame`

### `get_local_data`

**内部/客户端调用：**
- `_get_market_data_ex_ori_221207`
- `get_data_dir`
- `get_market_data_ex_ori`
- `timetag_to_datetime`

**外部/内置调用：**
- `pd.DataFrame`

### `get_l2_quote`

**内部/客户端调用：**
- `client.get_market_data3`
- `get_client`

**外部/内置调用：**
- `end_time.timestamp`
- `int`
- `isinstance`
- `start_time.timestamp`

### `get_l2_order`

**内部/客户端调用：**
- `client.get_market_data3`
- `get_client`

**外部/内置调用：**
- `end_time.timestamp`
- `int`
- `isinstance`
- `start_time.timestamp`

### `get_l2_transaction`

**内部/客户端调用：**
- `client.get_market_data3`
- `get_client`

**外部/内置调用：**
- `end_time.timestamp`
- `int`
- `isinstance`
- `start_time.timestamp`

### `get_divid_factors`

**内部/客户端调用：**
- `client.get_divid_factors`
- `get_client`

**外部/内置调用：**
- `pd.DataFrame`

### `getDividFactors`

**内部/客户端调用：**
- `client.get_divid_factors`
- `get_client`

**外部/内置调用：**
- `int`
- `isinstance`
- `len`
- `range`
- `res.items`

### `get_main_contract`

**内部/客户端调用：**
- `client.get_main_contract`
- `datetime_to_timetag`
- `get_client`
- `get_market_data_ex`

**外部/内置调用：**
- `code_market.split`
- `pd.Series`
- `res.ne`
- `res.shift`

### `get_sec_main_contract`

**内部/客户端调用：**
- `client.get_main_contract`
- `datetime_to_timetag`
- `get_client`
- `get_market_data_ex`

**外部/内置调用：**
- `code.endswith`
- `code_market.split`
- `pd.Series`
- `res.ne`
- `res.shift`

### `datetime_to_timetag`

**外部/内置调用：**
- `_TIME_.mktime`
- `_TIME_.strptime`
- `len`

### `timetag_to_datetime`

**内部/客户端调用：**
- `timetagToDateTime`

### `timetagToDateTime`

**外部/内置调用：**
- `_TIME_.localtime`
- `_TIME_.strftime`

### `get_trading_dates`

**内部/客户端调用：**
- `client.get_trading_dates_by_market`
- `get_client`

### `get_full_tick`

**内部/客户端调用：**
- `client.get_full_tick`
- `get_client`

**外部/内置调用：**
- `json.loads`

### `subscribe_callback_wrapper`

**外部/内置调用：**
- `_BSON_.BSON.decode`
- `_TRACEBACK_.print_exc`
- `callback`
- `print`
- `type`

### `subscribe_callback_wrapper_1820`

**内部/客户端调用：**
- `_covert_hk_broke_data`

**外部/内置调用：**
- `_BSON_.BSON.decode`
- `_TRACEBACK_.print_exc`
- `callback`
- `print`
- `type`

### `subscribe_callback_wrapper_convert`

**内部/客户端调用：**
- `_convert_component_info`
- `get_field_list`

**外部/内置调用：**
- `_BSON_.BSON.decode`
- `_TRACEBACK_.print_exc`
- `callback`
- `convert_data_list.append`
- `print`
- `type`

### `subscribe_quote`

**内部/客户端调用：**
- `subscribe_quote2`

### `subscribe_quote2`

**内部/客户端调用：**
- `_needconvert_period`
- `_validate_period`
- `get_client`
- `subscribe_callback_wrapper`
- `subscribe_callback_wrapper_1820`
- `subscribe_callback_wrapper_convert`
- `subscribe_quote`

**外部/内置调用：**
- `_BSON_.BSON.encode`
- `end_time.timestamp`
- `int`
- `isinstance`
- `start_time.timestamp`

### `subscribe_l2thousand`

**内部/客户端调用：**
- `client.subscribe_quote`
- `get_client`
- `subscribe_callback_wrapper`

**外部/内置调用：**
- `_BSON_.BSON.encode`

### `subscribe_l2thousand_queue`

**内部/客户端调用：**
- `client.subscribe_quote`
- `get_client`
- `subscribe_callback_wrapper`

**外部/内置调用：**
- `Exception`
- `_BSON_.BSON.encode`
- `int`
- `isinstance`
- `price.sort`
- `range`

### `get_l2thousand_queue`

**内部/客户端调用：**
- `client.commonControl`
- `get_client`

**外部/内置调用：**
- `_BSON_.BSON.decode`
- `_BSON_.BSON.encode`
- `int`
- `isinstance`
- `price.sort`
- `range`
- `result.get`

### `_get_index_mirror_data`

**内部/客户端调用：**
- `_BSON_call_common`
- `get_client`

### `get_transactioncount`

**内部/客户端调用：**
- `_get_index_mirror_data`

### `get_fullspeed_orderbook`

**内部/客户端调用：**
- `_get_index_mirror_data`

### `subscribe_whole_quote`

**内部/客户端调用：**
- `get_client`
- `subscribe_callback_wrapper`
- `subscribe_whole_quote`

**外部/内置调用：**
- `_BSON_.BSON.encode`

### `unsubscribe_quote`

**内部/客户端调用：**
- `client.unsubscribe_quote`
- `get_client`

### `run`

**内部/客户端调用：**
- `client.is_connected`
- `get_client`

**外部/内置调用：**
- `Exception`
- `_TIME_.sleep`

### `create_sector_folder`

**内部/客户端调用：**
- `client.commonControl`
- `get_client`

**外部/内置调用：**
- `_BSON_.BSON.decode`
- `_BSON_.BSON.encode`
- `result.get`

### `create_sector`

**内部/客户端调用：**
- `client.commonControl`
- `get_client`

**外部/内置调用：**
- `_BSON_.BSON.decode`
- `_BSON_.BSON.encode`
- `result.get`

### `get_sector_list`

**内部/客户端调用：**
- `client.get_sector_list`
- `get_client`

### `get_sector_info`

**内部/客户端调用：**
- `client.get_data_dir`
- `get_client`

**外部/内置调用：**
- `_get_sector_info_from_file`
- `append`
- `category.decode`
- `fe_metadata.get`
- `feather.read_table`
- `file.endswith`
- `name.decode`
- `os.listdir`
- `os.path.join`
- `os.path.splitext`
- `pd.DataFrame`

### `add_sector`

**内部/客户端调用：**
- `client.commonControl`
- `get_client`

**外部/内置调用：**
- `_BSON_.BSON.decode`
- `_BSON_.BSON.encode`
- `result.get`

### `remove_stock_from_sector`

**内部/客户端调用：**
- `client.commonControl`
- `get_client`

**外部/内置调用：**
- `_BSON_.BSON.decode`
- `_BSON_.BSON.encode`
- `result.get`

### `remove_sector`

**内部/客户端调用：**
- `client.commonControl`
- `get_client`

**外部/内置调用：**
- `_BSON_.BSON.decode`
- `_BSON_.BSON.encode`
- `result.get`

### `reset_sector`

**内部/客户端调用：**
- `client.commonControl`
- `get_client`

**外部/内置调用：**
- `_BSON_.BSON.decode`
- `_BSON_.BSON.encode`
- `result.get`

### `_get_instrument_detail`

**内部/客户端调用：**
- `client.get_instrument_detail`
- `get_client`

**外部/内置调用：**
- `ProductCode.endswith`
- `code.find`
- `code.startswith`
- `get`
- `len`
- `ret.get`
- `xtutil.read_from_bson_buffer`

### `get_instrument_detail`

**内部/客户端调用：**
- `_get_instrument_detail`

**外部/内置调用：**
- `convNum2Str`
- `inst.get`
- `inst_ex.get`
- `isinstance`
- `ret.get`
- `str`

### `get_instrument_detail_list`

**内部/客户端调用：**
- `get_instrument_detail`

### `download_index_weight`

**内部/客户端调用：**
- `client.down_index_weight`
- `get_client`

### `download_history_contracts`

**内部/客户端调用：**
- `client.down_history_contracts`
- `get_client`

### `_download_history_data_by_metaid`

**内部/客户端调用：**
- `_BSON_call_common`
- `get_client`

### `_download_history_data`

**内部/客户端调用：**
- `get_client`

**外部/内置调用：**
- `cl.supply_history_data`

### `download_history_data`

**内部/客户端调用：**
- `_download_history_data`
- `_download_history_data_by_metaid`
- `_validate_period`
- `download_history_data2`
- `get_client`

**外部/内置调用：**
- `end_time.strftime`
- `isinstance`
- `start_time.strftime`

### `download_history_data2`

**内部/客户端调用：**
- `_validate_period`
- `client.is_connected`
- `client.stop_supply_history_data2`
- `client.supply_history_data2`
- `get_client`

**外部/内置调用：**
- `Exception`
- `_BSON_.BSON.decode`
- `_BSON_.BSON.encode`
- `_TIME_.sleep`
- `_TRACEBACK_.print_exc`
- `callback`
- `data.get`
- `dt.datetime.fromtimestamp`
- `end_time.strftime`
- `info.get`
- `isinstance`
- `regino_result.items`
- `start_time.strftime`

### `download_financial_data`

**内部/客户端调用：**
- `download_history_data2`
- `get_client`

### `download_financial_data2`

**内部/客户端调用：**
- `client.is_connected`
- `client.supply_history_data`
- `get_client`

**外部/内置调用：**
- `Exception`
- `callback`
- `end_time.strftime`
- `isinstance`
- `len`
- `start_time.strftime`

### `get_instrument_type`

**内部/客户端调用：**
- `client.get_stock_type`
- `get_client`

**外部/内置调用：**
- `len`
- `v_dct.items`

### `download_sector_data`

**内部/客户端调用：**
- `download_history_data2`

### `download_holiday_data`

**内部/客户端调用：**
- `_BSON_call_common`
- `get_client`

### `get_holidays`

**内部/客户端调用：**
- `client.get_holidays`
- `get_client`

**外部/内置调用：**
- `str`

### `get_market_last_trade_date`

**内部/客户端调用：**
- `client.get_market_last_trade_date`
- `get_client`

### `get_trading_calendar`

**内部/客户端调用：**
- `client.get_holidays`
- `client.get_trading_dates_by_market`
- `download_holiday_data`
- `get_client`

**外部/内置调用：**
- `Exception`
- `dt.datetime`
- `dt.datetime.fromtimestamp`
- `dt.datetime.strptime`
- `dt.timedelta`
- `max`
- `res.append`
- `set`
- `tt.strftime`
- `tt.weekday`

### `is_stock_type`

**内部/客户端调用：**
- `client.is_stock_type`
- `get_client`

### `download_cb_data`

**内部/客户端调用：**
- `client.down_cb_data`
- `get_client`

### `get_cb_info`

**内部/客户端调用：**
- `client.get_cb_info`
- `get_client`

**外部/内置调用：**
- `_BSON_.BSON.decode`

### `get_option_detail_data`

**内部/客户端调用：**
- `_get_instrument_detail`

**外部/内置调用：**
- `ProductCode.endswith`
- `convNum2Str`
- `find`
- `get`
- `inst.get`
- `inst_ex.get`
- `isinstance`
- `str`

### `get_option_undl_data`

**内部/客户端调用：**
- `get_instrument_detail`
- `get_option_detail_data`
- `get_stock_list_in_sector`

**外部/内置调用：**
- `append`
- `data.append`
- `get_option_undl`
- `get_option_undl_uni`
- `len`
- `undl_code_ref.endswith`
- `undl_code_ref.split`

### `get_option_list`

**内部/客户端调用：**
- `get_instrument_detail`
- `get_option_detail_data`
- `get_stock_list_in_sector`

**外部/内置调用：**
- `find`
- `inst_data.get`
- `len`
- `min`
- `opt.find`
- `opttype.upper`
- `result.append`
- `undl_code.split`

### `get_his_option_list`

**内部/客户端调用：**
- `get_his_option_list_batch`

**外部/内置调用：**
- `data.get`

### `get_his_option_list_batch`

**内部/客户端调用：**
- `get_instrument_detail`
- `get_market_data_ex`
- `get_trading_dates`
- `timetag_to_datetime`

**外部/内置调用：**
- `data_all.eval`
- `detail.get`
- `drop`
- `dt.datetime.strptime`
- `get`
- `int`
- `len`
- `min`
- `reset_index`
- `str`
- `timestamp`
- `undl_code.rsplit`

### `get_ipo_info`

**内部/客户端调用：**
- `client.get_ipo_info`
- `get_client`

**外部/内置调用：**
- `datadict.get`
- `result.append`

### `get_wp_market_list`

**内部/客户端调用：**
- `_BSON_call_common`
- `get_client`

### `get_his_st_data`

**内部/客户端调用：**
- `get_data_dir`

**外部/内置调用：**
- `_OS_.path.join`
- `append`
- `data.split`
- `f.readlines`
- `len`
- `open`
- `status.append`

### `subscribe_formula`

**内部/客户端调用：**
- `get_client`
- `subscribe_callback_wrapper`

**外部/内置调用：**
- `_BSON_.BSON.decode`
- `_BSON_.BSON.encode`
- `cl.commonControl`
- `cl.subscribeFormula`
- `extend_param.get`
- `int`

### `get_formula_result`

**内部/客户端调用：**
- `get_client`

**外部/内置调用：**
- `Exception`
- `_BSON_.BSON.decode`
- `_BSON_.BSON.encode`
- `cl.commonControl`
- `get`
- `time.sleep`
- `time.time`

### `bind_formula`

**内部/客户端调用：**
- `get_client`
- `subscribe_callback_wrapper`

**外部/内置调用：**
- `_BSON_.BSON.encode`
- `cl.subscribeFormula`

### `unsubscribe_formula`

**内部/客户端调用：**
- `get_client`

**外部/内置调用：**
- `cl.unsubscribeFormula`

### `call_formula`

**内部/客户端调用：**
- `get_client`

**外部/内置调用：**
- `_BSON_.BSON.decode`
- `_BSON_.BSON.encode`
- `cl.commonControl`
- `cl.subscribeFormulaSync`

### `reset_market_trading_day_list`

**内部/客户端调用：**
- `_BSON_call_common`
- `get_client`

### `reset_market_stock_list`

**内部/客户端调用：**
- `_BSON_call_common`
- `get_client`

### `push_custom_data`

**内部/客户端调用：**
- `_BSON_call_common`
- `get_client`

**外部/内置调用：**
- `ans.append`
- `data.items`
- `get_field_name`

### `get_period_list`

**内部/客户端调用：**
- `client.commonControl`
- `get_client`

**外部/内置调用：**
- `_BSON_.BSON.decode`
- `_BSON_.BSON.encode`
- `__TUPLE_PERIODS.items`
- `i.get`
- `len`
- `result.append`
- `result.extend`

### `gen_factor_index`

**内部/客户端调用：**
- `_BSON_call_common`
- `get_client`
- `subscribe_callback_wrapper`

**外部/内置调用：**
- `_TIME_.sleep`
- `cl.registerCommonControlCallback`
- `data.get`
- `print`

### `create_formula`

**内部/客户端调用：**
- `_BSON_call_common`
- `get_client`

**外部/内置调用：**
- `data.update`

### `import_formula`

**内部/客户端调用：**
- `_BSON_call_common`
- `get_client`

### `del_formula`

**内部/客户端调用：**
- `_BSON_call_common`
- `get_client`

### `get_formulas`

**内部/客户端调用：**
- `_BSON_call_common`
- `get_client`

### `read_feather`

**外部/内置调用：**
- `_BSON_.BSON.decode`
- `feather.read_table`
- `metadata.get`
- `table.to_pandas`

### `write_feather`

**外部/内置调用：**
- `Schema.from_pandas`
- `Table.from_pandas`
- `_BSON_.BSON.encode`
- `feather.write_feather`
- `json.dumps`
- `with_metadata`

### `QuoteServer.__init__`

**外部/内置调用：**
- `info.get`

### `QuoteServer._BSON_call_common`

**外部/内置调用：**
- `_BSON_.BSON.decode`
- `_BSON_.BSON.encode`
- `interface`

### `QuoteServer.__str__`

**外部/内置调用：**
- `str`

### `QuoteServer.connect`

**内部/客户端调用：**
- `get_client`

**外部/内置调用：**
- `self._BSON_call_common`

### `QuoteServer.disconnect`

**内部/客户端调用：**
- `get_client`

**外部/内置调用：**
- `self._BSON_call_common`

### `QuoteServer.set_key`

**内部/客户端调用：**
- `get_client`

**外部/内置调用：**
- `self._BSON_call_common`

### `QuoteServer.test_load`

**内部/客户端调用：**
- `get_client`

**外部/内置调用：**
- `self._BSON_call_common`

### `QuoteServer.get_available_quote_key`

**内部/客户端调用：**
- `get_client`

**外部/内置调用：**
- `inst.get`
- `self._BSON_call_common`

### `QuoteServer.get_server_list`

**内部/客户端调用：**
- `get_client`

**外部/内置调用：**
- `QuoteServer`
- `inst.get`
- `self._BSON_call_common`

### `get_quote_server_config`

**内部/客户端调用：**
- `_BSON_call_common`
- `get_client`

**外部/内置调用：**
- `QuoteServer`
- `inst.get`

### `get_quote_server_status`

**内部/客户端调用：**
- `_BSON_call_common`
- `get_client`

**外部/内置调用：**
- `QuoteServer`
- `inst.get`
- `pair.get`

### `show_quote_server_status`

**内部/客户端调用：**
- `_BSON_call_common`
- `get_client`

**外部/内置调用：**
- `data.get`
- `info.get`
- `inst.get`

### `watch_quote_server_status`

**内部/客户端调用：**
- `_BSON_call_common`
- `get_client`
- `subscribe_callback_wrapper`

**外部/内置调用：**
- `cl.registerCommonControlCallback`

### `fetch_quote_server_from_config`

**内部/客户端调用：**
- `_BSON_call_common`
- `get_client`

**外部/内置调用：**
- `ET.parse`
- `QuoteServer`
- `_OS_.path.abspath`
- `_OS_.path.isfile`
- `_OS_.path.join`
- `append`
- `int`
- `qs.get_server_list`
- `qs.info.update`
- `qs.set_key`
- `qs.test_load`
- `qs_infos.values`
- `quoter_server_list.findall`
- `rs.info.get`
- `servers.items`
- `sort`
- `tree.find`
- `x.info.get`

### `get_etf_info`

**内部/客户端调用：**
- `_get_market_data_ex_tuple_period_ori`
- `_validate_period`
- `get_field_list`

**外部/内置调用：**
- `_self_convert_component_info`
- `all_data.items`
- `convert_data.update`
- `convert_field_list.get`
- `data.items`
- `isinstance`
- `stockcode.split`
- `str`

### `download_etf_info`

**内部/客户端调用：**
- `download_history_data`

### `download_his_st_data`

**内部/客户端调用：**
- `_BSON_call_common`
- `get_client`

### `get_hk_broker_dict`

**内部/客户端调用：**
- `_get_market_data_ex_tuple_period_ori`

### `_covert_hk_broke_data`

**内部/客户端调用：**
- `get_hk_broker_dict`

**外部/内置调用：**
- `broke_dict.get`
- `listask.append`
- `listbid.append`

### `get_broker_queue_data`

**内部/客户端调用：**
- `_covert_hk_broke_data`
- `get_market_data_ex_ori`

### `watch_xtquant_status`

**内部/客户端调用：**
- `subscribe_callback_wrapper`

### `get_full_kline`

**内部/客户端调用：**
- `_BSON_call_common`
- `get_client`

**外部/内置调用：**
- `all_data.get`
- `pd.DataFrame`

### `generate_index_data`

**内部/客户端调用：**
- `_BSON_call_common`
- `get_client`

**外部/内置调用：**
- `Exception`
- `float`
- `pbar.update`
- `status.get`
- `time.sleep`
- `tqdm`

### `download_tabular_data`

**内部/客户端调用：**
- `_BSON_call_common`
- `get_client`

**外部/内置调用：**
- `Exception`
- `_TIME_.sleep`
- `end_time.strftime`
- `isinstance`
- `max`
- `pbar.update`
- `start_time.strftime`
- `status.get`
- `tqdm`

### `get_trading_contract_list`

**内部/客户端调用：**
- `get_instrument_detail`
- `get_market_last_trade_date`
- `get_stock_list_in_sector`
- `timetag_to_datetime`

**外部/内置调用：**
- `code.replace`
- `int`
- `len`
- `list`
- `result_set.add`
- `set`
- `stockcode.rsplit`
- `upper`

### `get_trading_period`

**内部/客户端调用：**
- `_BSON_call_common`
- `get_client`

### `get_kline_trading_period`

**内部/客户端调用：**
- `_BSON_call_common`
- `get_client`

### `get_all_trading_periods`

**内部/客户端调用：**
- `_BSON_call_common`
- `get_client`

**外部/内置调用：**
- `result.get`

### `get_all_kline_trading_periods`

**内部/客户端调用：**
- `_BSON_call_common`
- `get_client`

**外部/内置调用：**
- `result.get`

### `get_authorized_market_list`

**内部/客户端调用：**
- `_BSON_call_common`
- `get_client`

**外部/内置调用：**
- `get`

### `compute_coming_trading_calendar`

**内部/客户端调用：**
- `_BSON_call_common`
- `get_client`
- `timetag_to_datetime`

**外部/内置调用：**
- `Exception`
- `de.timestamp`
- `ds.timestamp`
- `dt.datetime`
- `dt.datetime.strptime`
- `get`

### `get_tabular_formula`

**外部/内置调用：**
- `_parse_fields`
- `all_fields.keys`
- `all_fields.values`
- `append`
- `call_formula_batch`
- `enumerate`
- `field.find`
- `field.split`
- `head_fields.extend`
- `list`
- `res.get`
- `rst.get`
- `stock_formula_result.append`
- `stock_formula_result.insert`
- `str`
- `type`
- `xtbson.encode`

### `bnd_get_conversion_price`

**外部/内置调用：**
- `_get_tabular_data`

### `bnd_get_call_info`

**外部/内置调用：**
- `_get_tabular_data`

### `bnd_get_put_info`

**外部/内置调用：**
- `_get_tabular_data`

### `bnd_get_amount_change`

**外部/内置调用：**
- `_get_tabular_data`

### `get_tabular_data`

**内部/客户端调用：**
- `_get_market_data_ex_250414`

**外部/内置调用：**
- `_get_tabular_data`

### `get_order_rank`

**内部/客户端调用：**
- `_BSON_call_common`
- `get_client`

**外部/内置调用：**
- `dt.datetime.strptime`
- `int`
- `isinstance`
- `len`
- `order_time.timestamp`
- `timestamp`

### `get_current_connect_sub_info`

**内部/客户端调用：**
- `_BSON_call_common`
- `get_client`

**外部/内置调用：**
- `get`

### `get_all_sub_info`

**内部/客户端调用：**
- `_BSON_call_common`
- `get_client`

**外部/内置调用：**
- `get`

## 五、关键行情调用链

### 5.1 历史行情数据

```text
get_market_data()
    └─ get_market_data_ex()
        └─ _get_market_data_ex_221207()
            └─ client.get_market_data3()

get_market_data_ex2()
    └─ _get_market_data_ex_221207() 或 _get_market_data_ex_230208()
        └─ client.get_market_data3()
```

### 5.2 L2 行情数据

```text
get_l2_quote()
    └─ client.get_market_data3(period='l2quote', ...)

get_l2_order()
    └─ client.get_market_data3(period='l2order', ...)

get_l2_transaction()
    └─ client.get_market_data3(period='l2transaction', ...)
```

### 5.3 订阅与实时推送

```text
subscribe_quote()
    └─ client.subscribe_whole_quote() / client.subscribe_stock_quote()

run()
    └─ 启动回调线程，处理推送数据
```

### 5.4 财务/板块数据

```text
get_financial_data()
    └─ client.get_financial_data() / 相关 RPC 调用

get_stock_list_in_sector()
    └─ client.get_stock_list_in_sector()
```

## 六、说明

- `client` 实际类型为 `datacenter.IPythonApiClient`，定义在闭源 `.pyd` 扩展中。
- 本报告通过 `ast` 静态分析生成，动态调用（如 `getattr(client, name)`）无法被捕捉。
- 若需更细粒度的调用图，可结合 `pyan` 或 `pydeps` 生成可视化图表。
