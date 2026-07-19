# Electronics Store Sales Analysis

An end-to-end sales analysis of a fictional electronics retailer built to identify which products, cities and times of day generate the highest-value orders using **Power Query** for data cleaning, **Excel** for pivot table analysis and **Tableau** for interactive visualization

---

**Live Dashboard:** []

**Excel Workbook:** [`Sales_Analysis.xlsx`](./Sales_Analysis.xlsx)

## Question:

> Which product, city, and hour-of-day combination generates the highest-value orders, and does that change by month that marketing spend can be targeted by _when_, _where_, and _what_ to promote?

## Dataset

- **Source**: [KeithGalli's Pandas Data Science Tasks](https://github.com/KeithGalli/Pandas-Data-Science-Tasks)
- **Period:** 12 months (2019)
- **Original Columns:** Order ID, Product, Quantity Ordered, Price Each, Order Date, Purchase Address

## Process

### 1. Data Cleaning (Power Query)

- Removing duplicates, null/blank rows
- Changing data types
- Splitting Order Date into Month (name and number) and Order Hour
- Calculating Sales column
- Splitting Purchase Address into Address 1, City and ZIP Code
- Creating Order Size and Group Hour column

#### Derived Columns (Power Query)

| Column                         | Derived From                   | How | Why |
| ------------------------------ | ------------------------------ | --- | --- |
| Order Hour                     | Order Date                     |     |     |
| City, Address line 1, ZIP Code | Purchase Order                 |     |     |
| Sales                          | Price Each \* Quantity Ordered |     |     |
| Month Name                     | Order Date                     |     |     |
| Month Number                   | Order Date                     |     |     |
| Order Size                     |                                |     |     |
| Group Hours                    | Order Hour                     |     |     |

### 2. Data Analysis (Excel Pivot Tables & Charts)

Six Pivot Tables and Two Charts were built.

- **Product Performance Table**
- **City Performance Table**
- **Hour Performance Table**
- **Hour Sales Performance Chart**
- **Monthly Trend Table**
- **Monthly Sales Performance Chart**
- **Peak Sales Hours**
- **City-Product-Time Breakdown**

### 3. Data Visualization (Tableau)

## Key Findings

- The Macbook Pro Laptop ($7.85M) and iPhone ($4.70M) are top two products by sales and both are purchased as Single Item orders. This means marketing for these products should focus on driving getting someone to buy at all and not on cross-sell or bundle offers.

- The San Francisco generates the most total sales ($8.06M) and the most orders (42,898) but the Sales per Order ($187.77) is actually lower than New York City ($191.51) and other cities. This means that San Francisco lead reflects market size not higher-spending customers.

- The Orders are lowest overnight and climb toward two distinct peaks which is late morning and evening. This suggests two separate shopping windows rather than one steady climb can be worth targeting with separate campaigns.

- December sales ($4.51M) are more than double January ($1.78M) and are the highest than any month and with October ($3.65M) as a secondary peak. This points to a clear holiday-driven seasonal pattern worth planning inventory and spending around.

- AA and AAA Batteries have among the highest unit-order counts in all Order Size categories but even in their best-case Bulk Order they generate only $1,728-$4,105 combined which a fraction of what a single high-ticket product category brings in. Bulk purchase promotions are not an effective lever for these products.

- Across the cities, Macbook Pro Laptop and iPhone generate their highest revenue in the Evening this confirm that the daily sales peak identified in Hour performance is being driven primarily by premium product purchases, not accessories.

## Recommendation

Based on the analysis, the business should:

1.
2.
3.
4.
5.

## Tools Used

- **Power Query** - Data Cleaning, Derived Columns
- **Excel** - Pivot Tables, Pivot Charts
- **Tableau Public** - Interactive Dashboard and Visualization

## Repository Structure

```
├── data/
│   └── Raw Sales Data
│   │   ├── Sales_January_2019.csv
│   │   ├── Sales_February_2019.csv
│   │   ├── Sales_March_2019.csv
│   │   ├── ...
│   │   └── Sales_December_2019.csv
│   └── Clean_Sales_Data.xlsx
├── Sales_Analysis.xlsx
├── images/
│   └── dashboard_preview.png
└── README.md
```

## About This Project
