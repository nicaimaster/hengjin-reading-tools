<p align="center">
  <h1 align="center">恒溍读书工具</h1>
  <p align="center"><strong>Hengjin Reading Tools</strong></p>
  <p align="center">
    <img src="https://img.shields.io/badge/license-MIT-green" alt="License: MIT">
    <img src="https://img.shields.io/badge/platform-Any%20AI-blue" alt="Platform: Any AI">
    <img src="https://img.shields.io/badge/version-1.0.0-orange" alt="Version: 1.0.0">
  </p>
  <p align="center">
    两套 AI 提示词工具：<strong>选书</strong> × <strong>拆书</strong> | 兼容任意 AI 平台<br>
    Two AI prompt tools: <strong>Book Selection</strong> × <strong>Book Breakdown</strong> | Works with any AI assistant
  </p>
</p>

---

## 为什么需要这套工具？ / Why These Tools?

读书最大的成本不是钱，是**时间**。花 20 小时啃一本不值得的书，比买书浪费的 50 块钱代价大得多。

The biggest cost of reading is not money — it's **time**. Spending 20 hours on the wrong book costs far more than wasting ¥50 on a bad purchase.

这套工具解决两个核心问题 / These tools solve two core problems:

| 问题 / Problem | 工具 / Tool | 解决方式 / Solution |
|------|------|---------|
| 这本书值不值得读？ / Is this book worth reading? | [恒溍选书 / Book Selector](./hengjin-book-selector.md) | 5 分钟避坑评估 / 5-min evaluation |
| 这本书怎么高效读？ / How to read it efficiently? | [恒溍拆书 / Book Dismantler](./hengjin-book-dismantler.md) | 9 种名家读书法自动匹配 / 9 methods auto-matched |

---

## 工具一：恒溍选书 / Tool 1: Book Selector

**文件 / File**：[`hengjin-book-selector.md`](./hengjin-book-selector.md)

从时间投入性价比维度快速判断一本书是否值得读。

Quickly evaluate whether a book is worth your reading time from a cost-benefit perspective.

### 输入 / Input
- 书名 / Book Title（必填 / Required）
- 作者 / Author（强烈建议 / Strongly recommended）

### 输出 / Output
- 🟢 值得读 / Worth Reading | 🟡 有保留地读 / Read with Reservations | 🔴 不值得 / Not Worth Your Time
- 四类排查报告（内容拼凑、道听途说、伪学术、劣质工具书）
- Four-category checklist: compiled content, secondhand anecdotes, pseudo-academic, poor references
- 如值得读，推荐匹配的拆书法 / If worth reading, recommends a dismantling method

### 示例 / Example

```
输入 / Input：《纳瓦尔宝典》- Eric Jorgenson
输出 / Output：🟢 值得读 / Worth Reading
  - 内容拼凑排查 / Compiled content：✅ 通过 / Passed
  - 道听途说排查 / Secondhand anecdotes：⚠️ 部分章节偏碎片化 / Some chapters are fragmented
  - 伪学术排查 / Pseudo-academic：✅ 通过 / Passed
  - 建议 / Recommendation：搭配「分层取舍阅读法」精读核心章节
    Pair with "Layer & Filter" method, focus on core chapters
```

---

## 工具二：恒溍拆书 / Tool 2: Book Dismantler

**文件 / File**：[`hengjin-book-dismantler.md`](./hengjin-book-dismantler.md)

9 位中国名家读书法合集，根据你的读书目标自动匹配最优方法。

A collection of 9 classical reading methods from Chinese scholars. Auto-matched to your reading goal.

