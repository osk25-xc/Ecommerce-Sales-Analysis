# E-commerce Sales Analysis Plan

## Project Goal
Analyze transaction-level e-commerce data to understand sales performance, product demand, customer behavior, and changes over time. Final findings should be calculated from the actual dataset rather than assumed in advance.

## 1. Data Preparation
Before analysis:
- Check the dataset grain (for example, one row per order item or one row per order).
- Review column names, data types, date formats, and currency units.
- Count missing values and duplicate records.
- Check for invalid quantities, negative prices, and inconsistent category or status labels.
- Document any exclusions and cleaning decisions.

## 2. Core Business Metrics

| Metric | Definition | Important consideration |
|---|---|---|
| Total Revenue | Sum of line-item sales value | Confirm whether discounts, tax, and shipping are included |
| Total Orders | Count of distinct order IDs | Do not count order-item rows as separate orders |
| Units Sold | Sum of quantity | Exclude cancelled items if the business rule requires it |
| Average Order Value | Revenue / distinct orders | Use the same order and revenue filters |
| Revenue by Month | Revenue grouped by order month | Use the order date and a consistent timezone |
| Product Contribution | Product revenue / total revenue | Check product-level aggregation |
| Repeat Customer Rate | Repeat customers / customers with valid purchase history | Define the observation period clearly |

## 3. Analysis Questions
1. How does revenue change month over month?
2. Which products and categories contribute the most revenue?
3. Which products have high order volume but low revenue contribution?
4. How are orders distributed across available regions or channels?
5. What share of customers place more than one order?
6. Are there unusual spikes, drops, or data-quality issues that need investigation?

Only investigate dimensions that are present and sufficiently complete in the dataset.

## 4. Validation Checks
- Reconcile aggregated revenue with the source total.
- Compare distinct order counts before and after cleaning.
- Check that category and product totals reconcile to overall revenue.
- Verify date boundaries and treatment of cancelled or returned orders.
- Recalculate key KPIs independently before publishing results.

## 5. Deliverables
- Cleaned dataset or documented cleaning steps
- Reproducible SQL queries or notebook
- KPI summary and trend visualizations
- Key findings supported by calculated values
- Business recommendations with assumptions and limitations

## Current Status
This file records the analysis approach. Numerical findings and final recommendations will be added only after the source dataset and its columns have been verified.
