# Supply Chain Performance Analysis — Shipping Reliability & Revenue Impact

Analysis of 180,000+ orders from DataCo Global's supply chain to quantify how often
shipments arrive late, how much revenue is tied up in those late orders, where the
problem is concentrated, and a short-term order volume forecast for planning purposes.

## Business Problem
Late deliveries erode customer trust and tie up revenue in unresolved orders. This
project answers four questions a supply chain / operations team would actually ask:
1. How often do orders arrive late, and is premium shipping actually faster?
2. How much revenue sits inside late orders?
3. Is the problem concentrated in specific regions, or company-wide?
4. What's a reasonable near-term order volume forecast for capacity planning?

## Key Findings
- **54.8%** of all orders in the dataset were delivered late.
- **~$20.1M (54.7% of total revenue)** is tied up in late orders.
- **First Class shipping has a 95.3% late rate** — worse than the cheapest option
  (Standard Class, 38.1%). Customers pay a premium for a promise that isn't kept.
- Going one level deeper: delay *magnitude* by shipping mode shows First Class is
  **always exactly 1 day over schedule** for every single order, and other modes
  split evenly across a tiny fixed set of values — a pattern real courier delays
  don't produce. This looks like a synthetically generated pattern in the dataset
  rather than organic operational variability, and the report treats it as such.
- Late delivery rate is **flat (~54–58%) across every region and market**, pointing
  to a systemic/company-wide fulfillment issue rather than a localized one.
- A simple ARIMA(1,1,1) model forecasts next-quarter order volume with a validated
  error of ~1.5% of average monthly volume on a 6-month holdout test.


