# prompt-optimizer

**用户中心的交互式提示词优化技能**

**User-Centered Interactive Prompt Optimizer Skill**

`prompt-optimizer` 是一个用于优化提示词的自定义 AI 技能。它只在用户明确要求优化提示词时启动，通过澄清目标、识别场景、选择优化深度和实时迭代，把原始提示词改写成结构清晰、可直接使用的专业版本。

`prompt-optimizer` is a custom AI skill for prompt optimization. It activates only when the user explicitly asks to optimize a prompt, then clarifies the goal, detects the scenario, selects the right optimization depth, and iterates with the user to produce a clear, ready-to-use professional prompt.

适用于 ChatGPT、Claude、Gemini、Llama、Midjourney、Flux、Stable Diffusion / SD3 以及其他文本、图像、代码和 Agent 类 AI 工具。

Works with ChatGPT, Claude, Gemini, Llama, Midjourney, Flux, Stable Diffusion / SD3, and other text, image, coding, and agent-based AI tools.

## 目录 / Table of Contents

- [核心特性 / Features](#核心特性--features)
- [快速开始 / Quick Start](#快速开始--quick-start)
- [触发方式 / Trigger Phrases](#触发方式--trigger-phrases)
- [优化模式 / Optimization Levels](#优化模式--optimization-levels)
- [适用场景 / Use Cases](#适用场景--use-cases)
- [工作流程 / How It Works](#工作流程--how-it-works)
- [安装 / Installation](#安装--installation)
- [示例 / Examples](#示例--examples)
- [仓库结构 / Repository Structure](#仓库结构--repository-structure)
- [贡献 / Contributing](#贡献--contributing)

## 核心特性 / Features

- **显式触发 / Explicit activation**：只在用户明确提出“优化提示词”相关请求时启动，避免干扰普通对话。
- **三种模式 / Three levels**：支持 Speed（快速）、Medium（均衡，默认）、Expert（专家），适配不同时间和质量要求。
- **场景识别 / Scenario detection**：自动区分写作、图像生成、代码/设计、AI Agent、数据分析等提示词类型。
- **协作迭代 / Collaborative iteration**：先理解目标，再给出优化版和改动说明，并根据反馈继续调整。
- **多模型适配 / Multi-model support**：可用于文本模型、图像模型、代码助手和 Agent 工作流。
- **质量守护 / Quality guardrail**：尊重用户意图，同时避免输出含糊、低质量或不可执行的提示词。

## 快速开始 / Quick Start

1. 安装 `SKILL.md` 到你的 AI 平台技能目录。
2. 在对话中明确提出要优化提示词。
3. 选择 Speed、Medium 或 Expert 模式；如果不指定，默认使用 Medium。
4. 回答必要的澄清问题。
5. 复制最终优化后的提示词到目标 AI 模型中使用。

English quick start:

1. Install `SKILL.md` into your AI platform's skill directory.
2. Explicitly ask the assistant to optimize a prompt.
3. Choose Speed, Medium, or Expert; if omitted, Medium is used by default.
4. Answer the clarification questions.
5. Copy the final optimized prompt into your target AI model.

## 触发方式 / Trigger Phrases

可以使用以下表达触发技能：

Use explicit phrases like:

```text
帮我优化这个提示词
优化提示词
把这个提示词专业化
改进这个提示词
optimize prompt
refine this prompt
make this prompt better
prompt engineering
```

不会触发的情况：

The skill should not activate when:

- 用户只是正常聊天，没有要求优化提示词。
- 用户要求直接完成任务，而不是改写提示词。
- 用户只粘贴内容但没有表达“优化/改进/精炼提示词”的意图。

## 优化模式 / Optimization Levels

| 模式 | 适合情况 | Behavior |
| --- | --- | --- |
| Speed / 快速 | 时间紧，只需要快速可用版本 | Asks 1-2 key questions and returns a concise prompt quickly |
| Medium / 均衡 | 大多数日常使用场景，默认推荐 | Balances speed and quality with moderate clarification |
| Expert / 专家 | 高价值任务，需要深度打磨 | Uses deeper clarification, stronger structure, and more iteration |

## 适用场景 / Use Cases

| 场景 | 优化重点 / What it optimizes |
| --- | --- |
| 写作 / Writing | 受众、语气、结构、细节、故事性、行动建议 |
| 图片生成 / Image Generation | 主体、构图、风格、光线、镜头、负面提示词 |
| 代码与设计 / Code & Design | 技术栈、输入输出、边界情况、测试、可维护性 |
| AI Agent | 角色、工具、步骤、记忆、验证机制、输出格式 |
| 数据分析 / Data Analysis | 数据来源、分析目标、指标定义、图表、洞察总结 |

## 工作流程 / How It Works

1. **确认触发 / Confirm activation**：识别用户是否明确要求优化提示词。
2. **确定模式 / Select level**：按用户指定模式执行；未指定时使用 Medium。
3. **澄清目标 / Clarify intent**：根据模式询问必要问题，理解目标模型、用途、受众、格式和限制。
4. **生成版本 / Draft prompt**：输出可复制的优化提示词，并解释关键改动。
5. **迭代修改 / Iterate**：根据用户反馈继续调整，直到用户确认满意。
6. **最终交付 / Final delivery**：输出最终版提示词，可选提供使用建议或变体。

## 安装 / Installation

将 `SKILL.md` 放入你的 AI 工具或 Agent 平台支持的自定义技能目录中。

Copy `SKILL.md` into the custom skill directory supported by your AI tool or agent platform.

示例路径 / Example paths:

```bash
~/.codex/skills/prompt-optimizer/SKILL.md
~/.claude/skills/prompt-optimizer/SKILL.md
~/.grok/skills/prompt-optimizer/SKILL.md
```

具体路径以你的 AI 环境为准。安装后，使用明确触发语即可调用该技能。

The exact path depends on your AI environment. After installation, use an explicit trigger phrase to activate the skill.

## 示例 / Examples

### 中文示例

```text
帮我优化这个提示词，使用 Expert 模式：

写一篇关于 AI 如何改变教育的文章。
```

可能得到的优化结果：

```text
你是一位长期关注教育科技的中文专栏作者。请为对 AI 感兴趣但没有技术背景的教师和家长，写一篇约 1200 字的文章，主题是“AI 如何改变教育”。

写作要求：
1. 用清晰、亲切、专业但不艰涩的语气。
2. 结构包含：引言、3 个核心变化、具体应用案例、潜在风险、结尾建议。
3. 每个观点都配一个具体场景，避免空泛口号。
4. 最后给出 3 条教师或家长可以立即尝试的行动建议。

输出格式：
- 标题
- 导语
- 正文小标题
- 结尾行动建议
```

### English Example

```text
Optimize this prompt in Medium mode:

Write a product launch email for a new AI note-taking app.
```

Possible optimized result:

```text
You are an experienced SaaS copywriter. Write a concise product launch email for a new AI note-taking app aimed at busy knowledge workers.

Requirements:
1. Use a clear, confident, practical tone.
2. Highlight the core value: faster meeting notes, cleaner summaries, and searchable action items.
3. Include a subject line, preview text, email body, and call to action.
4. Avoid hype and vague claims. Use concrete benefits.
5. Keep the email under 180 words.
```

## 边界 / What This Skill Does Not Do

- 不直接完成用户原始任务；它只优化提示词。
- 不在普通对话中自动介入。
- 不忽略用户反馈，也不强行套用固定模板。
- 不输出含糊、低质量、缺乏结构的提示词。

English:

- It does not complete the original task directly; it optimizes the prompt.
- It does not interrupt normal conversations.
- It does not ignore user feedback or force one fixed template.
- It does not produce vague, low-quality, or unstructured prompts.

## 仓库结构 / Repository Structure

```text
prompt-optimizer/
|-- README.md   # Project overview, installation, usage, examples
`-- SKILL.md    # The actual prompt-optimizer skill definition
```

## 贡献 / Contributing

欢迎提交 Issue 或 Pull Request 来改进触发规则、优化流程、场景分类、示例和多语言表达。

Issues and pull requests are welcome. Useful contributions include better trigger phrases, clearer workflows, more scenario-specific examples, and improved multilingual wording.
