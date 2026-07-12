# Excel / Power Query — Data Cleaning Approach

This folder contains the Excel-based implementation of Project 1: Data Cleaning & Preparation, from the DecodeLabs Industrial Training Kit.

## Contents

| File | Description |
|---|---|
| `Dataset_for_Data_Analytics.xlsx` | The cleaned dataset, produced using Microsoft Excel (Power Query & native formatting) |
| `Change_Log_Project1.pdf` | Full change log documenting each cleaning operation (CR001–CR005), the reasoning behind it, and its measurable impact |

## Approach

The raw dataset (1,200 records, 14 fields) was cleaned entirely within Excel, using Power Query for transformations and native formatting for display standards. Key operations included:

- Filling missing `CouponCode` values with an explicit `"No CouponCode"` label
- Auditing for duplicate `OrderID`s, `TrackingNumber`s, and full-row duplicates
- Standardizing `UnitPrice` and `TotalPrice` to consistent 2-decimal currency formatting
- Reformatting the `Date` column to ISO 8601 (`YYYY-MM-DD`)
- Adding a derived `Month Year` helper column for downstream grouping and pivoting

Full details, reasoning, and verification results for each step are documented in `Change_Log_Project1.pdf`.

## See also

A parallel implementation of this same cleaning task using Python/Pandas is available in [`../python/`](../python/), for comparison across tools.
