# E-Commerce Sales, Customer & Product Analytics (Power BI)

An end-to-end Power BI project that analyses an e-commerce business across sales, customers, products, orders and payments. It includes data cleaning in Power Query, a star-schema data model, 22 DAX measures and a 6-page interactive dashboard.

> Note: this is a practice dataset, so the findings show what the dashboard can reveal, not the results of a real company.

## Dashboard Preview

![Executive Summary](screenshots/01_executive_summary.png)

Full dashboard (PDF): [Ecommerce_Dashboard.pdf](Ecommerce_Dashboard.pdf)

## Dataset

| File | Rows | Description |
|---|---|---|
| customers.csv | 100 | Customer name, city, signup date |
| products.csv | 50 | Product name, category, price, stock |
| orders.csv | 500 | Order date, status, payment method |
| order_items.csv | 1,500 | Quantity and unit price for each order line |

Orders cover 12 May 2025 to 12 May 2026.

## Tools Used

- Power BI Desktop
- Power Query (data cleaning and profiling)
- DAX (measures and calculated columns)

## What I Did

**1. Data cleaning (Power Query)**
- Profiled every column: all data is 100% valid, with no errors, nulls or duplicate IDs
- Converted dates from text to Date, price to fixed decimal, and quantity and stock to whole numbers
- Found 26 orders with no order items (zero revenue) and 1 customer who never ordered, and documented both

**2. Data model**
- Star schema with order_items in the centre, linked to orders, customers, products and a date table
- Date table linked to order_date, with a second inactive link to signup_date (used with USERELATIONSHIP)
- All relationships are one-to-many with single-direction filtering

**3. DAX**
- Calculated columns: Order Value, Customer Type (High Value, Repeat, Occasional, One-Time, Never Ordered), Stock Status
- 22 measures: Total Revenue, Net Revenue, AOV, Repeat Rate, Cancellation Rate, Revenue Growth and more

**4. Dashboard (6 pages)**
1. Executive Summary
2. Sales Performance
3. Customer Analytics
4. Product & Category
5. Orders & Payments
6. Customer Retention

## Key Findings

- Total revenue is Rs 116.15M, but only Rs 79.79M (about 69%) comes from delivered orders
- Electronics (Rs 38.5M) and Sports (Rs 33.2M) bring in about 62% of revenue
- Mumbai and Bengaluru lead the cities in revenue
- 96% of active customers ordered more than once, averaging about 5 orders each
- High Value customers are 29% of customers but about 48% of revenue (Rs 55.8M)
- Cash on Delivery has the highest cancellation rate (14.6%) and UPI the lowest (6.3%)
- 71 orders are still pending, worth about Rs 19.5M
- Monthly revenue ranges from Rs 6.1M to Rs 13.4M with no sustained growth (the first and last months are partial)
- Only 3 of 50 products are low on stock; Classic Incidunt and Pro Possimus sell well and should be restocked first

## Recommendations

- Protect High Value customers with loyalty rewards
- Encourage UPI over Cash on Delivery to reduce cancellations
- Investigate the high cancellation rate in Mumbai
- Restock fast-selling low-stock products and clear the pending order backlog

## Limitations

- Practice dataset, so results are not from a real business
- The data shows patterns, not causes
- The first and last months are partial months
- Customer segment rules are my own definitions (High Value means lifetime revenue of Rs 15 lakh or more)

## How to Open

1. Install Power BI Desktop (free, Windows only)
2. Download Ecommerce_Analytics.pbix from this repository
3. Open it in Power BI Desktop

## Screenshots

![Sales](screenshots/02_sales.png)
![Customers](screenshots/03_customers.png)
![Products](screenshots/04_products.png)
![Orders and Payments](screenshots/05_orders_payments.png)
![Retention](screenshots/06_retention.png)
![Data Model](screenshots/model_view.png)
![Power Query Steps](screenshots/power_query_steps.png)

## Author

**Aradabanda Arun Kumar**
Data Analyst | Excel, SQL, Power BI
LinkedIn: https://www.linkedin.com/in/aradabanda-arun-kumar
