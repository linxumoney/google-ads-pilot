# 🚀 Google Ads Pilot — AI 副驾驶

> Google Ads 操盘手的专业判断逻辑 × AI 执行力 = 10倍效率

把一个资深 Google Ads 操盘手的方法论，打包成你的 AI 副驾驶。

搜索词挖掘、否定词筛选、预算优化、账户诊断、周报分析——以前要花 20 小时的活，10 分钟指令搞定。

---

## ✨ 功能

| 命令 | 功能 |
|------|------|
| `/ads search-terms` | 搜索词三重评估 → 否定词清单（含理由） |
| `/ads negatives` | 否定词策略分析与建议 |
| `/ads budget` | 预算效率评分 + 迁移方案 |
| `/ads audit` | 账户10维健康度诊断（满分100分） |
| `/ads weekly` | 标准化周报分析框架 |
| `/ads copy <场景>` | RSA 广告文案生成（符合 Google 字符限制） |
| `/ads match-type` | 匹配类型策略建议 |

---

## 🧠 核心：三重搜索词评估法

传统做法：看转化数 → 留 or 否定  
**本工具做法：三重交叉验证**

```
1. 搜索词本身的意图
   → 这个用户真正想要什么？商业意图 or 信息意图？

2. 触发关键词的合理性
   → 什么词触发了它？匹配类型是否太宽泛？

3. 广告组主题一致性
   → 这个词和这个广告组的主题匹配吗？
```

每条搜索词都有明确理由，不是黑箱决策。

---

## 🚀 快速开始

### 安装

```bash
git clone https://github.com/linxumoney/google-ads-pilot.git ~/.claude/skills/google-ads-pilot
```

### 使用

**方式1：粘贴数据**
```
/ads search-terms

[粘贴你从 Google Ads 后台导出的搜索词报告]
```

**方式2：上传 CSV**
```
把导出的搜索词报告 CSV 发给我，说 /ads search-terms
```

**方式3：描述账户现状**
```
/ads audit
我的账户结构是：3个广告系列，总预算500元/天，
主要卖企业SaaS软件，目标是获取试用申请……
```

---

## 📐 账户健康度评分体系

| 维度 | 权重 |
|------|------|
| 广告系列结构 | 15% |
| 广告组粒度 | 15% |
| 否定词完整性 | 15% |
| 转化追踪 | 15% |
| 关键词匹配策略 | 10% |
| 广告文案质量 | 10% |
| 落地页相关性 | 10% |
| 出价策略 | 5% |
| 受众设置 | 2.5% |
| 广告附加信息 | 2.5% |

80分以上：账户健康 ✅  
60-80分：有优化空间 🔧  
60分以下：需系统重建 ⚠️

---

## 📁 文件结构

```
google-ads-pilot/
├── SKILL.md                           ← Claude Code skill 主文件
└── references/
    ├── search-term-methodology.md     ← 搜索词三重评估完整标准
    ├── budget-framework.md            ← 预算优化决策框架
    ├── account-health.md              ← 账户健康度检查清单
    └── copy-templates.md              ← RSA 广告文案模板与规则
```

---

## 📡 关注我

这是「**[林序聊AI · 开源计划](https://github.com/linxumoney)**」的开源项目之一。我会持续开源更多 AI 内容创作工具。

| 平台 | 链接 |
|------|------|
| 🐦 X (Twitter) | [@linxumoney](https://x.com/linxumoney) |
| 📺 YouTube | [@LinXuMoney](https://www.youtube.com/@LinXuMoney) |
| 💻 GitHub | [github.com/linxumoney](https://github.com/linxumoney) |

觉得有用的话，**点个 Star ⭐ 支持一下**，让更多人发现这个工具。

---

## 📄 License

MIT License — 自由使用、修改、分发。
