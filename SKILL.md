---
name: product-judgment
description: Use when evaluating product requirements, feature ideas, AI capability adoption, customer customization, product retrospectives, PM interview stories, or platform issues. Turns vague business requests into clear product judgment: whether the problem is real, whether it is worth solving, what solution boundary to choose, how to verify results, and who owns delivery, acceptance, operations, and review.
metadata:
  short-description: Turn vague requests into verifiable product judgment
---

# Product Judgment

Use this skill to compress any requirement, feature idea, AI capability, customer request, or project story into a defensible product judgment.

Core definition:

> A product manager is not the person who makes features. A product manager judges whether a problem is real, whether a solution is worth doing, whether cost and risk are controllable, and how to prove the result worked.

For AI products:

> An AI product manager is not someone who merely uses AI tools. They judge where AI belongs in the business workflow, where humans must stay in control, what fallback is needed, and how AI produces measurable business results.

## When To Use

Use this skill for:

- Business stakeholders proposing new requirements
- Customers asking for new fields, features, custom workflows, or delivery changes
- Leaders proposing product direction
- Teams discussing AI model, knowledge base, Agent, automation, or workflow adoption
- Product managers preparing project reviews, resumes, or interviews
- Platforms facing efficiency, quality, reliability, cost, or collaboration problems
- Any decision about whether a feature should be built, delayed, replaced by operations, or turned into a standard capability

## Inputs

Collect what is available. If key context is missing, ask only the smallest number of blocking questions before designing a solution.

```text
Original request:
Requester:
Business background:
Current problem:
Target user:
Current workflow:
Desired result:
Constraints:
AI involved:
Customer delivery involved:
Known metrics:
```

If context is incomplete, do not invent certainty. Mark assumptions clearly and proceed with a minimum viable judgment when possible.

## Guided Mode

Use guided mode when the user only provides a vague sentence, early idea, complaint, interview story, or feature request without enough context.

Do not immediately output the full template. First ask 3-5 short questions that unlock the judgment. Prefer questions from this list:

```text
Who提出这个需求？业务方、客户、老板、运营、技术，还是你自己判断？
当前卡在哪个用户或业务场景？
现在是怎么处理的？为什么不够好？
不解决会影响什么指标、成本、交付或风险？
这个需求是否涉及AI、客户交付、合同验收或长期维护？
有没有现有数据，例如频率、失败率、耗时、转化率、返工率？
你希望我输出完整判断、面试表达、复盘稿，还是方案取舍？
```

Ask fewer questions when possible:

```text
1 missing blocker: ask 1 question.
2-3 missing blockers: ask up to 3 questions.
Very vague request: ask up to 5 questions.
```

If the user asks for quick judgment or cannot provide more information, proceed with explicit assumptions:

```text
以下判断基于当前信息，缺失部分我会标为假设。
```

Then output the product judgment.

## Core Ability Model

Evaluate through six abilities:

```text
Problem judgment
Business translation
Workflow decomposition
Solution tradeoff
Result validation
Boundary governance
```

Reject three weak PM modes:

- Experience commentator: says "improve experience" without user, scenario, action, metric, or business result.
- Feature order taker: treats "someone asked for it" as proof the solution is valid.
- Tool mover: treats AI tools, prototypes, prompts, or generated PRDs as product capability.

## Workflow

### 1. Classify The Request

Pick one or more types:

```text
Feature: page, entry point, form, flow, interaction
Strategy: rules, segmentation, recommendation, ranking, trigger, experiment
Commercial: revenue, conversion, pricing, ROI, renewal
AI: model, knowledge base, Agent, automation, content generation
Delivery: customer customization, contract acceptance, project boundary, maintenance
Organization: responsibility, process, governance, collaboration efficiency
```

Different request types need different proof standards.

### 2. Translate The Request Into A Problem

Always answer:

```text
Who has the problem?
In what scenario?
How is it solved today?
Why is the current method insufficient?
How often does it happen?
What loss occurs if it is not solved?
```

Do not jump from "I want a feature" to "how to design the feature." First recover why the problem is worth solving.

### 3. Place It In The Business Workflow

Use the generic business chain when no domain chain is available:

```text
Acquisition -> Reach -> Understanding -> Decision -> Conversion -> Fulfillment -> Repurchase -> Referral
```

For AI marketing platforms, use:

```text
Requirement input -> Topic generation -> Prompt assembly -> Task scheduling -> Model generation -> Result return -> Human review -> Content publishing -> Data feedback -> Strategy iteration
```

Locate the bottleneck. Distinguish:

```text
Experience problem
Process problem
Rule problem
System problem
Organization problem
Model problem
Vendor problem
```

### 4. Decide Whether It Is Worth Doing

Judge priority with:

```text
How many users or customers are affected?
How frequent is the problem?
Does it affect a core metric?
How high is solution and maintenance cost?
Can it become a reusable standard capability?
```

