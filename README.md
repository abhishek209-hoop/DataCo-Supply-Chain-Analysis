DataCo Supply Chain Analytics

End-to-end analysis of an e-commerce supply chain: SQL and Python for the analysis, Power BI for interactive KPI dashboards, and a set of recommendations for reducing late deliveries.

Overview

DataCo is a global company selling clothing, sports and electronics products through multiple markets. Late deliveries hurt customer experience and profit, but the causes are spread across regions, shipping modes and product categories.

This project cleans the order data, analyzes what drives delivery delays, and presents the results as a Power BI dashboard that operations and sales teams can use to monitor supply chain performance.

Key numbers

Metric	Value
Orders analyzed	65K+
Customers	20K+
Attributes analyzed	53
Product categories	50
Regions	23
Markets	5
Orders flagged with late-delivery risk	54.8%
Business questions
How are revenue, profit and order volume performing overall?
How often are deliveries late, and where is the problem concentrated?
Which shipping modes, regions and product categories drive delivery delays?
How do customer segments differ in revenue and profitability?
What should the business change to improve delivery performance?
Dataset
Source: DataCo Smart Supply Chain for Big Data Analysis, published on Mendeley Data and mirrored on Kaggle.
Content: order, customer, product, shipping and financial fields covering provisioning, production, sales and distribution.
Note: the Late_delivery_risk field in the dataset is a flag on each order. The 54.8% figure is the share of orders carrying that flag.
Tools
Area	Tools
Analysis	Python (Pandas, NumPy), SQL
Visualization	Power BI (DAX, Power Query)
Supporting	Excel
<!-- Keep only the tools you actually used. Remove DAX / Power Query if they don't apply. -->
Approach
Data cleaning (Python, Pandas): checked missing values and duplicates, fixed data types and dates, and removed columns not useful for analysis.
Exploratory analysis (Python, SQL): summarized sales, profit and delivery performance by region, market, shipping mode, category and customer segment.
Delivery-delay analysis: compared scheduled and actual shipping days and measured late-delivery risk across all 53 attributes to find where delays concentrate.
Dashboard (Power BI): built KPI pages for revenue, profitability, shipping lead time and delivery performance, with filters for market, region, shipping mode and category.
Recommendations: turned the findings into actions for operations and sales.
Example query
sql
-- Late-delivery risk by shipping mode (adjust names to match your table)
SELECT
    shipping_mode,
    COUNT(*)                                   AS orders,
    ROUND(100.0 * AVG(late_delivery_risk), 1)  AS late_risk_pct,
    ROUND(AVG(days_for_shipping_real), 2)      AS avg_actual_days,
    ROUND(AVG(days_for_shipment_scheduled), 2) AS avg_scheduled_days
FROM orders
GROUP BY shipping_mode
ORDER BY late_risk_pct DESC;
Dashboard
Page	What it shows
Executive summary	Total sales, profit, orders, customers, overall late-delivery rate
Delivery performance	Scheduled vs actual shipping days, late-delivery risk by shipping mode and region
Product and category	Sales and profit across 50 categories
Market and region	Performance across 5 markets and 23 regions
Customer segments	Revenue and profitability by segment
<!-- Rename the pages to match your .pbix file and add a screenshot of each. -->
Key findings
54.8% of orders carry a late-delivery risk flag across the 65K+ orders analyzed.
Recommendations
[Review the shipping mode with the highest late-delivery risk: change scheduled lead times or switch carriers.]
[Prioritize the regions with the worst delivery performance for logistics improvements.]
[Set up regular KPI tracking in the dashboard, with alerts when the late-delivery rate goes above a set limit.]
Repository structure
DataCo-Supply-Chain-Analysis/
├── data/                  # raw and cleaned data (or a link, if the file is large)
├── notebooks/             # Python analysis (cleaning, EDA)
├── sql/                   # SQL queries
├── dashboard/             # Power BI file (.pbix) and PDF export
├── images/                # dashboard screenshots
└── README.md
<!-- Edit this tree to match your actual folders and file names. -->
How to reproduce
Download the dataset from the link above and place it in data/.
Install the Python packages: pip install pandas numpy jupyter.
Run the notebooks in notebooks/ in order to clean the data and reproduce the analysis.
Run the queries in sql/ against the cleaned data.
Open the .pbix file in dashboard/ with Power BI Desktop and refresh the data source path.
What I learned
Turning a wide dataset (53 attributes) into a focused set of KPIs.
Combining SQL, Python and Power BI in one workflow.
Linking operational findings to practical recommendations.
Author

Saranga Abhishek B.Tech, Mineral and Metallurgical Engineering, IIT (ISM) Dhanbad
