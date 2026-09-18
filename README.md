# 立项反问 · project-interrogation

> 在新项目 / 新合作 / 新标的 / 新通道**正式启动之前**，用六个逼问把"需求是真的吗、现在谁在解决、具体是谁、本周能收款的最小版本是什么、有没有现场观察、三年后还成不成立"逐条问到**有证据为止**。
>
> 一个 WorkBuddy / Claude Code 技能（Skill）。**只出诊断与一个现实动作，不出方案。**

**给谁用**：准备启动一个新项目 / 新合作 / 新标的，但说服不了自己"这是不是真需求"的人；要写立项报告、投决材料、合伙人沟通稿，想先把前提验一遍的人；反复被"市里有文件支持""这个行业都需要"这类理由说服过、也吃过亏的人。

**关键词**：立项前体检 · 项目评估 · 要不要做 · 需求真实性验证 · pre-mortem · 尽调前置 · 六问 · WorkBuddy 技能 · Claude Code 技能

## 它解决什么问题

绝大多数立项死在同一个地方：**把兴趣当成需求，把政策当成订单，把类别当成客户。**

- 「市里有文件支持」→ 这份文件能开出采购单吗？谁签？
- 「某类中资企业需要」→ 那是筛选条件，不是人。你没法给一个类别发邮件。
- 「银行说这个方案能做」→ 客户经理口头判断，还是授信审批书面结论？两者差一次否决。
- 「先把平台搭起来才能用」→ 那这周能收到钱的那一笔是什么？

本技能把"要不要做"从直觉判断，变成一次**有证据的体检**。

| 普通"项目评估清单" | 本技能 |
|---|---|
| 给你一张要自己填的表 | **一次只问一个问题**，逼你当场回答，答不实就继续追 |
| 顺着你的话往下给方案 | 反问期内**零产出**：不写文件、不做测算、不给方案、不说"这个想法不错" |
| 用"建议进一步调研"收尾 | 必须收口到 **GO / 收窄后 GO / PARK / KILL** 四选一 + 一个一周内可完成的动作 |
| 结论和事实混在一起 | 每条回答强制标注 `既有已确认` / `本会话新检索` / `待核实` |

## 硬闸门（不是建议，是约束）

1. **一次只问一个问题** —— 绝不把两问打包成一条消息
2. **反问期内零产出** —— 不写文件、不做测算、不给方案、不说"这个想法不错"
3. **不许用奉承换热场** —— 反谄媚五禁
4. **必须收口到四选一 + 一个动作** —— 不允许以"建议进一步调研"结尾
5. **证据分级强制** —— 每条回答标 `既有已确认` / `本会话新检索` / `待核实`

## 流程

| 步骤 | 做什么 |
|---|---|
| **Step 0** | 先摸已有材料（项目记忆、既有交付物），命中历史结论的不重问 |
| **Step 1** | 阶段路由：A 纯设想 / B 已有对接方 / C 已有付费 / D 合规工程 —— 决定问哪几问 |
| **Step 2** | 六问，一次一问，追问到有证据为止 |
| **Step 3** | 前提挑战：承重假设写成编号前提，逐条表态同意/反对 |
| **Step 4** | 结论四选一：**GO / 收窄后 GO / PARK（须写明重启条件）/ KILL** |
| **Step 5** | 一个现实动作：一周内能做完、能拿到外部回应、能证伪某个前提 |

### 六问

| # | 问的核心 | 追到什么时候算够 |
|---|---|---|
| **Q1** 需求真实性 | 有没有人**已经**为这件事付出代价（钱、时间、编制、签字）？ | 具体行为 + 具体代价 +「停掉他会不会来电话」 |
| **Q2** 现状替代 | 这件事**现在**是怎么被解决的（哪怕是土办法）？花了多少钱/时间/人？ | 一条具体工作流 + 一个可量化成本 |
| **Q3** 绝望的具体性 | 点名最需要它的那个**人**。什么岗位？做成什么会被提？ | 一个到岗位的具体人 + 一个具体后果 |
| **Q4** 最窄切口 | 这周就能收到钱的最小版本是什么？ | 几天内可交付、且有人愿掏钱的单点 |
| **Q5** 观察与意外 | 你**亲自**看过一次现场吗？哪里跟预想不一样？ | 一个具体的意外 |
| **Q6** 未来适配 | 三年后世界变了，这件事更重要还是更不重要？ | 一个关于"世界怎么变"的具体判断 |

完整追问清单、红旗判据、后果匹配 → [`references/six-questions.md`](references/six-questions.md)

## 安装

