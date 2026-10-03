# DataCo Supply Chain Dashboard (Power BI)

A three-page Power BI report for monitoring global supply chain activity and delivery performance at DataCo. It tracks orders, sales, profit, shipping lead time and on-time delivery so that logistics teams can spot trends and bottlenecks.

## Business problem

DataCo needs one place to monitor and assess its global supply chain operations. The report should:

- Track key logistics and sales KPIs and how they change over time (MTD and MoM)
- Separate on-time deliveries from late deliveries and show the financial impact of each
- Show where demand, delays and profit sit across regions, shipping modes, customer segments, product categories and departments

The full brief is in [`docs/DATACO_SUPPLY_CHAIN_REPORT_PROBLEM_STATEMENT.docx`](docs/DATACO_SUPPLY_CHAIN_REPORT_PROBLEM_STATEMENT.docx).

## Dashboard overview

### Dashboard 1: Summary

**Headline KPIs** (each with MTD value and MoM change)

| KPI | Definition |
| --- | --- |
| Total Orders | Number of orders in the selected period |
| Total Sales Revenue | Revenue from product sales |
| Total Profit | Net profit (benefit per order) on fulfilled orders |
| Average Shipping Lead Time | Average real shipping days |
| On-Time Delivery Rate | % of orders delivered within the scheduled time |

**On-time vs late delivery KPIs**

- **On-time** = delivery status *Shipping on time* or *Advance shipping*. Tracked as on-time %, orders, sales revenue and total profit.
- **Late** = delivery status *Late delivery*. Tracked as late delivery % (late delivery risk), orders, sales revenue and total profit impact.

**Delivery status grid view**: a table by delivery status (Late delivery, Advance shipping, Shipping on time, Shipping canceled) showing total orders, sales revenue, profit, average shipping lead time and on-time delivery rate.

### Dashboard 2: Overview

| # | Visual | Metrics | Breakdown |
| --- | --- | --- | --- |
| 1 | Line chart | Total orders, sales revenue, profit | Month of order date |
| 2 | Filled map | Total orders, sales revenue, avg. shipping lead time | Market / order region |
| 3 | Donut chart | Total orders, late delivery % | Shipping mode |
| 4 | Bar chart | Total orders, sales revenue, profit | Customer segment |
| 5 | Bar chart | Total orders, sales revenue, late delivery % | Product category |
| 6 | Tree map | Total orders, sales revenue | Department |

### Dashboard 3: Details

A consolidated detail view of order fulfilment, shipping routes, customer profiles and overall logistics performance, for drilling into the data behind the summary and overview pages.

## Screenshots

<!-- Add your exported dashboard images to the images/ folder and update the file names below. -->

| Summary | Overview | Details |
| --- | --- | --- |
| ![Summary](images/dashboard-1-summary.png) | ![Overview](images/dashboard-2-overview.png) | ![Details](images/dashboard-3-details.png) |

## Repository structure

```
.
├── README.md
├── Dashboard_1.pbix          # Power BI report file
├── docs/
│   └── DATACO_SUPPLY_CHAIN_REPORT_PROBLEM_STATEMENT.docx
└── images/                   # Dashboard screenshots
```

## How to open the report

1. Install [Power BI Desktop](https://powerbi.microsoft.com/desktop/) (Windows).
2. Download or clone this repository.
3. Open `Dashboard_1.pbix` in Power BI Desktop.
4. If prompted, refresh the data or point the data source to your local copy of the dataset.

## Tools used

- Power BI Desktop
- DAX (measures for MTD, MoM, on-time and late delivery metrics)
- Power Query (data preparation)

## Dataset

DataCo supply chain dataset. Add the source link here, e.g. `[Dataset name](https://...)`.

## Author

**Saranga Abhishek**
