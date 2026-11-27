# Sales Performance Investigation Using MySQL

## Project Overview

Management raised concerns about sales performance and wanted to understand which salespeople and regions were underperforming, what patterns might be contributing to weaker results, and what additional information would be needed before making business decisions.

I used **MySQL and SQL** to investigate sales performance across salespeople and regions.

---

## Business Questions

This analysis investigates:

- What are the overall sales, orders, returns, and average sales per order?
- Which salesperson generates the most and least sales?
- How does average sales per order differ between salespeople?
- Which salesperson has the highest returns and discount levels?
- Which region performs better?
- Does the regional performance gap remain after accounting for the number of salespeople?
- Are regional differences driven by order volume, order value, or both?
- What additional data is needed to determine the underlying cause of weak performance?

---

## Dataset

The analysis uses a `sales` table containing:

| Column | Description |
|---|---|
| `order_id` | Unique order identifier |
| `salesperson` | Name of the salesperson |
| `region` | Region assigned to the salesperson |
| `sales` | Sales value |
| `orders` | Number of orders |
| `returns` | Number of returned orders |
| `discount` | Discount associated with the sale |

The `sales.csv` file in this repository is an export of the dataset used for the analysis.

---

## Key Results

| Metric | Result |
|---|---:|
| Total Sales | KSh 280,000 |
| Total Orders | 57 |
| Total Returns | 9 |
| Average Sales per Order | KSh 4,912.28 |
| Highest Salesperson | Carol |
| Lowest Salesperson | Brian |
| Strongest Region | Western |
| Western Sales per Salesperson | KSh 107,500 |
| Eastern Sales per Salesperson | KSh 65,000 |
| Brian Return Rate | 33.33% |
| Brian Average Discount | 11.0% |

---

## Key Findings

### 1. Brian is the main salesperson requiring investigation

Brian has the lowest total sales and orders among the three salespeople.

He also has:

- The lowest average sales per order
- The highest average discount at **11.0%**
- The highest return rate at **33.33%**

These are warning signals that justify further investigation.

However, the available data does **not** prove that high discounting or returns are the cause of Brian's weaker performance.

### 2. Western outperforms Eastern

Western generates **KSh 215,000** compared with **KSh 65,000** in Eastern.

Western also has:

- More orders
- Higher average sales per order
- Higher sales per salesperson

### 3. The regional gap remains after accounting for salesperson count

Western has two salespeople while Eastern has only one.

To avoid comparing unequal team sizes, sales were normalized by salesperson count:

- **Western:** KSh 107,500 per salesperson
- **Eastern:** KSh 65,000 per salesperson

Eastern therefore remains weaker even after accounting for the difference in team size.

### 4. Eastern's weaker sales come from both order volume and order value

Eastern generates:

- **15 orders per salesperson**, compared with 21 in Western
- Approximately **KSh 4,333 per order**, compared with approximately KSh 5,119 in Western

This suggests that Eastern's weaker performance is associated with both **fewer orders** and **lower value per order**.

---

## Business Interpretation

The analysis identifies **Brian and the Eastern region as the main areas requiring attention**.

However, the current dataset cannot establish the underlying cause of the weaker performance.

Potential factors requiring further investigation include:

- Sales strategy and sales channels
- Product mix
- Customer segments
- Customer acquisition
- Customer service
- Reasons for returned products
- Product handling and delivery
- Seasonal or time-based sales patterns

These are **hypotheses rather than confirmed causes**.

---

## Recommendations

### Immediate Actions

- Investigate Brian's unusually high return rate.
- Review why Brian is applying higher discounts than the other salespeople.
- Review sales activity and order-generation methods in Eastern.
- Compare the products and customer types served in Eastern with those in Western.

### Additional Data

For a deeper root-cause analysis, additional data should be collected on:

- Product category
- Customer segment
- Sales channel
- Return reason
- Customer satisfaction
- Sales date/month

This would help determine whether the performance gap is primarily related to the salesperson, market, products, customers, or sales process.

---

## Important Limitation

Brian is the only salesperson in Eastern.

Therefore, the current dataset cannot cleanly separate the effect of **salesperson performance** from the effect of **regional or market conditions**.

The analysis should therefore be interpreted as identifying areas for further investigation rather than proving a single root cause.

---

## SQL Skills Demonstrated

This project demonstrates practical use of:

- `SELECT`
- `SUM()`
- `AVG()`
- `ROUND()`
- `GROUP BY`
- `ORDER BY`
- Subqueries
- Calculated metrics
- Percentage calculations
- Return-rate analysis
- Regional performance analysis
- Normalizing performance by salesperson count
- Translating SQL results into business insights
- Developing evidence-based recommendations

---

## Tools

- **MySQL**
- **MySQL Workbench**
- **SQL**
- **Jupyter Notebook**
- **GitHub**

---

## Project Structure

```text
sql-sales-performance-investigation/
│
├── README.md
├── Sales_Performance_Investigation_SQL_Portfolio.ipynb
└── sales.csv
```

---

## Conclusion

The investigation shows that **Brian and the Eastern region require further attention**.

The available data provides evidence of weaker performance through lower sales, fewer orders, lower average sales per order, higher discounting, and higher returns.

However, the data is not sufficient to identify the root cause with certainty. Additional product, customer, sales-channel, return-reason, customer-service, and time-based data would be required for a stronger investigation.
