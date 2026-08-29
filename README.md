# 孙哥 Skill (`sunge-narrative-writing`)

一个面向 Codex 的高级中文叙事写作 Skill。它把冲突设计、双尺度钩子、场景证据、物象回环、伏笔回收、重复与破例、时间跳切、对白潜台词、限知视角、节奏控制和余波结尾，整理成可执行、可检查的写作流程。

“孙哥 Skill”是便于人类记忆的名称；目录使用可发现的 ASCII 名称。项目灵感来自对公开文本《我的女友景甜》叙事工艺的分析，但不复制其独特句式、人物关系、情节或物象组合。

> [!IMPORTANT]
> 本项目非官方、无授权关联，不代表孙宇晨、景甜或任何同题项目。它不是任何在世作者的口吻模仿器，也不把文本中的私人陈述当作事实。

## 它解决什么问题

AI 已经很会生成顺滑句子，但长文真正难的是选择：哪一幕该写，哪一段该跳；什么要重复，哪一次必须破例；一个物件怎样从日用品变成结尾证据；情绪最重时，作者怎样忍住不替读者哭。

这个 Skill 服务普通人的真实经历、公众号文章、人物与品牌故事、项目案例、演讲和原创虚构。它不做“赢家叙事”或人物学派研究。

涉及真实人物时，Skill 会先区分“公开说过什么”和“事情是否真实发生”。公开原文结尾标注为虚构；[2026 年 8 月 28 日的媒体报道](https://www.thepaper.cn/newsDetail_forward_33966429)也记录了作者关于虚构部分和表达边界的回应。因此，本项目只分析公开文本的写作机制。

## 安装

把仓库放在任意稳定目录，然后链接到 Codex 的 skills 目录：

```bash
ln -s /absolute/path/to/sunge-narrative-writing \
  ~/.codex/skills/sunge-narrative-writing
```

也可以直接把整个目录复制到 `~/.codex/skills/`。重新启动或刷新 Codex 后即可发现。

## 使用

```text
Use $sunge-narrative-writing to turn these interview notes into a
2,000-character Chinese narrative nonfiction piece. Keep a claim ledger and
do not invent dialogue.
```

```text
用 $sunge-narrative-writing 把这段创业失败经历做成叙事蓝图：开头从一个
异常账单切入，结尾回到同一个物件，但不要先写全文。
```

```text
用 $sunge-narrative-writing 诊断这篇稿子的中段为什么松，重点检查场景因果、
重复与破例、伏笔回收和情绪解释过量。
```

要从零规划，复制 [`assets/narrative-blueprint.md`](assets/narrative-blueprint.md)；要做发布前检查，使用 [`references/revision-scorecard.md`](references/revision-scorecard.md)。

## 目录

```text
sunge-narrative-writing/
├── SKILL.md
├── agents/openai.yaml
├── assets/narrative-blueprint.md
├── references/
│   ├── fact-boundaries.md
│   ├── narrative-mechanics.md
│   └── revision-scorecard.md
├── LICENSE
└── README.md
```

## 设计原则

- 先确定事实边界，再制造叙事张力；
- 让细节承担证据、压力或回收任务，不做空洞装饰；
- 从结构层面保持原创距离，不做同义词改写；
- 用重复先建立规则，再让一次有后果的破例改变前文；
- 结尾回收行动或物象，少替读者总结情绪。

## 灵感与同题项目

- [X 原始文章《我的女友景甜》](https://x.com/i/article/2092711089305948160)（原文入口；部分网络环境可能无法直接访问）
- [澎湃号转载的媒体报道](https://www.thepaper.cn/newsDetail_forward_33966429)（用于核对发布时间、虚构说明与公开回应边界）
- [wuxie888/sunxue-skill](https://github.com/wuxie888/sunxue-skill)（已存在的同题开源项目，名称、方法与维护均独立；本项目未复用其“孙学/赢家叙事”体系或仓库内容）

## 许可证

本项目使用 [MIT License](LICENSE)。许可证覆盖本仓库代码和文字说明；不会改变你所输入素材的版权、隐私或事实责任。
