# study-skills

面向大学学习、工科备考与有据写作的跨平台 AI Agent Skills 合集（兼容 Claude Code、Codex、Cursor、Antigravity 等支持 `SKILL.md` 开放标准的工具）。

A curated collection of Agent Skills for bilingual STEM studying, interactive HTML+KaTeX+SVG lecture cards, and evidence-grounded academic writing.

---

## 包含技能一览

| Skill 名称 | 定位 | 核心特性 | 路径 |
| --- | --- | --- | --- |
| **`stem-study-tutor`** | 理工科全能双语导师 | 课件逐页三档精讲（大白话 100% 独立包揽）、原版课本视觉降维、中英真题带练（简单词汇减负 + Method Marks 步骤分保护）、错题定位、手写笔记/波形图看图解题 | [skills/stem-study-tutor](skills/stem-study-tutor/SKILL.md) |
| **`dual-track-html-notes`** | 双轨 HTML + SVG 讲义生成器 | 生成前强制全景复盘；输出单文件 HTML 讲义（KaTeX 公式 + 手绘原生 SVG 矢量图 + 单卡筛选 + `Esc` 一键纯净截图模式）并在聊天框同步输出 1:1 Markdown | [skills/dual-track-html-notes](skills/dual-track-html-notes/SKILL.md) |
| **`book-grounded-writing`** | 长书与史料有据写作 | 先建章节证据表与页码出处再起草，严格区分史料原意、作者解释与自身推论，杜绝编造页码与引文 | [skills/book-grounded-writing](skills/book-grounded-writing/SKILL.md) |

---

## 快速安装 (Installation)

### 方式一：命令行一键安装（推荐）

安装本仓库全部 3 个技能：

```bash
npx skills add Xi-Bei-70/study-skills
```

也可以按需只装单个技能：

```bash
npx skills add Xi-Bei-70/study-skills@stem-study-tutor
npx skills add Xi-Bei-70/study-skills@dual-track-html-notes
npx skills add Xi-Bei-70/study-skills@book-grounded-writing
```

### 方式二：手动复制到客户端技能目录

克隆本仓库后，把 `skills/` 下的对应文件夹复制到你使用的 AI 助手全局或项目技能目录即可：

| 客户端 | 常见技能目录 |
| --- | --- |
| **Claude Code** | `~/.claude/skills/` 或 `<项目>/.claude/skills/` |
| **Codex** | `~/.codex/skills/` |
| **Cursor** | `~/.cursor/skills/` 或 `<项目>/.cursor/skills/` |
| **Antigravity** | `~/.gemini/antigravity/skills/` 或工作区技能目录 |

---

## 常用触发方式示例 (Usage Prompts)

- **课件逐页精讲**：`用 stem-study-tutor 帮我从第 1 页开始精讲这份课件 PDF`（若同时附带往年期末卷，会自动提取真题雷达表并在讲每页时挂钩）
- **原版教材精读**：`用 2A 模式带我精读这几页英文教材，抓大放小把公式拆成大白话`
- **真题 / 习题带练**：`用 3A 模式讲这道英文计算题，注意写全步骤分` / `用 3C 模式给我一份能直接抄的中文答案和零基础拆解`
- **双轨 HTML+SVG 讲义卡片**：`帮我把这章内容生成双轨 HTML+SVG 讲义卡片，保留纯净截图模式和 1:1 Markdown`
- **手写笔记 / 波形图看图解题**：上传手写草稿或示波器图片，发送 `用模式 5+3A 帮我提取参数并解答`
- **读书论文 / 史料写作**：`用 book-grounded-writing 结合这本 PDF 建立章节证据表并起草论文提纲`

---

## 效果预览 (Live HTML Card Demo)

仓库内置一份开箱即可打开的交互式讲义卡片示例：[examples/markov-entropy-card-demo.html](examples/markov-entropy-card-demo.html)

下载或克隆后直接用任意浏览器打开即可体验：
- 顶部支持 **全部 / 单卡筛选** 与 **📸 纯净截图模式**（按 `Esc` 退出）
- 四色模块化卡片结构（数学定义 / 大白话拆解 / 考场流水线 / 记忆锚点）与手绘原生 `<svg>` 状态转移图

---

## 目录结构（渐进式按需加载设计）

为了让 AI 助手在日常对话中保持低上下文开销，所有技能均采用主入口瘦身 + 参考文档按需加载结构：

```text
study-skills/
├── README.md
├── LICENSE
├── examples/
│   └── markov-entropy-card-demo.html      # 交互式讲义卡片预览示例
└── skills/
    ├── stem-study-tutor/
    │   ├── SKILL.md                       # 核心铁律与模式路由表（精简主入口）
    │   └── references/                    # 各模式详细规则与跨学科范例（按需读取）
    │       ├── mode-1-slides.md
    │       ├── mode-2-textbook-and-sprint.md
    │       ├── mode-3-problems.md
    │       ├── mode-4-notes.md
    │       ├── mode-5-vision.md
    │       └── past-exam-radar.md
    ├── dual-track-html-notes/
    │   ├── SKILL.md                       # 双轨复盘与输出协议
    │   ├── assets/
    │   │   └── lecture-card-template.html # KaTeX + 原生 SVG 卡片源码母本
    │   └── references/
    │       └── workflow-and-examples.md
    └── book-grounded-writing/
        └── SKILL.md                       # 证据表与学术写作规范
```

---

## License

[MIT License](LICENSE) © 2026 Xi-Bei
