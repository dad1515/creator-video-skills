# Content Positioning Forward Tests

These cases are cross-domain validation inputs. They are not built-in creator categories or fixed positioning templates. The skill derives positioning dynamically from each user's answers.

## Release Gates

A test passes when:

1. Guided discovery asks no more than eight questions and explains why each matters.
2. Complete inputs do not trigger redundant discovery questions.
3. Three strategies differ on at least two of: audience, promise, creator role, pillar mix, business path.
4. Every recommended strategy scores at least 28/40 and has no critical score below 3.
5. Each strategy includes five aligned sample topics and at least one exclusion or risk.
6. No private profile is saved before the user confirms a strategy.

## Test Matrix

| Case | Mode | Result | Notes |
|---|---|---|---|
| AI comic educator | Guided discovery | Pass | Four high-value answers narrowed a vague creator identity into a concrete audience and observable outcome. User confirmed the three directions were understandable. |
| Home baking educator | Trigger/discovery | Pass | The skill asked one decisive audience-and-offer question, displayed `定位诊断 1/6`, and explained its impact. |
| Data analysis educator | Complete input | Pass | Generated beginner project, advanced business thinking, and portfolio outcome strategies; pairwise differences exceeded two dimensions. |
| Postpartum nutrition consultant | Complete input | Pass | Preserved medical and weight-claim boundaries; generated entry, diagnostic, and family-system strategies. |
| Miniature model hobbyist | Complete input | Pass | Preserved low-marketing community goal; generated beginner completion, material authority, and emotional community strategies. |

## Case Prompts

### 1. AI Comic Educator

```text
我是网络自媒体创作者，能够解决AI漫剧的角色统一、场景连续和视频生成难题。
受众包括零基础用户，以及会部分工具但无法完成全流程的人。
我希望他们最终独立完成一部60秒以上、角色与场景基本统一、包含配音字幕并可发布的AI漫剧。
目标是积累稳定粉丝、建立社群，后续提供教程或课程。
```

### 2. Home Baking Educator

```text
我做家庭烘焙内容，想吸引粉丝并最终销售线上课程，但还没有确定应该主要服务零基础爱好者、进阶玩家，还是想接单的人。
```

Expected behavior: ask one audience/outcome question before proposing strategies.

### 3. Data Analysis Educator

```text
我是有8年经验的数据分析师，做过电商和SaaS增长分析，也带过新人。
主要帮助刚转行、会工具但不会解决业务问题的人，完成一个能写进简历并经得住追问的真实分析项目。
目标是建立专业影响力，后续做训练营；表达直接务实，不做夸张薪资承诺。
请直接给我三套内容定位方案。
```

### 4. Professional Service Creator

```text
我是执业营养师，专注产后女性的饮食管理，有相关客户服务经验。
受众是没有时间复杂备餐、反复节食失败的产后妈妈。
希望她们建立一套可持续的一周家庭饮食方案，并通过内容承接咨询服务。
不讨论疾病治疗，不承诺具体减重数字。请生成三套不同策略。
```

### 5. Hobby Community Creator

```text
我业余制作微缩模型五年，擅长用低成本材料做城市街景，也有本地展览经历。
希望帮助工具预算有限、居住空间不大的新手，在书桌上完成第一个带灯光的微缩街景。
目标是寻找同好和建立社群，暂时不卖课；表达安静治愈、少营销。
请生成三套明显不同的定位。
```

## Current Alpha Result

All five cases satisfy their applicable gates. The alpha remains unverified for enterprise brands, entertainment accounts, pure affiliate accounts, and multi-person content teams; those are outside V1 scope.
