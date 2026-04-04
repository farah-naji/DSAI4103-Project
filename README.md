# Airbnb Price Prediction — DSAI4103 Course Project
# Farah Abu-Shariha - 60104384  

## Business Problem

Airbnb hosts often struggle to price their listings optimally — too high pushes guests away, too low leaves money behind. This project builds an end-to-end ML pipeline that **predicts the nightly price of an Airbnb listing** based on city, room type, host behavior, and calendar data.

---

## Datasets

| Dataset | Source | Size |
- listings.csv :  [Maven Analytics / Inside Airbnb] (https://mavenanalytics.io/data-playground/airbnb-listings-reviews) | 279,712 rows, 10 cities |
- reviews.csv:  [Maven Analytics / Inside Airbnb] (https://mavenanalytics.io/data-playground/airbnb-listings-reviews) 
- calendar.csv : [Inside Airbnb — Paris 2024] (https://data.insideairbnb.com/france/ile-de-france/paris/2024-09-06/data/calendar.csv.gz) 

> Datasets are not included in this repo due to size.

---

## ML Pipeline

1. **EDA** — Price distributions, city comparisons, seasonality, review trends
2. **Feature Engineering** — Calendar aggregations, log-price target, encoded categoricals
3. **Model** — Voting Ensemble (Gradient Boosting + Random Forest + Ridge)
4. **Explainability** — SHAP bar plot, beeswarm, waterfall, dependence plot
5. **Bias Analysis** — MAE by city and room type, disparity ratios
6. **Packaging** — `predict_price()` scoring function, saved with joblib

---

## Key Results

- **Paris** had the best model performance (MAE = $42.55)
- **Cape Town** was the hardest to predict (MAE = $348.24)
- **City Disparity Ratio:** 8.18 — significant pricing variation across markets
- **Top SHAP features:** city, room type, accommodates, avg calendar price

---

| Metric | Value |
|--------|-------|
| MAE | $132.12 |
| RMSE | $255.63 |
| R² | 0.5788 |
| CV R² | 0.7624 ± 0.0020 |

--- 

## Dashboard

Built in **Power BI** — covers market overview, pricing by city/room type, review trends, and model performance per city.
