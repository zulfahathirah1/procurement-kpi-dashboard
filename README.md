# Procurement KPI Analysis Dashboard (2022 – 2023)

## Overview

An interactive Excel dashboard built to consolidate procurement performance data from 2022 to 2023 across five suppliers and four item categories. The dashboard enables procurement and supply chain teams to monitor cost efficiency, supplier reliability, quality control, and operational lead times from a single view.

---

## Objective

To transform raw transactional purchase order data into a structured executive reporting tool that supports data-driven decisions in supplier management, cost optimisation, and procurement risk assessment.

---

## Dataset

| Property | Detail |
|---|---|
| Source | Kaggle: https://www.kaggle.com/datasets/shahriarkabir/procurement-kpi-analysis-dataset |
| Records | 777 purchase orders |
| Period | 2022 to 2023 |
| Suppliers | 5 (Alpha Inc, Beta Supplies, Delta Logistics, Epsilon Group, Gamma Co) |
| Item Categories | Electronics, MRO, Office Supplies, Packaging, Raw Materials |

**Key fields used:**

- PO ID, Supplier, Order Date, Delivery Date
- Item Category, Order Status, Quantity
- Unit Price, Negotiated Price
- Defective Units, Compliance Status

---

## Data Preparation

All data preparation was performed in Microsoft Excel and included the following steps:

- Data cleansing and deduplication
- Missing value identification and handling
- Data type standardisation (text-formatted dates converted to proper Date format)
- Date transformation to extract Month and Year for time-based analysis
- Creation of calculated fields:
  - **Cost Savings** = (Unit Price - Negotiated Price) x Quantity
  - **Lead Time** = Delivery Date - Order Date
  - **Defect Rate** = Defective Units / Quantity
- Data validation across all key fields

---

## KPI Cards

| KPI | Description |
|---|---|
| Total Spend | Sum of (Negotiated Price x Quantity) across all delivered orders |
| Total Savings | Aggregate cost savings achieved through price negotiation |
| Compliance Rate | Percentage of orders meeting internal procurement policy requirements |
| Average Lead Time | Mean number of days between order date and delivery date |
| Defect Rate | Overall ratio of defective units to total units ordered |

---

## Dashboard Components

### 1. Volume Order by Order Status (Stacked Bar Chart)
Shows order volume per supplier segmented by order status: Delivered, Partially Delivered, Pending, and Cancelled. Enables comparison of fulfilment reliability across suppliers.

### 2. Negotiation vs Original Price by Supplier (Clustered Column Chart)
Compares the sum of original unit prices against negotiated prices per supplier. Identifies which supplier relationships are generating the most value through negotiation.

### 3. Defect Rate by Item Category (Horizontal Bar Chart)
Ranks item categories by defect rate to highlight where quality issues are most concentrated and where corrective action should be prioritised.

### 4. Average Lead Time by Month (Line Chart)
Tracks monthly average lead time across 2022 and 2023 using two separate lines to show year-over-year comparison. Surfaces seasonal patterns or operational deterioration over time.

---

## Interactivity

The dashboard includes three slicers for dynamic filtering:

- Item Category
- Order Status
- Supplier

All charts and KPI cards update simultaneously when filters are applied.

---

## Tools and Techniques

- Microsoft Excel
- PivotTables and PivotCharts
- Advanced Formulas
- Data Validation
- Slicer-based Interactivity
- Procurement KPI Analysis
- Data Visualisation

---

## Known Limitations

- Dataset is sourced from Kaggle and uses anonymised data. Findings are illustrative and not representative of any real organisation.
- The dataset contains 777 records across only five suppliers, which limits the statistical depth of supplier-level analysis.
- A supplier risk score combining defect rate, compliance rate, and lead time into a single weighted ranking has been identified as a valuable addition and is planned for the next iteration.

---

## Folder Structure

```
procurement-kpi-dashboard/
│
├── README.md
├── data/
│   └── procurement_data.xlsx
└── dashboard/
    └── procurement_dashboard.xlsx
```
