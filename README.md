## 📌 Huawei – End-of-Study Project (Data & Business Analytics)
**Role:** Data & Business Analyst (Intern)  
**Period:** Apr 2025 – Oct 2025 · Tunis

**Project:** Sales performance analytics pipeline — **Data → DWH → ETL → BI → ML**  
- Built a **star-schema DWH** on SQL Server (fact opportunité + dims client/produit/secteur/région/statut/temps).
- Developed a **replayable SSIS ETL** (CSV → staging → DWH) with quality checks & stored procedures.
- Delivered a **Power BI dashboard** (KPI: revenue, won-rate, opportunity volume, ML probability).
- Trained a **Logistic Regression** pipeline (scikit-learn), produced **win-probability** scores,
  and **reintegrated** them into `ml.predictions` + `ml.vw_last_predictions` for BI consumption.

**Stack:** SQL Server, SSIS, Power BI, Python (pandas, scikit-learn)  
**Skills:** Data Modeling (Star schema), DAX, ETL, Feature Engineering, Model Validation (ROC/AUC), MLOps-lite

> **Deliverables:** DWH schema, SSIS package, Power BI report, ML notebook + predictions view  
> **Outcome:** Unified visibility of opportunity pipeline and probabilistic prioritization for sales.

[📄 Report (PDF)](#) · [📊 Power BI screenshots](#) · [🧠 ML notebook](#)
## How to Reproduce (Quickstart)

1. **SQL Server**  
   Run `/sql/ddl_dwh.sql` to create the star schema; then run `/sql/sp_load_dwh.sql`.

2. **SSIS**  
   Open `/ssis/ETL_DWH.dtsx` (control flow & data flow), source = `opportunites.csv` → `stg` → `dwh`.

3. **Power BI**  
   Open `/powerbi/report.pbix` (or see screenshots in `/assets/pbi_*`).

4. **ML (Python)**  
   Open `/ml/ml_notebook.ipynb` (Logistic Regression, ROC/AUC, confusion matrix).  
   Predictions loaded into `ml.predictions` and exposed via `ml.vw_last_predictions`.

## Deliverables

- **Report (PDF):** [`/assets/Rapport_PFE.pdf`](assets/Rapport_PFE.pdf)  
- **Power BI screenshots:** [`/assets`](assets)  
- **ML notebook:** [`/ml/ml_notebook.ipynb`](ml/ml_notebook.ipynb)

## Screenshots

<p align="center">
  <img src="assets/pbi_overview.png" alt="Power BI overview" width="800"><br>
  <em>Power BI overview page (KPI & trends).</em>
</p>

