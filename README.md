# Quantium Data Analytics Virtual Experience Program

> **Forage Virtual Internship** — Data Analytics Track  
> Completed via [Forage](https://www.theforage.com/)

---

## Overview

This repository documents my completion of the **Quantium Data Analytics Virtual Experience Program**, a job simulation offered through Forage. Quantium is one of the world's leading data science and AI firms, founded in 2002, with a strong focus on applying analytics to drive commercial outcomes.

The program simulates the work of a junior data analyst on the Quantium retail analytics team, supporting a major grocery client with transaction-level insights and experimental evaluation of in-store layout changes.

---

## Program Structure

The internship is divided into three tasks, each building on the previous:

---

### Task 1 — Data Preparation & Customer Analytics

**Objective:** Clean and analyse transactional and customer data to uncover purchasing behaviours and generate commercial recommendations.

**Key steps:**
- Loaded and inspected raw transaction and customer datasets (`QVI_transaction_data` and `QVI_purchase_behaviour`)
- Identified and resolved data quality issues: outliers, nulls, duplicate entries, and incorrectly labelled products (e.g. non-chip items miscategorised as chips)
- Engineered new features including brand name, pack size (grams), and a standardised date column
- Merged transaction and customer datasets into a unified analysis table
- Conducted exploratory analysis across customer segments (Mainstream, Premium, Budget × Young Singles/Couples, Families, Older demographics)
- Visualised sales drivers, top-performing brands, and preferred pack sizes by segment
- Identified the highest-value customer segments and formed targeted commercial recommendations

**Tools & Libraries:** `pandas`, `numpy`, `matplotlib`, `seaborn`, `re`

**Key Finding:** Mainstream Young Singles & Couples and Mainstream Retirees are the highest contributors to chip sales. Larger pack sizes (175g–200g) are consistently preferred across most segments.

---

### Task 2 — Experimentation & Uplift Testing

**Objective:** Evaluate whether a new store layout trial (in stores 77, 86, and 88) produced a statistically significant uplift in sales and customer numbers compared to matched control stores.

**Key steps:**
- Built monthly metrics per store: total sales, number of unique customers, transactions per customer, chips per transaction, and average price per unit
- Filtered stores to those with a complete 12-month observation period
- Selected control stores using a two-part similarity scoring approach:
  - **Pearson Correlation** — measures whether the two stores move together over time
  - **Normalised Magnitude Distance** — measures how close their absolute values are
  - Combined score across both `tot_sales` and `n_cust` metrics
- Validated control store selection with pre-trial visual comparison charts
- Scaled control store metrics to the trial store's pre-trial baseline
- Computed monthly t-statistics for each trial month (Feb–Apr 2019), using the pre-trial standard deviation and 7 degrees of freedom (df = 8 months − 1)
- Identified months where trial performance breached the 95th percentile confidence band

**Tools & Libraries:** `pandas`, `numpy`, `matplotlib`, `scipy.stats`

**Control Stores Selected:**

| Trial Store | Control Store |
|:-----------:|:-------------:|
| 77 | 233 |
| 86 | 155 |
| 88 | 237 |

**Key Findings:**
- **Store 77:** Statistically significant uplift in both total sales and customer numbers in March and April 2019. Primary driver: increased customer traffic.
- **Store 86:** Significant increase in customer numbers across all three trial months, but sales uplift was less pronounced — likely due to promotional pricing reducing per-unit revenue during the trial period.
- **Store 88:** Significant uplift in both sales and customers across two of the three trial months, consistent results across both metrics.

---

### Task 3 — Analytics & Commercial Application

**Objective:** Synthesise findings from Tasks 1 and 2 into a structured client-facing presentation for the Category Manager (Julia).

**Approach:**
- Applied the **Pyramid Principles** framework to structure the report: leading with the key recommendation, followed by supporting evidence and data
- Included data visualisations from both tasks
- Provided clear callouts for each trial store's performance
- Delivered actionable next steps for rolling out the new layout at scale

**Output:** A PowerPoint presentation designed for executive-level communication, combining analytical rigour with business clarity.

---

## Repository Structure

```
├── Task_1_updates2.ipynb       # Data preparation and customer analytics
├── task2_Updates.ipynb         # Experimentation and uplift testing
├── presentation.pdf            # Task 3 — client-facing report (Pyramid Principles format)
├── QVI_data.csv                # Cleaned dataset output from Task 1 (used as Task 2 input)
└── README.md
```

---

## Tools & Technologies

- **Language:** Python 3
- **Environment:** Jupyter Notebook / Google Colab
- **Libraries:** pandas, numpy, matplotlib, seaborn, scipy

---

## Skills Demonstrated

- Data wrangling and feature engineering on real retail transaction data
- Customer segmentation analysis
- Control store matching using correlation and magnitude-based scoring
- Statistical hypothesis testing (t-tests, confidence intervals)
- Data visualisation and insight communication
- Structured business reporting (Pyramid Principles)

---

## Certificate

Program completed through [Forage](https://www.theforage.com/) — Quantium Data Analytics Virtual Experience Program.

---

## About Quantium

Quantium was established in 2002 and has grown into a global leader in data science and AI. The firm partners with businesses across retail, financial services, healthcare, and government to turn data into measurable commercial outcomes.
