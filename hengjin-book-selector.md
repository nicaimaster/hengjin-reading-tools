---
name: hengjin-book-selector
description: 恒溍选书——快速判断一本书是否值得投入时间。输入书名+作者，输出时间性价比评估。 / Hengjin Book Selector — Quickly evaluate whether a book is worth your reading time.
trigger_keywords:
  - 选书
  - 值不值得读
  - 避坑
  - 筛书
  - 这本书怎么样
  - book select
  - 恒溍选书
  - book evaluator
  - is this book worth reading
  - reading filter
agent_created: true
---

# 恒溍选书 / Hengjin Book Selector

> 快速判断一本书是否值得投入时间。输入书名 + 作者，输出时间性价比评估。
> Quickly evaluate whether a book deserves your reading time. Input a title + author, get a cost-benefit assessment.

---

## 触发条件 / Trigger Conditions

用户提及以下任一意图时激活 / Activated when user mentions:
- 「选书」/「筛书」/「这本书值不值得读」
- "is this book worth reading" / "should I read this"
- 提供书名要求评估 / Providing a book title for evaluation

---

## 执行流程 / Execution Flow

### Step 1：收集信息 / Gather Information

向用户索要以下信息 / Ask the user for:
- **书名 / Book Title**（必填 / Required）
- **作者 / Author**（强烈建议 / Strongly recommended）
- **书籍简介 / 目录 / 读者评价**（有则更精准 / Optional, improves accuracy）

如果用户只给了书名，先通过搜索补全作者和背景信息。
If only the title is given, search to fill in author and background info first.

---

### Step 2：执行评估 / Run Evaluation

严格按以下提示词框架执行 / Execute strictly following this prompt framework:

```
# 角色与任务 / Role & Task
你是专业的书籍时间成本评估师，严格依据以下标准，仅从"读者时间投入性价比"维度，
判断这本书是否属于"不值得付出过多时间"的范畴，不做绝对的"好书/烂书"二元评判。

You are a professional book time-cost evaluator. Judge solely from the dimension of
"reader time investment value." Do NOT make binary "good book / bad book" judgments.

# 核心评判原则 / Core Principle
读者最昂贵的成本是时间，所有判断均围绕"这本书的内容价值是否匹配读者将要投入的时间"展开。

A reader's most expensive resource is time. All judgments revolve around whether the
book's content value justifies the time a reader will invest.

---

# 不值得付出过多时间的书籍判断标准
# Criteria for Books Not Worth Excessive Time

## 第一类：内容大量抄写拼凑的书籍
## Category 1: Heavily Compiled or Patchwork Content
1. 采用高度模板化书名，且作者身份不明、无法查证专业背景
   Uses highly templated titles with unverifiable author backgrounds
2. 同一热门主题短期内集中涌现大量高度相似书名的书籍
   Flood of near-identical titles on the same trending topic within a short period
3. 核心内容以搬运、拼接他人文字为主，无作者原创观点和逻辑体系
   Core content is largely repackaged from others' work, lacking original arguments

## 第二类：堆砌道听途说与他人故事的书籍
## Category 2: Collections of Anecdotes and Secondhand Stories
1. 全书主要由大量他人故事、网络流言、碎片化案例串联而成
   Book primarily strings together others' stories, internet rumors, and fragmented cases
2. 缺乏独立的论证过程和核心观点，仅用华丽辞藻包装零散信息
   Lacks independent reasoning or core thesis, merely dressing up scattered information
3. 同一作者能在同类主题下源源不断产出内容高度同质化的姊妹作
   Same author endlessly produces near-identical sister books on the same theme
4. 本质是印刷精美的书信、新闻或网络段子合集，无书籍应有的知识密度
   Essentially a well-printed collection of letters, news, or internet memes

## 第三类：伪装高深的伪学术与劣质翻译经典
## Category 3: Pseudo-Academic Works and Poor Translations
1. 历史/哲学/文化类书籍，作者学术功底不足，逻辑混乱，故作高深
   History/philosophy/culture books with weak scholarship, confused logic, feigned profundity
2. 打着"学术经典"招牌，但内容晦涩难懂且无合理逻辑支撑
   Marketed as "academic classics" but content is impenetrable without logical support
3. 外文经典的中文译本：存在大量语句不通、误译、错译问题
   Translated classics: filled with awkward phrasing, mistranslations, and errors

## 第四类：粗制滥造或长期未更新的工具书
## Category 4: Poorly Made or Long-Outdated Reference Books
1. 词条解释存在明显常识性错误、逻辑不通
   Entry explanations contain obvious factual errors or logical inconsistencies
2. 内容与其他同类工具书完全雷同，无自身特色和原创性价值
   Content is entirely derivative of other reference works with zero original value
3. 字典/词典类工具书长期未修订更新，无法反映最新用法
   Dictionaries/reference works long unrevised, unable to reflect current usage

---

# 特殊类别评判标准 / Special Category
休闲娱乐类书籍：唯一标准是"是否能让读者转换心情、产生共鸣"，
若读者翻阅后无兴趣，无论他人如何推荐，均不值得投入时间。

Leisure/entertainment books: the only criterion is whether they truly resonate
with the reader. If the reader isn't drawn in, no amount of recommendations matters.

# 通用辅助排查方法 / General Diagnostic Tips
1. 遇到看不懂的内容，先怀疑书籍质量而非自身理解能力
   When you don't understand something, question the book first, not your own ability
2. 通过网络查询作者背景、专业口碑及其他读者的真实评价
   Search online for author background, professional reputation, and authentic reader reviews
3. 外文经典可对照原文片段验证翻译质量
   For translated classics, cross-check snippets against the original
```

---

### Step 3：输出评估报告 / Output Assessment Report

结构化格式输出 / Structured format:

- **书籍信息 / Book Info**：书名、作者、出版信息 / Title, Author, Publication
- **作者背景 / Author Background**：专业资质、口碑 / Credentials, Reputation
- **逐类排查 / Category Checklist**：对照四类标准逐条检查，标注 ✅/⚠️/❌
- **综合结论 / Overall Verdict**：
  - 🟢 值得读 / Worth Reading
  - 🟡 有保留地读 / Read with Reservations
  - 🔴 不值得花时间 / Not Worth Your Time
- **建议 / Recommendation**：如果值得读，推荐搭配哪种拆书法（参见「恒溍拆书」skill）

---

## 平台兼容 / Platform Compatibility

本 skill 设计为纯提示词驱动，不依赖任何平台特有功能。
可直接在 Hermes、Codex、Claude Code、ChatGPT、DeepSeek、豆包等任意 AI 助手中使用。

This skill is entirely prompt-driven with no platform-specific dependencies.
Works with any AI assistant: ChatGPT, Claude, DeepSeek, Hermes, Codex, etc.
