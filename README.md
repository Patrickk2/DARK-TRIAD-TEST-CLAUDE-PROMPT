# 🧠 Dark Triad Personality Assessment

A high-accuracy, multi-phase Dark Triad assessment prompt for LLMs — built on the validated **Short Dark Triad (SD3)** scale by Jones & Paulhus (2014), extended with behavioral frequency scoring and social desirability detection.

---

## What it measures

| Trait | Description |
|---|---|
| **Machiavellianism** | Strategic manipulation, cynicism, long-game thinking |
| **Narcissism** | Entitlement, dominance-seeking, inflated self-view |
| **Psychopathy** | Impulsivity, callousness, thrill-seeking, low empathy |

---

## Structure

### Phase 1 — SD3 Core (27 items)
- All items randomized (no trait grouping)
- 9 items per screen, 3 screens
- 5-point Likert scale

### Phase 2 — Behavioral Frequency (6 items)
- Measures actual behavior, not just attitudes
- Cross-validates Phase 1 scores
- Flags inconsistencies > 0.8 delta

### Phase 3 — Social Desirability Check (4 items)
- Detects whitewashing / impression management
- Applies ⚠ Whitewash Warning if score ≥ 4.0

---

## Scoring

```
Final Score = (SD3_score × 0.65) + (Behavioral_score × 0.35)
```

Percentiles based on undergraduate norms (Jones & Paulhus, 2014):
- Machiavellianism: μ = 3.0, σ = 0.7
- Narcissism: μ = 2.9, σ = 0.7
- Psychopathy: μ = 2.1, σ = 0.7

---

## Output

- Score table (Raw SD3 / Behavioral / Adjusted / Percentile)
- Flags (social desirability, inconsistencies)
- Brutally honest psychological profile — no softening

---

## Usage

Paste `prompt.txt` as a **system prompt** in Claude or any LLM with interactive button support (Claude.ai recommended for `single_select` UI).

---

## Reference

> Jones, D. N., & Paulhus, D. L. (2014). Introducing the Short Dark Triad (SD3): A brief measure of dark personality traits. *Assessment, 21*(1), 28–41.

---

## License

MIT — see `LICENSE`
