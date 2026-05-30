# UI-skill

Hermes Agent 前端设计技能合集。

```
UI-skill/
├── README.md
└── frontend-craft/          ← 一个可独立安装的 Hermes Skill
    ├── SKILL.md
    └── references/
```

每个子目录都是一个完整的 Hermes Skill，可按需安装。

---

## frontend-craft

用于 Hermes Agent 的前端设计超级技能。融合三大前端设计体系：

1. **frontend-design** — 审美总纲，大胆独特的视觉方向
2. **google-ai-agent-design** — Google PAIR + Material Design for AI 交互规范
3. **hermes-terminal-ui** — 数据密集型量化终端风格

### 安装

> ⚠️ 注意：不要直接把整个仓库 clone 到 `~/.hermes/skills/frontend-craft/`。
> 仓库根目录包含 README 和外层包装，不是 skill 根目录。
> Skill 根目录是里面的 `frontend-craft/` 这一层。

**方式一：标准化复制（推荐）**

```bash
git clone git@github.com:qq612652125/UI-skill.git /tmp/ui-skill
mkdir -p ~/.hermes/skills/frontend-craft/references
cp /tmp/ui-skill/frontend-craft/SKILL.md ~/.hermes/skills/frontend-craft/
cp /tmp/ui-skill/frontend-craft/references/* ~/.hermes/skills/frontend-craft/references/
rm -rf /tmp/ui-skill
```

**方式二：符号链接（方便后续更新）**

```bash
git clone git@github.com:qq612652125/UI-skill.git /workspace/UI-skill
ln -s /workspace/UI-skill/frontend-craft ~/.hermes/skills/frontend-craft
```

更新时只需 `cd /workspace/UI-skill && git pull`，skill 自动同步。

### 验证

```bash
ls -la ~/.hermes/skills/frontend-craft/
# 应该看到:
#   SKILL.md
#   references/
```

### 使用

在 Hermes Agent 中，技能会自动加载。你也可以手动加载：

```markdown
skill_view("frontend-craft")
```

然后按照 **三步设计流程** 执行：

1. **确定场景类别** — 创意型 / 工具型 / AI交互型 / 数据密集型
2. **选择风格方向** — editorial / refined / playful / industrial / maximalist / luxury
3. **按指南执行** — 取对应章节

### 文件结构

```
~/.hermes/skills/frontend-craft/
├── SKILL.md                         # 主技能文件（核心设计规范）
└── references/
    ├── lumina-landing-fusion.md     # [示例] 创意型+editorial融合案例
    └── gridbot-dashboard.md         # [示例] 数据密集型+industrial案例
```

### 场景导航

| 你要做什么 | 看什么 |
|---|---|
| Landing page / 品牌展示 | 第2章 + 第4章 |
| SaaS后台 / 管理面板 | 第2章 + refine风格 |
| AI聊天界面 / Copilot | 第2章 + 第3章 |
| 交易终端 / 监控面板 | 第2章 + 第5章 |
| AI交易界面 | 第2章 + 第3章 + 第5章 |
| DEX / 链上交易所 | 第2章 + luxury风格 + 第5章（数字规范）|