Be cautious when the request is single-customer, low-frequency, unrelated to acceptance, expensive to maintain, or impossible to generalize.

### 5. Compare Solution Levels

Do not provide only one solution. Prefer three levels:

```text
Minimum solution: lowest cost, validates whether the problem is real
Standard solution: productized, reusable, suitable for iteration
Enhanced solution: more complete experience, higher cost and risk
```

State:

```text
Recommended solution
Why not the alternatives
What not to do now
What can be revisited later
```

### 6. If AI Is Involved, Define The Boundary

AI requests must answer:

```text
Is this problem suitable for AI?
Which workflow segment does AI handle?
Does AI output directly or assist a human?
What is the cost of AI error?
Is human review required?
Is knowledge citation required?
Is confidence scoring required?
What happens on failure, timeout, low confidence, or unsafe output?
```

Use this AI capability ladder:

```text
L1: AI generates; humans fully review
L2: AI suggests; humans decide
L3: AI handles low-risk standard tasks
L4: AI executes automatically with monitoring and rollback
L5: AI makes autonomous high-risk decisions; avoid unless strongly justified
```

Most enterprise AI products should start from L1-L3, not full automation.

### 7. Define Validation Metrics

Separate usage from value. AI generation count, call count, and active users are usage signals, not proof of value.

Result metrics:

```text
Conversion rate
Lead rate
Payment rate
Repurchase rate
Renewal rate
Content click-through rate
Content approval rate
Task completion rate
Customer delivery on-time rate
```

Efficiency metrics:

```text
Generation time
Review time
Manual edit count
Customer service handling time
Queue time
P50 / P90 / P99 completion time
```

Risk metrics:

```text
Failure rate
Timeout rate
Complaint rate
Human handoff rate
Wrong-answer rate
Rework rate
Customer acceptance failure rate
```

### 8. Confirm Cost And Risk

Every solution must account for:

```text
Development cost
Testing cost
Model call cost
Operations maintenance cost
Customer communication cost
Compatibility cost
Fallback cost
Long-term technical debt
```

For delivery-oriented products, also ask:

```text
Is it written into the contract?
Does it affect acceptance?
Is it mandatory for the customer?
Does it only serve one customer?
Can it become a standard capability?
Who pays for the added cost?
```

### 9. Output A Product Judgment

The final answer must be a judgment, not a feature description:

```text
Conclusion: do / do not do / delay / experiment first / replace with operations
Reason: why the problem is worth solving
Solution: minimum viable solution or recommended path
Boundary: what is in scope and out of scope
Metrics: how success will be proven
Risk: largest risk and fallback
Ownership: requester, product, engineering, model/API, operations, acceptance, review
```

## Output Template

```markdown
# 产品经理判断结果

## 1. 需求原话
[业务方/客户/老板提出的原始需求]

## 2. 需求类型
[功能类 / 策略类 / 商业化类 / AI类 / 交付类 / 组织类]

## 3. 真实问题
[不是要做什么功能，而是谁在什么场景下遇到了什么问题]

## 4. 业务链路位置
[这个问题影响哪一段链路]

## 5. 用户价值
[用户侧获得什么改善]

## 6. 业务价值
[转化、成本、效率、收入、风险中的哪一项被改善]

## 7. 可选方案
### 方案A：最小方案
- 做什么：
- 成本：
- 优点：
- 缺点：

### 方案B：标准方案
- 做什么：
- 成本：
- 优点：
- 缺点：

### 方案C：增强方案
- 做什么：
- 成本：
- 优点：
- 缺点：

## 8. 推荐判断
[推荐方案 + 原因]

## 9. 本期边界
### 本期做
-

### 本期不做
-

## 10. 验证指标
### 结果指标
-

### 效率指标
-

### 风险指标
-

## 11. 风险与兜底
-

## 12. 责任分工
- 业务负责人：
- 产品负责人：
- 技术负责人：
- 模型/API负责人：
- 运营负责人：
- 验收负责人：

## 13. 最终一句话
[这个需求为什么值得做，以及怎么证明做成了]
```

## Example: Slow Image Generation

Request:

```text
现在生图太慢了，能不能多接几个模型？
```

Product judgment:

```text
Do not directly integrate new models first.
First add segmented task monitoring to locate the bottleneck:
Coze time, queue time, worker pickup time, model generation time, polling/callback time, result return time, retry time.

If P90/P99 mainly stalls at model generation, evaluate multi-model routing.
If it stalls at worker queueing, optimize concurrency and queue strategy.
If it stalls at polling, optimize polling or switch to callback.
```

Metrics:

```text
P50 / P90 / P99 task completion time
Task success rate
Timeout rate
Retry rate
Average queue time
Average model generation time
Single-task cost
Human intervention rate
Customer delivery on-time rate
```
