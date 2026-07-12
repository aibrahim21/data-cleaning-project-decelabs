# data-cleaning-project-decelabs
Data Cleaning &amp; Preparation Project - DecodeLabs Internship
# 🧹 Data Cleaning & Preparation Project

## DecodeLabs Internship - Project 1

![Data Cleaning](https://img.shields.io/badge/Status-Completed-brightgreen)
![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![Pandas](https://img.shields.io/badge/Pandas-2.0%2B-orange)

## 📋 Project Overview

This project demonstrates the complete data cleaning and preparation process for raw business data. Following the DecodeLabs internship guidelines, I transformed a messy dataset into a "Gold Standard" dataset ready for analysis.

> *"80% of data analytics is cleaning & wrangling. Master the 80% to earn the right to do the 20%."*

## 🎯 Objectives

- ✅ Identify and handle missing values (309 missing → 0)
- ✅ Remove duplicate records (11 duplicates removed)
- ✅ Standardize data formats (ISO 8601 dates, proper case, 2 decimal precision)
- ✅ Create reproducible workflow using Python Pandas
- ✅ Document all changes in a change log

## 📊 Dataset Information

| Feature | Details |
|---------|---------|
| **Original Rows** | 1,200 |
| **Cleaned Rows** | 1,189 |
| **Columns** | 14 |
| **Duplicate Removed** | 11 |
| **Missing Values Fixed** | 309 |

### Key Columns

- `OrderID`: Unique order identifier
- `CustomerID`: Customer identifier
- `Product`: Product name (7 unique products)
- `Date`: Order date (ISO 8601 format)
- `Quantity`: Items ordered
- `UnitPrice`: Price per unit
- `TotalPrice`: Total order value
- `OrderStatus`: Shipped, Delivered, Pending, etc.

## 🔧 Cleaning Process

### 1. Handle Missing Values
```python
# Filled missing CouponCode with 'No Coupon'
df_clean['CouponCode'] = df_clean['CouponCode'].fillna('No Coupon')