| # | 方法 / Method | 来源 / Origin | 一句话 / One-Liner | 适用场景 / Best For |
|---|------|------|--------|---------|
| 1 | 学以致用 / Apply | 江恒源 Jiang Hengyuan | 读完要能用 / Read to use | 实用/方法类 / Practical books |
| 2 | 分层取舍 / Filter | 李泽厚 Li Zehou | 跳过废话，只拿干货 / Skip fluff | 学术专著 / Academic works |
| 3 | 观大略 / Big Picture | 诸葛亮 Zhuge Liang | 30分钟全局认知 / 30-min overview | 通识/入门 / Introductory books |
| 4 | 八面受敌 / Eight Angles | 苏轼 Su Shi | 多维度彻底吃透 / Multi-angle mastery | 复杂著作 / Complex works |
| 5 | 科学治学 / Scholarly | 梁启超 Liang Qichao | 做研究、找真相 / Research & verify | 国学/历史 / Classical texts |
| 6 | 课题驱动 / Thesis | 王云五 Wang Yunwu | 带着问题读 / Question-driven | 任何书 / Any book |
| 7 | 求证 / Verify | 钱钟书 Qian Zhongshu | 别被书骗了 / Cross-examine | 争议性著作 / Controversial works |
| 8 | 结合 / Triangulate | 老舍 Lao She | 三维拆解 / 3D analysis | 文学作品 / Literature |
| 9 | 精解知明 / Internalize | 冯友兰 Feng Youlan | 选→释→悟→评 / Digest & own it | 经典/教材 / Classics |

### 自动匹配逻辑 / Auto-Matching Logic

| 你说 / You Say | 自动匹配 / Auto-Matched |
|------|---------|
| 「读完要用」「学这个技能」 / "I need to use this" | → 学以致用 / Apply What You Learn |
| 「太长了帮我提炼」 / "Too long, extract key points" | → 分层取舍 / Layer & Filter |
| 「快速了解这个领域」 / "Quick overview" | → 观大略 / Grasp the Big Picture |
| 「彻底吃透」「深度学习」 / "Master this deeply" | → 八面受敌 / Attack from Eight Angles |
| 「做研究」「写论文」 / "Research, write a paper" | → 科学治学 / Scholarly Rigor |
| 「围绕XX问题读」 / "Read around question X" | → 课题驱动 / Thesis-Driven |
| 「这本书说的对不对」 / "Is this book correct?" | → 求证 / Verify & Cross-Examine |
| 「文学名著」「小说」 / "Literary classic, novel" | → 结合 / Triangulate |
| 「啃经典」「内化」 / "Digest a classic" | → 精解知明 / Interpret & Internalize |

### 完整示例 / Full Examples

#### 示例 1：快速入门新领域 / Quick Field Introduction

```
用户 / User：「帮我快速了解认知心理学」
AI 执行 / Execution：
  1. 锁定「观大略」模式 / Lock "Big Picture" mode
  2. 萃取核心概念：认知过程、注意、记忆、语言、思维、决策
     Extract core concepts: cognition, attention, memory, language, thinking, decision-making
  3. 输出学科框架图 + 各分支定义 + 推荐进阶路径
     Output: discipline map + branch definitions + learning path
```

#### 示例 2：深度学习经典 / Deep Dive into a Classic

```
用户 / User：「彻底吃透《思考，快与慢》」

AI 执行（八面受敌法） / Execution (Eight Angles):
  第1轮 / Round 1：核心观点 / Core thesis（System 1 vs System 2）
  第2轮 / Round 2：认知偏差清单 / Cognitive biases（anchoring, availability, framing…）
  第3轮 / Round 3：案例拆解 / Case analysis（Linda problem, Asian disease…）
  第4轮 / Round 4：争议与批评 / Controversies（Kahneman vs Gigerenzer）
  第5轮 / Round 5：跨领域应用 / Cross-domain applications（investing, medicine, policy）
  最终整合 → 完整知识图谱 / Final integration → knowledge map
```

#### 示例 3：读完就要用 / Read to Apply

```
用户 / User：「《非暴力沟通》读完了，帮我提炼方法论」

AI 执行（学以致用读书法） / Execution (Apply What You Learn):
  1. 结构化表解 / Structured framework：4-step communication model
  2. 要点摘录 / Key points：Observe → Feel → Need → Request
  3. 应用场景 / Application scenarios：workplace, relationships, conflict resolution
  4. 专属笔记 / Personal notes：reflections + transferable practices
```

---

## 快速开始 / Quick Start

### 方式一：直接复制 / Option 1: Copy & Paste

1. 打开 [hengjin-book-selector.md](./hengjin-book-selector.md) 或 [hengjin-book-dismantler.md](./hengjin-book-dismantler.md)
   Open either file
