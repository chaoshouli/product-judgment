# 产品经理判断力 Skill / Product Judgment Skill

把一句模糊需求，拆成一个能判断、能取舍、能验证的产品决策。

Turn a vague request into a product decision that can be judged, scoped, traded off, and verified.

很多产品经理不是不会写 PRD，也不是不会画原型，而是卡在更前面：

Many product managers are not blocked by writing PRDs or drawing prototypes. They are blocked one layer earlier:

```text
这个问题到底真不真实？
Is this problem real?

值不值得做？
Is it worth solving?

应该做到什么边界？
What should the solution boundary be?

为什么不是另一个方案？
Why this solution instead of another?

上线之后怎么证明有效？
How do we prove it worked after launch?

谁来验收、运营、复盘和长期维护？
Who owns acceptance, operations, review, and long-term maintenance?
```

这个 Skill 不是帮你“包装产品经理话术”，而是帮你训练更硬的产品判断力。

This skill is not for polishing PM buzzwords. It is for building harder product judgment.

## 它解决什么问题 / What It Solves

它会把业务方、客户、老板、运营或技术提出的诉求，从“我要一个功能”翻译成：

It translates requests from business teams, customers, leaders, operations, or engineering from "I want a feature" into:

```text
真实问题 / Real problem
业务链路位置 / Business workflow position
用户价值 / User value
业务价值 / Business value
方案取舍 / Solution tradeoff
AI边界 / AI boundary
验证指标 / Validation metrics
风险兜底 / Risk and fallback
责任分工 / Ownership
```

最终输出的不是功能清单，而是一份产品判断。

The final output is not a feature list. It is a product judgment.

## 适合谁 / Who It Is For

适合正在处理这些问题的人：

Useful for people dealing with:

- 产品经理想提升需求判断、方案取舍和复盘能力  
  Product managers improving requirement judgment, tradeoff thinking, and retrospectives
- AI 产品经理需要判断 AI 应该接入哪条业务链路  
  AI PMs deciding where AI should enter a business workflow
- 创业团队需要判断一个功能该不该做  
  Startup teams deciding whether a feature should be built
- B 端 / 交付型团队需要处理客户定制和验收边界  
  B2B or delivery teams handling customization and acceptance boundaries
- 业务负责人需要把模糊诉求变成可排期、可验收、可复盘的方案  
  Business owners turning vague requests into schedulable, acceptable, reviewable plans
- 准备产品经理面试、简历项目复盘、晋升答辩的人  
  People preparing PM interviews, resume project stories, or promotion reviews

## 核心能力模型 / Core Ability Model

这个 Skill 按 6 层能力判断一个需求：

This skill evaluates a request through six abilities:

```text
问题判断能力 / Problem judgment
业务翻译能力 / Business translation
链路拆解能力 / Workflow decomposition
方案取舍能力 / Solution tradeoff
结果验证能力 / Result validation
边界治理能力 / Boundary governance
```

一句话概括：

In one sentence:

> 产品经理不是负责把需求做出来的人，而是负责判断需求是否成立、方案是否合理、成本是否可控、结果是否可验证的人。

> A product manager is not the person who simply ships requests. A product manager judges whether a requirement is valid, whether the solution is reasonable, whether cost is controllable, and whether the result can be verified.

AI 时代再加一句：

For AI products:

> AI 产品经理不是会用 AI 的人，而是能判断 AI 应该接入哪条业务链路、在哪些环节辅助人、在哪些环节必须兜底，并最终证明 AI 产生业务结果的人。

> An AI product manager is not someone who merely uses AI tools. They decide where AI belongs in the workflow, where humans must stay in control, where fallback is required, and how to prove AI creates business results.

## 典型场景 / Typical Scenarios

你可以用它判断这些问题：

Use it to judge questions like:

```text
客户说要加一个字段，要不要做？
A customer asks for a new field. Should we build it?

业务方说要加一个活动入口，要不要做？
The business team wants a campaign entry point. Is that the right solution?

老板说接一个大模型，应该怎么判断？
Leadership wants to connect a large model. How should we evaluate it?

运营说生图太慢，是不是应该多接几个模型？
Operations says image generation is too slow. Should we add more models?

一个 AI 功能上线了，怎么证明它真的有价值？
An AI feature has launched. How do we prove it has real value?

一个项目经历怎么讲得像产品负责人，而不是功能执行者？
How can a project story sound like product ownership, not feature execution?
```

## 调用方式 / How To Use

在 Codex 里使用：

Use it in Codex:

