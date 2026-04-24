# A/B Testing: Packaging Optimization in Pharma Mobile App

> Does changing pill packaging color and copy move the needle on conversions? This project runs a rigorous statistical experiment to find out — and delivers a ship/no-ship recommendation backed by data.

[![Python](https://img.shields.io/badge/Python-3.11-blue?logo=python)](https://python.org)
[![Scipy](https://img.shields.io/badge/Stats-Z--test-8A2BE2)](https://scipy.org)
[![Notebook](https://img.shields.io/badge/Jupyter-Notebook-orange?logo=jupyter)](ab_testing.ipynb)
[![License](https://img.shields.io/badge/License-MIT-green)](LICENSE)

---

## Table of Contents

- [Problem Statement](#problem-statement)
- [Experiment Design](#experiment-design)
- [Key Results](#key-results)
- [Funnel Performance](#funnel-performance)
- [Segmentation Insights](#segmentation-insights)
- [Final Recommendation](#final-recommendation)
- [Tech Stack](#tech-stack)
- [Project Files](#project-files)
- [Run It Yourself](#run-it-yourself)
- [Future Work](#future-work)

---

## Problem Statement

A mobile pharmacy app wants to know whether switching product packaging from **Red** ("Relieves Pain") to **Blue** ("Quickly Reduces Inflammation") increases purchase conversion. The hypothesis: benefit-focused copy on a calmer color drives more add-to-cart and checkout actions.

This project designs, runs, and interprets the full A/B test — from sample sizing to segment-level breakdown — and delivers a clear go/no-go decision.

---

## Experiment Design

| Parameter | Detail |
|---|---|
| Control (A) | Red packaging — "Relieves Pain" |
| Treatment (B) | Blue packaging — "Quickly Reduces Inflammation" |
| Sample size | 1,000 users |
| Split | A = 511 users, B = 489 users (~50/50) |
| Primary metric | Conversion rate |
| Statistical test | Two-proportion Z-test |
| Significance level | α = 0.05 |

---

## Key Results

### Conversion lift

| Group | Conversion rate | 95% CI |
|---|---|---|
| Control (A) — Red | 16.05% | 13% – 19% |
| Treatment (B) — Blue | 25.36% | 21% – 29% |
| **Lift** | **+9.3 pp (~58% relative)** | No overlap |

### Statistical significance

- p-value = **0.00027** (well below α = 0.05)
- Confidence intervals do not overlap → treatment effect is robust
- Strong evidence the uplift is **not due to randomness**

---

## Funnel Performance

| Stage | Control (A) | Treatment (B) | Lift |
|---|---|---|---|
| Scroll | 36.2% | 38.2% | +2.0 pp |
| Add to cart | 39.3% | 46.2% | +6.9 pp |
| Conversion | 16.0% | 25.3% | +9.3 pp |

The biggest lever is the **add-to-cart stage** — blue packaging with benefit-focused copy significantly reduces drop-off before checkout.

---

## Segmentation Insights

### By age group

| Segment | Control (A) | Treatment (B) | Lift |
|---|---|---|---|
| 25–34 | 15.3% | 33.0% | **+17.7 pp** |
| 55+ | 17.4% | 31.3% | **+13.9 pp** |
| 45–54 | No significant change | — | — |

Strongest impact among young adults and older users. 45–54 segment warrants further investigation.

### By device

| Device | Control (A) | Treatment (B) | Lift |
|---|---|---|---|
| Android | 13.7% | 24.5% | +10.8 pp |
| iOS | 18.5% | 26.2% | +7.7 pp |

Android users show higher absolute lift — possibly due to screen rendering differences affecting color perception.

### By user type

| User type | Control (A) | Treatment (B) | Lift |
|---|---|---|---|
| New users | 17.6% | 25.4% | +7.8 pp |
| Returning users | 15.0% | 25.3% | +10.3 pp |

Treatment works across all users. Returning users show stronger gains — suggesting blue packaging reinforces brand trust on repeat visits.

---

## Final Recommendation

**Ship Treatment B (Blue packaging).**

- Statistically significant result (p = 0.00027)
- ~58% relative conversion lift with non-overlapping confidence intervals
- Consistent gains across funnel stages, devices, and user types
- No negative signals in any segment
- Estimated business impact: ~58% more conversions at current traffic volume, scalable across demographics

The only follow-up: investigate the 45–54 age segment separately — they show no significant response to either variant and may need a third design.

---

## Tech Stack

| Layer | Tools |
|---|---|
| Data processing | Python, pandas, NumPy |
| Statistical testing | Two-proportion Z-test (scipy.stats) |
| Analysis | Funnel analysis, segmentation, confidence intervals |
| Notebook | Jupyter |

---

## Project Files

```
pharma-ab-testing/
│
├── ab_testing.ipynb          # Full analysis — design, test, segments, recommendation
├── pharma_ab_test_data.csv   # Raw experiment dataset (1,000 users)
├── LICENSE
└── README.md
```

---

## Run It Yourself

```bash
# Clone the repo
git clone https://github.com/seema-kri/pharma-ab-testing
cd pharma-ab-testing

# Install dependencies
pip install pandas numpy scipy matplotlib seaborn jupyter

# Launch notebook
jupyter notebook ab_testing.ipynb
```

---

## Future Work

- **Sequential testing** — implement a stopping rule to catch significance earlier without inflating Type I error
- **Bayesian A/B test** — model posterior distributions for a probabilistic decision framework
- **45–54 segment deep-dive** — design a targeted variant for the non-responsive age group
- **Long-term retention** — track whether blue packaging users show higher 30-day repurchase rates

---

## About

I build data systems that surface decisions — not just charts.

**[LinkedIn](https://www.linkedin.com/in/seema-kumari-375763308/)** · **[GitHub](https://github.com/seema-kri)**
