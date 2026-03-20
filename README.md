# Compound

### The Writing System That Grows

> 一套会自我进化的 AI 创作系统。每发一篇内容，系统就比上次更懂你。

`Claude Code` `OpenClaw` `9 Skills` `开源` `CC BY-NC 4.0`

---

## Why Compound

**1. 不是提示词模板集**
大多数 AI 写作工具解决的是「这一次」的问题。Compound 解决的是「每一次都比上次好」的问题。你的发布数据、写作习惯、文风偏好，都会沉淀进系统。

**2. 为有话说的人设计**
如果你是创始人、Builder、行业专家——你不缺观点，缺的是把观点变成能传播的内容。Compound 不替你思考，它帮你把已有的想法结构化、深化、表达出来。

**3. 随时随地收集，坐下来就能写**
在手机上看到灵感？发一条消息就自动存档。打开电脑准备写？搜索之前存的素材，直接进入创作流程。

---

## 系统架构

```
     ┌─────────────────────────────────────────────────────────────┐
     │                                                             │
     │   ① 收集          ② 选题         ③ 创作         ④ 发布     │
     │                                                             │
     │   随时随地     →   找到方向   →   结构化写作  →  优化发布   │
     │   发消息存档       评估打分       深化+初稿       标题+钩子  │
     │                                                             │
     │   inbox-capture    topic-engine   ai-journalist   title-gen  │
     │                                   charlie-munger  hook       │
     │                                   writing-style              │
     │                                   content-struct             │
     │                                                             │
     │   ⑤ 复盘                                                    │
     │   数据分析 → 反哺知识库 → 下次创作更精准                     │
     │   content-review                                            │
     │                                                             │
     └─────────────────────────────────────────────────────────────┘
```

### 三个层次

| 层 | 内容 | 作用 |
|---|------|------|
| **Skills** | 9 个专项能力模块 | 选题、结构、深化、文风、标题、钩子、复盘、素材收集 |
| **Knowledge Base** | 行业素材 + 爆款样本 + 你的 Inbox | AI 创作时自动调用，不用手动复制粘贴 |
| **创作管道** | inbox → draft → published → archive | 内容从想法到发布的完整路径 |

---

## Quick Start

### 方式一：Claude Code

```bash
git clone https://github.com/rommn/compound.git
cd compound
claude
```

打开后直接说你的写作想法，系统自动调用对应 Skill。

### 方式二：OpenClaw

```bash
# 方法 A：从 ClawHub 安装
clawhub install compound

# 方法 B：直接发 GitHub 链接到 OpenClaw 聊天窗口
https://github.com/rommn/compound
```

安装后，在任意聊天频道发消息即可使用。支持文字和语音输入。

### 第一件事：建立你的文风

```
你：帮我建立文风
Claude：请提供 3-5 篇你觉得最像自己的文章...
```

5 分钟内完成，之后所有初稿都会匹配你的风格。

---

## Skills 速查

| 类别 | Skill | 你说 | 系统做 |
|------|-------|------|--------|
| **收集** | `inbox-capture` | 「存一下」「记录」 | 文字/语音自动存档到知识库，创作时可搜索 |
| **选题** | `topic-engine` | 「帮我找选题」「选题打分」 | 生成选题方向 / 五维评估现有想法 |
| **结构** | `content-structure` | 「帮我选结构」 | 诊断长短文，推荐 S1-S4 / A-D 结构 |
| **深化** | `ai-journalist` | 「采访我」 | 苏格拉底式提问，挖掘素材，输出 SCQA 框架 |
| **深化** | `charlie-munger` | 「升华一下」 | 跨学科思想升华，提炼普遍原则 |
| **文风** | `writing-style` | 「用我的文风写」 | 基于你的语料生成匹配你风格的初稿 |
| **标题** | `title-generator` | 「生成标题」 | 每平台 3 个备选 + 底层逻辑（100+ 模板库） |
| **钩子** | `tech-founder-hook` | 「帮我写钩子」 | 5 种开头钩子 + AI 感句式识别修改 |
| **复盘** | `content-review` | 「帮我做发布复盘」 | 三维度数据分析：整体 → 爆款拆解 → 规划 |

---

## 创作流程

> 这是一张地图，不是死板流程。从任意节点进入，跳过任意步骤。

### Phase 0：收集素材
随时在 OpenClaw 或 Claude Code 中发送想法、链接、语音。系统自动存档，创作时搜索调用。

### Phase 1：选题 → 选结构
说出你的想法，系统先用 `topic-engine` 评估选题质量，再用 `content-structure` 推荐最优结构。

### Phase 2：深化内容
两个工具可选：`ai-journalist` 通过提问挖掘素材；`charlie-munger` 把洞察升华为普遍原则。

