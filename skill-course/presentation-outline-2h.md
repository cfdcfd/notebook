# Skill 内训课 · 演讲大纲（约 2 小时）

> **定位**：基于 `part-1-cognition.md`（v3）、`part-2-practice.md`（2.0 + 2.1～2.3 节奏表）、`part-3-value.md`（骨架）、`00-course-map.md` 整合的幻灯片级大纲。  
> **讲稿与引用细节**仍以各 `part-*.md` 与 `references/` 为准；本文负责「页序 + 页类型 + 一句支撑」。  
> **迭代**：下方可按块讨论后改 headline / 增删页 / 调整与讲稿小节映射。

**总时长**：约 120 分钟（含机动 11～16 分钟，Q&A / demo / 互动可用）

**时段总览**


| 段                             | 颜色     | Slide # | 建议时长 | 主要对应稿                     |
| ----------------------------- | ------ | ------- | ---- | ------------------------- |
| 1 Opening（愿景 → 卡点 → 答案 → 三段路） | teal   | 1–6     | ~16m | part-1 · 1.1 入场 + 1.5 一句话 |
| 2 Skill 是什么                   | purple | 7–14    | ~30m | part-1 · 1.2 / 1.3 / 1.4  |
| 3 怎么造（专家）                     | green  | 15–24   | ~40m | part-2 · 2.1～2.3          |
| 4 怎么用（领导 + 落地）                | blue   | 25–32   | ~25m | part-2 · 2.0 + part-3     |
| 5 Closing                     | teal   | 33–35   | ~6m  | part-1 · 1.6 / 1.7 + 收束   |


> Opening 段叙事 = **行业愿景 → 行业卡点 + 诊断 → 行业答案（Skill 共识）→ 本课地图**；thesis 节从原先 1 页 supporting 复读，扩展为 Slide 3-5 完整三页弧线。  
> 仍保留 ~11-16 分钟机动，可用于 Q&A / demo / 部门便签互动。

---

## 1. Opening

**Section color:** teal

### Slide 1: Title

- **Type:** Title
- **Headline:** 全研发场景 Skill 开发与应用实战
- **Subtitle:** 从 Prompt 到研发组织级 Skill 资产
- **Sub-subtitle（italic 小字 · 主题落点）:** 让 agent 真过门禁、真上线、真救火
- **Footer（小字）:** 面向研发团队负责人 / 技术专家 / 平台与效能角色；讲师：XXX；日期：2026-04-XX；3 段路｜35 页｜2 小时

### Slide 2: 三层离场标准

- **Type:** Goals
- **Headline:** 今天围绕这三件事展开
- **Points（每条：line1 主问题 + line2 主题落点）:**
  - 🟣 **看懂** — Skill 是什么 / 为什么是它把 agent 推到能解决问题
  - 🟢 **会造** — 一个能让 agent 真过门禁的 Skill 长什么样 / 怎么造才稳、能反复用
  - 🔵 **能选** — 哪些研发场景先做 / 怎么从一个人做到一支团队

### Slide 3: AI Native 团队的愿景 — 从「看起来会干活」到「解决真实问题」

- **Type:** Statement + Evidence
- **Headline:** AI Native 团队的愿景：从「**看起来会干活**」到「**解决真实问题**」
- **上半 · 三场景卡（动词两字 + 全中文；每条"场景 — 流程 — 一个『真』字落点"）:**
  - **做完 一张需求单** — 读需求、改代码、跑测试、提 PR —— agent **真把它 merge、关单**
  - **上线 一次版本** — changelog / release note / 部署 / wiki 同步 —— agent **串起一条龙，可回滚**
  - **救火 一次故障** — 监控告警进来，开始排查 —— agent **真复现、真定位根因，补丁能直接打**
- **中间 · 标语过渡 · 12 个月相变叙事（双行 · 细横线分隔）:**
  > 上行（小字 · 灰）：**12 个月前**，业界为 "**30% 代码 AI 写**" 震撼——但当时大家心知肚明：有多少**真上生产、真过门禁**，没人敢说
  >
  > 下行（大字 · teal）：**今天，领跑团队把「真解决问题」的机制装上了——**
