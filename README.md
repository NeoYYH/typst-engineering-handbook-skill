# 工程手册 Typst 风格

可复用的 Cursor skill：用统一视觉与写作节奏写中文工程解读、协议与架构手册（Typst → A4 PDF）。

## 文件

- [`SKILL.md`](./SKILL.md) — skill 正文（YAML frontmatter + 配方）
- [`.cursor/skills/AutoText/SKILL.md`](./.cursor/skills/AutoText/SKILL.md) — 项目内安装副本（调用名为 `/AutoText`）

## 用途

写中文工程手册时按本风格：青绿/亮蓝/橙配色、初学者导读、证据边界、列举→分项、陷阱与优化清单、PDF + 预览 + NOTES 交付。

## 调用方式

在 Cursor Agent 聊天中输入：

```text
/AutoText
```

本 skill 设置了 `disable-model-invocation: true`，只会在你显式输入 `/AutoText` 时加载，不会由模型自动套用。

## 安装到本地（全局，所有项目可用）

```bash
mkdir -p ~/.cursor/skills/AutoText
curl -fsSL https://raw.githubusercontent.com/NeoYYH/typst-engineering-handbook-skill/main/SKILL.md \
  -o ~/.cursor/skills/AutoText/SKILL.md
```

或克隆本仓库后：

```bash
mkdir -p ~/.cursor/skills/AutoText
cp /path/to/typst-engineering-handbook-skill/SKILL.md ~/.cursor/skills/AutoText/SKILL.md
```

文件夹名与 frontmatter `name` 必须都是 `AutoText`，这样 slash 命令才是 `/AutoText`。

## 项目内使用

本仓库已包含 `.cursor/skills/AutoText/`。在 Cursor 中打开本仓库后，Agent 聊天里可直接用 `/AutoText`。

## 许可

按仓库所有者意愿另行补充。内容来自个人工程手册实践沉淀，可自由改编。
