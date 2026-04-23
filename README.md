# 🛒 Retail Store Sales Analysis

## Overview

This project focuses on cleaning and analyzing a **real-world-style retail sales dataset** containing intentional inconsistencies and missing values. The goal was to transform raw, noisy data into a structured format and extract meaningful insights from it.

The project emphasizes **data preprocessing, logical imputation, and exploratory analysis**, which are critical steps in any data-driven workflow.

---

## Problem Statement

Real-world datasets are often incomplete and inconsistent. This project addresses:

* How to handle missing and inconsistent values effectively
* How to clean and standardize transactional data
* How to derive meaningful insights after preprocessing

---

## Dataset

* **Source:** Kaggle
  https://www.kaggle.com/datasets/ahmedmohamed2003/retail-store-sales-dirty-for-data-cleaning

* **Details:**

  * Rows: 12,575
  * Columns: 11
  * Contains multiple product categories with intentionally introduced data issues

---

## Approach

### Data Loading & Inspection

* Loaded dataset using Pandas
* Performed initial inspection using `head()`, `info()`, and `describe()`

### Missing Data Handling

* Analyzed column-wise and row-wise missing values
* Applied **business logic-based imputation**:

  * `Total Spent = Quantity × Price Per Unit`
* Used:

  * Mean / median for numerical columns
  * Mode for categorical columns
* Reconstructed missing item names using price mapping

### Data Cleaning

* Removed duplicate records
* Standardized text fields (lowercase, trimmed spaces)
* Ensured consistency across categorical values

### Feature Engineering

* Created a ranking feature based on total spending
* Identified high-value customers and transactions
* Analyzed categories and items contributing to top sales

### Outlier Detection

* Used **IQR method** to detect anomalies in:

  * Price Per Unit
  * Total Spent

### Encoding

* Applied **one-hot encoding** to categorical variables

### Final Output

* Generated a cleaned dataset: `cleaned_retail_store_sales.csv`

---

## Key Highlights

* Applied **domain-driven data imputation** instead of relying solely on statistical methods
* Built a structured and reproducible data cleaning pipeline
* Extracted insights from a noisy, real-world-like dataset

---

## Outcome

The project successfully converts messy transactional data into a clean and analysis-ready format, enabling reliable insights and further modeling.

---

## Project Structure

```bash id="retail-standalone"
retail-store-sales-analysis/
│
├── notebook.ipynb
├── dataset/
    └── retail_store_sales.csv
├── outputs/
    └── cleaned_retail_store_sales.csv
```

---

## Conclusion

This project highlights the importance of data preprocessing in real-world scenarios. Clean data is the foundation for accurate analysis and decision-making.

---

## Disclaimer

This project is intended for educational purposes and demonstrates data cleaning and analysis techniques on a synthetic dataset.
