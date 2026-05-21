---
name: high-info-density-dashboard-designer
description: |
  Audit / design / refactor any dashboard for INFORMATION DENSITY (decision value per token).
  Triggered when user mentions: "dashboard / 仪表盘 / 看板 / cockpit / 驾驶舱 / 信息密度审计 / 重构 dashboard / 像 yiru 那样 / 像 odyssey 那样 / 12 维审计 / 决策密度".
  Uses 12-dimension rubric distilled from yiru-macro-cockpit (N=1) and OSA cockpit v3 (N=2).
maturity: experimental
status: n=2-completed
created: 2026-05-15
maintainer: liming
distilled_from:
  - "[[reference_yiru_macro_cockpit]] · N=1 范本(投资仪表盘/odysseyinst.com)"
  - "OSA cockpit v3 重构(2026-05-15) · N=2 范本(战略管理仪表盘)"
related:
  - osa-matrix-builder
  - dashboard-design-coach
---

# High-Info-Density Dashboard Designer

> **N=2 dry-run 完成**(yiru 量化投资 / OSA 战略管理 两业务跨域验证)。N=3 待复用 — 候选:管培生招聘后台 / 知识星球管理 / 飞书工作台 / 个人 GTD。
>
> **核心信念**:信息量 ≠ 信息密度。
> - 信息量 = 单位面积塞了多少数据(堆 100 个指标 → 信息量高)
> - 信息密度 = 每 token 携带的决策价值(一行字 → 一个 actionable insight)
>
> 厉害的 dashboard 是后者。

## 触发条件

| 关键词 | 行为 |
|---|---|
| "审计这个 dashboard 信息密度" | 跑 12 维 audit rubric |
| "设计一个 dashboard / 仪表盘 / 驾驶舱" | 12 维 design checklist 强迫思考 |
| "我想做一个像 yiru / odyssey 那样的产品" | 给 yiru/OSA N=2 蓝本 + 6 模块移植路径 |
| "重构这个 dashboard" | 8 反模式扫描 + 推荐重构模块 |
| "为什么我的 dashboard 看不出洞察" | 大概率缺 D2 判定密度 / D9 行动建议,直接定位 |

## 12 维信息密度 rubric(每维 1-10 分 · 总 120)

| # | 维度 | 定义 | 满分典型 | 0 分典型 |
|---|---|---|---|---|
| **D1** | 时间密度 | 每指标带时序 / Δ / history | 5d Δ + UTC + history.json + 微时序图 | 只有当前快照,无 Δ 无累积 |
| **D2** | 判定密度 | 数据 → 判定的翻译已替用户做完 | "顺风局" 一句话 + Conviction 0-10 | 只有数字,要用户自己判 |
| **D3** | 不确定性显式化 | 缺数据 / 接口挂 / 73% 完整度 公开承认 | "—缺数据" + 三态 + 数据脉象 | 缺数据用 0 充数;假绿色 ✓ |
| **D4** | 多源交叉 | 单点 = 噪音,多源 = 信噪比 | 黄金 4 驱动 + A股 13 检验 | 单源,无回链 |
| **D5** | 共识/分歧切片 | 不显示原始观点,显示共识 + 分歧 | 雪球 102 → 6 共识 + 看多 X% | 列原始观点不聚合 |
| **D6** | frozen × dynamic 分层 | 方法论 IP 与数据燃料分层 | methodology.md → system prompt | LLM 自由发挥 + 无方法论锁 |
| **D7** | 状态机化 | 离散状态 > 连续数值 | 4 象限 + 3 阶段 + 三态判定 | 只显数值不命名状态 |
| **D8** | 高维降维 | N 数据源 → 5 Tab → 1 句 hero | 26 源 → 5 Tab → 1 hero | 平铺数据无层级 |
| **D9** | 行动建议 | 是什么 → 该做什么 | strategy_matrix + core_strategy | 只描述状态不派发动作 |
| **D10** | 元信息层 | dashboard 自报家底 | Tab V 数据脉象 26 状态灯 | dashboard 不知道自己有多新 |
| **D11** | 历史轨迹 | 单点 + 轨迹 = 完整故事 | 美林象限迁移 + Conviction 演变 | 快照思维,无演化 |
| **D12** | 个人意义 | 用户的延伸大脑 != 通用工具 | frozen methodology 是用户的 | 千人一面通用 dashboard |

**评分门槛**:
- ≥ 90 → 高密度(yiru/odyssey 级)
- 60-89 → 及格,但有改进空间
- 30-59 → 「精美的快照」(OSA cockpit 改造前 = 35.5%)
- < 30 → 数据陈列,无决策价值

## 8 条反模式 · 设计禁忌(自动扫描清单)

```
❌ 数据陈列癖    : 堆 50+ 指标但无一个翻译成判定        → 加 D2 / D9
❌ 假装全知      : 缺数据填 0 / 接口挂用昨天的           → 加 D3 / D10
❌ 颜色作弊      : 全绿 ✓ 蒙混(用户看混合才会想)        → 限制绿色用法
❌ 单点快照      : 只显当下,不显轨迹                     → 加 D1 / D11
❌ 通用主义      : 每个用户看到一样的(缺归属感)          → 加 D12
❌ 自由 AI       : LLM 自由发挥(漂移/违反 frozen)        → 加 D6 frozen 锁
❌ 黑盒判定      : 给 conviction 5 但不告诉为啥(不可追溯)→ 加 D6 + D4 多源
❌ 无元层        : dashboard 不知道自己有多新            → 加 D10 数据脉象
```

