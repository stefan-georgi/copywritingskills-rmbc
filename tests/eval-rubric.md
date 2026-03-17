# RMBC Copy Audit — Blind Evaluation Rubric

## Instructions

You are evaluating two audit outputs (labeled "Output 1" and "Output 2") produced by different versions of the same RMBC Copy Audit skill. You do NOT know which version produced which output. Judge purely on output quality.

## The Ad Being Audited

Read the original ad copy to understand what was being audited. This gives you ground truth to assess calibration and completeness.

## Scoring Dimensions (0-10 each, max 60)

| # | Dimension | What to look for | 0-3 (Weak) | 4-6 (Adequate) | 7-10 (Strong) |
|---|-----------|-----------------|------------|-----------------|----------------|
| 1 | **Triage clarity** | Can a copywriter immediately identify what to fix FIRST? | Fixes are listed but no clear priority; reader must decide what matters most | Some prioritization present; top issue identifiable but not obvious | Crystal clear "fix this first" signal; reader knows exactly where to start |
| 2 | **Specificity** | Does it quote the copy? Name exact passages and changes? | Generic advice ("improve your hook"); no quotes or passage references | Some quotes and references; mix of specific and generic advice | Every finding cites exact text; proposed fixes reference specific passages |
| 3 | **Completeness** | Are all significant RMBC gaps identified? | Major gaps missed; only surface issues caught | Most significant issues identified; 1-2 gaps missed | All significant RMBC weaknesses surfaced; nothing important overlooked |
| 4 | **Calibration** | Does the numeric score match the expected quality tier? | Score significantly off from expected band (±15+ points) | Score within reasonable range (±10 points) | Score matches expected quality tier precisely (±5 points) |
| 5 | **Prioritization** | Most impactful issues surfaced before minor ones? | Issues listed in seemingly random order | Rough grouping by importance but not consistent | Clear severity ordering; most impactful issues first, minor ones last |
| 6 | **Actionability** | Can a copywriter execute the recommendation without guessing? | Vague directives ("make it better"); requires interpretation | Partially actionable; some recs clear, others need more detail | Every recommendation is a specific, executable editing instruction |

## Output Format

For each output, score all 6 dimensions and provide brief justification. Then determine the winner.

```json
{
  "output_1": {
    "triage_clarity": N,
    "specificity": N,
    "completeness": N,
    "calibration": N,
    "prioritization": N,
    "actionability": N,
    "total": N,
    "strengths": ["..."],
    "weaknesses": ["..."]
  },
  "output_2": {
    "triage_clarity": N,
    "specificity": N,
    "completeness": N,
    "calibration": N,
    "prioritization": N,
    "actionability": N,
    "total": N,
    "strengths": ["..."],
    "weaknesses": ["..."]
  },
  "winner": "Output 1" | "Output 2" | "Tie",
  "reasoning": "..."
}
```