- **下半 · 对照墙（2 × 2 · 左产量层 + 右机制层）:**

  | 产量层 ·「看起来会干活」已成常态                                                                               | 机制层 ·「真解决问题」已上场                                                                 |
  | ----------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------- |
  | 🟢 **Google 75%** 新代码 AI 生成（2026-04 Pichai @ Cloud Next）[R12·§1]                                | ⭐ **Anthropic 16% → 54%** 自家 PR 评审覆盖（多 agent 自动评，2026-03-09 官方博客）[R12·§2]       |
  | ⚠️ 但 Opsera 实测：**AI PR 等审 4.6×** 慢于人写代码——产量上去了，评审跟不上                                            | 真实 case：**一行代码改动差点破坏 production auth**——quick-approved 中被多 agent 评出 critical    |
  | ⚠️ **反例 · Microsoft 30%** 代码 AI 写（2025-04）[R12·§4]                                              | 🟢 **Cursor 35%** 合并 PR 由 cloud agents 写 [R10·§2]                               |
  | + 2026-01 Windows 11 一个月三次 emergency 修复 → 2026-02 设 **Engineering Quality Czar** 直接向 Nadella 汇报 | + Bugbot + sandbox 自验：**merge-ready** 而非 generate-only；bug resolution 52% → 76% |

- **底部 · 相变收口（一行加粗 · 居中）:**
  > **12 个月，相变的不只是产量——领跑团队同时把「真解决问题」的机制装上了；没装的，付出了 Windows 11 reliability 危机的代价。**
- **Speaker note:** 这页核心叙事是「**看起来会干活 ≠ 真解决问题**」——12 个月前 LlamaCon 业界为 30% AI 写代码震撼时，**没人敢谈这部分代码的产线 / 门禁 / 业务效果**；今天领跑团队不只是把比例推到 75%，更重要的是把"真解决问题"的机制（多 agent 评审 / sandbox 验证 / Bugbot 自修）装上了。**口播节奏（~1.5 分钟）**：上半三动词 ~30 秒 + 中间相变叙事 ~20 秒（"30% 是震撼数据，但当时质量没人敢说"）+ 下半对照墙 ~50 秒（**重点讲 Anthropic 一行代码 auth 案例** + **反例 Microsoft**："光推 30% 产量，半年后 Windows 11 一个月内出三次紧急修复 → CEO 下令设 Quality Czar"）+ 底部相变收口"相变的不只是产量"。**Meta 65×75% OKR 不上 PPT**——核查发现 Meta 只公开 adoption 输入指标，未公开质量 / outcome 数据，纯属"看起来会干活"叙事；可在 Q&A 一句带过：「Meta 把 75% 写进 H1 OKR，但只公开了产量指标，没公开质量数据——典型的'还在产量层'」。三场景覆盖三类听众：**做完需求单** → 一线工程师 / 技术专家；**上线版本** → 团队负责人；**救火故障** → 平台 / 效能 / Owner。这页温度要高，下一页（gap）才能形成落差。**深挖资料**：references/11-ai-native-leader-companies-2026-04.md（R12）。
- **视觉建议:** 上半三动词卡 ~30%（teal 主色 + 大字 + 图标），中间双行过渡 ~10%（灰小字 + teal 大字 · 细横线分隔），下半对照墙 2×2 ~50%（**左 2 卡用 inkMute / star 警示色调**——产量层 + 反例 ⚠️；**右 2 卡用 teal / tealLite**——机制层 + ⭐ 闭环），**Anthropic 那张卡的"16 → 54%"用最大字号 + 一行小字 bug 案例**作为页面情绪锚点；Microsoft 反例卡用 ⚠️ 图标 + 灰底 + dashed 边框（暗示反例）；底部相变收口 ~10% 加粗居中。
- **引用:** [R2] 长任务 agent 范式 / [R10·§2] Cursor 35% PR by cloud agents（含 Bugbot 数据）/ [R12·§1] Google 75% / [R12·§2] Anthropic 16→54% + auth bug case / [R12·§4] Microsoft 30% + Quality Czar / Opsera AI Coding Impact Benchmark 2026（AI PR 4.6× review wait · 待 R13 收录）

### Slide 4: 那我们和领跑团队，差在哪？

- **Type:** Statement
- **Headline（双行衔接 Slide 3 的相变）:**
  - 上行（问）：**那我们和领跑团队，差在哪？**
  - 下行（答）：**缺的不只是模型，是让 agent 真能解决问题的「know how」**
- **Supporting（左右对照表 · 与 Slide 3 三场景对位 · 强调"真做到"对照）:**

  |              | 我们的研发现状                            | 领跑团队的 AI Native              |
  | ------------ | ---------------------------------- | ---------------------------- |
  | **做完** 一张需求单 | Done / 口径 / 门禁规则**分散在文档、评审、口头约定**里 | 一份**能让 agent 真过门禁的「团队规矩」**   |
  | **上线** 一次版本  | 工具链多、步骤散，**缺一条可重复执行的流程资产**         | 一份**能让 agent 真跑通流程的「流程蓝本」**  |
  | **救火** 一次故障  | 经验**停在口述与临时群消息**里，沉淀不下来            | 一份**能让 agent 真复现问题的「修复经验包」** |

