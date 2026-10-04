Apple Sales Data Analysis

Project Overview

An independent data analysis project built on a global Apple product sales dataset (2022–2024). It combines a data quality review of the source file with an interactive Power BI dashboard covering sales, products, regions, customers, returns, and discounts.

Business Objective

Analyze sales performance, revenue, quantity sold, products, categories, regions, customer ratings, returns, sales channels, payment methods, and discount performance, and present the findings through an interactive dashboard.

Key Business Questions

1. How have revenue, sales count, average order value, and quantity sold changed over time?
2. Which products and categories drive revenue and units sold?
3. Which regions and cities contribute the most?
4. How is revenue distributed across sales channels and payment methods?
5. How common are discounts, and how do discounted sales compare with non-discounted ones?
6. How do returns and customer ratings vary by category, age group, and region?

Dataset

Item| Detail
File| "apple_global_sales_dataset.csv"
Size| 11,500 rows × 27 columns
Period| 2022–2024
Coverage| 47 countries, 8 regions, 514 cities, 43 products, 6 categories
Granularity| One row represents one sale record
Total revenue| $18,035,669.25
Total units sold| 23,270
Total sales| 11,500
Source / license| Not specified

Data Quality & Limitations

Checks passed: no duplicate rows, date fields are consistent with the sale date, and revenue is consistent with discounted price × units sold in every row.

Issues and limitations:

- "storage" contains 4,804 "N/A" values (Accessories, Apple Watch, AirPods).
- "previous_device_os" contains 8,056 "N/A" values (all non-iPhone rows).
- "customer_rating" is missing in 3,360 rows (29.2%).
- 22 rows differ by $0.01 between the discounted price and unit price × (1 − discount %), consistent with rounding.
- Russia and Turkey are grouped in a combined "Europe/Asia" region (480 rows).
- Each currency uses a single fixed FX rate across all three years.
- There is no customer ID.
- There is no cost or profit field.
- Source and license: Not specified.

Tools & Technologies

Power BI · Power Query · DAX · Field Parameters · Data Visualization · Data Analysis

Dashboard Structure

The report uses a 1280×720 canvas with custom page backgrounds and navigation buttons between pages. It contains four analytical pages.

Page| Focus| Main content
KPIs| Overall performance and trend| Revenue, # Sales, AOV and quantity cards with growth indicators; monthly revenue line; revenue by category and sales channel; return status donut; Year and Month slicers
Revenue| Sources of revenue| Revenue by payment method, city, category and discount category; revenue gauge with min/max/target; Year, Month and field-parameter slicers
Quantity| Units sold| Product table with quantity, previous-month quantity, growth %, and top-selling color; quantity by category, region and discount category; quantity gauge; Year, Month and field-parameter slicers
Customers| Ratings and returns| Average rating by age group and region; return status by age group; rating category donut; region field-parameter slicer

Field parameters allow selected charts to switch between different dimensions, including city, region, category, and product-related views.

On the KPIs page, the Month slicer is configured not to filter the monthly revenue line or the Revenue year-over-year growth card.

The file also contains a fifth page, Report, which duplicates the Customers page and is not counted as a separate analytical page.

Key Insights

1. Mac is the main revenue driver. Mac represents only 16% of orders but generates 46% of revenue, while iPhone accounts for 30% of orders and 32% of revenue, highlighting Mac's significant contribution to overall sales.

2. Mac Pro (M2 Ultra) has a major impact on total revenue. It generates 20.7% of total revenue from only 2.4% of orders, making it the strongest individual product contributor to revenue.

3. Mac Pro drove most of the 2024 revenue growth. Of the $432K increase in revenue from 2023 to 2024, approximately $399K (92%) came from Mac Pro, particularly the Mac Pro (M2 Ultra).

4. iPhone has the highest return rates. iPhone has recorded the highest return rates among product categories over the past three years, particularly among customers aged 45+.

5. Apple.com is the only sales channel showing sustained decline. Online (Apple.com) revenue fell 7.1% in 2024 and declined 16.8% compared with 2022, while Authorized Resellers grew 35.5% and Carrier Stores grew 14.4%.

6. Growth is increasingly coming from smaller markets. Europe (34.4%) and Asia (30.1%) account for approximately 65% of revenue, while the fastest growth in 2024 came from the Middle East (+24%), Africa (+20%), and Oceania (+16%). The Middle East also recorded the highest AOV at $1,676, compared with $1,432 in South America.

Recommendations

1. Prioritize Mac in revenue performance monitoring and track Mac separately from other categories, given its disproportionate contribution to revenue relative to order volume.

2. Monitor Mac Pro (M2 Ultra) as a key revenue contributor and track its performance separately to understand its impact on overall revenue.

3. Analyze the sustainability of Mac Pro's growth by monitoring its performance across future periods and identifying whether growth is broadening across other Mac products.

4. Investigate iPhone returns among customers aged 45+ to identify potential product, service, or customer-experience factors contributing to the higher return rate.

5. Review Apple.com's declining performance and compare its product mix, customer segments, and regional performance with Authorized Resellers and Carrier Stores to identify areas for improvement.

6. Evaluate growth opportunities in the Middle East, Africa, and Oceania, particularly the Middle East given its combination of strong growth and the highest AOV.

Technical Skills Demonstrated

- Data quality assessment (completeness, duplicates, and consistency checks)
- Power BI dashboard development
- KPI analysis
- DAX measures and calculated columns
- Power Query
- Field Parameters for dynamic dimension selection
- Slicers and customized visual interactions
- Data visualization using cards, line charts, bar charts, column charts, donut charts, gauges, and tables
- Business insight generation
- Data storytelling

Project Limitations

- Profitability cannot be assessed because there is no cost or profit field.
- Customer-level or customer purchase-history analysis is limited because there is no customer ID.
- Discount findings are descriptive and do not establish causal impact on sales or volume.
- The causes behind changes in revenue cannot be determined from the available dataset alone.
- Regional analysis depends on the region labels provided in the dataset, including the combined "Europe/Asia" region.
- Customer ratings are missing for 29.2% of records.
- The dataset's source and license are not specified.

Conclusion

The analysis highlights Mac as the primary revenue driver, with Mac Pro (M2 Ultra) playing a particularly significant role in both total revenue and 2024 growth. The analysis also identifies higher iPhone return rates among older customers, a sustained decline in Apple.com's revenue, and strong growth opportunities across smaller markets, particularly the Middle East.

The findings demonstrate how Power BI can be used to transform transactional sales data into actionable business insights while recognizing the limitations of the available data.

Dashboard Preview

KPIs

KPIs.png


Revenue

![Revenue.png]

Quantity

![Quantity.png]

Customers

![Customers.png]
