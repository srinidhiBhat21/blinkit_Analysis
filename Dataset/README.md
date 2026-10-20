# BlinkIT Grocery Dataset Documentation

## Overview

This folder contains the Excel dataset used for the BlinkIT Grocery Sales Analysis Dashboard project.

The dataset contains product-level and outlet-level information for exploring sales performance, item categories, product characteristics, and outlet attributes.

## Dataset Profile

- **Total records:** 8,523
- **Total columns:** 12
- **File format:** Excel (`.xlsx`)
- **Missing values:** 1,463 in the `Item Weight` column

## Column Dictionary

| Column | Description |
|---|---|
| `Item Fat Content` | Fat-content category of the item |
| `Item Identifier` | Identifier assigned to the product |
| `Item Type` | Product category |
| `Outlet Establishment Year` | Year the outlet was established |
| `Outlet Identifier` | Unique outlet identifier |
| `Outlet Location Type` | Outlet location tier |
| `Outlet Size` | Outlet size category |
| `Outlet Type` | Type of grocery outlet |
| `Item Visibility` | Visibility value associated with the item |
| `Item Weight` | Weight of the item |
| `Sales` | Sales value recorded for the item |
| `Rating` | Rating associated with the item |

## Data Quality Observations

### 1. Missing Item Weights

The `Item Weight` column contains 1,463 missing values.

Recommended approach:
- Investigate the missing records.
- Decide whether to retain, exclude, or impute missing weights based on the analysis requirements.
- Avoid replacing missing weights with zero without justification.

### 2. Inconsistent Fat-Content Labels

The dataset contains different representations of similar categories:

- `Low Fat`
- `low fat`
- `LF`
- `Regular`
- `reg`

These labels should be standardized before category-level comparisons.

Example Power Query mappings:

| Original value | Standardized value |
|---|---|
| `low fat` | `Low Fat` |
| `LF` | `Low Fat` |
| `reg` | `Regular` |
| `Low Fat` | `Low Fat` |
| `Regular` | `Regular` |

### 3. Data Type Validation

Check that:
- Establishment year is numeric or a suitable year field.
- Item weight, sales, visibility, and rating are numeric.
- Item and outlet identifiers are treated as categorical identifiers rather than quantities.

## Potential Analysis

The dataset can support analysis of:

- Sales by item type
- Sales by fat content
- Sales by outlet type
- Sales by location tier
- Sales by outlet size
- Sales by establishment year
- Item visibility and weight
- Rating distributions

## Important Considerations

- The `Sales` field should not be interpreted as profit because the dataset does not provide the cost information required for profit calculations.
- Missing item weights may affect analyses involving weight.
- Standardize categorical labels before comparing group-level metrics.
- Validate any calculated KPIs against the original data.

