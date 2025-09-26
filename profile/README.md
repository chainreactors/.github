## ChainReactor

**chainreactor** 专注于 **offensive security** 领域.

以统一的设计风格去重构各个细分领域"**allinone**"工具, 去实现以人为核心的红队工具链与工程化实践, 我们将其命名为 **redboot** . 最终计划实现面向 **面向红队** 的 **一体化平台** ,提供一整套完整的 **红队工程基础设施** .

通过达到 **临界质量** 以实现工件之间的 **链式反应**。

## Redboot Roadmap

为了达成我们的终极目标. 我们的蓝图从 ASM 拓展到了 C2 框架+流量控制工件+ASM 框架三个部分. 这三个领域将覆盖攻击模拟流程中的 Pre-Exploit <--> Post-Exploit

目前我们的计划中有三条链式反应的链路, 分别对应了后渗透[IoM](https://chainreactors.github.io/wiki/IoM), 前渗透/信息收集([mapping](https://chainreactors.github.io/wiki/mapping)), 以及打通 IoM 与 mapping 的流量工具[rem](https://chainreactors.github.io/wiki/rem)

### Chain1 [IoM](https://chainreactors.github.io/wiki/IoM)


IoM(`Internal of Malice`) 的定位是下一代 C2 框架, 同样以高度模块化与可拓展性为核心设计理念. 基于这个理念去实现插件化的 OPSEC, 插件化的社区生态, 插件化的一切.

更重要的是, IoM 将结合 C2 与 webshell, 将同一套插件化的基建共享给完全不同的后渗透场景.

IoM 已经发布 v0.0.1, 这个版本离我们最初的 v0.0.1 设计目标还有很多遗憾, 但是为了防止闭门造车, 我们想提前从社区中接收反馈.


已经发布 v0.1.0, 实现了约 sliver 的 80%, cs 的 70%功能, 也有非常多 sliver 与 cs 都没有的功能

目前提供了 IoM 的[设计文档](https://chainreactors.github.io/wiki/IoM/design)与[用户手册](https://chainreactors.github.io/wiki/IoM/manual) ,可以在[这里](https://github.com/chainreactors/malice-network)体验到 IoM 的 v0.0.4

### Chain2 [mapping](https://chainreactors.github.io/wiki/mapping)


ASM 是 chainreactor 的初衷, gogo/spray/zombie 之类的工具实际上都是为了这个目标设计的. 通过极高的拓展性与细粒度实现的完全可控的攻击面管理引擎.

现在这个目标已经完成了 v0.0.1, 但因为一些数据源与部署方式的问题, 暂时无法发布.

目前提供了 mapping 的[设计文档](https://chainreactors.github.io/wiki/mapping/design), 可以在这里看到 mapping 作为红队向的协作式攻击面引擎的设计理念.

### Chain3 [rem](https://chainreactors.github.io/wiki/rem)

rem 是全场景的流量/代理工具. 能用来解决绝大多数场景的代理与转发需求, 也用来打通 mapping 与 IoM, 让 mapping 能通过 rem+IoM 接入内网. rem 提供了在传输层, 应用层, 加密层, 混淆层的拓展接口. 可以被轻松修改为自定义特征, 也将是 IoM 在流量端的能力拓展.

目前提供了 rem 的[设计文档](https://chainreactors.github.io/wiki/rem)

---

_目前这三个 thread 都已经完成了 v0.0.1, 将逐步发布._
