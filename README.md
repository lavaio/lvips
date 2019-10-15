# LVIP
Lava Improvement Proposals http://lavatech.org

LVIP：Lava Improvement Proposal（Lava改进提案）

### LVIP-0001：

```
LVIP: 0001
Title: A Proposal for LVIP
Author: 
Status: Draft
Type: Process
Created: 2019-10-12
Superseded-By: None
```

<br />

### 文档说明：

LVIP是Lava（简写LV）的改进提案系统。

上文的LVIP-1是第一例改进提案，用于定义LVIP的设计思想、操作流程以及基本格式规范。因此，本文本身也是LVIP-0001的提议内容。

<br />

### LVIP的定义：

LVIP是以文本文件形式维护和管理的Lava改进提案机制。

LVIP本身是一个设计文档，用于提供与Lava有关的重要信息、提出关于Lava协议的新特性、或者提出关于Lava相关各项流程的改进建议。

LVIP的初衷是希望通过规范的、可追溯的形式管理社区和开发者提出的建议，以及关于这些建议的思考和讨论过程。LVIP将成为Lava的协议升级和社区治理管理机制的重要决策制度。这将符合Lava作为一个开源的、完全去中心化的区块链协议的核心价值观。

<br />

### LVIP的类型：

LVIP可被分为以下两种类型`Type`：

①协议类`Protocol`：涉及Lava协议层面的改进，此类改进往往要求对Lava协议代码作出变动。

②非协议类`Non-Protocol`：涉及协议层面以外的改进，例如关于用户使用，挖矿，以及包括对LVIP机制本身的修改。此外，LVIP也可能不涉及任何新的特性或功能，仅仅对重要问题作出规范性的解释或告知，或者是提供某种面向社区/用户/矿工的准则。总而言之，非协议类可能包含信息告知、管理流程与其他规范性问题，并不影响Lava协议代码的改动升级。

LVIP的提出者和审核者应当谨慎对待分类的准确性，不同的分类有不同的结果导向和处理流程。

<br />

### LVIP的处理流程标准：

![process.png](https://github.com/lavaio/lvips/blob/master/lvip-0001/process.png)
 
一个LVIP的生命周期包含以下状态节点：

①`Draft`：草案阶段。LVIP的提出者可在对特定问题形成初步建议与解决方案时撰写LVIP草案，并与社区讨论。社区讨论不是强制性的，但是我们仍然希望草案的提出者能够至少就草案在技术社区范围内发起讨论，并引收集来自社区的意见，这个过程将极大地收集技术社区的群体智慧，也会成为LVIP评审小组（Panel）进行最终评定赋予LVIP身份的重要参考。

②`Accepted`：正式生效阶段。这意味着该草案已经正式成为LVIP，并被赋予唯一编号。LVIP的编号按照Accept时间顺序赋予。对于较晚的LVIP替代先前的LVIP的情况，两者仍然保留自己的编号，不会发生覆盖。

对于正式生效的LVIP，Lava开发团队将其列入一个公开的`LVIP List`，其详细信息将被长期保留并对外公开展示。

对于协议类LVIP，涉及是否更新Lava协议代码的问题，是最为事关重大的LVIP类型。一个已经生效的协议类LVIP应当引起更大范围的社区讨论，并通过可被书面记录的形式进行协议更新的决策。需要注意的是，协议类LVIP应当要求提出者在`Accepted`阶段前提供较为成型的代码方案，否则不应予以生效。

协议类LVIP的提出者可以在LVIP中约定所希望的决策形式，以决定改协议改动是否应当被实现在最新版本的Lava协议代码中。

<br />

### LVIP的Panel：

Panel（评审小组）是常设的、非营利的机构。

原则上要求Panel小组成员来自于Lava核心开发团队以及活跃的技术社区成员，并且有过参与Lava核心协议代码或其他重要技术工作的经验。

Panel小组成员应当对社区公开联系方式（电子邮箱），以便于社区成员可以就LVIP草案内容与Panel进行提前沟通与讨论。

LVIP草案的提出者应当在准备完成较为成熟的构思、描述以及代码解决方案后，联系Panel小组成员。Panel将以集体形式最终选择Accept或Reject草案，并按规定赋予LVIP编号（如果Accept）。无论Panel最终决定Accept或Reject草案，都应当以书面形式给出理由。因此，Panel既承担日常流程维护的角色，也承担对LVIP内容进行判断和决策的角色。

Panel小组成员以集体讨论和集体决策为核心组织制度维持Panel和LVIP体系的日常运转。Panel小组成员是可流动的，成员之间可以通过讨论协商进行变动安排，但应当要求任何时候Panel小组成员的联系方式都对社区公示（以Mail List形式）。

<br />

### LVIP的文档格式标准：

所有LVIP草案都应当遵循以下格式标准编写LVIP的Header：

```
LVIP: 编号
Title: 名称（能够表达该LVIP的主要内容）
Author: 作者，可以匿名
Status: LVIP状态，包括Draft、Accepted、Replaced
Type: LVIP的类型，包括Protocol、Non-Protocol
Created: 创建时间
Superseded-By: 如果被Replaced，则展示后继者的LVIP编号。
```

此外，作者应在LVIP的正文中描述以下内容：

·提出LVIP的动机，和试图解决的问题。

·与技术社区成员或更广泛社区成员讨论后的意见整理。虽然该内容不是必须的，但我们鼓励LVIP作者就LVIP的构思、内容和解决方案获取更大范围的支持与认同。对于没有经过讨论、没有得到反馈和支持的LVIP草案，Panel可能需要慎重考虑是否Accept该草案。

·对于非协议类LVIP，作者可以直接在正文中详细描述需要表达的内容，如想要给出的informational content。

·对于协议类LVIP，作者应当提出较为成熟的解决方案构想与代码内容。


