# 证据地图：能力产品化与 CLG

这份清单记录 CLG 模型目前依赖的主要材料，更新于 2026-06-12。规范和官方产品说明行业
正在发生什么；理论帮助提出问题；真实实践和增长实验负责修改模型。表格最后一列用于提醒
证据强度，而不是给观点贴上科学标签。

## 技术与厂商实践

| 方向 | 一手证据 | 从中可见 | 暂时看不出 | 强度 |
|---|---|---|---|---|
| 开放 Skill 格式 | [Agent Skills Specification](https://agentskills.io/specification) | Skill 可用目录、`SKILL.md` 和渐进披露封装流程知识 | 通用结果契约、质量或商业效果 | 事实 |
| 能力增量评测 | [Evaluating skills](https://agentskills.io/skill-creation/evaluating-skills) | 可比较 with-skill / without-skill 的成功率、时间和 Token | 评测提升必然带来增长 | 事实 |
| 跨产品采用 | [Anthropic](https://docs.anthropic.com/en/docs/claude-code/skills)、[OpenAI Codex](https://developers.openai.com/codex/skills)、[GitHub Copilot](https://docs.github.com/en/copilot/concepts/agents/about-agent-skills)、[Microsoft](https://learn.microsoft.com/en-us/agent-framework/agents/skills)、[AWS](https://docs.aws.amazon.com/agent-toolkit/latest/userguide/skills.html) | 同类 Skill 形态正在多个 Agent 产品中扩散 | 完全兼容、统一运行时或统一商业市场 | 观察 |
| 工具调用标准 | [MCP Tools](https://modelcontextprotocol.io/specification/2025-11-25/server/tools) | 工具可发现、可调用并声明输入输出 Schema | 工具等于用户结果、增长或可信能力 | 事实 |
| Agent 发现与协作 | [A2A Specification](https://a2a-protocol.org/latest/specification/) | Agent Card 可描述身份、接口、版本、能力和安全 | `AgentSkill` 是独立能力制品 | 事实 |
| Skill Registry | [Google Cloud Skill Registry](https://cloud.google.com/blog/topics/developers-practitioners/io26-news-for-agent-developers-on-google-cloud) | Google Cloud 宣布用于 packaged domain logic 复用与治理的预览目录 | 已降低治理成本或形成统一市场 | 事实 |
| MCP Server Registry | [GitHub MCP Registry](https://github.blog/ai-and-ml/github-copilot/meet-the-github-mcp-registry-the-fastest-way-to-discover-mcp-servers/) | GitHub 提供 MCP Server 发现目录 | 与 Skill Registry 对象或治理范围相同 | 事实 |
| 验证与信任 | [NVIDIA Verified Agent Skills](https://developer.nvidia.com/blog/nvidia-verified-agent-skills-provide-capability-governance-for-ai-agents/) | Skill 可被扫描、签名、编目并附机器可读 Skill Card | 验证等于持续质量、安全或跨平台认证 | 事实 |
| 模型公司能力包 | [SenseNova Skills](https://github.com/OpenSenseNova/SenseNova-Skills)、[Google Gemini Skills](https://github.com/google-gemini/gemini-skills)、[NVIDIA Skills](https://github.com/NVIDIA/skills) | 模型厂商正在发布任务级能力包 | 能力包产生了可归因的商业增长 | 观察 |
| 嵌入式分发 | [Apps in ChatGPT](https://openai.com/index/introducing-apps-in-chatgpt/)、[GPT Store](https://openai.com/index/introducing-the-gpt-store/) | 能力或应用可在对话环境中发现和使用 | 供应商一定能保留关系与价值 | 观察 |
| 平台格式风险 | [GitHub Copilot Extensions deprecation](https://github.blog/changelog/2025-09-24-deprecate-github-copilot-extensions-github-apps/) | 分发格式和平台策略可能快速变化 | 跨平台能力一定能消除依赖 | 事实 |

## 相邻 PLG 与营销案例

| 案例 | 一手证据 | 对 CLG 的作用 |
|---|---|---|
| Website Grader | [HubSpot Website Grader](https://website.grader.com/)、[HubSpot 案例](https://inspire.hubspot.com/hubspot-website-grader-expertise-with-a-click-of-a-mouse) | 真实任务可以同时承担价值交付、需求教育和获客 |
| Grammarly | [Where Grammarly Works](https://www.grammarly.com/where-grammarly-works) | 产品能力可以进入大量第三方工作环境持续交付价值 |
| Calendly | [Calendly sales tips](https://calendly.com/blog/pro-tips-for-sales) | 用户使用能力时，可以自然把能力分发给下一位参与者 |
| Canva Creators | [Canva Creators](https://www.canva.com/creators/) | 可复用资产可以形成创建、审核、发现、复用和收益循环 |
| ChatGPT Apps | [OpenAI 发布说明](https://openai.com/index/introducing-apps-in-chatgpt/)、[目录提交文档](https://developers.openai.com/apps-sdk/deploy/submission) | Agent 可以在用户意图出现时发现和调用第三方能力 |

## 增长测量与运营框架

| 框架 | 一手证据 | 对 CLG 的作用 |
|---|---|---|
| North Star Framework | [Amplitude North Star](https://amplitude.com/books/north-star/about-north-star-framework) | 用代表用户价值的北极星和输入指标连接产品行为与商业结果 |
| Time to Value | [Amplitude TTV](https://amplitude.com/blog/time-to-value-drives-user-retention) | 区分任务启动、首次价值和持续价值，避免把完成流程当作获得价值 |
| Product-Qualified Lead | [Pocus PQL](https://www.pocus.com/blog/pql-guide-part-3-advanced-product-qualified-lead-scoring-concepts) | 用价值、匹配和意图识别值得承接的使用关系 |
| Incrementality | [Meta Conversion Lift](https://www.facebook.com/business/measurement/conversion-lift)、[Google Meridian](https://developers.google.com/meridian/docs/causal-inference/intro) | 区分归因与因果，判断能力分发真正新增了什么 |

## 可以借用的理论

| 理论 | 原始来源 | 对本研究的作用 |
|---|---|---|
| 模块化与设计规则 | [Baldwin & Clark, Design Rules](https://papers.ssrn.com/sol3/papers.cfm?abstract_id=312404) | 模块价值来自架构、接口、替换与组合，不来自无限拆小 |
| 分层模块化数字架构 | [Yoo, Henfridsson & Lyytinen, 2010](https://dl.acm.org/doi/10.1287/isre.1100.0322) | 解释 Skill、协议、服务和内容为何可处于不同层级 |
| Service-Dominant Logic | [Vargo & Lusch, 2004](https://journals.sagepub.com/doi/abs/10.1509/jmkg.68.1.1.24036) | 支持“价值在使用情境中实现”；“使用即可信证明”是本文待测推演 |
| Boundary Resources | [Ghazawneh & Henfridsson, 2013](https://onlinelibrary.wiley.com/doi/abs/10.1111/j.1365-2575.2012.00406.x) | 解释平台如何同时促进第三方创新并控制生态 |

## 公开供给信号

以下 Star / Fork 只作为公开兴趣与分发信号，**不是商业采用或增长证据**。快照日期：
2026-06-12。

| Repository | Stars | Forks |
|---|---:|---:|
| `anthropics/skills` | ~149k | ~17.6k |
| `modelcontextprotocol/servers` | ~87k | ~11k |
| `a2aproject/A2A` | ~24k | ~2.5k |
| `agentskills/agentskills` | ~20k | ~1.3k |
| `OpenSenseNova/SenseNova-Skills` | ~4.3k | ~290 |
| `google-gemini/gemini-skills` | ~3.6k | ~350 |
| `NVIDIA/skills` | ~1.2k | ~150 |

## 还缺什么

现有材料足以说明，能力封装、调用、发现和治理正在受到更多关注。但以下问题仍没有可靠的
公开答案：

1. 能力单元相较白皮书、普通免费工具和产品试用的增量转化；
2. 同一能力跨多个运行时的任务成功率、成本和风险差异；
3. Registry 是否改善匹配与留存，还是加剧低质量供给和安全成本；
4. 能力提供方是否能在第三方环境中保留归属、反馈和商业关系；
5. 验证状态是否能预测未来真实任务表现和组合后可靠性。