- **Evidence corner（页面右下约 ¼～⅓）：** **群内截图粘贴位**。制作幻灯片时将 OpenClaw 推广相关聊天记录截图置入此处即可（小版面、不上主叙事）；建议使用文件 `outline/assets/slide-04-openclaw-chat.png`（可自行创建目录后放入，打码昵称 / 头像 / 群名）。
- **Speaker note:** 本页 gap 的本质：**「看起来会干活」→「真解决问题」之间，差的是把"规矩"塞进一种 agent 能消费的形态**。右栏每条用"**能让 agent 真做到 X**"——**与 Slide 3 三场景落点对位**（真过门禁 / 真跑通流程 / 真复现问题），但**不曝光"Skill"这个词**——下一页（Slide 5）才告诉答案。口播节奏：先承接 Slide 3 的相变收口（"领跑团队装上了机制，那机制是什么？"）→ 左栏念症状 ~30 秒 → 右栏念"真做到 X"对照 ~30 秒 → Evidence 一句共鸣。可一句点题 [R7] 三连症状：*全量加载 / 关键指令被淹没 / 改一段动整篇*——作为旁证。Evidence 口播一句即可：`我们推工具时也听到过类似声音`——**不甩锅、只共鸣**。
- **视觉建议:** 双行 Headline（上行问 + 下行答 · 一灰一 teal 形成视觉对话），左右对照表占 ~⅔ 宽（右下 Evidence corner ~⅓ 宽 · 截图位 dashed 边框）；右栏每条用 teal 高亮 "**能让 agent 真做到 X**" 短语作为视觉锚；与 Slide 3 三场景卡 + 对照墙形成"现实 → 落差"的连贯视觉叙事。
- **引用:** [R7]（长 Prompt 病灶，作旁证）/ [R2]（工作流与可重复性）

### Slide 5: Skill — 行业愿景里，缺的那一环

- **Type:** Framework + Evidence
- **Headline:** Skill：行业愿景里，缺的那一环
- **Sub-headline（小字 · 副线）:** Prompt / Workflow / RAG / MCP 之后，行业接住了「会干活」
- **上半 · 演进图（横向 4+1 · 每个前任 1 行 1 句）：**

  | 范式                 | 它解决的              | 它**没解决**的             |
  | ------------------ | ----------------- | --------------------- |
  | **Prompt**         | 给模型一次性指令，「开机键」    | 承载不了复杂、可复用、可维护的业务     |
  | **Workflow / 编排链** | 用流程把任务串起来         | 重、维护成本高、不灵活           |
  | **RAG**            | 给模型补外部知识          | 解决「知道什么」，不解决「怎么做」     |
  | **MCP**            | 标准化工具调用接口         | 能调工具，但**不封装流程**       |
  | **★ Skill ★**      | 把上面四样的经验**打包成模块** | **可发现 + 可复用 + 可按需加载** |

- **下半 · 行业把它落地了（三栏精简 · 每栏 2–3 条 · 仅作旁证）：**
**🅛 领跑 · Anthropic（2025-10）**
  - **Agent Skills** 方法论 [R2]
  - 概念三件套：**description + instructions + scripts + resources**
  - 加载机制：**progressive disclosure**
  **🅢 跟随 · 顶流采纳（2025-12 ~ 2026-04）**
  - **Cursor 3** 直接采纳 "Skills" 命名 · Marketplace = **MCPs / Skills / Subagents** [R10·§2]
  - 🔥 Cursor 自家 **35% 合并 PR by cloud agents**（同 Slide 3 锚）[R10·§2]
  - 业界第三方独立分类：Skill = **第三种 AI Agent 架构** [R10·§3]
  **🅑 破圈 · OpenClaw 生态（2026-03）**
  - 🔥 **2026-03-02 单日 +15K stars**（230K → 244K）[R10·§1]
  - 累计 **365K ★** / **ClawHub 3,200+ 社区 Skill**
  - 跨 **23+** 消息平台 / 多模型
- **Bottom line（细横线下，两行 · 回扣 Slide 3/4 主题）:**
  - 上行（小字 · italic 行业判断）：业界已把它命名为「**第三种 AI Agent 架构**」——不只是 Anthropic 的产品形态
  - 下行（大字 · 主题收口）：让 agent 从「**看起来会干活**」真正走到「**解决真实问题**」的那一环 = **Skill**
