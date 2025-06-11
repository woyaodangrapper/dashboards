| 名称          | 字段名                                     | 推荐图表类型                                 | 类型分类      | 说明                                                    |
| ----------- | --------------------------------------- | -------------------------------------- | --------- | ----------------------------------------------------- |
| 当前连接数       | `nanomq_connections_count`              | Time series + Stat（当前值突出显示）            | 连接与会话监控   | 连接数随时间变化趋势用折线图，单点状态用Stat面板快速感知连接量                     |
| 最大连接数       | `nanomq_connections_max`                | Stat + Bar gauge                       | 连接与会话监控   | 最大值适合用Stat突出显示，并用Bar gauge反映当前与最大值比例                  |
| 当前CPU使用率    | `nanomq_cpu_usage`                      | Time series + Gauge                    | 系统资源使用情况  | CPU使用率动态趋势用折线图，当前百分比用Gauge表现，易于判断压力程度                 |
| 最大CPU使用率    | `nanomq_cpu_usage_max`                  | Stat + Bar gauge                       | 系统资源使用情况  | 最大值用Stat显著展示，Bar gauge辅助判断当前使用率是否逼近极限                 |
| 当前内存使用      | `nanomq_memory_usage`                   | Time series + Gauge                    | 系统资源使用情况  | 内存使用趋势和当前使用率同时展示，利于定位资源瓶颈                             |
| 最大内存使用      | `nanomq_memory_usage_max`               | Stat + Bar gauge                       | 系统资源使用情况  | 同CPU最大使用率，突出最大值与当前值对比                                 |
| 当前会话数       | `nanomq_sessions_count`                 | Time series + Stat                     | 连接与会话监控   | 会话数量动态趋势与当前状态监控                                       |
| 最大会话数       | `nanomq_sessions_max`                   | Stat + Bar gauge                       | 连接与会话监控   | 最大会话数监控，判断是否达到容量极限                                    |
| 当前订阅者数      | `nanomq_subscribers_count`              | Time series + Stat                     | 主题与订阅管理   | 订阅者数变化趋势及当前状态                                         |
| 最大订阅者数      | `nanomq_subscribers_max`                | Stat + Bar gauge                       | 主题与订阅管理   | 最大订阅者数状态突出显示                                          |
| 当前主题数       | `nanomq_topics_count`                   | Time series + Stat                     | 主题与订阅管理   | 主题数量动态监控                                              |
| 最大主题数       | `nanomq_topics_max`                     | Stat + Bar gauge                       | 主题与订阅管理   | 最大主题数状态监控                                             |
| 接收消息数       | `nanomq_messages_received`              | Time series + Bar chart                | 消息处理状态    | 消息流量趋势折线图，Bar chart可做不同时间段分组对比                        |
| 发送消息数       | `nanomq_messages_sent`                  | Time series + Bar chart                | 消息处理状态    | 同上                                                    |
| 丢弃消息数       | `nanomq_messages_dropped`               | Time series + Stat + Alert list        | 消息处理状态    | 丢弃消息重点监控，Stat显示最新丢弃数，Alert list提醒异常                   |
| 抓取耗时（秒）     | `scrape_duration_seconds`               | Time series + Heatmap                  | 抓取与指标采集性能 | 抓取时长动态趋势折线，Heatmap可展示抓取耗时分布密度                         |
| 抓取样本数       | `scrape_samples_scraped`                | Time series + Histogram                | 抓取与指标采集性能 | 样本数量趋势折线，Histogram展示分布情况                              |
| Relabel后样本数 | `scrape_samples_post_metric_relabeling` | Time series + Histogram                | 抓取与指标采集性能 | 同上                                                    |
| 新增序列数       | `scrape_series_added`                   | Time series + Bar chart                | 抓取与指标采集性能 | 序列数变化趋势与分段对比                                          |
| 服务状态（up）    | `up`                                    | Stat + State timeline + Status history | 服务运行状态    | 单值Stat快速显示状态，State timeline 和 Status history 展示状态变化历史 |
