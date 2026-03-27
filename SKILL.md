---
name: google-ads-pilot
description: |
  Google Ads AI 副驾驶。把专业操盘手的判断逻辑固化成可复用工作流：搜索词挖掘与评估、
  否定关键词筛选、预算优化建议、账户诊断、周报分析。
  不需要手动 Excel，AI 替你干脏活累活。
  触发词：/ads、/google-ads、搜索词挖掘、否定词、预算优化、Google Ads分析、广告账户诊断、关键词评估
  Trigger: /ads, /google-ads, search terms, negative keywords, budget optimization, Google Ads audit
---

# Google Ads Pilot — AI 副驾驶

> 把你的 Google Ads 专业判断逻辑固化成 AI，让 AI 替你干脏活。

---

## 命令速查

| 命令 | 功能 |
|------|------|
| `/ads search-terms` | 搜索词挖掘 + 三重评估 + 输出否定词清单 |
| `/ads negatives` | 否定词策略分析与建议 |
| `/ads budget` | 预算分配优化建议 |
| `/ads audit` | 账户结构诊断 |
| `/ads weekly` | 周报分析框架 |
| `/ads copy <关键词/场景>` | 生成广告文案（标题+描述，符合字符限制） |
| `/ads match-type` | 匹配类型策略建议 |

---

## 核心工作流

### /ads search-terms — 搜索词挖掘与评估

**三重交叉验证逻辑**（读取 `references/search-term-methodology.md`）：

1. **筛选范围**：只处理 status=NONE（未处理）的搜索词，按消耗降序排列
2. **三重验证**：
   - 搜索词本身的意图（用户真正想要什么）
   - 触发该词的关键词（匹配是否合理）
   - 所在广告组的主题（是否与组主题一致）
3. **判断标准**：相关性优先，而非单纯看转化数据
4. **输出格式**：
   - ✅ 保留词（含理由）
   - ❌ 否定词（含理由 + 建议否定级别：广告组/广告系列/账户）
   - 🔍 待观察词（数据不足，建议继续跑）

**如何使用**：
把你的搜索词报告（CSV 或直接粘贴）发给我，说 `/ads search-terms`，我按这套逻辑逐条评估。

---

### /ads budget — 预算优化建议

**分析框架**（读取 `references/budget-framework.md`）：

1. 识别「预算受限」的高 ROAS 广告系列 → 建议加预算
2. 识别「消耗过快」但转化差的系列 → 建议削减或暂停
3. 计算各系列的「预算效率分」= 实际消耗/目标消耗 × ROAS 指数
4. 给出具体的预算迁移方案（从哪里移、移多少、移到哪里）

---

### /ads audit — 账户结构诊断

检查以下10个维度（读取 `references/account-health.md`）：

1. 广告系列结构是否清晰（品牌/非品牌/竞品分离）
2. 广告组粒度是否合适（单主题原则）
3. 关键词匹配类型策略
4. 否定词列表完整性
5. 广告文案数量和质量（每组至少3条RSA）
6. 落地页相关性
7. 转化追踪设置
8. 出价策略与目标一致性
9. 受众叠加设置
10. 广告附加信息完整性

---

### /ads weekly — 周报分析框架

标准周报结构：
1. **核心指标对比**：本周 vs 上周 vs 同比（点击/展现/CTR/CPC/转化/CPA/ROAS）
2. **异常信号**：哪些系列/广告组有显著波动（±20%以上）
3. **搜索词动态**：新增高价值词 / 新增需否定词
4. **预算执行率**：各系列实际消耗 vs 预算
5. **下周行动清单**：优先级排序的3-5条具体操作

---

## 数据输入方式

支持三种方式提供数据：

1. **直接粘贴**：把 Google Ads 后台的数据表格内容直接粘贴进对话
2. **上传 CSV**：把导出的报告文件发给我
3. **手动描述**：口述关键指标，我帮你做定性分析

---

## 参考文档

- `references/search-term-methodology.md` — 搜索词评估完整标准
- `references/budget-framework.md` — 预算优化决策框架
- `references/account-health.md` — 账户健康度检查清单
- `references/copy-templates.md` — RSA 广告文案模板与规则
