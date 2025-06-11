# Daikibo-Machine-Performance-Analysis-Task_1
## 📊 Task Overview

This project is part of the **Deloitte Data Analytics Virtual Experience** on Forage. The goal was to analyze machine telemetry data collected from multiple factories operated by **Daikibo Industrials** to identify performance issues and downtime patterns.

---

## 🧠 What I Learned

- How to process and analyze telemetry data.
- How to use **Tableau** to build interactive dashboards.
- How to identify operational inefficiencies through data visualization.

---

## 🏭 Client Background

Daikibo Industrials operates four global factories:
- **Meiyo** (Tokyo, Japan)
- **Seiko** (Osaka, Japan)
- **Berlin** (Berlin, Germany)
- **Shenzhen** (Shenzhen, China)

Each location has 9 different machine types, reporting telemetry data every 10 minutes throughout **May 2021**.

---

## 🎯 Client Questions

1. **Which location experienced the most machine breakdowns?**
2. **Which machines in that location were responsible for most breakdowns?**

---

## 📈 Dashboard Features

The dashboard was created using **Tableau Desktop**, and includes:

- **Location-wise breakdown frequency** chart.
- **Machine-type breakdown heatmap**.
- Filters to explore factory-specific data.
- Time-series line graphs showing breakdown trends over time.

> 📍 Findings: The dashboard helped identify the **Shenzhen** factory as having the highest number of breakdowns, and **Machine Type 3** and **Machine Type 7** as the most frequent culprits in that location.

---
1. dashboard/ Deloitte_Task_1_Machine_Performance_Analysis.twb
3. images/ dashboard_screenshot.png
4. data/ telemetry_data.json # provided upon request. 



# Gender Pay Equality Analysis – Forensic Technology Task_2

🕵️‍♂️ Project Overview

This project is a simulation-based forensic analysis for **Daikibo Industrials**, focusing on internal gender pay inequality concerns. As part of the **Deloitte Data Analytics Virtual Experience** on Forage, I performed data classification to help the client draw insights from salary data.

---

🎯 Objective

To assist the Forensic Technology team by:
- Reviewing job-level gender pay equality scores.
- Classifying each score into an understandable category.
- Helping Daikibo leadership take data-backed decisions.

---

🗃️ Dataset

- **File**: `Task 5_Equality_Table 4_KrishnaSuthar.xlsx`
- **Source**: Provided as part of the Deloitte Forage program.
- **Contains**:
  - Role titles
  - Locations
  - Equality Score (calculated algorithmically)
  - (New) Equality Class — classification column added during analysis

---
🔍 Methodology

1. **Explored the dataset** for completeness.
2. **Created a new column** named `Equality Class`, using the following classification rules:

   | Equality Score Range | Classification         |
   |----------------------|------------------------|
   | Between -10 and +10  | Fair                   |
   | Between -20 to -10 or +10 to +20 | Unfair   |
   | Less than -20 or more than +20  | Highly Discriminative |

3. Used **Excel formulas** to apply conditional logic for classification.

---

🧮 Formula Used:

=IF(AND([@[Equality Score]] >= -10, [@[Equality Score]] <= 10), "Fair", IF(AND([@[Equality Score]] > -20, [@[Equality Score]] < -10) + AND([@[Equality Score]] > 10, [@[Equality Score]] < 20), "Unfair", "Highly Discriminative"))
