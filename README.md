# Macroeconomics Revision Site

A **zero-dependency, zero-build, fully offline** study site for an undergraduate
*Principles of Macroeconomics* course — 12 lecture walkthroughs, 11 problem sets,
an interactive quiz engine, and a reverse index that lets you look things up by
*variable* rather than by lecture.

**→ [Live site](https://YOUR-USERNAME.github.io/eco120-macro-revision/)**

No CDN, no external fonts, no framework, no bundler. 27 HTML files and one
stylesheet. Double-click any page and it works — on a plane, on a locked-down
exam-prep laptop, or on GitHub Pages.

---

## Why it's built this way

| Decision | Reason |
|---|---|
| **53 hand-authored inline SVG diagrams** | Economics diagrams are only worth marks when the axes, every curve, the initial equilibrium E₀, the new equilibrium E₁ and the shift arrows are all labelled. Inline SVG stays sharp at any zoom, is searchable as text, and adds no binary assets to the repo. |
| **Vanilla JS, no framework** | The quiz engine (instant marking, wrong-answers-only filter, reset) and the hub's keyword search are a few dozen lines each. A framework would introduce a build step and break the "double-click to open" property. |
| **One stylesheet, CSS custom properties** | A single dark palette defined once; 27 pages share the same component classes — cards, formula blocks, callouts, collapsible answers. |
| **Answers collapsed by default** (`<details>`) | Deliberate learning design: you must attempt a question before the answer is reachable. Reading a worked solution feels like understanding; reproducing it is the only proof. |
| **Chinese explanations, English terminology** | The course is taught and examined in English. Prose explanations are in the reader's first language for speed, while every technical term, formula and model answer stays in English — because that is what has to be written under exam conditions. |

## What's inside

**12 lecture pages** — each one covers the through-line of the lecture (why these
topics, how they connect to the neighbouring lectures), a section-by-section
walkthrough, a formula quick-reference, an "exam focus & common traps" list, and
at least one full worked answer in English.

**11 tutorial pages** — questions, collapsible reference answers, and a structural
commentary explaining how each question should be organised under exam conditions
and where the marks actually sit.

**Interactive MCQ drill** (`mcq-drill.html`) — 56 self-authored questions targeting
the details that are easy to get backwards: which way the money multiplier moves,
what counts inside a monetary aggregate, whether a change shifts a curve or moves
along it. Instant marking, a wrong-answers-only filter, and every question links
back to the page that teaches it.

**Reverse variable index** (`variable-index.html`) — exam questions ask
*"interest rates rise; what happens to investment?"*, which is a lookup by
**variable**, not by lecture. Six core variables (I, C, M, π, U, exchange rate),
each with: what it depends on, which policies move it and in which direction,
which diagram it lives on, and the traps. Plus five transmission chains.

**Hub with client-side search** (`index.html`) — filter all 23 lecture/tutorial
pairs by keyword.

## The answer standard

Every worked answer on the site follows the four-part structure that British
economics marking schemes reward:

1. **Define** — precise one-sentence definitions of every technical term, the key
   formulas, and an explicit statement of the model's assumptions
   (closed/open economy, fixed/flexible prices, short run/long run).
2. **Diagram** — axes, curve names, E₀, E₁ and shift arrows all labelled, *plus*
   prose in the body text saying what the diagram shows. A diagram left to speak
   for itself scores less than one that is narrated.
3. **Analyse** — a step-by-step causal chain with the mechanism given at every
   step and no skipped links, distinguishing short run from long run, impact
   effect from final effect, and nominal from real.
4. **Conclude** — answer the question in its own words, state the direction and
   size of the net effect, and name the conditions it depends on.

## Running it locally

```bash
git clone https://github.com/YOUR-USERNAME/eco120-macro-revision.git
```

Then open `index.html` in any browser. That's the whole setup — there is nothing
to install and nothing to build.

If you prefer to serve it over HTTP:

```bash
python3 -m http.server 8000
```

## Structure

```
.
├── index.html            # hub, with client-side keyword search
├── assets/style.css      # single shared stylesheet (dark theme)
├── lectures/             # lecture-01 … lecture-12
├── tutorials/            # tutorial-01 … tutorial-11
├── mcq-drill.html        # 56-question interactive quiz engine
└── variable-index.html   # reverse index by economic variable
```

## Attribution and scope

This repository contains **personal study notes**: my own explanations, diagrams,
commentary and self-authored practice questions, written while studying the
subject.

Course slides, lecture handouts and the set textbook
(Begg, Vernasca, Fischer & Dornbusch, *Economics*) remain the copyright of their
respective owners. **No lecture slides, no textbook material, no past examination
papers and no examination content are included in this repository.** Reference
answers on the tutorial pages are summaries written for study purposes and should
not be treated as an official answer key.

Shared in case the explanations or the diagrams are useful to someone else. If you
are a rights holder and would like something removed, please open an issue.

---

<a name="chinese"></a>

# 宏观经济学复习站点

一套**零依赖、零构建、完全离线**的本科《宏观经济学原理》学习站点：12 讲逐节讲解、
11 次习题课、交互式刷题引擎，以及一份**按变量反查**（而非按讲次查）的索引。

**→ [在线访问](https://YOUR-USERNAME.github.io/eco120-macro-revision/)**

没有 CDN、没有外部字体、没有框架、没有打包器。27 个 HTML 文件加一份样式表，
**双击任何一页就能打开**——断网可用，放上 GitHub Pages 也可用。

## 为什么这样造

| 设计决策 | 原因 |
|---|---|
| **53 张全手写内联 SVG** | 经济学图必须标全坐标轴、每条曲线、初始均衡 E₀、新均衡 E₁ 和移动箭头才有分。内联 SVG 任意缩放都清晰、可被文本搜索，且不给仓库引入二进制资源。 |
| **原生 JS，不用框架** | 刷题引擎（即时判分 / 错题过滤 / 重做）和总目录搜索各只需几十行。引入框架就会带来构建步骤，破坏「双击即用」这个前提。 |
| **单一样式表 + CSS 自定义属性** | 深色主题色板集中定义一次，27 个页面共享同一套组件类：卡片、公式框、提示条、折叠答案。 |
| **答案默认折叠**（`<details>`） | 刻意的学习设计：必须先自己做，答案才够得着。读懂一份解答的感觉很像会了，但只有能复现出来才算数。 |
| **讲解用中文，术语与范例用英文** | 课程用英文授课与考试。解释用母语理解更快，但所有术语、公式和答题范例保持英文——因为考场上要写的就是英文。 |

## 里面有什么

**12 个讲次页面** —— 每页包含本讲逻辑主线（为什么讲这些、和上下讲怎么衔接）、
逐节讲解、公式速查、考点与陷阱，以及至少一个完整的英文答题范例。

**11 个习题课页面** —— 题目、可折叠的参考解答，以及**答题结构点评**：这道题在考试中
该怎么组织、分数具体落在哪里。

**交互式 MCQ 特训**（`mcq-drill.html`）—— 56 道自制题，专攻容易记反的细节：货币乘数
往哪个方向动、某个数该不该算进某个货币口径、一个变化是让曲线平移还是沿线移动。
即时判分、错题过滤，每题都链接回讲解它的页面。

**变量反向索引**（`variable-index.html`）—— 考题问的是**「利率上升，投资会怎样？」**，
这是按**变量**查而不是按讲次查。六个核心变量（I、C、M、π、U、汇率）各自列出：
依赖什么、什么政策能动它及方向、对应哪张图、有什么陷阱，另附五条传导链。

**带搜索的总目录**（`index.html`）—— 关键词筛选全部 23 个讲次/习题页面。

## 答题标准

站内所有范例都遵循英式经济学评分标准认可的四段结构：

1. **Define 定义** —— 用一句精确的英文定义每个术语，写出关键公式，并明确说明模型假设
   （封闭/开放经济、价格黏性/弹性、短期/长期）。
2. **Diagram 图形** —— 坐标轴、曲线名、E₀、E₁、移动箭头全部标注，**并且**在正文中用文字
   交代图上发生了什么。只放一张图让考官自己看，比配上文字说明的图拿分低。
3. **Analyse 分析** —— 逐步因果链，每一步都给出机制、不跳步，并区分短期与长期、
   即期效应与最终效应、名义与实际。
4. **Conclude 结论** —— 用题目本身的措辞作答，说明净效应的方向与大小，
   并指出它依赖什么条件。

## 本地运行

克隆后直接用浏览器打开 `index.html` 即可——不需要安装任何东西，也没有构建步骤。

## 内容与版权说明

本仓库是**个人学习笔记**：其中的讲解、图形、点评与自制练习题均为作者本人所写。

课程课件、讲义与教材（Begg, Vernasca, Fischer & Dornbusch, *Economics*）版权归各自
权利人所有。**本仓库不包含任何课件、教材内容、历年试卷或考试材料。**
习题页上的参考解答为学习用途的整理与归纳，不应被当作官方答案。

分享出来，是想着这些讲解或图形也许对别人有用。如果您是权利人并希望移除某部分内容，
请提交 issue。