```text
用 $product-judgment 帮我判断这个需求该不该做：
现在生图太慢了，能不能多接几个模型？
```

English example:

```text
Use $product-judgment to evaluate whether we should build this requirement:
Image generation is too slow. Should we integrate more models?
```

如果信息不足，它会先追问关键问题；如果信息充分，它会直接输出结构化判断。

If context is missing, it asks guided questions first. If context is enough, it produces a structured product judgment directly.

## 输出结构 / Output Structure

默认输出包括：

Default output includes:

```text
1. 需求原话 / Original request
2. 需求类型 / Request type
3. 真实问题 / Real problem
4. 业务链路位置 / Business workflow position
5. 用户价值 / User value
6. 业务价值 / Business value
7. 可选方案 / Optional solutions
8. 推荐判断 / Recommended judgment
9. 本期边界 / Current scope boundary
10. 验证指标 / Validation metrics
11. 风险与兜底 / Risks and fallback
12. 责任分工 / Ownership
13. 最终一句话 / Final one-sentence judgment
```

## 示例 / Example

输入：

Input:

```text
现在生图太慢了，能不能多接几个模型？
Image generation is too slow. Should we integrate more models?
```

这个 Skill 不会直接说“去调研模型供应商”。

This skill will not directly jump to "research model vendors."

它会先判断：

It first reframes the problem:

```text
真实问题可能不是缺模型，而是批量生图任务在交付场景下完成时间不可控，
导致运营无法稳定预估交付周期，影响客户内容生产效率。

The real problem may not be "lack of models."
It may be that batch image-generation tasks have unpredictable completion time in delivery scenarios,
making operations unable to estimate delivery schedules and hurting customer content production efficiency.
```

然后拆链路：

Then it decomposes the workflow:

```text
用户提交 / User submission
↓
提示词拼接 / Prompt assembly
↓
任务入库 / Task creation
↓
Worker领取 / Worker pickup
↓
模型生成 / Model generation
↓
轮询/回调 / Polling or callback
↓
结果返回 / Result return
```

推荐判断可能是：

The recommended judgment may be:

```text
不建议直接先接新模型。
先做任务链路监控和分段耗时统计，再判断瓶颈是否真在模型。

Do not integrate new models first.
First add segmented task monitoring and duration tracking to locate the real bottleneck.

如果 P90/P99 主要卡在模型生成，再考虑多模型路由。
If P90/P99 mainly stalls at model generation, then evaluate multi-model routing.

如果主要卡在 Worker 排队，先扩并发和任务调度。
If it mainly stalls at worker queueing, optimize concurrency and scheduling first.

如果主要卡在轮询，先优化轮询策略或改回调。
If it mainly stalls at polling, optimize polling or switch to callbacks first.
```

验证指标会包括：

Validation metrics may include:

```text
P50 / P90 / P99 任务完成时间 / P50 / P90 / P99 task completion time
任务成功率 / Task success rate
任务超时率 / Timeout rate
失败重试率 / Retry rate
平均排队时间 / Average queue time
模型平均生成时间 / Average model generation time
单任务成本 / Cost per task
人工介入率 / Human intervention rate
客户交付准时率 / Customer delivery on-time rate
```

## 安装 / Install

把仓库复制到你的 Codex skills 目录：

Copy this repository into your Codex skills directory:

```bash
git clone https://github.com/chaoshouli/product-judgment.git
cp -R product-judgment ~/.codex/skills/product-judgment
```

然后在 Codex 中调用：

Then invoke it in Codex:

```text
用 $product-judgment 帮我判断这个需求
Use $product-judgment to evaluate this requirement.
```

## 文件结构 / File Structure

```text
SKILL.md
agents/openai.yaml
README.md
```

## 适合收藏的原因 / Why Star This

如果你经常遇到这些情况，这个 Skill 会很有用：

This skill is useful if you often face:

```text
需求很多，但不知道哪些该做
Too many requests, but unclear which ones are worth doing

功能上线了，但说不清业务价值
Features shipped, but business value is unclear

AI 工具很多，但不知道该接在哪条链路
Many AI tools, but no clear workflow placement

客户定制很多，但边界和维护成本越来越失控
Too much customer customization, with expanding scope and maintenance cost

项目做了不少，但复盘时讲不出负责人视角
Many projects completed, but retrospectives still sound like execution rather than ownership
```

它的目标不是让你“看起来像产品经理”，而是让你真的像产品负责人一样判断问题。

Its goal is not to make you sound like a product manager. It helps you judge problems like a product owner.
