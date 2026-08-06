# ☕ Coffee Shop Data Curation Pipeline

A complete data curation pipeline built on a real-world Coffee Shop business dataset — cleaning, deduplication, labeling, and outlier detection to transform a noisy 43,182-row dataset into a reliable, analysis-ready resource. Includes a bonus predictive modeling exercise using the curated data.

**Project by:** Sameer | **Institute:** NIELIT Gorakhpur | **Guide:** Rupunjay Rai
**Course:** Fundamentals of Data Curation using Python (Samsung Innovation Campus)

---

## 📌 Overview

Raw datasets collected from real-world sources are rarely ready for direct use — they typically contain duplicates, missing values, inconsistent formatting, and unlabeled attributes. This project implements a systematic 10-stage curation pipeline on a Coffee Shop business dataset to convert raw, messy data into a trustworthy, analysis-ready dataset.

## 📊 Dataset

- **Source:** Samsung Innovation Campus (SIC) course training material
- **Raw size:** 43,182 records, 3 columns (Year of Start, Current State, Size of Site)
- **Issues found:** 11,747 duplicate rows (~27%), 19 missing values per column

## 🛠️ Tech Stack

- **Python** — core language
- **Pandas** — data manipulation and cleaning
- **NumPy** — numerical operations
- **Matplotlib** — data visualization
- **scikit-learn** — bonus predictive modeling (Logistic Regression)

## 🔄 Pipeline Stages

1. **Load** — Import raw CSV data
2. **Profile** — Compute row counts, missing values, duplicate counts
3. **Flag Duplicates** — Mark duplicate rows before removing anything
4. **Deduplicate** — Remove duplicates, keep first occurrence
5. **Handle Missing Values** — Median imputation / drop as appropriate
6. **Filter** — Validate categorical values
7. **Label** — Derive Size Category (Small / Medium / Large) from Size of Site
8. **Detect Outliers** — IQR method on Size of Site
9. **Format** — Standardize column names and data types
10. **Summarize & Export** — Print insights, save cleaned CSV

## 📈 Results

| Metric | Value |
|---|---|
| Raw records | 43,182 |
| Duplicate records removed | 11,747 (~27%) |
| **Final curated records** | **31,434** |
| Shops currently operating ("In") | 21,202 (67.5%) |
| Shops closed ("Out") | 10,232 |
| Outliers detected (IQR method) | 2,142 (6.81%) |
| Most common size category | Medium |

## 🤖 Bonus: Predictive Modeling

A Logistic Regression model was trained on the curated dataset (`year_of_start`, `size_of_site`) to predict operating status, achieving **71.39% accuracy** — demonstrating that a well-curated dataset is directly usable for downstream machine learning without further preparation.

## 📁 Repository Structure

```
Coffee_Shope2/
├── Coffee_Shop.ipynb                              # Main Jupyter notebook (full pipeline)
├── data_coffeeshop.csv                            # Raw dataset
├── coffeeshop_cleaned.csv                         # Final curated dataset
├── Data_Curation_Coffee_Shop_Report(SR).docx       # Full project report
├── Data_Curation_Coffee_Shop_Report(SR).pdf        # Report (PDF version)
└── README.md
```

## 🚀 How to Run

```bash
git clone https://github.com/sameerraza-ops/Coffee-Shop-Data-Curation.git
cd Coffee-Shop-Data-Curation
pip install pandas numpy matplotlib scikit-learn
jupyter notebook Coffee_Shop.ipynb
```

## 📄 Full Report

The complete project report — including system design, requirement analysis, and all findings — is available in this repository as a Word document and PDF.

---

⭐ If you found this project useful, consider giving it a star!
