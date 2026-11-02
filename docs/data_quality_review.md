# E-commerce Data Quality Review

Use this checklist before publishing any sales result.

## Structural checks
- Identify the grain: order, order line, shipment, or payment.
- Confirm primary identifiers and expected uniqueness.
- Parse dates consistently and record the observed date range.
- Check numeric types for quantity, unit price, discount, and sales.

## Business-rule checks
- Investigate zero or negative quantities and prices.
- Check discount values against the documented scale.
- Identify cancelled, refunded, or returned transactions and define their treatment.
- Reconcile line-level sales to order-level totals where both are available.

## Reporting checks
Define revenue, order count, and customer count before analysis. Use distinct identifiers at the correct grain. Include filters, denominator, and date window with every KPI.

## Findings
Keep observations separate from hypotheses. Add numeric findings only after rerunning the analysis on the current repository data.