2. 复制文件中的提示词 / Copy the prompt
3. 粘贴到任意 AI 对话窗口（ChatGPT / Claude / DeepSeek / 豆包 等）
   Paste into any AI assistant
4. 附上你要读的书的信息（全文 > 章节 > 摘要 > 书名）
   Attach your book content (full text > chapters > summary > title only)

### 方式二：安装为 AI Skill / Option 2: Install as AI Skill

```bash
# Claude Code / Codex / Hermes
cp hengjin-*.md ~/.workbuddy/skills/
```

### 效果递减法则 / Effectiveness Hierarchy

提供的书籍信息完整度直接影响分析质量 / Input completeness directly affects output quality：

```
全书完整原文 > 关键章节 > 详细摘要 + 目录 > 仅目录 > 仅书名
Full text > Key chapters > Detailed summary + TOC > TOC only > Title only
```

---

## 设计哲学 / Design Philosophy

1. **纯提示词驱动 / Prompt-Only**：不依赖 API、插件或平台特性，不受平台锁定
   No APIs, plugins, or platform lock-in required
2. **名家方法论溯源 / Verifiable Origins**：每种方法均有明确的学术/文化来源
   Every method has a traceable scholarly or cultural origin
3. **按需匹配 / Goal-Matched**：根据目标自动选择最优路径，不预设「唯一正确」的读书方式
   Auto-selects the optimal method for your goal — no "one right way" assumption
4. **平台无关 / Platform-Agnostic**：同一套提示词在 DeepSeek 和 Claude 上都能工作
   Same prompts work across DeepSeek, Claude, ChatGPT, and others

---

## 学术溯源 / Scholarly Origins

| 方法 / Method | 来源 / Origin | 出处 / Source |
|---------|------|------|
| 学以致用 / Apply | 江恒源 Jiang Hengyuan | 《怎样读书》「对于读书问题的我见」(1935) |
| 分层取舍 / Filter | 李泽厚 Li Zehou | 《读书与写文章》（《李泽厚散文集》） |
| 观大略 / Big Picture | 诸葛亮 Zhuge Liang | 裴松之注《三国志·诸葛亮传》引《魏略》 |
| 八面受敌 / Eight Angles | 苏轼 Su Shi | 《又答王庠书》（《经进东坡文集事略》） |
| 科学治学 / Scholarly | 梁启超 Liang Qichao | 《古今名人读书法》（《饮冰室合集》） |
| 课题驱动 / Thesis | 王云五 Wang Yunwu | 王云五读书方法体系 |
| 求证 / Verify | 钱钟书 Qian Zhongshu | 钱钟书治学方法论 |
| 结合 / Triangulate | 老舍 Lao She | 老舍谈读书与写作 |
| 精解知明 / Internalize | 冯友兰 Feng Youlan | 四字读书法（《三松堂全集》） |

---

## FAQ

**Q: 这些提示词在 Claude 上好用还是 DeepSeek 上好用？ / Which model works best?**

A: 提示词本身与平台无关。推理能力越强的模型（Claude 3.5 Sonnet、GPT-4、DeepSeek R1），分析深度越好。
The prompts are platform-agnostic. Stronger reasoning models produce deeper analysis.

**Q: 我能只用书名就让 AI 拆书吗？ / Can I just give a book title?**

A: 能，但效果差很多。书名只能触发 AI 的训练记忆，不是真正的「读这本书」。输入全文或章节效果最佳。
Yes, but much less effective. A title only triggers the AI's training memory — it's not truly "reading the book."

**Q: 和 Readwise / Notion AI 有什么区别？ / How is this different from Readwise or Notion AI?**

A: 那些是工具，这个是方法论。你可以把这里的提示词和任何阅读工具组合使用。
Those are tools; this is methodology. You can combine these prompts with any reading tool.

**Q: 可以贡献新方法吗？ / Can I contribute new methods?**

A: 欢迎 PR。请确保新方法有明确的学术/文化来源，并遵循现有提示词格式。
PRs welcome. Please ensure new methods have verifiable scholarly origins and follow the existing prompt format.

---

## 相关项目 / Related Projects

- [十套读书拆解提示词](./十套读书拆解提示词.md) — 10 种方法的单文件快速参考 / Single-file quick reference

---

## License

MIT © 恒溍
