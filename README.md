# 📚 Books Dataset — Exploratory Data Analysis
**CodeAlpha Data Analytics Internship | Task 2**

## 📌 Overview
A statistical Exploratory Data Analysis (EDA) on 1,000 books scraped from 
books.toscrape.com (Task 1). This analysis focuses purely on statistical 
methods — distribution analysis, outlier detection, hypothesis testing, 
and multivariate comparisons — without visualizations (reserved for Task 3).

🔗 **Task 3 (Dashboard) repository:** https://github.com/sammanmumtaz76/books-eda-codealpha-task3

---

## 📂 Repository Structure
Books-EDA-Project/

├── notebooks/

│   └── Books_EDA.ipynb       # Main analysis notebook

└── data/

└── books_full.csv        # Raw dataset (1,000 books)

---

## 🔍 What This Notebook Covers

| Section | Description |
|---------|-------------|
| Data Quality Assessment | Checked for nulls, duplicates, and scraping artifacts |
| Feature Engineering | Created `Price_Segment` and `Rating_Label` columns |
| Univariate Analysis | Price, category, and rating distributions |
| Outlier Detection | IQR method applied to price data |
| Bivariate Analysis | Price vs. Rating comparison |
| Multivariate Analysis | Category × Price × Rating combined view |
| Hypothesis Testing | ANOVA test for price differences across rating groups |

---

## 🔑 Key Findings

1. **Price is nearly perfectly symmetrical** — Mean (£35.07) ≈ Median (£35.98), skewness = −0.04
2. **Price and rating are statistically independent** — ANOVA: F = 0.37, p = 0.833, η² = 0.0015
3. **No price outliers exist** — all books fall within a uniform £10–£60 range
4. **21.9% of category labels were scraping artifacts** ("Default", "Add a comment") — cleaned before category-level analysis
5. **Highest priced genres ≠ highest rated genres** — Travel averages £39.79 but only 2.73★
6. **Best value genre: Historical Fiction** — £33.64 average price with a solid 3.23★ rating
7. **All books are listed as "In stock"** — this column has zero variance and was excluded from analysis

---

## ⚠️ Limitations
- This is a practice/synthetic dataset — price ranges and stock status appear artificially generated
- Ratings may be randomly assigned rather than genuine customer reviews
- No author, publication year, or review count columns — limits deeper analysis

---

## 🛠️ Tools Used
Python · pandas · numpy · scipy (ANOVA)

## 👤 Author
Samman — BSCS, University of Sargodha# books-eda-codealpha
