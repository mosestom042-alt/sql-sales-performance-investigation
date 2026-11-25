# Sales Performance Investigation Using SQL

A MySQL portfolio project investigating salesperson and regional sales performance.

## Business Objective

Management wants to understand where sales performance is weak, what patterns may be contributing to the problem, and what additional data is required before making business decisions.

## Key Findings

- Brian is the primary salesperson requiring investigation.
- Brian has the lowest sales and orders, lowest average sales per order, highest average discount (11%), and highest return rate (33.33%).
- Eastern is weaker than Western even after adjusting for salesperson count.
- Eastern generates 15 orders per salesperson compared with 21 in Western.
- Eastern generates approximately KSh 65,000 sales per salesperson compared with KSh 107,500 in Western.
- Eastern also has a lower average sales per order.

## Important Limitation

Brian is the only salesperson in Eastern, so the dataset cannot cleanly separate salesperson effects from regional effects. The analysis identifies areas requiring investigation but does not prove a single root cause.

## Tools

- MySQL
- SQL
- Jupyter Notebook
- GitHub
