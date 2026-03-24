---
name: idea-review
description: Use when reviewing an early-stage PhD research idea in AI/ML or adjacent areas for novelty, feasibility, and research-direction judgment, including requests like "这个 idea 靠谱吗", "帮我看看这个方向", "这个课题怎么样", "review 一下我的 idea", "评估一下可行性", or "值不值得做".
---

# 博士生研究想法评审（Idea Review）

本目录是项目内的 Codex 适配版 skill。评审标准与 `.claude/skills/idea-review/` 保持一致。

## 适用范围

- **对象**：博士生的早期研究想法草稿（AI/ML 核心方向及交叉领域）
- **输入**：`ideas/` 目录下的文件，或用户直接粘贴的文本片段
- **不适用**：完整基金申请书 → 使用 `nsfc-i2-review`

## 工作流程

1. 读取完整审查指南：`references/review-prompt.md`
2. 接收研究想法（若输入过于简短，先追问关键信息再评审）
3. 按三关递进逻辑审查，每关前先联网检索相关文献进行对标
4. 输出五段式评审报告（综合判断 → 学术价值 → 风险 → 改进建议 → 文献对标）

## 参考资源

- **完整审查指南**：[references/review-prompt.md](references/review-prompt.md) — 角色定义、警惕清单、三关审查细则、五段式输出模板。开始审查前必须完整读取。