### Phase 3：出初稿 → 打磨
`writing-style` 基于结构和文风生成初稿。你主导多轮修改，`tech-founder-hook` 专门处理开头。

### Phase 4：发布优化
`title-generator` 生成标题，每平台 3 个备选。

### Phase 5：数据复盘
`content-review` 分析发布数据，高效内容沉淀进知识库，让下次创作更精准。

---

## All-in-one Inbox

Compound 的独特能力：**随时收集，坐下来就能写**。

```
对话中说「存一下：[你的想法]」
        ↓
  AI 自动提取标签，存为 Markdown
        ↓
02-knowledge-base/_inbox/
        ↓
  创作时说「找关于 X 的素材」
        ↓
  进入创作流程
```

支持的输入：
- **文字消息**：对话中说「存一下」+ 内容，自动提取标签存档
- **语音消息**：OpenClaw 用户发语音，内置 Whisper 自动转文字后存档

详见 `skills/inbox-capture/` 的完整说明。

---

## 建立你的文风 Skill

文风 Skill 是 Compound 的核心差异化——让 AI 写出来的东西像你自己写的。

### 三步完成

1. **提供语料**：3-5 篇你觉得「最像自己」的文章
2. **AI 自动分析**：提取思维模式、语言习惯、句式特征
3. **你确认感觉**：对了就用，不对只调句式

### 四模块结构

| 模块 | 谁填 | 内容 |
|------|------|------|
| 个人信息 | 你 | 身份、读者、写作目标（5分钟） |
| 思维模式 | AI | 叙事弧线、论证偏好、世界观 |
| 句式校准 | AI + 你 | 句长、特有词汇、禁止清单 |
| 迭代记录 | 自动 | 每次改稿的规律更新 |

模板位置：`skills/writing-style/SKILL.md`

---

## 系统进化

Compound 不是静态工具。三条路径让它越用越好：

**Skills 迭代**：同一类修改出现 3 次以上 → 更新进对应 Skill，不再重复手工改。

**知识库扩充**：每 2-4 周，把高效内容加入 knowledge-base。AI 创作时自动参考。

**文风进化**：随着你发布更多内容，文风 Skill 会持续校准，输出越来越接近你的真实风格。

---

## 文件结构

```
compound/
├── README.md                       ← 你现在在这里
├── CLAUDE.md                       ← Claude Code 配置
├── TERMS.md                        ← CC BY-NC 4.0 许可
├── 01-创作管道/                     ← 内容生命周期管理
│   ├── 01-inbox/                   ← 碎片想法
│   ├── 02-draft/                   ← 草稿
│   ├── 03-published/               ← 已发布
│   └── 04-archive/                 ← 归档
├── 02-knowledge-base/              ← 知识库
│   ├── _inbox/                     ← All-in-one Inbox 存档
│   ├── 本专业信息/                  ← 你的背景、产品信息
│   └── 爆款素材/                    ← AI / IP / Web3 / 商业 / 心理学
├── skills/                      ← 9 个专项能力模块
│   ├── inbox-capture/              ← 素材收集 + 存档
│   ├── topic-engine/               ← 选题生成 + 评估（含 library.md）
│   ├── content-structure/          ← 结构诊断（含 frameworks.md）
│   ├── ai-journalist/              ← 素材挖掘 + SCQA 框架
│   ├── charlie-munger/             ← 思想升华
│   ├── writing-style/              ← 个人文风（模板，你来定制）
│   ├── title-generator/            ← 标题生成（含 library.md）
│   ├── tech-founder-hook/          ← 推文情绪钩子
│   └── content-review/             ← 发布复盘分析
└── 04-发布复盘/                     ← 数据记录与优化
```

---

## 与传统方案的区别

| 维度 | 传统 AI 写作 | Compound |
|------|------------|----------|
| 素材 | 手动搜集复制粘贴 | 随时发消息存档，AI 自动调用 |
| 选题 | 靠灵感，碰运气 | 50 个选题公式 + 五维评分 |
| 结构 | 凭感觉写 | 8 种爆款结构，数据验证 |
| 文风 | 每次靠运气 | 文风 Skill 保证 DNA 稳定 |
| 深度 | 想到哪写到哪 | 记者式提问 + 跨学科升华 |
| 进化 | 用多少年都一样 | 每次使用都在喂数据 |

---

## License

本项目采用 [CC BY-NC 4.0](https://creativecommons.org/licenses/by-nc/4.0/) 许可证。

你可以自由使用、修改、分享，但不可用于商业用途。

---

*由 [Viola](https://x.com/aspect_viola) 创建 | the 1% Founder Program | 基于 Claude Code 构建*

*每一篇发出去的内容，都是对这套系统的一次训练。*
