# Nigerian Car Sales Analysis Dashboard (H1 2026)

[![Excel](https://img.shields.io/badge/Microsoft_Excel-217346?style=for-the-badge&logo=microsoft-excel&logoColor=white)](https://www.microsoft.com/)
[![MySQL](https://img.shields.io/badge/MySQL-005C84?style=for-the-badge&logo=mysql&logoColor=white)](https://www.mysql.com/)
[![Power Query](https://img.shields.io/badge/Power_Query-217346?style=for-the-badge&logo=microsoft-excel&logoColor=white)](https://www.microsoft.com/)

> **19,943 vehicles sold. 5 brands. 10 Nigerian states. 1 messy dataset.**  
> Here's how I cleaned it, and turned it into a 5-page Excel dashboard that reveals Toyota's 63% market dominance, Lanre Shittu's revenue leadership, and the underutilization of discounts across the Nigerian automotive market.

> **Note:** Data was synthetically generated to mirror real car sales records, including realistic data quality issues.

## 📌 Project Overview

This project simulates the complete workflow of an automotive market analyst. Raw, messy car sales exports land on the desk every month; the goal is to clean them, and deliver a decision-ready, automated dashboard that the sales leadership can act on—without starting from scratch each month.

**Time Period:** January – June 2026  
**Final Clean Dataset:** 19,943 transactions  
**Total Market Value:** ₦642.05 Billion  
**Total Profit:** ₦102.68 Billion

## 🎯 Business Objectives

- Analyze dealer performance, brand profitability, and regional sales trends across six months.
- Identify which brands, dealers, and regions are driving the most revenue and profit.

## 🛠️ Tools & Skills Demonstrated

| Stage | Tool | Key Skills |
| :--- | :--- | :--- |
| **Data Cleaning** | Microsoft Excel | Remove Duplicates, TRIM/PROPER, Text-to-Columns, Conditional Formatting, Median/Mode Imputation, KPI Formulas |
| **Visualization & Automation** | Excel Dashboard | Power Query Refresh from SQL Views, Multi-page Report Design, PivotTables, Slicers, Brand-Specific Dashboards |

## 🧩 Pipeline Architecture

```mermaid
graph LR
    A[Raw Excel Export<br>10,000+ rows, 16 cols] --> B(Excel: Cleaning & Validation);
    B --> C[Cleaned CSV<br>19,943 rows, 0 nulls];
    C --> D[Analysis-Ready Views<br>Monthly, Dealer, Brand, Region];
    D --> E(Excel Dashboard)
    E --> F[Automated 5-Page Report];

==========================================================================
PHASE 1: EXCEL DATA CLEANING
------------------------------
Addressed realistic data entry errors to build a trustworthy foundation:

  · Deduplication
      Removed 57 exact duplicate rows.

  · Text Standardization
      Applied TRIM / PROPER to all categorical columns.

  · Currency Stripping
      Stripped "₦", "$", and commas from 4,200+ price values.

  · Invalid Value Correction
      Corrected 180 out-of-range values.
      Imputed 210 missing values using stratified median/mode imputation.

PHASE 2: EXCEL DASHBOARD AUTOMATION
-------------------------------------
Connected Excel to MySQL views via Power Query with a scheduled refresh.
The dashboard is built across five interactive pages:

  · Main Dashboard
      KPI cards, sales by brand, quantity by dealer,
      total sales by state, transmission breakdown,
      and payment method distribution.

  · Toyota Dashboard
      Toyota-specific KPIs, model breakdown, regional sales,
      and dealer performance.

  · Honda Dashboard
      Honda-specific KPIs, model breakdown, regional sales,
      and dealer performance.

  · Hyundai Dashboard
      Hyundai-specific KPIs, model breakdown, regional sales,
      and dealer performance.

  · Lexus Dashboard
      Lexus-specific KPIs, model breakdown, regional sales,
      and dealer performance.
============================================================================

===========================================================================
KEY FINDINGS & INSIGHTS
===========================================================================

  · Total Market Value
      ₦642.05 billion across 19,943 vehicles sold in H1 2026.

  · Total Profit
      ₦102.68 billion (16.0% average profit margin).

  · Toyota Dominates
      63.1% of all units sold (12,584 vehicles) and 63.3% of total sales
      revenue (₦406.35 billion).

  · Lexus Leads in Profitability
      Highest average transaction value and premium positioning.

  · Top Performing Dealer
      Lanre Shittu — ₦131.78 billion in total sales.

  · Largest Market by Volume
      Oyo State — 2,055 vehicles sold.

  · Transmission Preference
      Auto transmission leads with 10,172 units (51%)
      vs Manual with 9,771 units (49%).

  · Payment Method Distribution
      Near-even split: Cash (3,345), Transfer (3,338), Loan (3,317).

  · Discounts Underutilized
      ₦28.97 billion in discounts = <4.5% of total sales,
      suggesting either a high-demand market or untapped promotional
      opportunities.

  · Best-Selling Models
      Hilux leads with 2,520 units, followed by Corolla (2,469),
      Camry (2,446), Highlander (2,537), and RAV4 (2,612).
===========================================================================
