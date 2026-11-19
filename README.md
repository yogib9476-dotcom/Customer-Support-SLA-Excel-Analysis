# Customer Support SLA & Escalation Performance Analysis (Excel)
<img width="1192" height="787" alt="Dashboard_Overview" src="https://github.com/user-attachments/assets/318fc37a-67bc-4fb5-9df2-6216e1a06d7d" />

## Project Overview
An end-to-end operational analytics project evaluating **8,469 customer support tickets** across multiple channels and priority tiers. The objective is to identify Service Level Agreement (SLA) breach drivers, quantify financial penalty exposure, and provide actionable recommendations to improve resolution speed and Customer Satisfaction (CSAT).
## Business Questions Answered
1. What is the overall SLA compliance rate, open backlog volume, and total breach penalty exposure?
2. Which ticket categories (`Billing`, `Cancellation`, `Technical`, `Refund`, `Product`) experience the highest SLA breach rates?
3. How do support channels (`Chat`, `Email`, `Phone`, `Social Media`) compare across resolution speed, penalty costs, and CSAT scores?
4. What monthly trends exist in ticket volume and SLA breach costs?
## Tools & Excel Techniques Used
* **Data Cleaning & Structuring:** Standardized mixed timestamp formats, removed PII columns, handled `NaN`/open ticket nulls without skewing averages, and structured the dataset as a dynamic Excel Table (`TicketsTable`).
* **Lookup & Relational Modeling (`VLOOKUP` + `TRIM`):** Built a separate `SLA_Reference` table mapping priority tiers (`Critical: 4h`, `High: 12h`, `Medium: 24h`, `Low: 48h`) to target resolution windows and financial breach penalties (`$10`–`$150` per breach).
* **Calculated Metrics (`IF`, `ABS`, `ROUND`, `ISBLANK`):** Engineered `Resolution_Hours`, `Target_SLA_Hours`, `SLA_Status` (`Met`, `Breached`, `In Progress`), and `Penalty_Cost`.
* **Pivot Tables & Interactive Dashboard:** Built 4 interconnected Pivot Tables feeding KPI cards, a 100% Stacked Bar Chart, a Dual-Axis Combo Trend Chart, and dynamic Slicers (`Ticket Channel` and `Ticket Priority`).
## Key Findings & Recommendations
* **High Open Backlog (67.3% In Progress):** Over two-thirds of tickets remain unresolved, creating significant latent SLA breach risk if aged queues are not triaged.
* **Cancellation Requests Lead Breaches (8.3%):** Cancellation inquiries have the highest SLA breach rate—implementing automated self-service cancellation workflows can reduce breach penalties immediately.
* **Email & Social Media Drive Highest Penalties ($22,950 & $22,350):** Chat achieves the highest customer satisfaction (**3.08 CSAT**) and lowest penalty cost (**$19,275**), highlighting a clear opportunity to shift complex Email escalations toward live Chat support.
## Repository Files
* `Customer_Support_SLA_Analysis.xlsx` — Full workbook containing `Dashboard`, `Clean_Data`, `SLA_Reference`, and `Pivot_Table` tabs.
* `dashboard_overview.png` — High-resolution preview of the interactive dashboard.
