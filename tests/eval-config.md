---
created: 2026-03-17
title: "A/B Test Decision Record: rmbc-copy-audit Skill Variants"
---

# A/B Test Decision Record: rmbc-copy-audit Skill Variants

## Decision

**Replace `SKILL.md` with `SKILL-mpe-transfer.md`** (the code-review methodology variant).

## Evidence

Version B (MPE-transfer) won all 5 blind evaluations with an average margin of **+9.8 points** on a 60-point scale.

| Ad | Type | Version A | Version B | Margin |
|----|------|-----------|-----------|--------|
| 1 | Strong DR control | 45/60 | 54/60 | +9 |
| 2 | Generic SaaS | 39/60 | 50/60 | +11 |
| 3 | Strong mechanism, weak copy | 43/60 | 52/60 | +9 |
| 4 | Strong copy, weak research | 42/60 | 53/60 | +11 |
| 5 | One fix away | 44/60 | 53/60 | +9 |
| **Average** | | **42.6** | **52.4** | **+9.8** |

## Why Version B Wins

The decisive factors, ranked by impact:

1. **Triage clarity** (9.0 vs 6.2 avg): The severity summary line (`N Rewrite | N Major Fix | N Minor Fix`) gives copywriters instant orientation. Version A requires reading the full recommendations to understand scope.

2. **Completeness** (9.0 vs 6.4 avg): Version B's separate Findings section surfaces 5-8 issues per audit vs Version A's 3 recommendations. Version A systematically misses secondary issues.

3. **Prioritization** (8.8 vs 7.0 avg): Severity labels (Rewrite/Major Fix/Minor Fix) create explicit triage ordering. The escalation gate (2+ Rewrite → recommend full rewrite) correctly fired on Ads 2 and 5.

4. **Actionability** (9.0 vs 7.6 avg): Every finding in Version B includes a concrete rewrite example. Version A provides rewrites for its 3 recommendations but not for issues it doesn't surface.

## What Version A Does Better

- **Brevity**: ~40% shorter output. Faster to read.
- **Calibration parity**: Numeric scores are equivalent (avg diff 1.8 pts). The scoring rubric works equally well in both formats.

These advantages are outweighed by the actionability gains.

## Changes Made

1. `SKILL.md` → `SKILL-standard-archived.md` (preserved for reference)
2. `SKILL-mpe-transfer.md` → `SKILL.md` (new canonical)
3. Attribution URL in new `SKILL.md` changed from `stefangeorgi.com` to `copyaccelerator.com/join`

## Methodology

- 5 test ads sourced to cover different quality bands and RMBC imbalance patterns
- Both skill versions ran on all 5 ads (10 total outputs)
- Blind comparator agents scored each pair on 6 dimensions (triage clarity, specificity, completeness, calibration, prioritization, actionability)
- Output 1/Output 2 assignment randomized per ad to prevent positional bias
- Full data: `benchmark.json`

## Test Artifacts

| File | Description |
|------|-------------|
| `fixtures/ads/ad-{1-5}-*.md` | 5 test ad fixtures |
| `results/ad-{N}-version-{a,b}.md` | 10 audit outputs |
| `results/eval-ad-{1-5}.json` | 5 blind evaluation results |
| `benchmark.json` | Aggregated scores and decision |
| `eval-rubric.md` | 6-dimension evaluation rubric |
