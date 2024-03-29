

# CraneSched 架构 #

**Cranectld**是调度系统的“大脑”，负责集群节点生命周期的管理、作业队列的调度及管理、节点资源管理及调度，处理来自用户指令的作业提交、修改、查询等请求。

**Craned**是部署在计算节点上的守护进程，主要用来监控节点资源及作业状态，接受用户的各种指令，并将其发送给Cranectld，并向用户传送Cranectld的返回结果。

![architecture](./images/architecture.png)

在设计Craned的时候，综合考量高性能计算和云计算服务的特点与不同，在资源分配的时候，设计了Resouces Manager这个对象，当
- **用户提交高性能计算作业时**，调用Cgroup Manager这个组件，用来为高性能计算服务分配资源，并用Cgroup来隔离作业资源。
- **用户提交云计算作业时**，调用Contain Manager这个组件，基于K8S为云计算作业分配资源并打包APP 容器，并对容器声明周期进行管理。

# CraneSched 应用场景 #
Crane支持高性能计算+云计算的复杂分布式计算场景，结合“东数西算”时代背景，将分布于全国各地的集群通过一个云端联通，Crane通过调度算法将用户的作业提交到最“空闲”的集群上，充分利用各集群资源，减少用户排队时间。

![scenario](./images/scenario.png)
