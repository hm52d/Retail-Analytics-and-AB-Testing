# Retail Analytics & Store A/B Testing 📊🛒

## 📌 Overview
This repository contains a comprehensive data analytics and experimentation project focusing on FMCG (Fast-Moving Consumer Goods) retail sales. The objective is to analyze customer purchasing behavior, identify key target segments, and evaluate the commercial impact of a new store layout through rigorous A/B testing (Uplift Testing).

Unlike standard exploratory projects, this analysis bridges the gap between raw transaction data and actionable commercial strategies.

## 🎯 Business Objectives
1. **Customer Analytics:** Understand purchasing behaviors across different demographic segments to optimize promotional strategies and inventory placement.
2. **Experimentation & Uplift Testing:** Scientifically evaluate the performance of a trial store layout implemented in three specific stores against carefully selected control stores.

## 🛠️ Tech Stack & Methodologies
* **Language:** Python
* **Data Manipulation:** `pandas`, `numpy`
* **Data Visualization:** `matplotlib`, `seaborn`
* **Statistical Analysis:** `scipy.stats` (Independent T-Tests, Pearson Correlation, Magnitude Distance)
* **Techniques Used:** Feature Engineering, Time-Series Analysis, Control Store Selection algorithms, Statistical Significance Testing.

## 🔬 Methodology Highlight: A/B Testing Framework
To accurately assess the new store layouts, a robust control-store selection algorithm was developed. Instead of random assignment, control stores were matched to trial stores based on historical pre-trial data using a composite score:
* **Pearson Correlation:** Ensuring the stores' sales trends move together over time.
* **Normalized Magnitude Distance:** Ensuring the absolute volume of sales and customer footfall are historically similar.

## 📈 Key Business Insights

### 1. Purchasing Behavior & Seasonality
* **Peak Sales:** December 24th is the single highest sales day of the year, indicating a critical 4-day promotional window (Dec 21-24) where larger pack sizes (380g) dominate.
* **The "Impulse Buyer" Segment:** *Mainstream Young Singles/Couples* demonstrate statistically confirmed impulse buying behavior. A T-test (p < 2.2e-16) proved they pay significantly more per unit compared to their Budget/Premium counterparts.
* **Brand Affinities:** The aforementioned segment is 24% more likely to purchase *Tyrrells* and 27% more likely to buy 270g *Twisties*, making these prime candidates for high-traffic discretionary placements.

### 2. Store Trial Results (Uplift Testing)
* **Store 77 & Store 88:** Both stores showed a statistically significant uplift in both total sales and customer numbers during the trial period (exceeding the 95th percentile confidence interval of their respective control stores).
* **Store 86:** While customer numbers saw a significant increase, total sales did not breach the significance threshold. This discrepancy highlighted a crucial commercial insight: promotional pricing during the trial likely diluted the revenue impact despite increased footfall.
* **Conclusion:** The layout changes successfully drive customer acquisition. A broader rollout is recommended for stores matching the profiles of Store 77 and 88.

## 📁 Repository Structure
```text
├── data/                       # Raw and processed datasets (Ignored in git)
├── notebooks/
│   ├── 01_Data_Preparation_and_Customer_Analytics.ipynb
│   └── 02_Experimentation_and_Uplift_Testing.ipynb
├── presentations/
│   └── Category_Review_Presentation.pdf
└── README.md
