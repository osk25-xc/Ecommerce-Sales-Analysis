# E-commerce Data Quality & KPI Checklist

Use this checklist before publishing sales or customer-revenue findings. Confirm the actual dataset columns and grain first; the checks below are business rules, not assumptions about column names.

## 1. Grain and keys
- [ ] State whether each row represents an order, order line, payment, or event.
- [ ] Identify the order key and, if applicable, the order-line key.
- [ ] Check missing keys and duplicate keys at the declared grain.
- [ ] Count distinct orders separately from row counts.

## 2. Field validation
- [ ] Check date fields parse correctly and fall within the documented period.
- [ ] Review missing customer, product, quantity, price, and status values where present.
- [ ] Flag non-positive quantities or prices for investigation rather than silently deleting them.
- [ ] Standardize category and status labels without losing source values.

## 3. Revenue reconciliation
- [ ] Document whether revenue is gross or net of discounts, refunds, and returns.
- [ ] Reconcile line-level totals to order-level totals where both are available.
- [ ] Define AOV as the selected revenue measure divided by distinct eligible orders.
- [ ] State the population and denominator for return and repeat-customer rates.

## 4. Reporting checks
- [ ] Reconcile segment totals to the overall total.
- [ ] Show sample sizes with segment rates.
- [ ] Record filters, date range, exclusions, and assumptions.
- [ ] Add numerical conclusions only after reproducing them from the current dataset.

## Limitations
If the source is synthetic practice data, label it clearly. These checks do not establish real commercial performance.