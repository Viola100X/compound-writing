# Compound — The Writing System That Grows

**V1.0 | 通用版 | CC BY-NC 4.0**

---

## 交互协议（所有 Skill 共用）

### 提问格式

每次向用户提问或引导下一步时，必须按 `skills/_templates/ask-format.md` 的 4 部分结构输出：
1. **定位**：当前在哪，刚完成了什么
2. **下一步**：大白话解释接下来要做什么
3. **建议**：推荐一个选项 + 理由
4. **选项**：A/B/C 字母编号

### 进度面板

每个阶段转换时，展示 `skills/_templates/progress-panel.md` 的进度面板，让用户始终知道自己在哪。

### 阶段导航

每个阶段完成后，提供三个选项：
- A) 继续 → 下一阶段
- B) 跳到 → 指定阶段
- C) 暂停 → 下次继续

### 结束面板

当用户完成完整流程或说「结束」时，展示 `skills/_templates/closing.md` 的三段式结束面板。

---

## 新用户引导

每次新对话开始时，按以下顺序检查：

### 第一步：检查 Personal OS

检查 `skills/personal-os/SKILL.md` 中品牌定位模块是否完成。

**如果未完成 → 触发引导（遵循交互协议）：**

```
欢迎使用 Compound！

Compound 的核心理念是：先知道你是谁，再开始写作。
所以第一步先花几分钟建立你的 Personal OS。

建议：从品牌定位开始，5 分钟就能完成，后续所有内容都会更精准。

A) 开始品牌定位（5 分钟）
B) 跳过，直接进入写作（使用通用风格）
C) 先看看系统有什么功能
```

**如果 Personal OS 已完成但文风未初始化：**
在第一次出初稿时提醒：
> 你还没有建立文风 Skill，当前初稿使用通用风格。随时说「建立文风」来初始化。

**如果都已完成 → 直接进入写作流程，不做任何提示。**

---

## 写作流程

> 这是一张地图，不是死板流程。从任意节点进入，跳过任意步骤。

```
Personal OS（一次性初始化）
    ↓
日常创作循环：
收集 → 选题 → 选结构 → 深化 → 初稿 → 标题/钩子 → 发布 → 复盘
```

| 阶段 | 你说什么 | 系统做什么 | Skill |
|------|---------|----------|-------|
| 初始化 | 「初始化」「我是谁」 | 品牌定位 + 经历素材库 + 文风 | `personal-os` |
| 随时记录 | 「存一下」「记录」 | 存档到 `_inbox/`，自动提取标签 | `inbox-capture` |
| 找选题 | 「帮我找选题」「选题打分」 | 生成选题方向 / 五维评估 | `topic-engine` |
| 选结构 | 「帮我选结构」 | 诊断长短，推荐 S1-S4 / A-D | `content-structure` |
| 深化素材 | 「采访我」 | 苏格拉底式提问，SCQA 框架 | `ai-journalist` |
| 升华思想 | 「升华一下」 | 跨学科/哲学/奥派三种模式 | `thought-elevation` |
| 出初稿 | 「用我的文风写」 | 按你的文风生成初稿 | `writing-style` |
| 标题/钩子 | 「生成标题」「帮我写钩子」 | 钩子诊断 + 标题/封面文案优化 | `title-generator` |
| 发布复盘 | 「帮我做发布复盘」 | 三维度数据分析报告 | `content-review` |

### 流程中的 Skill 调用规则

1. 用户说出触发词 → 读取对应 Skill 的 SKILL.md → 按其中的流程执行
2. 每个 Skill 执行完毕 → 展示进度面板 → 提供导航选项
3. 用户可以随时说「跳过」「下一步」「暂停」

---

## Skills 目录

| # | Skill | 路径 | 说明 |
|---|-------|------|------|
| 0 | `personal-os` | `skills/personal-os/` | 个人品牌操作系统 |
| 1 | `inbox-capture` | `skills/inbox-capture/` | 素材收集 + 自动存档 |
| 2 | `topic-engine` | `skills/topic-engine/` | 选题生成 + 评估（含 library.md） |
| 3 | `content-structure` | `skills/content-structure/` | 结构选择（含 frameworks.md） |
| 4 | `ai-journalist` | `skills/ai-journalist/` | 素材挖掘 |
| 5 | `thought-elevation` | `skills/thought-elevation/` | 思想升华（跨学科/理论透镜/奥派） |
| 6 | `writing-style` | `skills/writing-style/` | 个人文风（模板，需初始化） |
| 7 | `title-generator` | `skills/title-generator/` | 钩子 + 标题 + 封面文案（三合一） |
| 8 | `content-review` | `skills/content-review/` | 发布复盘 |
| — | `_templates` | `skills/_templates/` | 交互格式模板（不直接调用） |

---

## Knowledge Base

写作时可直接说：「在知识库找关于 Agent 的内容」「找之前存的素材」

知识库目录 `02-knowledge-base/` 在首次使用 `inbox-capture` 时自动创建。

---

## 系统进化规则

同一类修改出现 3 次以上 → 更新进对应 Skill，不要重复手工改。
每隔 2-4 周，把高效内容加入知识库。
