# frontend-craft

用于 Hermes Agent 的前端设计超级技能。融合三大前端设计体系：

1. **frontend-design** — 审美总纲，大胆独特的视觉方向
2. **google-ai-agent-design** — Google PAIR + Material Design for AI 交互规范
3. **hermes-terminal-ui** — 数据密集型量化终端风格

## 安装

### 方式一：通过 skills 目录（推荐）

```bash
mkdir -p ~/.hermes/skills/frontend-craft/references
cp SKILL.md ~/.hermes/skills/frontend-craft/SKILL.md
# 可选参考文件
cp references/* ~/.hermes/skills/frontend-craft/references/
```

### 方式二：直接克隆仓库

```bash
cd ~/.hermes/skills
git clone https://github.com/qq612652125/UI-skill.git frontend-craft
```

## 使用

在 Hermes Agent 中，技能会自动加载。你也可以手动加载：

```markdown
skill_view("frontend-craft")
```

然后按照 **三步设计流程** 执行：

1. **确定场景类别** — 创意型 / 工具型 / AI交互型 / 数据密集型
2. **选择风格方向** — editorial / refined / playful / industrial / maximalist / luxury
3. **按指南执行** — 取对应章节

## 文件结构

```
frontend-craft/
├── SKILL.md                         # 主技能文件（核心设计规范）
└── references/
    ├── lumina-landing-fusion.md     # [示例] 创意型+editorial融合案例
    ├── gridbot-dashboard.md         # [示例] 数据密集型+industrial案例
    └── google-ai-agent-design.md    # 继承引用 - Google PAIR原文
```

## 场景导航

| 你要做什么 | 看什么 |
|---|---|
| Landing page / 品牌展示 | 第2章 + 第4章 |
| SaaS后台 / 管理面板 | 第2章 + refine风格 |
| AI聊天界面 / Copilot | 第2章 + 第3章 |
| 交易终端 / 监控面板 | 第2章 + 第5章 |
| AI交易界面 | 第2章 + 第3章 + 第5章 |
