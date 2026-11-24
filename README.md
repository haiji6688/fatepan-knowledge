# fatepan-knowledge

> Zi Wei Dou Shu (紫微斗数) knowledge base for LLM interpretation — San He school calibrated, classics-sourced.
>
> 在线活案例（排盘 + AI 解读 + 本知识库全量应用）：**[fatepan.com](https://fatepan.com)**

把确定性计算交给脚本，把口径和出处写进 references，把边界写进文档——AI 只负责解读。

## 这是什么

一个面向 LLM 的紫微斗数解读知识库，也是 [fatepan.com](https://fatepan.com)（免费在线紫微排盘 + AI 解读）的知识层全量开源。

设计对标「AI 术数工程化」实践：减少幻觉的方式不是调教模型语气，而是**拆开链路**——排盘交确定性代码、解读口径固定到文件、每条论断带经典出处。

## 三条自查（评估同类项目也适用）

| 标准 | 本仓库的做法 |
|---|---|
| ① 有没有确定性计算 | fatepan.com 排盘引擎基于 lunar-javascript（农历换算）+ 真太阳时校正 + 1986–1991 夏令时平移，见 `references/methodology.md` |
| ② 有没有出处清单 | 70 段论断全部带【经典出处】marker，源自《紫微斗数全集》《骨髓赋》《太微赋》及诸星问答论，见 `references/classics.md` |
| ③ 有没有边界声明 | 本 README 与 SKILL.md 均声明娱乐文化用途，不构成现实决策建议 |

## 目录结构

```
├── SKILL.md                    # 可安装为 AI 助手 skill（解读工作流 + 输出约束）
├── references/
│   ├── methodology.md          # 流派与排盘口径（三合派 / 真太阳时 / 闰月策略 / 夏令时）
│   ├── classics.md             # 典籍出处清单与引用口径
│   └── 14-stars/               # 14 主星 × 5 宫位语境，共 70 段论断
│       ├── 紫微.md
│       ├── 天机.md
│       └── ...
└── README.md
```

## 14 主星 × 5 宫位语境

每颗主星一个文件，覆盖 5 个高频论断场景：

| 话题 | 内容 |
|---|---|n| 命格总览 | 格局定调、成格条件、大运走向 |
| 性格 | 优点 / 短板 / 修炼方向 |
| 夫妻宫 | 配偶画像、相处之道、婚期早晚 |
| 官禄宫 | 行业定向、职场角色、成败关键 |
| 财帛宫 | 进财模式、理财风险、守财建议 |

每段四段式结构：**一句话定调 → 核心论断 → 命盘依据 → 经典出处**。

## 用法

### 作为 AI 助手 skill 安装

把本仓库克隆进支持 Agent Skills 的环境（Claude Code / WorkBuddy 等），AI 将按 `SKILL.md` 的工作流解读命盘：先声明流派口径 → 读取对应星曜的 references → 按四段式输出 → 落 disclaimer。

### 作为网站知识层

[fatepan.com](https://fatepan.com) 的 AI 解读服务直接引用本知识库（宫位语境路由 → 星曜论断注入 system prompt）。排盘部分未开源，见 methodology.md 的口径说明。

## 边界声明（Disclaimer）

- 本仓库内容用于传统术数的工程化表达与 AI 约束实验，仅供学习与文化参考
- 不构成医疗、法律、财务、婚姻或其他现实决策建议
- 所引古籍（明清刻本）已进入公有领域；现代整理表述为原站原创
- 解读结果具有解释性与娱乐性，命由己造，盘不决定人生

## 关联

- 在线排盘 + AI 解读：[fatepan.com](https://fatepan.com)
- 口径细节：[references/methodology.md](references/methodology.md)