```bash
# WorkBuddy / CodeBuddy
git clone https://github.com/g1og1ogo/project-interrogation.git ~/.workbuddy/skills/project-interrogation
git clone https://gitee.com/myworkbuddy/project-interrogation.git  ~/.workbuddy/skills/project-interrogation   # Gitee 镜像

# Claude Code
git clone https://github.com/g1og1ogo/project-interrogation.git ~/.claude/skills/project-interrogation
```

纯 Markdown，无依赖、无脚本、不联网。技能清单在会话启动时注入，**装完需重开会话才生效**。

## 怎么触发

说「值不值得做」「要不要启动」「帮我捋一下这个想法」「帮我评估这个项目」「该不该投 / 该不该签」会命中。也会在**你为一个还不存在的东西做规划时主动介入**，而不是顺着你的话往下答。

反向边界（不触发）：已确定要做、只问怎么做的执行类问题；纯信息查询；纯排版类请求。

## 文件结构

```
project-interrogation/
├── SKILL.md                            主流程：闸门 / 六步 / 五禁 / 逃生舱
└── references/
    ├── six-questions.md                六问原文＋适配改写＋追问清单＋红旗
    ├── pushback-patterns.md            五种推法 BAD/GOOD 对照
    └── output-and-assignment.md        四选一判据＋动作五标准＋HTML 模板
```

## 常见问题

**Q：它会不会问到我烦？**
会。这是设计目标。反谄媚是硬闸门，允许它在你说"我觉得这个方向挺好"时不接话、继续追问证据。如果你要的是一个帮你完善方案的助手，这个技能不适合你。

**Q：能只问其中几问吗？**
可以。Step 1 会先做阶段路由：纯设想只问 Q1/Q3/Q4；已有对接方追加 Q2/Q5；合规/工程类事项（D 档）只问 Q2/Q4。

**Q：和上游 gstack 的 `office-hours` 是什么关系？**
是本领域的**移植改写**，不是翻译。见下方「来源与改动」。

**Q：结论是 GO 就代表能做成吗？**
不代表。它只保证一件事：**你已经把最关键的前提当着证据的面说了一遍**。GO 的意思是"没有发现致命前提缺口"，不是"这事能成"。

## 相关项目

- [**token-usage-dashboard**](https://github.com/g1og1ogo/token-usage-dashboard) —— 同作者的 Token 消耗看板技能：按业务主线归因 AI 花销，用数据而不是感觉决定要不要换低价模型。

## 来源与改动

改写自 [garrytan/gstack](https://github.com/garrytan/gstack) 的 `office-hours` v2.0.0（MIT，原文抓取于 2026-09-12），**非逐句翻译**。主要重构：

- **阶段路由换成本地四档** —— 原文的 Pre-product / 有用户 / 有付费不适配尽调与境外架构类立项，新增 D 档（合规/工程事项，只问 Q2 Q4）
- **六问重写为投研·尽调·跨境版**，每条带本领域改写示例与追问清单
- **证据三级标注写成硬闸门** —— `既有已确认` / `本会话新检索` / `待核实`
- **六问本体改用纯文本单问**，不用选项式提问 —— 选项会诱导用户"选一个"而不是"说清楚"，这里要的是长句和具体事实
- **加收口** —— 四选一结论 + 现实动作五标准，动作模板里「失败也算结果」一栏不得为空

保留自原文的核心姿态：*"Be direct to the point of discomfort. Comfort means you haven't pushed hard enough. Your job is diagnosis, not encouragement."*

## License

MIT —— 全文见 [`LICENSE`](LICENSE)。

本仓库改编自 [garrytan/gstack](https://github.com/garrytan/gstack) 的 `office-hours` v2.0.0，原作品 **Copyright (c) Garry Tan**，以 MIT 许可发布。按 MIT 的要求，原作品的版权声明与许可声明在此一并保留；原许可全文见上游仓库。

---

<details>
<summary><b>English</b></summary>

**project-interrogation** — a Skill for WorkBuddy / Claude Code that runs a six-question pre-mortem *before* you commit to a new project, partnership, deal, or channel. It asks one question at a time and keeps pushing until each answer is backed by evidence: who has already paid for this, how it is solved today, who specifically needs it, what the smallest version you could bill for this week is, have you personally watched the process, and will it matter more or less in three years.

Hard gates: one question per turn, zero deliverables during the interrogation, no flattery, mandatory close-out to GO / NARROW-GO / PARK / KILL plus one action doable within a week, and every claim tagged as *previously confirmed* / *retrieved this session* / *unverified*. Markdown only, no dependencies.

Adapted (not translated) from `office-hours` v2.0.0 in [garrytan/gstack](https://github.com/garrytan/gstack), MIT.
</details>
