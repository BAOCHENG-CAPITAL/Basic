| 表           | 理论                                                         | 个人理解                                                     | tips         |
| ------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------ |
| 交易日历     | 交易日历是首先考虑的 没有时间就没有一切                      | 其实就是个时间序列 但我建议主键设为0，1，2对应20230215,20230216,20230217类似这样 | 需要增量更新 |
| 股票列表     | 其次考虑的是股票列表 每天的股票列表可能都不太一样 但我们现在可以先存一部分 | 股票列表根据交易日而变化 每一天有的股票退市有的上市          | 需要增量更新 |
| 停牌列表     | 有的股票会在某段时间进行调整 一般我交易选择过去1个月没有停牌的股票 也有研报设置2个月 所以我建议把停牌列表单独做成一个表 | 之所以去掉停牌 我的感觉是因为不稳定的系统是没意义的 但这部分其实也可以做策略。。。 | 需要增量更新 |
| 涨停列表     | 有的股票会开盘涨停 我们今天就买入不了了 所有的计算逻辑策略都是为我们实盘服务的 我们当然要剔除这部分股票列表 | 我们交易不了不代表券商交易不了 他们手段还是很多的            | 需要增量更新 |
| st列表       | 有的股票会风险警告，面临退市风险，这部分不交易               | 这块我其实算过 带上st的收益会比去掉st低                      | 需要增量更新 |
| 日线数据     | 也叫量价数据，有大部分因子是根据这些数据构成的               | 至关重要                                                     | 需要增量更新 |
| 每日指标     | 同上                                                         | 至关重要                                                     | 需要增量更新 |
| 个股资金流向 | 同上                                                         | 至关重要                                                     | 需要增量更新 |
|              |                                                              |                                                              |              |
|              |                                                              |                                                              |              |

