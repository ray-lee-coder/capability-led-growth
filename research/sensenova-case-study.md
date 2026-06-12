# SenseNova Skill Pack：模型公司为什么开始交付“能力”

SenseNova Skills 值得研究，不是因为它发明了 Skill，而是因为它来自一家模型公司。

模型公司过去主要交付模型、API 和文档。SenseNova Skill Pack 往前走了一步：它把模型
能力组织成用户可以直接调用的办公任务。这个变化看似简单，背后其实改变了产品交付的
对象。用户拿到的不只是模型，也是一套已经设计过的工作方法。

## 我看到了什么

本次审阅使用的是 2026-06-12 的本地样本：
`/Volumes/LILEI/workspace/SenseNova-Skills`。目录中没有 `.git`，因此下面的数量只对应这份
样本，不能代表远端仓库的当前状态。

样本中共有 73 个 `SKILL.md`，其中 47 个位于能力子树。更有意思的不是数量，而是层次：

- `sn-image-base` 这类底层 Skill 封装模型或 API 能力，并不直接面向最终用户；
- `sn-deep-research` 这类工作流 Skill 负责多阶段任务和中间制品；
- `sn-ppt-entry` 这类入口 Skill 根据用户意图选择流程；
- Excel 相关工作流把复杂任务拆给大量子能力，并按需加载；
- 部分 Skill 已经描述结构化返回、时间预期或质量结果。

这不是一堆平铺的 Prompt，更像一套初步的能力架构：底层能力可以复用，上层工作流负责
组合，入口负责路由。

复查命令：

```bash
find /Volumes/LILEI/workspace/SenseNova-Skills -name SKILL.md | wc -l
find /Volumes/LILEI/workspace/SenseNova-Skills -path '*/capabilities/*/SKILL.md' | wc -l
rg -l '^version:' /Volumes/LILEI/workspace/SenseNova-Skills -g SKILL.md | wc -l
find /Volumes/LILEI/workspace/SenseNova-Skills -iname '*test*' -o -iname '*eval*'
```

## 它改变了我的判断

SenseNova 让我更确信，“能力单元”值得继续研究。

模型能力不一定只能通过 API 参数和聊天界面被消费。它也可以被包进一个任务边界中，带着
方法、工具和交付规范一起发布。对用户来说，这比理解底层模型容易得多；对模型公司来说，
它提供了一个展示模型在真实任务中表现的界面。

但这里也存在一个反方向：如果 Skill 足够通用、底层模型可以替换，它可能帮助用户采用
能力，却没有帮助模型公司建立壁垒。

## 仍然缺少的部分

这份样本没有统一的能力级版本字段，也没有看到系统化的测试或评测文件。公开仓库同样
没有提供能力使用到模型采用、付费或留存的归因数据。

目前最清楚的是产品形态：能力可以被组织成分层、路由和组合结构，模型公司也可以用能力包
提供更具体的任务入口。公开仓库能够承担分发和开发者教育，但仅凭 Star 和目录规模，还
看不出真实采用和商业结果。

## 对当前产品的影响

`skill-asset-operations-tool` 暂时不需要变成一个统一的 Skill、MCP、Agent 编辑器。那会
过早假定它们共享同一种产品边界。

更有价值的升级，是先把一个 Skill 当作能力产品来经营：

1. 说清任务边界、依赖、来源和支持环境；
2. 建立质量、成本和风险评测；
3. 把能力本体、运行时适配和增长设计分开；
4. 检查归属和转化机制是否损害结果；
5. 记录后续关系，而不只记录安装与调用。

这条链路无论是否带来增长，都应该留下可复用的认识：什么样的能力边界容易被采用，什么
分发方式保留了关系，哪些承接机制破坏了结果。等这些认识在多个实践中重复出现，再向其他
载体扩展会更有依据。
