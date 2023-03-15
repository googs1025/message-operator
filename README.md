## message-operator 简易型集群内消息中心

### 项目思路与设计
设计背景：本项目基于k8s的扩展功能，实现Message的自定义资源，实现一个集群内的消息下发渠道的controller应用。调用方可在cluster中部署与启动相关配置即可使用。
思路：当应用启动后，会启动一个controller，controller会监听所需的资源，并执行相应的业务逻辑(如：消息发送)。

### 项目功能
1. 支持消息人配置的热加载、热更新等功能。
2. 实现deployment、pod与service变更与删除后的消息通知。
3. 提供qq邮箱的发送功能。
