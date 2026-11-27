# Sales Performance Investigation Using MySQL

## Project Overview

Management raised concerns about sales performance and wanted to understand which salespeople and regions were underperforming, what patterns might be contributing to weaker results, and what additional information would be needed before making business decisions.

I used **MySQL and SQL** to investigate the sales table by salesperson and region.

## Business Questions

- What are the overall sales, orders, returns, and average sales per order?
- Which salesperson generates the most and least sales?
- How does average sales per order differ by salesperson?
- Which salesperson has the highest returns and discount levels?
- Which region performs better?
- Does the regional performance gap remain after accounting for salesperson count?
- Are regional differences driven by order volume, order value, or both?
- What additional data is needed to determine the underlying cause of weak performance?

## Key Findings

- **Carol** has the highest total sales and orders.
- **Brian** has the lowest sales and orders and the lowest average sales per order.
- Brian has the highest average discount at **11.0%**.
- Brian has the highest return rate at **33.33%**.
- **Western** generates **KSh 215,000** compared with **KSh 65,000** in Eastern.
- After adjusting for salesperson count, Western generates **KSh 107,500 per salesperson**, compared with **KSh 65,000** in Eastern.
- Eastern has fewer orders per salesperson (**15 vs. 21**) and a lower average sales per order (**~KSh 4,333 vs. ~KSh 5,119**).

## Important Limitation

Brian is the only salesperson in Eastern. Therefore, the current data cannot cleanly separate salesperson performance from regional or market effects.

The analysis identifies areas requiring further investigation, but it does **not** prove that discounts, returns, customer service, products, or sales strategy are the root cause.

## Recommended Next Analysis

Additional data on:

- Product category
- Customer segment
- Sales channel
- Return reason
- Customer satisfaction
- Sales date/month

would allow a deeper root-cause investigation.

## Tools

- MySQL
- MySQL Workbench
- SQL
- Jupyter Notebook
- GitHub
