# Product Judgment Skill

Turn vague product requirements, feature ideas, AI capability requests, customer customization, platform issues, retrospectives, and PM interview stories into clear product judgments.

Core judgment:

```text
Is the problem real?
Is it worth solving?
What solution boundary should be chosen?
How will success be verified?
Who owns delivery, acceptance, operations, and review?
```

## Install

Copy this folder into your Codex skills directory:

```bash
cp -R product-judgment ~/.codex/skills/product-judgment
```

Then invoke it with:

```text
Use $product-judgment to evaluate this requirement.
```

## Wake Phrase

```text
$product-judgment
```

## Main Files

```text
SKILL.md
agents/openai.yaml
```

## Typical Use

```text
Use $product-judgment to judge whether we should add multi-model image generation routing for our AI marketing platform.
```

The skill will either ask guided questions when context is missing, or produce a structured product judgment with scope, options, metrics, risks, and ownership.
