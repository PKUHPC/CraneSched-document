## CraneSched 最新动态

[2025/04/08] 发布 v1.1.2，升级编译工具至 GCC 15/Clang 20，新增节点维护/恢复事件、分区账户控制，集成 [Vault](https://developer.hashicorp.com/vault)。

[2025/01/24] 发布 v1.1.0，新增 X11 转发、用户 QoS 限制、多 GID 支持，支持 cgroupv2 和昇腾 NPU，调度算法与事件库优化。

[2024/10/24] 发布 v1.0.0，新增作业监控、插件模块、设备支持，优化调度算法，完善资源与作业管理，支持 IPV6。

# CraneSched 简介 #

**鹤思（CraneSched）**是北京大学高性能计算校级公共平台自主研发的**分布式智能调度系统**，团队在总结高性能公共平台运行近六年的管理和维护经验之后，
从高性能计算任务调度的资源管理、资源查看、作业提交、作业查询和资源隔离等作业调度系统最基本的需求出发，结合智能计算的作业调度场景，
采用C++、go等语言进行开发，完全自主研发的**融合高性能计算和智能计算调度为一体**的**开源**分布式智能调度系统。

CraneSched分为前端和后端，前端主要是用Go开发，后端主要是用C++开发，欢迎开发者一起加入。

**CraneSched 前端开源地址**：[CraneSched-FrontEnd](https://github.com/PKUHPC/CraneSched-FrontEnd)

**CraneSched 后端开源地址**：[CraneSched](https://github.com/PKUHPC/CraneSched )

**CraneSched 文档地址**：[CraneSched Documents](https://pkuhpc.github.io/CraneSched/)

**CraneSched Demo 集群**（试用账号：demo_admin，密码：demo_admin）：[CraneSched-Demo](https://hpc.pku.edu.cn/demo/cranesched)