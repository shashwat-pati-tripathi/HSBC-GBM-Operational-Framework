# 🏦 Global Markets Trade Risk & Settlement Intelligence Dashboard
### Modelled on HSBC GBM Operational Framework | Excel + Power BI

> **Independent Project** — Built to demonstrate institutional-grade Middle Office and Trade Support capability across the full post-trade lifecycle. Not affiliated with or endorsed by HSBC.

---

## 📌 Project Overview

A 6-sheet institutional-grade dashboard covering **50 trades** across Equities, Fixed Income, FX, and Multi-Asset securities — built to the same operational standards used in Global Banking & Markets environments.

| Metric | Value |
|---|---|
| Total Notional Tracked | £693M+ |
| Asset Classes Covered | Equities · Fixed Income · FX · Multi-Asset |
| Settlement Breaks Identified | 13 breaks · £402,693 exposure |
| SLA Adherence (KPI Dashboard) | 97.3% (intentionally realistic — not 100%) |
| Settlement Efficiency (Week-on-Week) | 75% → 92.1% |
| CSDR Penalty Exposure | £167K across 10 counterparties |
| Counterparty flagged HIGH Risk | BNP Paribas — 30.8% break rate · £108K exposure |

---

## 🗂️ Workbook Structure (6 Sheets)

### 1. `Trade Blotter`
- 50 live trades across 4 asset classes with real **ISIN / SEDOL** references
- Correct **T+1 / T+2 settlement logic** applied by asset class (equities T+2, gov bonds T+1, FX T+1)
- Fields: Trade ID · Asset Class · Counterparty LEI · Notional · Currency · Settlement Date · Status

### 2. `Settlement Breaks`
- 13 breaks totalling **£402,693** in unresolved exposure
- Root-cause classification using industry fail codes: **DMON** (money difference) · **DQUA** (quantity mismatch)
- Aging analysis (0–5 days / 6–10 days / 10+ days escalation tiers)
- Counterparty LEI references mapped to break severity
- P&L impact estimation per break

### 3. `P&L Attribution`
- Daily mark-to-market P&L explained by driver across 4 asset class desks:
  - **Delta** (directional equity sensitivity)
  - **Gamma** (convexity — options / structured products)
  - **FX Translation** (GBP/USD cross-currency impact)
  - **Carry** (fixed income accruals)
  - **Duration** (interest rate sensitivity — bond desk)
- Includes **realistic loss days** to reflect genuine market conditions — not fabricated performance

### 4. `CSDR Compliance`
- CSDR-compliant penalty rates applied: **1bps for equities · 0.5bps for bonds**
- Penalty accrual by counterparty, with escalation flags
- Tracks £167K penalty exposure across 10 counterparties

### 5. `NAV Reconciliation`
- Cash positions, securities holdings, and settlement fails reconciled against fund admin records
- 5 custodians covered
- IF-logic risk tiering framework across counterparties (LOW / MEDIUM / HIGH / CRITICAL)

### 6. `KPI Dashboard`
- SLA adherence tracking (weekly view)
- Settlement efficiency trend: 75% → 92.1% week-on-week improvement
- Aging bucket breakdown (0–5d / 6–10d / 10d+)
- Counterparty break rate league table
- CSDR penalty exposure summary

---

## ⚙️ Technical Build

```
Tool            : Microsoft Excel (Advanced) + Power BI
Formulas Used   : COUNTIFS · SUMIFS · AVERAGEIF · IFERROR · Nested IF · VLOOKUP
Data Model      : Zero hardcoded values — fully formula-driven workbook
Settlement Logic: T+1 / T+2 by asset class (equities, bonds, FX, money market)
Fail Codes      : DMON (money) · DQUA (quantity) — SWIFT/DTCC standard classifications
Compliance      : CSDR Settlement Discipline Regime (EU 2021)
Risk Tiering    : IF-logic escalation framework — counterparty break rate + exposure thresholds
```

---

## 🧠 Key Design Decisions

**Why 97.3% SLA and not 100%?**
Real-world operations never achieve 100% SLA. Showing a realistic figure with a breakdown of why the 2.7% failed (aging breaks, counterparty delays) demonstrates operational maturity that hiring managers notice.

**Why include loss days in P&L Attribution?**
Any trader, risk manager, or operations analyst knows markets have bad days. Showing only positive P&L signals the model is fabricated. Loss days on the FX desk and fixed income duration exposure make the data credible.

**Why BNP Paribas flagged HIGH risk?**
Counterparty risk scoring is based on formula-driven logic: break rate × exposure value. At 30.8% break rate and £108K exposure, BNP Paribas crosses the HIGH threshold automatically — the model decides, not the analyst.

---

## 🔗 Related Projects

| Project | Description | Link |
|---|---|---|
| Trade Settlement & NAV Reconciliation Tracker | 75 trades · 5 custodians · £693M notional | [View Repo](../Trade-Settlement-Reconciliation) |
| BlackRock DCF Equity Valuation | Institutional DCF · WACC 9.29% · HOLD recommendation | [View Repo](../BlackRock-DCF-Valuation) |

---

## 👤 Author

**Shashwat Pati Tripathi**
Operations Analyst — Trade & Capital Markets | Coforge Limited
CFA Level I Candidate

📧 shaswat8001@gmail.com
🔗 [LinkedIn][www.linkedin.com/in/shashwat-pati-tripathi-64aa75350

---

> *This project was independently built to demonstrate institutional-grade analytical capability. All trade data, ISINs, counterparty references, and metrics are constructed for educational and portfolio purposes. Not investment advice.*
