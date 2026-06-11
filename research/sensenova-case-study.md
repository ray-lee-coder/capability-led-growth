# 个案：SenseNova Skill Pack 与“模型 + 能力包”

## 为什么值得研究

[SenseNova Skills](https://github.com/OpenSenseNova/SenseNova-Skills) 不是单个演示 Skill，
而是模型公司发布的能力组合。它提示模型厂商的产品边界可能从“提供基础模型/API”扩展到
“提供可直接完成任务的能力包”。

## 样本与复查方法

本次审阅对象为 2026-06-12 本地提取样本
`/Volumes/LILEI/workspace/SenseNova-Skills`。该目录不含 `.git`，因此无法声明对应官方
仓库的具体 commit。下列数量只描述该本地样本，不代表仓库历史或当前远端状态。

可复查查询：

```bash
find /Volumes/LILEI/workspace/SenseNova-Skills -name SKILL.md | wc -l
find /Volumes/LILEI/workspace/SenseNova-Skills -path '*/capabilities/*/SKILL.md' | wc -l
rg -l '^version:' /Volumes/LILEI/workspace/SenseNova-Skills -g SKILL.md | wc -l
find /Volumes/LILEI/workspace/SenseNova-Skills -iname '*test*' -o -iname '*eval*'
```

结构审阅发现：

- 共发现 73 个 `SKILL.md`，其中 47 个位于能力子树；
- `sn-image-base` 等底层 Skill 封装模型/API 能力，并明确不直接面向最终用户；
- `sn-deep-research` 等工作流 Skill 编排多阶段任务和中间制品；
- `sn-ppt-entry` 等入口 Skill 根据意图路由到不同流程；
- Excel 相关流程把任务步骤映射到大量子能力，并按需加载；
- 部分 Skill 定义结构化返回、时间预期或质量结果。

这更像一套分层能力架构，而不是一组 Prompt 文件。

## 它证明了什么

| 观察 | 可以支持的判断 |
|---|---|
| 底层能力、工作流、入口路由分层 | 能力包可以被组织成组合与路由架构 |
| 多种办公任务共享模型与工具 | 模型公司可以把模型能力产品化为任务入口 |
| 目录化发布并获得公开关注 | 能力包可作为公开分发与开发者教育载体；关注不等于采用 |

## 它没有证明什么

本地样本中未发现统一的能力级版本字段或系统化测试/评测文件；公开仓库也没有提供：

- 跨运行时的可重复质量；
- 能力级成本、风险和生命周期治理；
- 从能力使用到模型采用或付费的归因数据；
- 与普通文档、Demo、API 示例的增量对照；
- 能力包是否加强模型壁垒，还是让模型更容易被替换。

所以，SenseNova **展示了能力产品化的一种可构造形态**，但不证明该形态具有普遍性，
更不证明 CLG 增长机制。

## 对产品方向的启发

当前的 `skill-asset-operations-tool` 不应急于扩张成统一 Skill/MCP/Agent 编辑器。更合理的
升级路径是围绕一个具体 Skill 建立能力级控制面：

1. 声明任务边界、依赖、来源和支持的运行时；
2. 建立 with-unit / without-unit 的质量与成本评测；
3. 区分运行时适配、能力本体与 CLG Hook；
4. 对归属、转化、隐私和结果污染进行审计；
5. 记录能力使用是否产生增量关系，而不是只记录安装和 Hook。

这条路径既服务当前 Skill，也能检验未来是否真的需要跨载体的能力治理层。