- **Speaker note:** 主论证在**上半演进图**（~~3 分钟）：依次点过 Prompt / Workflow / RAG / MCP **解决了什么、没解决什么**；最后一列 Skill **不要展开内部结构**（那是紫段任务），只强调"它是把前四样经验打包成模块"。下半三栏（~~2 分钟）只作"行业真在用"的旁证——每栏挑 1 条说，**🔥 35% PR + 🔥 +15K stars** 是两个视觉锚点；OpenClaw +15K 可顺势回扣 Slide 4 截图。
- **视觉建议:** 上半演进图占版面 ~50%，4 前任灰色色调（淡灰底 + 中性字），**Skill 列高亮 teal 色 + ★** 让"答案"立刻被看见；下半三栏占 ~35%（紧凑、白底、项目符号），保留两个 🔥 高亮硬数据；Bottom line 占 ~15%，细横线分隔，双行收口。
- **引用:** [R2] [R10·§1] [R10·§2] [R10·§3] · 演进图四前任的描述参考课程私录"Skill 行业语境（用户消息 2026-04-29）"

### Slide 6: 今天的三段路

- **Type:** Framework
- **Headline:** 一张地图，三段路
- **Points（建议三段进度条，段长按时间比例 30 : 40 : 25 · desc 紧扣"真做到 X"主题）:**
  - 🟣 **是什么**（~30 分钟）— 看懂 Skill 怎么让 agent 真过门禁、真跑通、真复现
  - 🟢 **怎么造**（~40 分钟）— 从能跑、能稳，到团队反复套用、长期维护
  - 🔵 **怎么用**（~25 分钟）— 哪些研发场景先做，怎么从一个 Skill 长成一片资产
- **Speaker note:** 本页不是 Slide 2 的翻版——Slide 2 答"**我能拿到什么**"（收益），本页答"**接下来怎么走**"（路径 + 时长）。可口播一句衔接：「前三页讲『为什么是 Skill』，接下来三段讲『怎么把 agent 真送进生产』。」每进入新一段，section divider 上重复同色块（紫 / 绿 / 蓝），听众随时知道走到哪儿了。
- **视觉建议:** 用横向**三段进度条**（不是三卡），段长按 30:40:25 比例画——空间感本身就传达了重心；与 Slide 2 的三卡布局**形成对比**，避免视觉重复；唯一的数字强调是三个时长。

---

## 2. Skill 是什么（解剖 → 机制 → 栈位置）

**Section color:** purple  
**对应讲稿：** `part-1-cognition.md` · 1.2 / 1.3 / 1.4

### Slide 7: Section divider

- **Type:** Section divider
- **Headline:** 🟣 是什么 — 解剖、机制、栈上位置
- **Speaker note:** 进段前可花 30 秒口播 1 个真实卡点（周报 / 合同），把"规矩"具象化，再切入解剖。

### Slide 8: 三大误解一次清空

- **Type:** Framework
- **Headline:** 你以为的 Skill — 多半都不是
- **Supporting（两栏对照，部署建议表格 / 卡片对）:**


| 误区                 | 真实的 Skill              |
| ------------------ | ---------------------- |
| 把 Prompt 写到 5000 字 | 主体很轻，**按需**取细节         |
| 把单个工具 / API 包一层    | 完整工作流 **+** 编排，不是原子动作  |
| 把文档丢给模型（RAG）       | **程序性知识 + 可执行步骤**，不是检索 |


- **Speaker note:** 第一行可口播 [R7] 的三连症状——*全量加载 / 关键指令被淹没 / 改一段动整篇*；右栏"真实样子"由 **Slide 9 解剖**一页兑现。
- **引用:** [R7]（长 Prompt 病灶）/ [R4] 第 5 节（Skills vs Tools, MCP）/ [R2] *procedural knowledge*

### Slide 9: 解剖（PDF Skill 目录树）

- **Type:** Code
- **Headline:** 一个真正的 Skill 长什么样
- **Supporting:**

```text
pdf-skill/
├── SKILL.md                  ← 主体很轻：何时触发 + 整体流程
├── reference.md              ← 长说明，按需读
├── forms.md                  ← 仅「填表单」子任务时拉进来
└── scripts/
    └── extract_form_fields.py  ← 确定性逻辑，作为工具被执行
```

- **目录 + 主体 + 子文件 + 脚本** = Skill 的最小完整骨架
- **Speaker note:** 官方引文 *"Code is deterministic..."* 让给 Slide 10 做 Big statement supporting，避免本页文字密度过高。

### Slide 10: 教一次，永久复用

- **Type:** Big statement
- **Headline:** 教一次，永久复用
- **Supporting:**
  - *"Teach once, use forever."* — Anthropic [R2]
  - 它有目录、有分工、有可执行代码 — **代码资产线，不是文档线**
  - *"Code is deterministic; this workflow is consistent and repeatable."* — [R2]

### Slide 11: 渐进式披露 — 三层加载

