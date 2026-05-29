# Sales Dashboard Power BI Project

## Project Objective
The objective of this project was to develop an interactive Power BI dashboard for analyzing sales performance, referral sources, payment methods, customer orders, and revenue trends.

---
## Dashboard Features

- KPI Cards
- Monthly Revenue Trend
- Revenue by Referral Source
- Revenue by Product
- Revenue by Payment Method
- Order Status Distribution
- Interactive Slicers and Filters

---
## Dataset Description

The dataset contains:
- Sales transactions
- Products
- Referral sources
- Payment methods
- Coupon information
- Revenue values
- Order statuses
- Customer orders
---
## Tools Used

- Power BI Desktop
- DAX
- Excel
- GitHub
---

## DAX Measures Used

```DAX
Total Revenue = SUM(Orders[TotalPrice])

Total Orders = COUNT(Orders[OrderID])

Total Quantity Sold = SUM(Orders[Quantity])

Average Order Value = AVERAGE(Orders[TotalPrice])

Coupon Usage Rate % = DIVIDE(
    [Orders Using Coupons],
    [Total Orders],
    0
)

Orders Using Coupons = CALCULATE(
    COUNT(Orders[OrderID]),
    FILTER(
        Orders,
        Orders[CouponCode] <> "NO COUPON"
            && NOT(ISBLANK(Orders[CouponCode]))
    )
)
```
---
## Key Insights

- Highest revenue was generated in June
- Chair generated the highest product revenue
- Instagram generated the highest referral revenue
- Credit Card was the most used payment method
- Cancelled orders accounted for approximately 21% of total orders

---
## Files Included

- Sales_Dashboard.pbix
- sales_dataset.csv
- dashboard_report.pdf
- dashboard_overview.png
- dax_measures.txt

---
## Skills Demonstrated

- Power BI Dashboard Development
- Data Visualization
- KPI Reporting
- DAX Calculations
- Business Intelligence
- Interactive Dashboard Design
---

## Conclusion

This dashboard successfully visualizes sales performance and customer purchasing behavior through interactive charts, KPIs, and business intelligence reporting techniques.
