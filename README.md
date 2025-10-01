# Shunyaya Symbolic Mathematical Symbols (SSMS)
*White Paper v1.8*

Shunyaya Symbolic Mathematical Symbols (SSMS) — plain-ASCII, stability-aware operator canon for symbolic numerals (m, a).

![GitHub Release](https://img.shields.io/github/v/release/OMPSHUNYAYA/Symbolic-Mathematical-Symbols?style=flat&logo=github) ![GitHub Stars](https://img.shields.io/github/stars/OMPSHUNYAYA/Symbolic-Mathematical-Symbols?style=flat&logo=github) ![License](https://img.shields.io/badge/license-CC%20BY%204.0-blue?style=flat&logo=creative-commons)

## Quick links (PDF)

**SSMS v1.8**  
- Preview: https://github.com/OMPSHUNYAYA/Symbolic-Mathematical-Symbols/blob/main/Shunyaya_Symbolic_Mathematical_Symbols_ver1.8.pdf  
- Download: https://github.com/OMPSHUNYAYA/Symbolic-Mathematical-Symbols/raw/main/Shunyaya_Symbolic_Mathematical_Symbols_ver1.8.pdf

## What’s inside

- **Canon & Operators**
  - symbolic numeral `x = (m, a)`, collapse `phi(m, a) = m`
  - operators: `s_sum` (U/W), `s_add`/`s_sub`, `s_mul`/`s_div` (M1/M2), `s_pow`
  - helpers: `min`, `max`, `abs`, `round`; rapidity path `u = atanh(clamp_a(a, eps_a))`, then `a = tanh(u)`

- **Comparisons (banded)**
  - `dv`, `du`, scores `s_gt`, `s_eq`; thresholds `tau_hi`, `tau_eq`
  - optional environment gate `g_t in [0,1]` attenuates **alignment only** (magnitudes unchanged)

- **Manifest & Reproducibility**
  - declare once: `eps_a, eps_w, V_eps, gamma, beta_v, lambda_u, beta_u, tau_hi, tau_eq`
  - minimal JSON snippet for audit-ready runs

- **Appendix D — Interactive Demo**
  - single-file HTML (non-normative), CC BY 4.0
  - equality-first mapping; optional note for near-zero `dv`

## Key defaults (declare once per study)

```text
gamma    = 1
eps_a    = 1e-6     # alignment clamp; keep |a| <= 1 - eps_a
eps_w    = 1e-12    # denominator guard; W_safe = max(W, eps_w)
V_eps    = 1e-12    # magnitude guard for dv
beta_v   = 1.0      # magnitude weight (greater-than / equality)
lambda_u = 1.0      # alignment weight (greater-than)
beta_u   = 1.0      # alignment weight (equality)
tau_hi   = 0.70     # decision band for "x > y" or "x < y"
tau_eq   = 0.80     # decision band for "equal"
```

## Scope & caution

- **Scope:** mathematics-first, observation-grade, plain-ASCII, reproducible.
- **Compatibility:** conservative extension; classical results preserved under `phi(m, a) = m`.
- **Caution (observation-only):** research release; requires broader peer review; not for safety-critical decisions.

## License

© The Authors of Shunyaya Framework and Symbolic Mathematics.  
Released under **CC BY 4.0** (with attribution).

## Third-party datasets

We reference only publicly available datasets; rights/terms remain with original owners. We don’t re-host raw files—see the PDF for citations and links. For any derived figures/tables, include the source and terms, note changes made, and state that no endorsement is implied.

## Topics (GitHub About)

symbolic-math, operator-canon, rapidity, tanh, atanh, alignment, bounded-combine, banded-decisions, gating, reproducibility, plain-ascii, shunyaya, ssms

## Search keywords

symbolic mathematics, symbolic numerals, rapidity pooling, tanh atanh, alignment clamp, bounded operators, banded comparison, portable math canon, plain ASCII formulas, reproducible symbolic math, Shunyaya, SSMS
