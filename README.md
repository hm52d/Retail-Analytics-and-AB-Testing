# Retail Analytics & Store A/B Testing 📊🛒

## 📌 Overview
This repository contains a comprehensive data analytics and experimentation project focusing on FMCG (Fast-Moving Consumer Goods) retail sales. The objective is to analyze customer transaction data to uncover purchasing behaviors, identify key target segments, and scientifically evaluate the commercial impact of a new store layout through rigorous A/B testing (Uplift Testing).

Unlike standard exploratory projects, this analysis bridges the gap between raw transaction data and actionable commercial strategies, culminating in an executive-level business presentation.

---

## 🔬 Phase 1: Data Preparation & Customer Analytics
**Objective:** Clean and analyze transactional and customer data to identify high-value segments and generate commercial recommendations.

**Methodology & Key Steps:**
* **Data Wrangling:** Loaded and inspected raw transaction and customer datasets, resolving data quality issues such as outliers, nulls, duplicate entries, and miscategorized products (e.g., removing non-chip items).
* **Feature Engineering:** Extracted and standardized new features including brand names, pack sizes (grams), and date formatting.
* **Data Modeling:** Merged transaction and customer datasets into a unified analysis architecture.
* **Exploratory Data Analysis (EDA):** Analyzed customer segments (Mainstream, Premium, Budget across various life stages). Visualized sales drivers, top-performing brands, and preferred pack sizes.

**Key Findings:**
* **Peak Seasonality:** December 24th is the single highest sales day of the year, creating a crucial 4-day promotional window (Dec 21-24).
* **High-Value Segments:** *Mainstream Young Singles/Couples* show statistically confirmed impulse buying behavior (t-test p < 2.2e-16), paying significantly more per unit.
* **Product Affinities:** Larger pack sizes (175g) are consistently preferred year-round, while 380g packs dominate the holiday season.

---

## 📈 Phase 2: Experimentation & Uplift Testing
**Objective:** Evaluate whether a new store layout trial (in stores 77, 86, and 88) produced a statistically significant uplift in sales and customer numbers compared to matched control stores.

**Methodology & Key Steps:**
* **Metric Creation:** Built monthly KPIs per store: total sales, unique customers, transactions per customer, chips per transaction, and average unit price.
* **Control Store Selection:** Developed a two-part similarity scoring algorithm to match trial stores with control stores based on 12 months of pre-trial data:
  1. **Pearson Correlation:** Measures if the two stores' trends move together over time.
  2. **Normalized Magnitude Distance:** Measures how close their absolute sales/customer volumes are.
* **Statistical Testing:** Scaled control store metrics to the trial store's baseline. Computed monthly t-statistics for each trial month (using pre-trial standard deviation and 7 degrees of freedom) to identify performance breaching the 95th percentile confidence band.

**Key Findings:**
* **Store 77 & 88:** Showed a statistically significant uplift in both total sales and customer numbers. The primary driver was increased customer traffic.
* **Store 86:** Showed a significant increase in customer numbers, but sales uplift was less pronounced—highlighting a crucial insight that promotional pricing likely diluted per-unit revenue during the trial.

---

## 💼 Phase 3: Commercial Application
**Objective:** Synthesize analytical findings into a structured, executive-facing strategy.

**Output:**
* Applied the **Pyramid Principles** framework to structure the final report: leading with the key recommendations, followed by supporting data visualizations.
* Delivered actionable next steps for rolling out the new layout at scale to maximize ROI.

---

## 📁 Repository Structure
```text
├── Task_1_updates2.ipynb       # Data preparation, EDA, and customer analytics
├── task2_Updates.ipynb         # Control store selection and A/B statistical testing
├── presentation.pdf            # Executive-facing report (Pyramid Principles format)
├── QVI_data.csv                # Cleaned dataset (input for Phase 2)
└── README.md
