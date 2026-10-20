# BlinkIT Grocery Sales Dashboard | Power BI

## Overview

This project uses Microsoft Power BI to analyze grocery sales and outlet information. The report is designed to make it easier to explore sales performance, product categories, outlet characteristics, and ratings through visual analytics.
The dataset contains 8,523 records and 12 columns.

## Tools Used

- Microsoft Power BI
- Power Query
- DAX, where applicable
- Microsoft Excel

## Dashboard Objectives

- Summarize grocery sales performance.
- Compare sales across product categories.
- Explore differences between outlet types and location tiers.
- Analyze item fat content and product characteristics.
- Examine outlet size and establishment year.
- Present data through clear and interactive visualizations.

## Suggested KPIs

The following KPIs can be used if they are present and correctly calculated in the report.

### Total Sales

```dax
Total Sales =
SUM('BlinkIT Grocery Data'[Sales])
```

### Average Sales per Record

```dax
Average Sales =
AVERAGE('BlinkIT Grocery Data'[Sales])
```

### Number of Items

```dax
Number of Items =
DISTINCTCOUNT('BlinkIT Grocery Data'[Item Identifier])
```

### Number of Outlets

```dax
Number of Outlets =
DISTINCTCOUNT('BlinkIT Grocery Data'[Outlet Identifier])
```

### Average Rating

```dax
Average Rating =
AVERAGE('BlinkIT Grocery Data'[Rating])
```

Replace the table name in these examples if your Power BI model uses a different name.

## Suggested Visualizations

### 1. Sales by Item Type
Use a bar chart to compare sales across product categories.

### 2. Sales by Outlet Type
Compare sales across different outlet formats.

### 3. Sales by Location Tier
Explore sales distribution across outlet location tiers.

### 4. Sales by Fat Content
Compare sales for Low Fat and Regular products after standardizing inconsistent labels.

### 5. Sales by Outlet Size
Investigate sales across outlet size categories.

### 6. Sales by Establishment Year
Explore how sales vary by the year an outlet was established.

### 7. Product Characteristics
Use item weight, visibility, and ratings to explore product-level patterns where appropriate.

These are suggested analysis areas; retain only the visuals and KPIs actually implemented in the PBIX report.

## Data Preparation

Recommended Power Query steps:

1. Import the Excel workbook.
2. Check data types and column names.
3. Standardize `Item Fat Content` values.
4. Review missing values in `Item Weight`.
5. Validate sales and rating values.
6. Apply appropriate data types.
7. Load the cleaned data into Power BI.
8. Validate KPI calculations against the source dataset.

## Interactivity

Useful slicers include:
- Item Type
- Item Fat Content
- Outlet Type
- Outlet Location Type
- Outlet Size
- Outlet Establishment Year

Configure visual interactions so that the slicers filter the intended charts and KPI cards.

## Design Recommendations

- Keep KPI cards near the top of the dashboard.
- Use consistent colors and readable labels.
- Sort bar charts meaningfully.
- Avoid overcrowding the report with visuals.
- Use clear titles and units.
- Ensure slicers are easy to find and use.
- Use a consistent formatting style across report pages.

## Skills Demonstrated

- Data transformation
- Data modeling
- KPI development
- Data visualization
- Business intelligence
- Sales and outlet performance analysis


