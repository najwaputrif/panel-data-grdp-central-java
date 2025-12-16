# Panel Data Econometrics: Drivers of GRDP in Central Java (2011–2015)

Econometrics project analyzing factors associated with **Gross Regional Domestic Product (GRDP/PDRB)** across **districts/cities in Central Java** using **panel data regression**.

This repo compares:
- **Pooled OLS**
- **Fixed Effects Model (FEM)**
- **Random Effects Model (REM)**

with model selection tests (**F-test, Breusch–Pagan LM, Hausman**) and classical assumption checks (normality, autocorrelation, heteroskedasticity, multicollinearity).  
Data source: **BPS (Badan Pusat Statistik)**.

---

## Research Question
Which factors significantly influence GRDP/PDRB in Central Java districts/cities during 2011–2015?

**Variables**
- Dependent: **GRDP/PDRB (constant price)**
- Predictors: **PAD**, **productive-age employment (15+ working)**, **savings position**, **credit position**

---

## Methodology (High-level)
1. Transform panel data to long format (district × year)
2. Apply log transformation (ln)
3. Estimate:
   - Pooled OLS
   - FEM (entity effects / time effects / two-way)
   - REM (and comparison)
4. Select best model using:
   - **F-test (Pooled vs FEM)**
   - **Breusch–Pagan LM (Pooled vs REM)**
   - **Hausman (FEM vs REM)**
5. Run diagnostics:
   - Normality (Shapiro–Wilk)
   - Autocorrelation (Durbin–Watson)
   - Heteroskedasticity (Breusch–Pagan / Goldfeld–Quandt)
   - Multicollinearity (VIF)

---

## Key Results (Summary)
- Model comparison indicates **Fixed Effects (entity effects)** performs strongly for capturing district-level heterogeneity.
- **Employment (15+), savings, and credit** show meaningful relationships with GRDP/PDRB, while **PAD** tends to have a smaller direct effect in the studied period.

> Full tables and equations are available in the report.

---

## How to Run (Reproducibility)
### Option A — Jupyter Notebook
```bash
pip install -r requirements.txt
jupyter notebook
