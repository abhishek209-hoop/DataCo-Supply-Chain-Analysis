# DataCo Supply Chain Analysis — Power BI

An interactive Power BI report for exploring sales performance, profitability, delivery operations, and customer segments using the cleaned DataCo Smart Supply Chain dataset.

## Report file

Open [`Report.pbix`](./Report.pbix) with **Microsoft Power BI Desktop** to interact with the report pages, slicers, and visuals.

## Report pages

### 1. Sales Report

Explore commercial performance across markets, countries, regions, product categories, and individual products.

- KPI cards for total sales, order-ID count, and order profit
- Sales by market and order country
- Geographic distribution of sales by order region
- Profit per order by product category
- Top and bottom five products by sales
- Slicers for order year and order country

### 2. Delivery Report

Compare delivery outcomes, shipping duration, order status, shipping mode, and payment type.

- Average delay KPI
- Sales by order status
- Delivery-status distribution using order-item records
- Actual versus scheduled shipping duration by delivery status
- Shipping duration by shipping mode
- Quantity mix by delivery status and shipping mode
- Payment-type distribution
- Slicers for order year and order country

### 3. Customer Segment Report

Compare customer segments and geographic markets, and identify products associated with sales and customer value.

- Sales by customer segment
- Sales by product
- Benefit per order by customer segment
- Customer distribution by country and order region
- KPI cards for customer count, category count, and order profit
- Slicers for order year and order country

## Questions this report helps answer

- Which markets, countries, regions, categories, and products contribute the most sales?
- How does profit per order vary across product categories?
- How do delivery outcomes differ by shipping mode and order status?
- How do actual and scheduled shipping durations compare across delivery statuses?
- How are sales and benefit per order distributed across Consumer, Corporate, and Home Office segments?
- Where are customers located across countries and order regions?

## Dataset and metric notes

The report uses the cleaned `DataCoSupplyChainDataset_cleaned` model. Key fields include `Order Item Total`, `Order Profit Per Order`, `Order Status`, `Delivery Status`, `Shipping Mode`, `Days for shipping (real)`, `Days for shipment (scheduled)`, `Customer Segment`, `Customer Country`, `Order Region`, and `Type`.

**Interpret row-level metrics carefully:** the dataset contains order-item records. Some visuals count non-null `Order Id` or `Order Item Id` values rather than distinct orders. Those counts therefore should not automatically be interpreted as unique-order counts. Similarly, totals and averages should be interpreted using the aggregation shown in the relevant visual.

## Tools

- Microsoft Power BI Desktop
- Power BI visualizations, report measures, and interactive slicers

## How to use

1. Download or clone this repository.
2. Open `Report.pbix` in Microsoft Power BI Desktop.
3. Use the order-year and order-country slicers where available to filter the visuals.
4. Select chart elements to cross-filter other visuals on the same report page.

## Source

The analysis is based on the DataCo Smart Supply Chain dataset. This repository contains the Power BI report file; any separate source-data distribution remains subject to the dataset provider's terms.

## Author
**Saranga Abhishek**
 