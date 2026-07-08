# Keepwell — Regulatory Grounding (cited)

Real compliance hooks used in the app + sizzle site. Federal baseline = 40 CFR Part 141/142; Pennsylvania implements via 25 Pa. Code Ch. 109 (often stricter — relevant since the audience is Penn Water Center).

## The pain (quantified)
- **Monitoring & reporting (M/R) is the #1 violation category.** ~1 in 5 water systems (≈29,700) failed an M/R requirement in the latest EPA report; 29.6% of community systems had M/R violations vs. 7% health-based. — EPA National Public Water Systems Compliance Report: https://www.epa.gov/compliance/providing-safe-drinking-water-america-2022-national-public-water-systems-report
- **Small systems carry it:** ~94% of systems in EPA enforcement-priority status serve ≤3,300 people. — same source.
- **Silver tsunami:** 30–50% of the water workforce eligible to retire within 5–10 years (EPA); the paperwork can't retire with them. — https://www.circleofblue.org/2024/fresh-great-lakes/fresh-october-1-2024-silver-tsunami-of-retirements-leading-to-water-sector-worker-shortages/

## Sanitary surveys
- Community water systems inspected **every 3 years** (non-community every 5; "outstanding performer" can drop to 5). Covers 8 elements incl. monitoring/reporting and operator compliance. — https://www.epa.gov/dwreginfo/sanitary-surveys
- A **significant deficiency** → written notice in 30 days, **120 days** to correct or be on schedule, else a treatment-technique violation. — Ground Water Rule.

## Monitoring & reporting rules
- **RTCR:** smallest systems take ≥1 routine coliform sample/month; a Level 1 assessment (triggered by e.g. ≥2 TC-positives/month or a missed repeat) must be **completed + form filed within 30 days**. MCL is now E. coli only. — https://www.epa.gov/dwreginfo/revised-total-coliform-rule-and-total-coliform-rule
- **Disinfectant residual:** federal — can't be <0.2 mg/L entering distribution for >4 hrs; must be detectable in ≥95% of monthly distribution samples. **PA is stricter: 0.2 mg/L maintained throughout distribution** (25 Pa. Code §109.710). — https://www.law.cornell.edu/cfr/text/40/141.72
- **Distribution pressure ≥20 psi** at all points, all flow conditions (normal 35–80 psi) — *Recommended Standards for Water Works* ("Ten States Standards," PA is a member). State code, not a federal MCL. — https://files.dep.state.pa.us/Water/BSDW/Public_Water_Supply_Permits/2022_Recommended_Standards_for_Water_Works.pdf
- **Report by the 10th** of the following month (25 Pa. Code §109.810). Late is a violation even when the water was fine. — https://www.pacodeandbulletin.gov/Display/pacode?file=%2Fsecure%2Fpacode%2Fdata%2F025%2Fchapter109%2Fs109.810.html
- **Stage 2 DBPR:** TTHM MCL 80 ppb / HAA5 60 ppb, by locational running annual average.
- **Lead & Copper:** action levels 15 ppb Pb / 1.3 ppm Cu; **service-line inventory was due Oct 16, 2024**; LCRI drops Pb action level to **10 ppb on Nov 1, 2027**.
- **CCR:** annual to customers by **July 1**.

## Public notification tiers
- **Tier 1 = 24 hours** (acute — E. coli / fecal → **boil-water notice**, nitrate, lead exceedance).
- **Tier 2 = 30 days** (non-acute MCL/TT).
- **Tier 3 = annual** (non-health, e.g. a missed monitoring sample). — https://www.epa.gov/dwreginfo/public-notification-rule

## Wastewater (lift stations)
- **NPDES permits**; **DMRs** usually monthly via NetDMR; **SSOs** to waters of the U.S. are prohibited and reportable; **CMOM** is the O&M/records framework for collection systems. — https://www.epa.gov/npdes/sanitary-sewer-overflows-ssos

## Workflow → record map (used in the app)
| Workflow | Satisfies | Record |
|---|---|---|
| Lift-station inspection | NPDES O&M · CMOM · SSO prevention | Lift-station inspection log (backs DMR / SSO defense) |
| Water-quality sampling (well house) | RTCR routine sample · residual (141.857 · 141.72 · PA §109.710) | Coliform + residual log → Monthly Operating Report, due the 10th |
| Booster / pumping startup | Distribution pressure ≥20 psi | Pressure-verification record |
| Valve exercising | Distribution O&M · sanitary-survey element | Valve-exercise log |

## Caveats (don't overstate)
- Residual monitoring **cadence** (daily vs. continuous) is set per-system in the permit, not a single federal number.
- Federal 40 CFR 141.31 "within 10 days" parallels PA §109.810; **cite §109.810** for the PA audience.
- RTCR full population sample table (141.857) referenced, not reproduced (smallest = 1/month).
- Operator certification **grades** are state-specific; the federal mandate for a program (SDWA §1419) is the anchor.
