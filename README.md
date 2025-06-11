
# Gender Pay Equality Analysis – Forensic Technology Task

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