- **Type:** Framework
- **Headline:** 模型按需把上下文「取出来」，不是「塞进去」
- **Supporting:**
  - **Level 1 · 元数据** — 50 个 Skill 各 ~100 字常驻（约 **7K token**）
  - **Level 2 · 指令** — 触发后才读 SKILL.md 主体
  - **Level 3 · 资源** — 子文件 + 脚本，按需取用
  - 全塞 25 万字 vs 元数据 7K token —— **差两个数量级**
- **Speaker note:** 紫段 AHA 时刻。可口播 T0→T1→T2→T3 序列：metadata 常驻 → 命中 Skill 读主体 → 子任务读子文件 → 脚本输出不入上下文。 [R2]

### Slide 12: 实测：轮次 15→2，错误 3→0

- **Type:** Data
- **Headline:** 实测 — 轮次 **15→2**，错误 **3→0**
- **Supporting:** Token **12K→6K**；交互效率提升约 **7×**。 [R7]

### Slide 13: PR Review 的五种形态

- **Type:** Framework
- **Headline:** PR Review 的五种形态
- **Supporting:**
  - **Prompt** — 一次性，难坚持
  - **Tool** — 原子动作
  - **MCP** — 接 GitHub 等系统的通道
  - **Skill** — 公司口径 + 清单 + 与 Tool 编排的**完整工作流**
  - **Subagent** — 隔离上下文的专职子 Agent
- **Speaker note:** 部署到 PPT 时建议做成**对比卡片**或**表格**而非 5 行 bullets，避免 16:9 上挤糊。

### Slide 14: 一句比喻

- **Type:** Quote
- **Headline:** MCP 是厨房，Skill 是食谱
- **Supporting:**
  - 光有厨房，新人不知道做什么菜；光有食谱，没厨房做不出来
  - Tool / MCP / Skill / Subagent — **不是替代关系，是组合关系**
  - [R7]；[R4] 第 5 节整节讲 Skills vs Tools, MCP, Subagents

---

## 3. 怎么造（专家收据）

**Section color:** green  
**对应讲稿：** `part-2-practice.md` · 2.1～2.3（讲稿多节仍待展开，此处为幻灯片主线）

### Slide 15: Section divider

- **Type:** Section divider
- **Headline:** 🟢 怎么造 — 60 分跑起来，95 分守得住

### Slide 16: 60 分骨架

- **Type:** Framework
- **Headline:** 第一个 Skill 的五块
- **Supporting:** **触发 / 边界 / 步骤 / 输出 / 验收（DoD）**。[R3] 模板；[R6] 命名与路径约定。

### Slide 17: 触发命门

- **Type:** Statement
- **Headline:** description 决定会不会被用对
- **Supporting:** [R7] 自检：*"When would you use the X skill?"*

### Slide 18: description 正反例

- **Type:** Framework
- **Headline:** 模糊 vs 可用
- **Supporting:** `Helps with documents` vs 带场景 + 正向触发 + **Do NOT use for** 的完整 description（例见 part-1 · 1.6）

### Slide 19: 拆分艺术

- **Type:** Statement
- **Headline:** 主指令薄，细节厚
- **Supporting:** SKILL.md 分流；细节 `references/`；确定性 `scripts/`。[R8 · baoyu-translate]

### Slide 20: 确定性 vs 启发式

- **Type:** Framework
- **Headline:** 什么给代码，什么给模型
- **Supporting:** 能规格化、要数清的事 — 脚本；需要综合与判断 — 模型。[R2] [R5]

### Slide 21: 少样本陷阱

- **Type:** Statement
- **Headline:** 给推理链，不要只给答案
- **Supporting:** [R5]；[R8] 隐喻与案例（口播展开）

### Slide 22: 负向触发

- **Type:** Code
- **Headline:** 防重叠 — Do NOT use for …
- **Supporting:** [R7]

### Slide 23: 三轴测试

- **Type:** Framework
- **Headline:** 上线前 DoD
- **Supporting:** **Triggering** / **Functional** / **Performance**。[R1] [R7]

### Slide 24: 健康库信号

- **Type:** Statement
- **Headline:** 敢删、敢瘦
- **Supporting:** [R8] 演进 — 删代码、规则条数反向减肥；与 2.3 治理成稿互链。

---

## 4. 怎么用（领导收据 + 部门落地）

**Section color:** blue  
**对应讲稿：** `part-2-practice.md` · 2.0；`part-3-value.md`

### Slide 25: Section divider

- **Type:** Section divider
- **Headline:** 🔵 怎么用 — 从写一个 Skill 到改一家公司

### Slide 26: 三层叙事

- **Type:** Framework
- **Headline:** 个人 → 团队 → 组织（每层一句话）
- **Supporting:** 个人升一格视角；团队 Skill 库 = **转型体温计**；组织 = **基础设施与治理**。 [R9] 与 2.0 全文金句。

