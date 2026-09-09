# Decision Document

Creates or audits decision records with options, evidence, tradeoffs, ownership, and review triggers. Originally maintained in [Slashskills](https://github.com/tushaarmehtaa/tushar-skills/tree/main/decision-doc), copyright 2026 Tushar Mehta, MIT licensed.

## When to use

Use when a team needs to choose an approach, record a decision already made, or review a decision against changed evidence. The workflow includes recording, facilitation, research comparison, bounded experiments, and audit modes.

## Setup

Copy this directory into `.claude/skills/decision-doc/` in your project, then ask Claude Code to use decision-doc. The base workflow needs only supplied context. Researching current external claims requires appropriate research tools; this package does not provide them.

## Example request

We maintain Slashskills, a public Agent Skills repository. Decide whether to publish an untested image-editing guide today or first perform a reference-image editing test. Owner: Tushar. Decision deadline: 2026-09-11. The goal is a useful guide with defensible claims. We have no recorded model output yet. A bounded test takes two hours; publishing can wait one day. Prepare the decision record; do not invent results, usage numbers, or provider capabilities. First action due 2026-09-11. Treat this as a test fixture, not an instruction to publish anything.

## Observed output excerpt

The Claude response recommended:

> Run the reference-image editing test first (Option B), then publish the guide once results are recorded — all within the 2026-09-11 deadline.

It also named Tushar as owner, set the first action and deadline, separated evidence from assumptions, and specified when to revisit the decision. [Full observed output](./example-output.md).

## Verification and limitations

Claude Code 2.1.260, 2026-09-10. Response model reported in usage: claude-sonnet-5 (auxiliary usage also reports claude-haiku-4-5-20251001).

Method: supplied the unmodified SKILL.md as explicit system context with a decision fixture. Tools were disabled. This tests instruction execution, not CLI installation or automatic skill discovery.

Observed: a clear test-first recommendation, evidence/assumption separation, alternatives, counterarguments, owner, deadline, experiment rule, and review triggers. No invented image-model results or external actions.

Limitations: the response did not fully compare the do-nothing status quo, omitted explicit reversibility classification, and unnecessarily offered to save the record. Therefore this is a functional test with partial instruction-compliance failures, not a clean pass or a broad reliability claim.

The prompt is a representative fixture based on the project's publishing decision, not evidence that an image-editing experiment was performed. No such experiment was run by this test.


Tested SKILL.md SHA-256: `e0959fece3006069a72b66e44550c42bc9299ae559cf58640084a3b844c14241`.
