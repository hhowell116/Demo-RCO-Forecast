# RCO Demand Forecasting Platform (Demo)

> **This repo is for demo purposes only.** Sensitive business information has been redacted. Firebase authentication removed. Project is currently in progress.

**View the demo site:** [hhowell116.github.io/Demo-RCO-Forecast](https://hhowell116.github.io/Demo-RCO-Forecast/)

**View the real project code:** [github.com/hhowell116/RCO-Forecast](https://github.com/hhowell116/RCO-Forecast)

---

A custom demand forecasting and data platform being built for a hand-manufactured organic products company. Replaces manual spreadsheet forecasting with a unified data pipeline pulling from Shopify, Amazon, and on-premises ERP, feeding ML-powered demand predictions through Azure infrastructure.

## Architecture (Proposed)

```
Shopify API  ─┐
Amazon SP-API ─┤──→  Azure Data Factory  ──→  Azure SQL Database  ──→  Power BI Dashboards
ERP (SQL)     ─┘          (ETL)                  (Data Lake)              (Reporting)
                                                      │
                                                      ▼
                                              Nixtla ML Stack
                                          (StatsForecast + LightGBM)
                                                      │
                                                      ▼
                                          Demand Forecasts by SKU
                                          (Daily/Weekly/Monthly)
```

## Status: In Progress

This project is an active engineering effort. The demo site shows the project plan, architecture decisions, and build-vs-buy analysis that was presented to leadership.
