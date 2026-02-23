# 🧹 Data Cleaning Documentation — Credit Delinquency Project

## 📌 Overview
This document describes all the data cleaning and preprocessing steps performed on the **“Give Me Some Credit”** dataset before analysis and dashboard creation.

- **Dataset Size:** 15,000 Records × 11 Features  
- **Target Variable:** SeriousDlqin2yrs (Binary)

---

# 1️⃣ Missing Value Treatment

## 🔹 MonthlyIncome
- ~20% values were missing.
- Dropping rows could lead to data loss and bias.

**✅ Action Taken:**
- Applied **Median Imputation**.

**💡 Reason:**
- Income distribution was skewed.
- Median handles outliers better than mean.

---

## 🔹 NumberOfDependents
- Few missing values detected.

**✅ Action Taken:**
- Filled using **Median values**.

**💡 Reason:**
- Maintains dataset distribution.

---

# 2️⃣ Outlier Treatment

## 🔹 RevolvingUtilizationOfUnsecuredLines
- Values > 200% detected.
- Considered unrealistic / data errors.

**✅ Action Taken:**
- Capped at **2.0 (200%)**.

**💡 Business Logic:**
- Utilization >100% possible.
- >200% treated as anomaly.

---

## 🔹 DebtRatio
- Extreme high values present.

**✅ Action Taken:**
- Applied percentile-based capping.

**💡 Reason:**
- Prevents skewed risk interpretation.

---

# 3️⃣ Invalid Record Removal

## 🔹 Age Column
- Some records had **Age = 0**.

**✅ Action Taken:**
- Removed invalid rows.

**💡 Reason:**
- Borrower age cannot be zero.

---

# 4️⃣ Data Type Validation

**Steps Performed:**

- Converted all numeric fields properly.
- Removed string contamination.
- Target column standardized to **Binary (0/1)**.

---

# 5️⃣ Duplicate Check

**✅ Action Taken:**
- Dataset scanned for duplicates.
- No major duplicates found (removed if detected).

---

# 6️⃣ Feature Integrity Checks

Validated logical ranges:

- DebtRatio ≥ 0  
- Utilization ≥ 0  
- PastDue Counts ≥ 0  
- MonthlyIncome ≥ 0  

Invalid entries treated/removed.

---

# 7️⃣ Final Clean Dataset Summary

| Metric | Value |
|--------|-------|
| Total Records | ~15,000 |
| Features | 11 |
| Missing Values | 0 |
| Outliers | Treated |
| Invalid Ages | Removed |

---

# ✅ Cleaning Summary

- Median imputation applied  
- Outliers capped  
- showing business thresholds  
- Invalid records removed  
- Data types standardized  
- Logical validation checks completed  

---

# 🚀 Outcome

The dataset is now:

- Clean & analysis-ready  
- Bias-reduced  
- Business validated  
- Suitable for dashboard & risk modeling  

---

**Prepared By:**  
Credit Risk Analytics Team — Group 3  
Newton School of Technology
