## 📌 Huawei – End-of-Study Project (Data & Business Analytics)
**Role:** Data & Business Analyst (Intern)  
**Period:** Jun 2025 – Nov 2025 · Tunis

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
1. **SQL Server**: run `/sql/ddl_dwh.sql` to create the star schema; run `/sql/sp_load_dwh.sql`.
2. **SSIS**: open `/ssis/ETL_DWH.dtsx` (screens & control flow), source = CSV `opportunites.csv` → `stg` → `dwh`.
3. **Power BI**: open `/powerbi/report.pbix` (or see screenshots in `/assets/powerbi_*`).
4. **ML**: open `/ml/notebook.ipynb` (Logistic Regression, ROC/AUC, confusion matrix). Predictions loaded into `ml.predictions` and exposed via `ml.vw_last_predictions`.
## Deliverables
- **Report (PDF)**: [/assets/Rapport_PFE.pdf](assets/Rapport_PFE.pdf)
- **Power BI screenshots**: [/assets](assets/)
- **ML notebook**: [/ml/notebook.ipynb](ml/notebook.ipynb)
