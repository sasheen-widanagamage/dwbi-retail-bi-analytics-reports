# 📊 Retail Business Intelligence Analytics and Reporting Project

This project was completed for the **IT3021 - Data Warehousing and Business Intelligence** module at **Sri Lanka Institute of Information Technology (SLIIT)**.

## 🚀 Project Overview

This project demonstrates the Business Intelligence and analytics stage of a retail data warehouse solution.

The project uses the **Retail_DW2** data warehouse created in Assignment 1 as the main data source. It extends the data warehouse solution by implementing an **SSAS cube**, **Excel OLAP analysis**, and **Power BI reports**.

The main focus of this project is to perform multidimensional analysis and create interactive business intelligence reports for retail sales data.

---

## 🛠️ Tools and Technologies

- Microsoft SQL Server
- SQL Server Management Studio
- SQL Server Analysis Services
- SQL Server Data Tools / Visual Studio
- Microsoft Excel
- Pivot Tables
- Microsoft Power BI Desktop
- Power BI Service
- OLAP
- Cube Design
- Star Schema
- Drill-down Reports
- Drill-through Reports
- Cascading Slicers

---

## 🗄️ Data Source

The main data source used for this project is **Retail_DW2**.

`Retail_DW2` is the retail data warehouse created in Assignment 1. It follows a **Star Schema** design and contains one central fact table connected to multiple dimension tables.

---

## 🏗️ Data Warehouse Tables

| Table Name | Type | Description |
|---|---|---|
| `DimDate` | Dimension Table | Stores date details such as year, quarter, month, and full date |
| `DimCustomer` | Dimension Table | Stores customer details and historical customer information |
| `DimProduct` | Dimension Table | Stores product category, brand, type, and product name |
| `DimOrderProfile` | Dimension Table | Stores feedback, shipping method, payment method, order status, and ratings |
| `FactRetailSales` | Fact Table | Stores retail sales transactions and numerical measures |

---

## 🧊 SSAS Cube Implementation

An SSAS cube was created using the `Retail_DW2` data warehouse.

### SSAS Project Details

| Item | Value |
|---|---|
| SSAS Project Name | `CubeProject_IT23641006` |
| Cube Name | `Retail_DW2_Cube` |
| Data Source Name | `DS_Retail_DW2` |
| Data Source View | `DSV_Retail_DW2` |
| SSAS Database | `Retail_DW2_SSAS_IT23641006` |

---

## 📏 Cube Measures

The following measures were selected from the `FactRetailSales` table:

- Quantity
- Unit Amount
- Sales Amount
- Transaction Process Time Hours
- Fact Retail Sales Count

These measures support sales analysis, quantity analysis, transaction counting, and operational process-time analysis.

---

## 🧭 Cube Hierarchies

Two main hierarchies were implemented in the SSAS cube.

### Date Hierarchy

**YearNo → QuarterNo → MonthName → FullDate**

### Product Hierarchy

**Product_Category → Product_Brand → ProductName**

These hierarchies support drill-down analysis in SSAS, Excel, and Power BI.

---

## 📈 Excel OLAP Analysis

Microsoft Excel was connected to the deployed SSAS cube using an Analysis Services connection.

Excel Pivot Tables were used to demonstrate OLAP operations.

### OLAP Operations Demonstrated

| OLAP Operation | Description |
|---|---|
| Roll-up | Summarizes sales data at a higher level, such as year |
| Drill-down | Expands data from year to quarter, month, and full date |
| Slice | Filters the cube using one dimension value |
| Dice | Filters the cube using multiple dimension values |
| Pivot | Rotates the analysis view by changing rows and columns |

---

## 📊 Power BI Reports

Power BI was used to create interactive reports using the `Retail_DW2` data warehouse.

The Power BI model uses the star schema relationship where dimension tables are connected to the `FactRetailSales` table.

---

## Report 1: Matrix Report

A matrix visual was created to display sales data using row and column groupings.

### Fields Used

- `Product_Category` as rows
- `YearNo` as columns
- `SalesAmount` as values
- `Quantity` as values

This report helps compare sales and quantity across product categories and years.

---

## Report 2: Cascading Slicer Report

This report was developed using cascading geographic slicers.

### Slicers Used

- Country
- State

When a country is selected, the state slicer is automatically filtered based on the selected country.

### Visuals Included

- Monthly sales column chart
- Payment method pie chart
- Product category quantity bar chart
- Total sales card

This report allows users to filter sales analysis by location while viewing sales trends, payment method contribution, product category quantity, and total sales value.

---

## Report 3: Drill-down Report

A drill-down report was created using the date hierarchy.

### Drill-down Path

**Year → Quarter → Month → Date**

Sales Amount was used as the main value.  
This report allows users to start from yearly sales and drill down into more detailed time levels.

---

## Report 4: Drill-through Report

A drill-through report page was created using `ProductName`.

When a user right-clicks a product from another report page and selects drill-through, Power BI opens a detailed page filtered for that selected product.

### Drill-through Page Includes

- Detailed table visual
- Sales summary card
- Monthly sales chart

This report helps analyze detailed sales information for a selected product.

---

## ☁️ Power BI Service Publishing

After creating and testing the reports in Power BI Desktop, the report was published to **Power BI Service**.

Publishing the report allows users to view and interact with the reports online.

---

## ⭐ Key Features

- SSAS cube implementation
- Data Source View using data warehouse tables
- Cube measures from `FactRetailSales`
- Date hierarchy
- Product hierarchy
- Excel PivotTable OLAP analysis
- Roll-up operation
- Drill-down operation
- Slice operation
- Dice operation
- Pivot operation
- Power BI matrix report
- Cascading slicer report
- Drill-down report
- Drill-through report
- Power BI Service publishing
