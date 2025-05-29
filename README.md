# 📊 AdvantureWorks Power BI Dashboard

This project showcases a sales analytics dashboard built in Power BI using data from AdventureWorks SQL Server sample database.

## 📁 Project Structure
- '/screenshots/' - ER diagram and charts
- 'adventureworks-sales-dashboard.pbix' - Power BI '.pbix' file with the full model and visuals
- 'README.md' - this file

## 🧩 ER Diagram
The data model is based on a subset of tables from the db, including tables Customers, SalesOrderHeader, SalesOrderDetail, SalesTerritory from the schema Sales. 
- Customer.CustomerID (1) -> SalesOrderHeader.CustomerID (∞). One to many: each customer can have multiple sales orders.
- SalesOrderHeader.SalesOrderID (1) -> SalesOrderDetail.SalesOrderID (∞). One to many: each order can have multiple line items.
- SalesTerritory.TerritoryID (1) -> SalesOrderHeader.TerritoryID (∞). One to many: each territory is associated with many orders.
- Customer (∞) -> Territory (∞). Many to many: each customer can have multiple territories, as well as each territory can have multiple customers. This connection is resolved through the SalesOrderHeader table. 
![ER Diagram](screenshots/er-diagram.jpg)

## 💼 The Executive Dashboard
This executive dashboard presents high-level KPIs and tracks overall sales performance over time.
### The KPIs include:
- **Total sales** - the total revenue generated from all orders
- **Sales Involving a Saleperson** - revenue from orders handled by assigned salesperson
- **% Sales with Assigned Saleperson** - the share of sales that involved a saleperson
The line chart below shows the overall trend in sales from 2001 to 2004.
![Executive Dashboard](screenshots/executive_dashboard.jpg)
### Key insights:
- Around **73%** of all sales revenue was generated through orders involving a saleperson, indicating a strong reliance on the sales team.
- Sales show a generally **stable trend with minor fluctuations**, with a slight increase in later periods.
- There may be opportunities to analyze the remaining 27% of sales that occur without saleperson  - e.g. self-service, online channels or store-driven purchases.

## 🚀 How to run

1. Open the 'adventureworks-sales-dashboard.pbix' file in Power BI Desctop
2. Connect to your AdventureWorks database

## Author
Anna Nesterova | [GitHub](https://github.com/annanesta)