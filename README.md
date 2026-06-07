# Retail Sales Intelligence
### End-to-End Analytics Pipeline | Python · SQL · Power BI · Excel

---

## Business Problem
A retail company was experiencing inconsistent profitability 
despite growing overall revenue. The objective was to identify 
which products, regions, and discount patterns were causing 
profit leakage — and quantify the recovery opportunity.

---

## Key Findings
- **$156K profit leakage** identified in the Furniture category
- **Central region** operating at **-18.5% profit margin** 
  driven by excessive discounting
- **78% of revenue** concentrated in just **8 sub-categories** 
  (Pareto Analysis)
- Orders with discounts **above 20%** produce negative profit 
  **73% of the time**
- Revenue grew **29.5% YoY** but profit margin simultaneously 
  compressed — growth without profitability
- **20% discount cap** identified as break-even threshold 
  via Excel Goal Seek modeling

  <img width="1425" height="800" alt="image" src="https://github.com/user-attachments/assets/80a0d0a2-c5f9-4c07-bc8b-cac4c6b27316" />


---

## Tools & Technologies
| Tool | Purpose |
|------|---------|
| Python (Pandas, Seaborn, Matplotlib) | EDA, cleaning, visualization |
| SQL (CTEs, Window Functions) | Business queries, Pareto analysis |
| Power BI (DAX, Star Schema) | Executive dashboard |
| Excel (Goal Seek, What-If) | Sensitivity modeling |

---

## Project Structure
## Python Analysis Highlights
- Analyzed **9,994 transactions** across 4 years
- Engineered **Profit Margin %** and **Shipping Days** features
- Segmented customers into **3 value tiers** using `pd.cut()`
- Built correlation matrix revealing discount-profit relationship
- Exported clean dataset for SQL and Power BI consumption

---

## SQL Highlights
- **Pareto Analysis** using CTEs and `SUM() OVER()` 
  window function
- **MoM Growth** calculated using `LAG()` window function
- **Regional margin** breakdown using `GROUP BY` + `HAVING`
- **Discount band classification** using `CASE WHEN`

---

## Power BI Dashboard
- **3-page dark-mode executive dashboard**
- Star Schema data model with Calendar table
- 4 DAX measures:
  - Profit Leakage Isolation (`$156K`)
  - Dynamic Discount Sensitivity Slicer
  - YoY Growth Tracking (`29.5%`)
  - Policy Violation Flag (`>20% cap`)
- Geographic drill-through to state-level margin breakdown

---

## Excel Modeling
- **Goal Seek** analysis determining 20% break-even threshold
- **What-If Analysis** across 3 discount scenarios
- **Pivot Tables** for regional and category validation
- Cross-verified all Python and SQL findings

---

## Dataset
Sample Superstore — publicly available retail dataset  
Source: Kaggle

---

## Key Business Recommendation
Implement a **hard 20% discount ceiling** for the Furniture 
category in the Central region. Based on current order volumes, 
this policy change represents a **$156K annual profit 
recovery opportunity**.