### Slide 27: 压舱句

- **Type:** Big statement
- **Headline:** 贡献者不是被替代，是被升维

### Slide 28: 三问决策卡

- **Type:** Framework
- **Headline:** 值不值得 Skill 化？
- **Supporting:** 三个月重复几次？错了谁买单？产出是否可检查？— part-3 · 3.1

### Slide 29: 管理反模式

- **Type:** Framework
- **Headline:** 三种典型翻车
- **Supporting:** 唯数量 KPI；无 Owner / 无验收；长 Prompt 当 Skill — part-3 · 3.2 + part-1 · 1.6

### Slide 30: 部门候选场景

- **Type:** Framework
- **Headline:** 不看岗位，看工作流
- **Supporting:** 市场 / HR / 法务 / 研发 … 各 1 动词 + 1 产出；听众填「本部门 1 号实验」。 part-3 · 3.3；灵感 [R3] 类目。

### Slide 31: 安全抬杆

- **Type:** Quote
- **Headline:** Disclaimer（原文上屏）
- **Supporting:** [R3] README；与 2.2 ⑩、part-3 · 3.4 一致。

### Slide 32: ROI 半页

- **Type:** Framework
- **Headline:** 给老板的「可审计证据」
- **Supporting:** 轮次、错误、token、首稿可用率 — 方向性；慎用无对照的 FTE。 part-3 · 3.5；[R7]

---

## 5. Closing

**Section color:** teal

### Slide 33: Recap

- **Type:** Recap
- **Headline:** 回顾（一行一段）
- **Points:**
  - **定调** — 行业愿景 → 卡点 → 答案：把规矩打包给 Agent = Skill（Slide 3-5）
  - **是什么** — 结构包 + 渐进式披露 + 栈上位置
  - **怎么造** — 触发 / 拆分 / 确定性 / 三轴测试 / 敢删敢瘦
  - **怎么用** — 三问决策 / 三层升维 / ROI 半页 / Disclaimer

### Slide 34: 收尾金句

- **Type:** Big statement
- **Headline:** Skill 不是 AI 红利的产生器，是 AI 红利的沉淀器
- **Supporting:** part-1 · 1.6

### Slide 35: Resources & Q&A

- **Type:** Resources + Q&A
- **Headline:** 资料与答疑
- **References:**
  - **一手** — [R1] PDF 指南 / [R2] 工程博客 / [R3] `anthropics/skills` / [R4] DLAI 短课
  - **二手与浓缩** — [R5] [R6] [R7]
  - **案例与行业** — [R8] [R9] [R10]
  - **本仓** — `outline/part-*.md`，`references/00-index.md`，`outputs/ai-agent-skills-industry-report.md`

---

## 附录 A：压时 / 加时（供讨论改页数时用）

**压时（约减 8～10 分钟）**  
优先删或口播代过：**Slide 21（少样本）**、**Slide 24（健康信号 — 合并进 Slide 23 三轴测试或口播）**、**Slide 29（反模式 — 合并进 Slide 28 决策卡）**。

**加时**  

- **Slide 13（PR Review 五形态）后**：一页现场互动「用一句话区分四种形态」。  
- **Slide 16～18 间**：**5～7 分钟 demo**（`/plugin install document-skills@anthropic-agent-skills`，PDF 表单 — 见 [R3] 与 `part-2` 节奏表）。  
- **Slide 30 后**：**5 分钟**便签 — 「本部门 1 号实验场景」。  
- **机动 11～16m** 充足，可优先用于 Q&A 与现场互动。

---

## 附录 B：与 `part-1` 1.6 / 1.7 的映射（避免漏讲）

- **三条专家立场**（Skill ≠ 长 Prompt / 不是越多越好 / description 是护城河）：主落在 **Slide 8、17–18、29**；1.6 全文金句在 **Slide 34**。  
- **1.7 钩子**（OMCC / 更大格局）：本大纲 **不单独占页**，由 **Slide 26–27** 与 **part-2 · 2.0** 口播展开；若希望 PPT 上也「留题」，可在 Slide 27 后加 **Slide 27b**（可选）：*「OMCC 是又一个工具，还是基础设施？」— 答案在 2.0。*

---

## 修订记录


