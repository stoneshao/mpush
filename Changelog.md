#### v0.0.6

1. 网关服务增加UDP及组播支持，后续网关部分的TCP部分将逐步淘汰
2. 新增用户打标，修改标签，取消标签功能
3. 全网推送增加按标签过滤，按条件过滤，条件表达式目前支持javascript
4. Service模块代码优化，增加同步启动/停止，超时监控
5. 推送模块增加流控功能, 分为全局流控和广播流控，以及基于Redis实现的实时流控
6. 由于网关采用了UDP，PushClient模块和踢人模块增加UDP支持
7. 线程池代码优化，线程命名调整, 支持配置调整Netty boss和work的线程数
8. 路由模块:客户端定义增加SPI支持, 用户可自定义控制多端在线策略
9. 日志及配置项优化，增加mp.home配置项
10. 心跳检测优化，连接一建立就开始检测心跳，防止客户端握手失败或未握手的情况




#### v0.0.5

1. redis 增加redis3.x集群支持， 配置项不再兼容
2. 绑定用户调整，校验重复绑定，以及未解绑，就绑定的场景
3. 新增client push上行功能, 并支持用户以SPI方式集成自己的Handler
4. 全网推送增加按标签过滤推送用户
5. 增加流量控制，tcp发送缓冲区检测代码优化
6. 修复ACK超时方法调用错误bug，增加ack超时时间设置
7. 解码优化, 不再抛出解码异常，取消循环解码
8. NettyServer 增加IoRate设置，优雅停止流程优化，先关闭main reactor
9. 心跳优化，连接建立后就开始计算心跳
10. sessionId生成器性能优化，采用jdk8 LongAdder
11. Service模块开始使用java8 CompletableFuture
12. SPI模块优化增加@Spi注解，多个实现可以指定顺序
13. Profile 性能分析模块优化，增加性能监控开关配置，加入javassist优化性能
14. zk client 代码优化，修改临时节点重复注册问题，增加DNS ZK Node
15. 脚步修改start-foreground不能加载配置项bug, 修改windows启动命令bug
16. 其他bug fix




#### v0.0.4

1. push client API 调整
2. push 接口增加了全网推送功能
3. 用户下线后路由信息不再删除，而是修改为下线状态
4. 修复ZK Client临时节点断开后，不能恢复注册的bug
5. 其他bug fix

#### v0.0.3

1. 增加了消息ACK功能
2. 修复脚本换行问题
3. bug fix

### v0.0.2

1. 增加多端同时在线攻能
