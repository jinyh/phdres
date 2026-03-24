# phdres — 博士研究想法孵化与评审工作台

博士生研究想法的管理、评审与迭代平台，提供 AI/ML 领域研究想法的学术评审和方向检查工具。

同一套 skill 分别适配 **Claude Code**（`.claude/`）和 **Codex**（`.agents/`），两者共享相同的评审逻辑与参考资料。

## Skills

### idea-review

支持两种模式：

**完整评审**：三关递进评审 + 五段式报告
- 第一关：问题定位与新颖性
- 第二关：方法可行性与理论潜力
- 第三关：研究定位与路线图

触发词：「评审我的 idea」「这个 idea 靠谱吗」「值不值得做」

**方向检查**：评估研究领域在当前时间点的时效性
- 领域活跃度分析
- 核心质疑与争议梳理
- 竞争格局对比
- 风险判断表

触发词：「这个方向还能做吗」「XX 领域还合适吗」「方向检查」

## 目录结构

```
phdres/
├── CLAUDE.md                          # 项目指令（Claude Code）
├── AGENT.md                           # 项目指令（Codex，symlink → CLAUDE.md）
├── .claude/
│   └── skills/
│       └── idea-review/               # Claude Code 版 skill
│           ├── SKILL.md
│           └── references/
│               └── review-prompt.md
└── .agents/
    └── skills/
        └── idea-review/               # Codex 版 skill
            ├── SKILL.md
            └── references/
                └── review-prompt.md
```

## 使用方式

**Claude Code**：在项目目录下启动 Claude Code，直接用自然语言触发。

```bash
# 方向检查
"知识编辑这个方向在 2026 年还合适吗"

# 完整评审（提供 idea 草稿）
"帮我评审一下这个研究想法：[粘贴内容]"
```

**Codex**：在项目目录下使用 Codex，skill 自动从 `.agents/skills/` 加载。

## 适用领域

AI/ML 核心方向及交叉领域（AI for Science、AI+医疗等）。