| 日期         | 说明                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| ---------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 2026-04-29 | 初版：由聊天中的 presentation-outline 定稿写入本文件                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| 2026-04-29 | Opening 改 v2：Slide 1 课程名上位 / Slide 2 看懂·会造·能选 / Slide 3 改 thesis 站位 / Slide 4 五段色块导航                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| 2026-04-29 | 删红段（原 Slide 5–9）：thesis 已在 Slide 3 喊出，红段为复读；总页 43→38；Slide 4 改四段路；附录页码同步更新                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| 2026-04-29 | 紫段 v2：Slide 6 改三大误解清单（长 Prompt / 工具包装 / RAG）；Slide 8 用 [R2] *Teach once, use forever* 替换复读句；Slide 9 升级为三层加载机制图；Slide 10 数字打到 headline；Slide 11 简化 + 部署提示；Slide 12 supporting 补足比喻双面                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| 2026-04-29 | 删黄段（原 Slide 13–17，"为什么是现在"）：业界三段叙事在 Slide 3 supporting 已浓缩，独立成页信息密度低；总页 38→33；Slide 4 改三段路；Slide 3 supporting 补时间锚点；附录页码同步更新；机动从 8～12m 提到 15～20m                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| 2026-04-29 | Opening 重写：Slide 1 加讲师/日期/3 数字锚点；Slide 2 改"今天围绕这三件事展开" + 双小句；thesis 节由 1 页扩为 3 页（行业愿景 Slide 3 / 卡点+诊断 Slide 4 / 答案+时间线 Slide 5）；后续页面编号 +2；总页 33→35；附录与时段总览同步更新                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| 2026-04-29 | Slide 4 改版：与 Slide 3「接 Jira / 发 release / on-call」三卡逐行对位；主叙事从 [R7] 长 Prompt 三连上屏改为「规矩没进系统」；[R7] 降级为 speaker note 旁证，避免与 Slide 8 抢戏                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| 2026-04-29 | Slide 5 改版：三时间锚点排版从「横向时间线」改为「三组并列信号卡」（领跑 / 跟随 / 破圈），避免顺序冲突；OpenClaw +15K 移至最右作压轴，回扣 Slide 4 截图；Bottom line 与三卡用细横线分隔，独立成行；增视觉建议（teal 浅中深三档 + ★ 单一高亮）                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| 2026-04-29 | Slide 6 改版：与 Slide 2 拉开分工——Slide 2 答"收益"、Slide 6 答"路径+时长"；三条加时长（30/40/25 分钟）+ 半句研发落点；布局从 bullet 改为横向三段进度条（段长按时间比例），与 Slide 2 三卡布局形成视觉对比                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| 2026-04-29 | Slide 5 v2：原"三组并列信号卡"信息密度过低（仅 3 条 / 1 个硬数据），升级为"三栏信息墙"——14 条具体证据、5 个硬数据、5 家具名（Anthropic / Cursor / OpenAI / Cobus / OpenClaw 生态）；引用从模糊 [R2/R9/R10] 收紧为精确 [R2/R3/R10·§1/§2/§3]；Bottom line 加一行"第三架构"行业判断；Opening 段时长 14m→16m；机动 13-18m→11-16m                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| 2026-04-29 | thesis 弧 v3 重写（Slide 3 / 4 / 5）：Opening 段主语从"通用 AI"升维为"AI Native 团队"，主线"会聊天 → 会干活"穿过三页。Slide 3 改为"AI Native 团队的愿景"、加底部 35% PR 硬锚；Slide 4 改为"普通研发 vs AI Native"左右对照表，右栏先用占位词「打包成 Skill」、不展开形态；Slide 5 改为"演进图（Prompt / Workflow / RAG / MCP → ★ Skill）+ 三栏精简旁证"，论证从"行业达成共识"升维为"Skill 补全行业愿景里缺的那一环"。三栏证据从 14 条精简到 9 条，保留两个 🔥 硬数据（35% PR / +15K stars）。                                                                                                                                                                                                                                                                                                                                                                                                              |
| 2026-04-29 | Slide 3 v3.1 加证据：底部硬数据从单一 Cursor 35% PR 扩为 **4 家领跑公司硬数据墙**（Google 75% / Meta 65×75% H1 2026 OKR / Anthropic 16%→54% / Cursor 35%），论证"AI Native 不是未来时，是 2026 春的现状"。新增引用 [R12]（references/11-ai-native-leader-companies-2026-04.md），含 5 家公司一手 / 二手出处与口径说明。Slide type 从 Statement 升级为 Statement + Evidence。                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| 2026-04-29 | Slide 3 v3.2 改为"12 个月相变"叙事：中间标语过渡升级为双行对比（一年前：Microsoft 30% / Google 25% / Meta "明年大概一半" → 今天：4 张领跑硬数据墙），底部加"**12 个月，从'30% 是业界头部'到'75% 是 H1 OKR'——相变，不是渐变**"一行收口；Microsoft 30% 从"舍弃数据"重新定位为"对比锚"，论证"对 AI Native 的期待本身在 12 个月里相变"。视觉上灰小字（一年前）与 teal 大字（今天）形成对比。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| 2026-04-29 | **Slide 5 v3 build.js 落地**：发现 build.js 仍停在 v2「6 个月，行业给出了同一个答案」三栏信息墙，与大纲 v3「演进图（Prompt/Workflow/RAG/MCP → ★ Skill）+ 三栏精简旁证」不一致。整段重写 Slide 5：① Headline 改回 `Skill：行业愿景里，缺的那一环`；② Sub-headline italic 副线 `Prompt / Workflow / RAG / MCP 之后，行业接住了「会干活」`；③ 上半新增 5 行 × 3 列演进图表格（4 灰前任 + 1 ★ Skill ★ teal 高亮行）；④ 下半三栏精简（5 条 → 3 条，保留 🔥 35% PR + 🔥 +15K stars 两个硬锚），栏头日期挪到 who 同行避免截断；⑤ Bottom line 双行不动（v3.4 主题对齐已写入）。                                                                                                                                                                                                                                                                                                                                                 |
| 2026-04-29 | **Opening 段主题贯穿（Slide 1 / 2 / 5 / 6 同步对齐）**：Slide 3 v3.4 / Slide 4 v4.1 升级到主题「看起来会干活 → 解决真实问题」后，Slide 1 / 2 / 5 / 6 也按主题落点同步：① **Slide 1** 副标颜色 tealLite → tealMid 提对比，新增 italic 副副标 *「让 agent 真过门禁、真上线、真救火」*；② **Slide 2** 三件事 line1/line2 重写：看懂 → "为什么是它把 agent 推到能解决问题"，会造 → "一个能让 agent 真过门禁的 Skill 长什么样"，能选 → "怎么从一个人做到一支团队"；③ **Slide 5** Bottom line 双行重写，回扣 Slide 3/4 主题：「让 agent 从『看起来会干活』真正走到『解决真实问题』的那一环 = Skill」；④ **Slide 6** 三段 desc 紧扣三动作（真过门禁 / 反复套用 / 长成一片资产），衔接句更新为"前三页讲『为什么是 Skill』，接下来三段讲『怎么把 agent 真送进生产』"。build.js 同步更新，重新生成 6 页 PNG 已视觉验收。                                                                                                                                                                                                 |
| 2026-04-29 | **Slide 3 v3.4 / Slide 4 v4.1 — 动词中文化**：三动词卡「接 Jira / 发 release / 修 on-call」改为**三场景卡「做完 一张需求单 / 上线 一次版本 / 救火 一次故障」**。解三个问题：① 中英混搭（Jira / release / on-call 换成需求单 / 版本 / 故障）；② "真 X、真 Y、真 Z" 在单条里堆砌（每条收敛到**一个"真"字落点**，形式 = 场景 — 流程 — 真 X）；③ 单字动词对称感弱（改两字动词，对齐工程师日常口语）。Slide 4 对照表左列标签同步改为"做完 / 上线 / 救火"。三场景对应听众不变（工程师 / 负责人 / 平台 Owner）。                                                                                                                                                                                                                                                                                                                                                                                                                           |
| 2026-04-29 | **Slide 3 v3.3 / Slide 4 v4.0 — 愿景升维**：经联网核查 4 条主数据后，把 Slide 3 主线从「会聊天 → 会干活」升级为「**看起来会干活 → 解决真实问题**」。① **Slide 3** 数据墙重组为 **2×2 对照墙**（左产量层 / 右机制层）：左上 Google 75% + Opsera 4.6× review wait 旁证；左下 Microsoft 30% **反例升数据卡**（Windows 11 reliability 危机 → Quality Czar）；右上 Anthropic 16→54% + 一行代码差点破坏 production auth 真实 case；右下 Cursor 35% + Bugbot/sandbox 闭环。**Meta 65×75% OKR 撤出**——核查发现仅公开 adoption 输入指标，无质量 outcome 数据，纯属"看起来会干活"叙事，降级到 speaker note。三动词描述升级为"真做到 X"（真过门禁 / 真交付 / 真复现）。底部相变收口改写为"**相变的不只是产量——领跑团队同时把'真解决问题'的机制装上了；没装的，付出了 Windows 11 reliability 危机的代价**"。② **Slide 4** Headline 升级为双行（问 + 答）：「那我们和领跑团队，差在哪？」/「缺的不是模型，是让 agent 真能解决问题的『规矩』」；右栏从占位词「打包成 Skill」改为画面对照"**能让 agent 真做到 X 的『团队规矩 / 流程蓝本 / 修复经验包』**"——不曝光 Skill 名字、保留 Slide 5 的揭示感。 |


