#  Strategic Credit Delinquency Analysis  
### Predictive Modeling for Financial Risk Mitigation

---

## Sector
**Banking, Financial Services, and Insurance (BFSI)**

---

## Project Overview

In an era of volatile financial markets, **credit delinquency** (failure to repay debt for 90+ days) remains one of the biggest drivers of capital loss for lending institutions.

Traditional credit scoring models are static and fail to capture modern borrower behavior.

This project builds a **data-driven predictive framework** to identify high-risk borrowers using financial and behavioral indicators.

---

## Objectives

- Categorize borrowers based on **probability of serious delinquency (2-year window)**
- Analyze the impact of **credit utilization & debt behavior**
- Build an **interactive risk dashboard** in Google Sheets
- Design a **recommendation engine** for credit risk mitigation

---

## Dataset Description

**Source:** *Give Me Some Credit Dataset*

| Attribute | Details |
|----------|---------|
| Total Records | 15,000 |
| Variables | 11 (1 Target + 10 Features) |
| Target Column | SeriousDlqin2yrs |
| Age Range | 21 – 98 |

### Key Features

- RevolvingUtilizationOfUnsecuredLines  
- DebtRatio  
- MonthlyIncome  
- NumberOfOpenCreditLines  
- Past Due History (30–59, 60–89, 90+ days)

---

## Data Cleaning & Preparation

### Handling Missing Values
- `MonthlyIncome` → Median Imputation (20% missing)  
- `NumberOfDependents` → Filled with 0  

### Outlier Treatment
- Removed invalid ages (age = 0)  
- Utilization capped at **200%**

### Feature Engineering
- Created **Behavioral Stress Score**  
  (Sum of all past-due delays)

---

## KPI Framework

| KPI | Formula | Purpose |
|-----|---------|---------|
| Delinquency Penetration Rate | Defaulted / Total Borrowers | Portfolio risk level |
| Credit Utilization Efficiency | Avg Utilization | Over-leverage signal |
| Debt-to-Income Volatility | DebtRatio / Income | Debt stress indicator |

---

## Exploratory Data Analysis (EDA)

### Key Visual Studies

- **Correlation Heatmap** → Utilization strongest predictor  
- **Age vs Delinquency** → Younger borrowers riskier  
- **Income Distribution** → Default exists across all incomes  

---

## Advanced Analysis

### Borrower Segmentation

| Tier | Criteria | Risk Level |
|------|-----------|------------|
| Tier 1 | Age > 45, Util < 30%, No past due | Safe |
| Tier 2 | Age 30–45, Util 30–70% | Monitor |
| Tier 3 | Util > 70%, Past dues present | Critical |

**Silent Default Group Identified:**  
0 past dues + 100% utilization → 40% default rate

---

## Dashboard Design

**Built Using:** Google Sheets

### Components
- Delinquency Rate Cards  
- Age-wise Pivot Charts  
- Filters (Dependents, Income Brackets)  

**Purpose:** Real-time credit risk monitoring

---

## Key Insights

- Utilization > 70% → Strongest default indicator  
- 30–59 day delays → Early warning signal  
- Age < 35 → 12% higher delinquency risk  
- 3+ dependents → Higher debt stress  
- 10+ credit lines → Higher default complexity  

---

## Recommendations

1. Limit new credit if utilization > 60%  
2. Offer debt consolidation to Tier 2 borrowers  
3. Deploy early warning system for repeat delays  

---

## Impact Estimation

| Metric | Improvement |
|--------|-------------|
| Cost Savings | $1.2M / 10K loans |
| Manual Review Time | ↓ 40% |
| Delinquency Rate | ↓ 15% (Projected) |

---

## Limitations

- Google Sheets scalability limit (~15K rows)  

---

## Future Scope

- Alternative data integration  
- Machine Learning (XGBoost, Random Forest)  
- Real-time credit bureau APIs  

---

## Conclusion

Credit delinquency is **predictable, not random**.

By analyzing:

- Credit utilization  
- Past-due behavior  
- Debt ratios  

Financial institutions can proactively mitigate risk and build resilient lending portfolios.

---

## Team Details — Section A, Group 3

| Name | Role Highlights |
|------|----------------|
| Avishkar Meher | Dataset Sourcing (Primary) |
| Aryu Rao | PPT (Primary) |
| Sameer Khan | KPI & Analysis (Primary) |
| Satyam Swarnakar | Dashboard (Primary) |
| Krishna Dave | Report Writing (Primary) |
| Ritik Atri | Data Cleaning (Primary) |


