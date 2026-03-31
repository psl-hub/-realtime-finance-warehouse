# -realtime-finance-warehouse
项目描述：基于金融信贷业务流程，搭建实时数据处理链路，实现从用户借款申请 → 三级风控审批 → 授信额度计算 → 合同生成与签约全流程实时化。保证审批低延迟、数据一致性、流程可追溯，支撑信贷业务高并发、稳定运行。 掌握实时大数据技术栈：Flink + Kafka 主流实时架构；理解金融风控业务逻辑；能支撑高并发申请场景，实现低延迟审批与授信，提升业务处理效率与用户体验。
项目内容：使用 Maxwell 解析 MySQL binlog，结合 Kafka 实现高并发实时数据接入；基于 FlinkCDC 完成 MySQL 变更数据的合并与过滤，实时写入 HBase 构建 DIM 层数据；通过 Flink 流计算将业务数据状态实时写入 Kafka 对应主题，构建事务实时表；在 DWS 层借助 Redis 缓存维度数据，使用 FlinkSQL 对 Kafka 流数据进行窗口聚合，实时计算用户近 30 天累计申请额等动态特征；将聚合结果写入 Doris，对外提供后端接口，并基于 Sugar 可视化工具搭建监控看板，支持业务指标实时查询与分析。
技术栈：Hadoop,zookeeper,MySQL,Maxwell,Kafka,Hbase,Flink,Maven,Redis,Doris,Sugar
