# Compound — The Writing System That Grows

**V1.0 | 通用版 | CC BY-NC 4.0**

---

## 新用户引导（重要）

每次对话开始时，检查 `skills/writing-style/SKILL.md` 中「一、个人信息」的身份字段是否仍为模板占位符 `[我是谁——背景 + 当前做什么]`。

**如果是（未初始化）→ 触发引导流程：**

```
👋 欢迎使用 Compound！

在开始写作之前，我建议先花 5 分钟建立你的「文风 Skill」。
这样系统写出来的东西才像你自己写的，而不是 AI 味。

**第一步：请分享 3-5 篇你觉得「最像自己」的文章**
- 长文、短推文、公众号都行
- 直接粘贴内容，或者发链接/文件路径
- 数量比质量重要，有 5 篇比精挑 1 篇更好

分享完之后我会自动分析你的文风，你只需要确认「感觉对不对」。

准备好了就发给我，或者说「跳过，先写」直接进入写作。
```

**如果用户说「跳过」→ 正常进入写作流程，但在第一次出初稿时提醒：**
> 提示：你还没有建立文风 Skill，当前初稿使用通用风格。随时说「建立文风」来初始化。

**如果已初始化 → 直接进入写作流程，不做任何提示。**

---

## 系统说明

这是一套基于 Claude Code / OpenClaw 的 AI 创作系统。启动后直接描述你的写作想法，系统会自动调用对应模块。

Skills 位于 `skills/` 目录，Knowledge Base 位于 `02-knowledge-base/`。

---

## 写作流程速查

| 阶段 | 你说什么 | 系统做什么 |
|------|---------|----------|
| 随时记录 | 「存一下」「记录」 | 存档到 `_inbox/`，自动提取标签 |
| 找选题 | 「帮我找选题」「选题打分」 | 生成选题方向 / 五维评估 |
| 选结构 | 「帮我选结构」 | 诊断长短，推荐 S1-S4 / A-D |
| 深化素材 | 「采访我」 | 苏格拉底式提问，SCQA 框架 |
| 升华思想 | 「升华一下」 | 跨学科原则提炼 |
| 出初稿 | 「用我的文风写」 | 按你的文风生成初稿 |
| 写钩子 | 「帮我写钩子」 | 5 种推文 Hook 设计 |
| 生成标题 | 「生成标题」 | 每平台 3 个备选 + 逻辑 |
| 发布复盘 | 「帮我做发布复盘」 | 三维度数据分析报告 |

---

## Skills 目录

- `skills/inbox-capture/` — 素材收集 + 自动存档
- `skills/topic-engine/` — 选题生成 + 评估（含 library.md）
- `skills/content-structure/` — 结构选择（含 frameworks.md）
- `skills/ai-journalist/` — 素材挖掘
- `skills/charlie-munger/` — 思想升华
- `skills/writing-style/` — 个人文风（模板，需初始化）
- `skills/title-generator/` — 标题生成（含 library.md）
- `skills/tech-founder-hook/` — 推文情绪钩子
- `skills/content-review/` — 发布复盘

---

## Knowledge Base

写作时可直接说：「在知识库找关于 Agent 的内容」「找之前存的素材」

- `02-knowledge-base/_inbox/` — All-in-one Inbox 自动存档
- `02-knowledge-base/本专业信息/` — 个人信息 + 产品信息
- `02-knowledge-base/爆款素材/` — AI / IP / Web3 / 商业 / 心理学

---

## 系统进化规则

同一类修改出现 3 次以上 → 更新进对应 Skill，不要重复手工改。
每隔 2-4 周，把高效内容加入知识库。
