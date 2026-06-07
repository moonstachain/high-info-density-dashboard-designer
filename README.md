# high-info-density-dashboard-designer

> **Audit / design / refactor any dashboard for INFORMATION DENSITY** (decision value per token).

[![Claude Code Skill](https://img.shields.io/badge/Claude%20Code-Skill-c9a96a?style=flat-square)](https://claude.com/claude-code) [![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg?style=flat-square)](LICENSE) [![N=3 Verified](https://img.shields.io/badge/N=3-Verified-7fb88a?style=flat-square)](#n2-已实测案例)

## 核心信念

**信息量 ≠ 信息密度。**
- 信息量 = 单位面积塞了多少数据(堆 100 个指标 → 信息量高)
- 信息密度 = 每 token 携带的决策价值(一行字 → 一个 actionable insight)

厉害的 dashboard 是后者。本 skill 提供 **12 维 rubric + 6 模块 + 8 反模式**,把任何 dashboard 从"精美的快照"重构成 yiru/odyssey 级"决策密度"。

## 触发条件

| 关键词 | 行为 |
|---|---|
| "审计 dashboard 信息密度" | 跑 12 维 audit rubric |
| "设计 dashboard / 仪表盘 / 驾驶舱" | 12 维 design checklist 强迫思考 |
| "像 yiru 那样 / 像 odyssey 那样" | 给 yiru/OSA N=2 蓝本 + 6 模块移植路径 |
| "重构 dashboard" | 8 反模式扫描 + 推荐重构模块 |
| "为什么看不出洞察" | 大概率缺 D2 判定密度 / D9 行动建议 |

## 12 维 rubric(每维 1-10 分 · 总 120)

D1 时间密度 / D2 判定密度 / D3 不确定性显式化 / D4 多源交叉 / D5 共识/分歧 / D6 frozen×dynamic / D7 状态机化 / D8 高维降维 / D9 行动建议 / D10 元信息层 / D11 历史轨迹 / D12 个人意义

- ≥ 90 高密度(yiru/odyssey 级)
- 60-89 及格
- 30-59 精美的快照
- < 30 数据陈列

## 6 大重构模块

A. Hero 决策句 / B. 时序累积层 / C. 数据脉象层 / D. ACTION 派发卡 / E. 状态机标签 / F. 多源交叉链

## N=3 已实测案例

| 业务 | 日期 | 改造前 | 改造后 |
|---|---|---|---|
| 量化投资 yiru | 2026-05-07 | N=1 原创 | **100/120** |
| 战略管理 OSA | 2026-05-15 | 39/110 (35.5%) | **~94/110 (85%)** ⚡ |
| 某寺院战略 | 2026-05-21 | 93/120 (v1.0) | **108/120 (v2.0)** ⚡ |

## 关联

- [`yuanli-strategic-data-workbook`](https://github.com/moonstachain/yuanli-strategic-data-workbook) — xlsx 数据交付版
- [`yuanli-dual-layer-data-workbook`](https://github.com/moonstachain/yuanli-dual-layer-data-workbook) — 双层数据栈

## 安装

```bash
mkdir -p ~/.claude/skills
git clone https://github.com/moonstachain/high-info-density-dashboard-designer ~/.claude/skills/high-info-density-dashboard-designer
```

Skill 入口在 `SKILL.md`。

## License

MIT
