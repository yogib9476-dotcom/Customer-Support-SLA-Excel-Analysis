# Customer Support SLA & Escalation Performance Analysis (Excel)
![Dashboard Overview](images/dashboard_overview.png)
## Project Overview
An end-to-end operational data analytics project evaluating **8,469 customer support tickets** across multiple communication channels and priority tiers[cite: 6]. The objective is to identify Service Level Agreement (SLA) breach drivers, quantify financial penalty exposure, and deliver actionable recommendations to improve resolution speed and Customer Satisfaction (CSAT).
## Data Source
* **Dataset:** *Customer Support Ticket Dataset* (`customer_support_tickets.csv`)
* **Dataset Author:** Suraj Jha (Kaggle)
* **Scope:** 8,469 support records across 5 ticket types and 4 support channels[cite: 6]
## Business Questions Answered
1. What is the overall SLA compliance rate, open ticket backlog, and total financial penalty exposure?
2. Which ticket categories (`Billing`, `Cancellation`, `Technical`, `Refund`, `Product`) experience the highest SLA breach rates?[cite: 7, 9]
3. How do support channels (`Chat`, `Email`, `Phone`, `Social Media`) compare across resolution speed, penalty costs, and CSAT scores?[cite: 6]
4. What monthly trends exist in ticket volume and SLA breach penalties?[cite: 9]
## Excel Techniques & Workflow
* **Data Cleaning & Structuring:** Standardized mixed timestamp formats, removed PII fields, preserved `NaN`/open ticket nulls to avoid skewing resolution averages, and structured the dataset as a dynamic Excel Table (`TicketsTable`).
* **Relational Lookup (`VLOOKUP` + `TRIM`):** Built a dedicated `SLA_Reference` table mapping priority tiers (`Critical: 4h`, `High: 12h`, `Medium: 24h`, `Low: 48h`) to target resolution windows and breach penalties (`$10`–`$150` per breach).
* **Feature Engineering (`IF`, `ABS`, `ROUND`, `ISBLANK`):** Created calculated columns for `Resolution_Hours`, `Target_SLA_Hours`, `SLA_Status` (`Met`, `Breached`, `In Progress`), and `Penalty_Cost`[cite: 7].
* **Pivot Tables & Interactive Reporting:** Built 4 interconnected Pivot Tables powering dynamic KPI cards, a horizontal SLA breakdown chart, a dual-axis monthly combo trend chart, and interactive Slicers (`Ticket Channel` and `Ticket Priority`)[cite: 9].
## Key Findings & Recommendations
* **High Open Backlog (67.3% In Progress):** Over two-thirds of tickets remain unresolved, creating significant latent SLA breach risk if aged queues are not triaged[cite: 7, 9].
* **Cancellation Requests Lead Breaches (8.3%):** Cancellation inquiries experience the highest SLA breach rate—implementing automated self-service cancellation flows can reduce penalties immediately[cite: 7, 9].
* **Email & Social Media Drive Highest Penalties ($22,950 & $22,350):** Chat achieves the highest customer satisfaction (**3.08 CSAT**) and lowest penalty cost (**$19,275**), highlighting an opportunity to route complex Email escalations toward live Chat[cite: 6, 9].
## Interactive Slicer Demo
![Filtered Dashboard View](images/dashboard_filtered_chat_critical.png)
*Example view filtered dynamically by `Channel = Chat` and `Priority = Critical` (504 tickets, 7 hrs avg resolution, $15,150 penalty, 3.13 CSAT)[cite: 9].*
## Repository Structure
* `Customer_Support_SLA_Analysis.xlsx` — Complete Excel workbook (`Dashboard`, `Clean_Data`, `SLA_Reference`, `Pivot_Table`)[cite: 9].
* `images/` — High-resolution dashboard screenshots for portfolio preview.
![Filtered Dashboard View](images/dashboard_filtered_chat_critical.png)
*Example view filtered dynamically by `Channel = Chat` and `Priority = Critical` (504 tickets, 7 hrs avg resolution, $15,150 penalty, 3.13 CSAT)[cite: 9].*
## Repository Structure
* `Customer_Support_SLA_Analysis.xlsx` — Complete Excel workbook (`Dashboard`, `Clean_Data`, `SLA_Reference`, `Pivot_Table`)[cite: 9].
* `images/` — High-resolution dashboard screenshots for portfolio preview.
