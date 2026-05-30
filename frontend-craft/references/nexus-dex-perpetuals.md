# frontend-craft 融合案例：Nexus DEX 永续合约交易界面

**场景：** 品牌+金融混合型（To B / To C 链上交易所）
**风格：** luxury（奢华）+ industrial（金融数字规范）
**框架：** React + Vite

## 设计目标

展示财力、建立安全感、吸引增量资金。
本质上是一个商业金融机构的前端，所以调性对标：**高盛 / BlackRock 级别的品牌感，叠加链上原生的科技透明度。**

## 设计系统

| Token | 值 | 意图 |
|---|---|---|
| `--bg-base` | `#060A14` | 深海蓝黑，比纯黑更有深度 |
| `--gold` | `#C9A84C` | 暖金——财富感和信任感的锚点 |
| `--sapphire` | `#2E6BE6` | 蓝宝石——科技实力的冷色平衡 |
| `--font-display` | DM Serif Display | 衬线体——传统金融的权威感 |
| `--font-ui` | Space Grotesk | 现代科技UI，干净利落 |
| `--font-mono` | JetBrains Mono | 所有数字 tabular-nums |

## 组件架构

```
┌─Top Bar─────────────────────────────────────┐
│ Nexus  │ Trade Markets Portfolio Earn  │ Wallet │
├──────────────────────────────────────────────┤
│ TVL $2.84B │ Vol $847.2M │ OI $1.24B │ Liq $12.8M │
├─── LEFT ────────────┬─── RIGHT ─────────────┤
│ [Long] [Short]      │ Order Book             │
│ ETH/USDC Perp ▲1.24%│ Asks 10档 + depth bar  │
│ Leverage 1×–100×    │ Mark Price $3,508.20   │
│ Size Input [MAX]    │ Bids 10档 + depth bar  │
│ Entry / Liq / Fee   │                       │
│ [Open Long][Short]  │                       │
│ Positions Table      │                       │
│ ETH Long / BTC Short│                       │
└──────────────────────┴───────────────────────┘
```

## 从三个技能汲取的精华

### frontend-design → 品牌视觉
- DM Serif Display 衬线字体做品牌 logo（金叉号 N）— 稀有材质感
- 金色+深蓝的奢侈品牌配色，不是普通交易所的蓝白或红黑
- 毛玻璃 topbar（`backdrop-filter: blur(20px)`）
- 多图层背景：径向光晕 + 60px 网格线（`opacity: 0.15`），层次感深
- 金色 hover glow（`box-shadow: 0 4px 24px var(--gold-glow)`）

### google-ai-agent-design → 信任透明（迁移应用）
- 虽然不是 AI 界面，但其"展示数据来源"原则可迁移：Top bar 显示链上区块号 `#18,423,592`
- Stats bar 4 个核心指标全部展示具体数值 + 变化方向，零模糊
- 流动性数据透明（TVL / OI / Volume），这是 To B 客户最看重的安全感信号

### hermes-terminal-ui → 交易数据规范
- 所有数值 monospace + tabular-nums（`$2.84B` / `$3,508.20` / `42.5`）
- 涨跌色+符号双编码（绿+↑ / 红+↓）
- Order Book 10 档深度 + depth bar 可视化
- 位置表格：密排版、1px 边框、uppercase 小标题

## 组件交互

| 组件 | 交互 |
|---|---|
| Trade Tab | Long / Short 切换，active tab 金线指示 |
| Leverage | 点击 1/2/3/5/10/20/50/100 档位，active 金色 |
| Size Input | 文字输入 + MAX 按钮一键填满 |
| Trade Buttons | Open Long / Short，hover 发光 + 渐变背景 |
| Order Book | 行 hover 高亮，depth bar 可视化 |
| Positions Tab | Positions / Open Orders / History 切换 |

## 预览

运行在 `http://localhost:4173`，项目 `/root/nexus-dex/`
