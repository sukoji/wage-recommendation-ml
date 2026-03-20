# Wage recommendation for small businesses

[![Python](https://img.shields.io/badge/Python-3.10+-3776AB?style=flat-square&logo=python&logoColor=white)](https://www.python.org/)
[![scikit-learn](https://img.shields.io/badge/scikit--learn-ML-F7931E?style=flat-square&logo=scikit-learn&logoColor=white)](https://scikit-learn.org/)

Machine-learning service concept: suggest **part-time hourly wages** for small shops based on business context (industry, location, reviews, nearby transit, etc.).

> **SMU AI+X Midterm team project** · model + data engineering notebook  
> Originally developed with teammates; migrated here as a portfolio artifact.

## Goal

Help small-business owners pick a competitive hourly wage for part-time hires given local context — not a production API, but an end-to-end **EDA → feature selection → model comparison → ensemble** pipeline.

## What's in the repo

| File | Description |
|------|-------------|
| `notebooks/modeling.ipynb` | Feature analysis, model training, ensemble (R² ≈ 0.47 on hold-out) |
| `data/sample_stores.csv` | Sample tabular dataset used in the notebook (`datakt.csv`) |

## Pipeline (high level)

1. **Data collection** — store metadata, foot traffic proxies, blog review counts, distance to subway
2. **Feature engineering** — dropped low-signal columns (delivery flag, gender, weekday noise)
3. **Modeling** — compared 6 regressors, ensembled top performers
4. **Evaluation** — feature importance + R² on test split

## Run locally

```bash
python -m venv .venv
pip install -r requirements.txt
jupyter notebook notebooks/modeling.ipynb
```

## Notes

- Figures in the original README pointed at a teammate's fork; this version keeps the **code + data** self-contained.
- R² ≈ 0.47 — modest, but the point was an explainable baseline for a class/patent deliverable.

## Author

**Suko Jim** · Sangmyung University, AI+X program