## 6 大重构模块(N=2 已落地 · 可移植)

每个模块对应 1-3 维度,可单独移植:

| 模块 | 对应维度 | 干啥 | yiru 范本 | OSA cockpit v3 范本 |
|---|---|---|---|---|
| **A · Hero 决策句** | D2 + D8 | 顶部 1-3 行替用户做完一周决策 | "实际利率下行+美元走弱,定调顺风局" | "🔥 本周焦点:LTV 域 P25 必启动" |
| **B · 时序累积层** | D1 + D11 | history.json + 7d/30d Δ + 迁移轨迹 sparkline | 美林象限迁移 + Conviction 演变 | osa-history.json + 每卡 Δ + Top 8 sparkline |
| **C · 数据脉象层** | D10 + D3 | dashboard 自报家底(完整度/信任度/stale 警告) | Tab V 26 状态灯 + 缺口列 | 数据完整度 + 信任度警告 + 状态机分布 |
| **D · ACTION 派发卡** | D9 + D7 | 自动从 Top 焦点产 70/20/10 资源分配 + 该做/别做 | strategy_matrix + core_strategy | 7 人 × 5 日 ACTION 派发 + Top5/不该做 |
| **E · 状态机标签** | D7 | 把数值 1-5 替换为 5 个语义状态 | 4 象限 + 三态 | 🟦概念/🟨设计/🟧落地中/🟩已稳/🟪自动化 |
| **F · 多源交叉链** | D4 + D6 | 每张卡底部 N 源回链(L0/H5/wiki/feishu/minute) | 黄金 4 驱动 / A股 13 检验 | 每卡 5 源:cockpit + V8 + LLM-Wiki + 飞书 + 妙记 |

## 流程 · 5 步(audit + 重构)

### Step 1 · 12 维 audit(15 min)
读 dashboard 截图 + 代码,逐维打分(1-10),计算总分。
**输出**:12 维评分表 + 总分 + 5 大弱点排序。

### Step 2 · 反模式扫描(5 min)
对照 8 条禁忌清单,标出该 dashboard 触发的反模式。
**输出**:命中反模式清单 + 对应应加的维度。

### Step 3 · 重构方案(15 min)
基于 audit + 反模式 → 推荐 6 大模块中的 N 个移植。
**输出**:模块优先级排序(按 ROI:每模块带几分提升)。

### Step 4 · AskUserQuestion 拍板(5 min)
不直接动手 — 让用户在 3 档中选(轻档 / 中档 / 重档)。

### Step 5 · 落地 + 验证(2-4 小时)
按选定档执行,每模块独立 commit。完成后用浏览器截图复审。

## 边界(不要越界)

- ❌ **不替代领域知识**:本 skill 只给"信息密度元方法",不替你做投研判断 / 战略决策 / 医疗诊断
- ❌ **不要重发明轮子**:遇到 yiru/OSA 已有的模块,直接移植,不要为差异化而差异化
- ❌ **不要 dashboard 主义**:有时候解决方案不是 dashboard 是别的(如 cron + email),要诚实
- ✅ **诚实是最高的决策价值** — D3 不确定性显式化 / D10 元信息层 是最反直觉但最值钱的两维

## N=2 已实测案例

| 业务 | 日期 | dashboard | 改造前分 | 改造后分 | 移植模块 |
|---|---|---|---|---|---|
| 量化投资 | 2026-05-07 | yiru / odysseyinst.com | N=1 范本(原创) | 100/120 | 全 12 维原生设计 |
| 战略管理 | 2026-05-15 | OSA cockpit v3 | 39/110 (35.5%) | ~94/110 (85%) ⚡ | A+B+C+D+E+F 全 6 模块 |

## N=3 候选(待复用验证)

- 管培生招聘后台(guanpei-recruit skill)
- 原力星球管理后台(yuanli-zsxq-coevolution-assistant)
- 个人 GTD(daily standup)
- 客户 LTV 池(a-ltv 资产卡的实例化)
- 学员阶段诊断(student-stage-router)

## 复用规范

1. **每次审计必输出 audit 表**(120 总分,不只是说"信息密度高/低")
2. **每次设计前必跑 8 反模式扫描**(防止重蹈)
3. **6 模块按 ROI 排序移植**(轻档先 A+E+C,重档加 B+D+F)
4. **诚实标注「模拟基线」**(如 OSA history.json 的 5/8 / 4/15 是模拟,标 "待累积")
5. **N=3 起做轻量化模板**(目前模板 hard-code 在 osa-cockpit / yiru,N=3 起抽出公共组件)

## 关联

- `[[osa-matrix-builder]]` 是 OSA 卡集 → 矩阵热图的具体实现,本 skill 是更高一层的"信息密度元方法"
- `[[dashboard-design-coach]]` 偏视觉 / 排版,本 skill 偏信息架构 / 决策价值
- `[[reference_yiru_macro_cockpit]]` 是 N=1 范本的 memory pointer
