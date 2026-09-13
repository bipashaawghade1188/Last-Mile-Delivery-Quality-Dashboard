# Last-Mile-Delivery-Quality-Dashboard
An Excel-based analytics dashboard that evaluates last-mile delivery performance across regions and couriers — built to practice the exact skills used in catalogue and delivery-quality analytics roles (data cleaning, lookup formulas, conditional aggregation, and PivotTable/PivotChart reporting).
# Last-Mile Delivery Quality Dashboard

An Excel-based analytics dashboard that evaluates last-mile delivery performance across regions and couriers — built to practice the exact skills used in catalogue and delivery-quality analytics roles (data cleaning, lookup formulas, conditional aggregation, and PivotTable/PivotChart reporting).

# Project Overview

This project analyzes 150 mock delivery orders to answer a simple business question:
**Which regions and couriers are causing the most delivery delays, and how severe are those delays?**

## Dataset

Each order record includes:
- Order ID, ASIN
- Region (North, South, East, West)
- Courier (Courier A, B, C)
- Order Date, Promised Delivery Date, Actual Delivery Date
- Delay Reason (Weather, Address Issue, Courier Delay, Warehouse Delay, None)

Two calculated fields were added:
- **Delay (Days)** = Actual Delivery Date − Promised Delivery Date
- **Delivery Status** = "Delayed" if Delay > 0, else "On Time"

## Techniques Used

| Skill | Applied As |
|---|---|
| `COUNTIFS` | Count of On-Time / Delayed orders by Region and Courier |
| `AVERAGEIFS` | Average delay (days) for delayed orders only, by Region and Courier |
| `IF` + `IFERROR` | Delivery status classification and safe division |
| Conditional logic | "Repeat Offender" flag for Region/Courier with >30% delay rate |
| PivotTable | Cross-tab summary of orders by Region and Courier |
| PivotChart | Visual comparison of average delay and delayed-order counts |
| Conditional Formatting | Highlighting delayed orders and flagged regions/couriers |

## Key Insights

- **North** region has the highest number of delayed orders (17) and an above-average delay time (3.59 days).
- **South** region has fewer delayed orders (9), but when delays happen, they tend to be longer (4.22 days average).
- **East** region performs best overall — lowest delayed-order count (6) and moderate average delay.
- **Courier B** shows a higher delay rate across multiple regions, flagged as a repeat offender.

## Charts

**Average Delay (Days) by Region and Courier**
<img width="1545" height="681" alt="image" src="https://github.com/user-attachments/assets/49902d98-6dd5-4d75-b011-c59dcad4f46e" />


**Count of Delayed Orders by Region and Courier**
<img width="1632" height="657" alt="image" src="https://github.com/user-attachments/assets/8c949dc3-3634-4945-a058-bd8bba266a5f" />



## File

- `Last_Mile_Delivery_Quality_Dashboard.xlsx` — full workbook with raw data, summary formulas, PivotTables, and PivotCharts

## What This Demonstrates

- Structuring raw operational data into an analysis-ready format
- Formula fluency: `COUNTIFS`, `AVERAGEIFS`, `IF`, `IFERROR`
- Root-cause style thinking (not just delay %, but *where* and *why*)
- Communicating findings visually through PivotTables and PivotCharts

---

*Built as a practice project for Excel-based analytics and quality roles.*
