# **Business Insights 360**
**Uncovering Key Metrics Across Finance, Sales, Marketing, and Supply Chain**

---

## **Project Overview**

**Company**: AtliQ Hardware - A fast-growing electronics manufacturing company.  
**Products**: PCs, Mouse, Keyboards, Printers, and other electronic accessories.  
**Problem**: AtliQ experienced significant losses in Latin America (LATAM) due to decisions based on intuition and limited surveys.  
**Solution**: AtliQ decided to onboard a Data Analytics team for data-driven decision-making to ensure transparency and avoid future losses.  
**Competitor**: Dell, with a large data analytics team, bases its decisions entirely on data insights.  
**Objective**: Develop a 360-degree view dashboard to provide key insights across Finance, Sales, Marketing, and Supply Chain.

**Interact with the [Live Dashboard](https://app.powerbi.com/view?r=eyJrIjoiNjk1ZjNmMmMtNWIyYy00ODExLTlhZTAtY2JhNGNlNGVlOTUzIiwidCI6ImM2ZTU0OWIzLTVmNDUtNDAzMi1hYWU5LWQ0MjQ0ZGM1YjJjNCJ9)**

---

## **Project Summary**

Transformed decision-making at AtliQ Hardware by developing a dynamic Power BI dashboard that enhanced data visibility and provided strategic insights across finance, sales, marketing, and supply chain functions. The dashboard empowered teams to make data-driven decisions, optimize operations, and improve business performance.

1. ***Finance View:*** Delivered in-depth financial analytics covering revenue trends, expenses, and profit margins, improving financial planning.
2. ***Sales View:*** Analyzed product performance and customer behavior, refining sales strategies and optimizing efforts.
3. ***Marketing View:*** Measured campaign effectiveness and ROI, enhancing customer engagement.
4. ***Supply Chain View:*** Improved inventory management and demand forecasting for operational efficiency.
5. ***Executive View:*** Provided real-time insights for senior management to support strategic decisions.

This comprehensive integration of data empowered AtliQ Hardware to enhance operational efficiency and drive strategic growth.

## **Business Terms Used**

1. **Gross Sales (GS)**  
2. **Pre-Invoice Deduction**  
3. **Net Invoice Sales (NI)**  
4. **Post-Invoice Deduction**  
5. **Net Sales (NS)**  
6. **Manufacturing Cost**  
7. **Freight Cost**  
8. **Other Cost**  
9. **Cost of Goods Sold (COGS)**  
10. **Gross Margin (GM)**  
11. **Operational Expenses**  
12. **Net Profit (NP)**  
13. **Net Error**  
14. **ABS Error**  
15. **Forecast Accuracy (FA)**  
16. **Risk**  
17. **Fiscal Year**  
18. **YTD (Year to Date)**  
19. **YTG (Year to Go)**  
20. **Target**

---

## **AtliQ Business Structure**

- **Platforms**: Brick & Mortar and E-Commerce (Collectively known as Retailers).  
- **Channels**: Retailers, Direct, Distributor.  
- **Customers**: Chroma, Vijay Sales, Flipkart, Amazon, and more.  
- **Sales Flow**: AtliQ sells to customers, who in turn sell to consumers (individuals).

---

## **Tools Used**

1. **Power BI Desktop**  
2. **MySQL**  
3. **Microsoft Excel**

---

## **Key Learnings in Power BI**

- Important questions to ask before starting the project.
- Importing data from MySQL into Power Query.
- Importing CSV/Excel files into Power Query.
- Data cleaning and transformation in Power Query.
- Data modeling using Star and Snowflake schemas.
- Understanding Fact Tables and Dimension Tables.
- Creating measures and calculated columns using DAX.
- Dynamic titles based on the applied filters.
- Designing and customizing Power BI visuals.
- Using advanced features like Bookmarks, Field Parameters, Buttons, and Shapes.
- Report optimization using DAX Studio.
- Understanding business KPIs such as Net Sales, Gross Margin, Profit/Loss, Forecast Accuracy.
- Report design and aesthetics.
- Publishing reports to Power BI Service.

---

# Data Set Understanding

<details>
<summary>Click to expand</summary>

## Dimension Tables

### `dim_customer`
- **Distinct Markets**: 27 (e.g., India, USA, Spain)
- **Distinct Customers**: 75 across markets
- **Platform Types**:
  - **Brick & Mortar**: Physical/offline stores
  - **E-commerce**: Online stores (e.g., Amazon, Flipkart)
- **Channels**:
  - Retailer
  - Direct
  - Distributors

### `dim_market`
- **Distinct Markets**: 27 (e.g., India, USA, Spain)
- **Sub-Zones**: 7
- **Regions**: 4
  - APAC
  - EU
  - NAN
  - LATAM

### `dim_product`
- **Divisions**:
  - P & A
  - Peripherals
  - Accessories
  - PC
  - Notebook
  - Desktop
  - N & S
  - Networking
  - Storage
- **Categories**: 14 (e.g., Internal HDD, Keyboard)
- **Variants**: Multiple variants available per product

## Fact Tables

### `fact_forecast_monthly`
- **Purpose**: Forecast customer needs in advance to:
  - Increase customer satisfaction
  - Reduce warehouse storage costs
- **Structure**: Denormalized for data warehousing and analytical purposes
- **Date Handling**: All dates of the month are replaced by the start date of the month
- **Columns**:
  - All relevant dimension keys and attributes
  - `forecast_quantity`: Forecasted quantity needed by the customer

### `fact_sales_monthly`
- **Purpose**: Track actual sales data
- **Structure**: Similar to `fact_forecast_monthly`
- **Columns**:
  - All relevant dimension keys and attributes
  - `sold_quantity`: Actual quantity sold

### `freight_cost`
- **Details**: 
  - Travel costs and other expenses for each market
  - Associated with fiscal years

### `gross_price`
- **Details**: 
  - Gross prices linked to product codes

### `manufacturing_cost`
- **Details**: 
  - Manufacturing costs linked to product codes and years

### `pre_invoice_deductions`
- **Details**: 
  - Pre-invoice deduction percentages for each customer
  - Associated with years

### `post_invoice_deductions`
- **Details**: 
  - Post-invoice deductions and other related details

## Importing Data into Power BI

- **Database**: MySQL
- **Steps**:
  1. Open Power BI Desktop.
  2. Select **Get Data** > **MySQL Database**.
  3. Enter the MySQL server details and database name.
  4. Provide the necessary database access credentials.
  5. Select the required tables and load them into Power BI for analysis.

</details>

---

## **Data Model Overview**

The data model contains 9 fact tables, 7 dimension tables, and 7 additional tables using DAX & Power Query.

**Data Model Structure:**
<p align="center">
  <img src="https://github.com/GOKUL-R18/Business-Insights-360/blob/main/Resource/Data_model.png" alt="Data Model" width="600">
</p>

---

## **Project Dashboard Views**

### **Overall Report**

<p align="center">
  <img src="https://github.com/GOKUL-R18/Business-Insights-360/blob/main/Resource/overall_report_BI_360.gif" alt="Overall Report" width="600">
</p>

### **Home Page**

<p align="center">
  <img src="https://github.com/GOKUL-R18/Business-Insights-360/blob/main/Resource/home%20page.png" alt="Home Page" width="600">
</p>

### **Finance View**

<p align="center">
  <img src="https://github.com/GOKUL-R18/Business-Insights-360/blob/main/Resource/finance%20view.png" alt="Finance View" width="600">
</p>

### **Sales View**

<p align="center">
  <img src="https://github.com/GOKUL-R18/Business-Insights-360/blob/main/Resource/sales%20view.png" alt="Sales View" width="600">
</p>

### **Marketing View**

<p align="center">
  <img src="https://github.com/GOKUL-R18/Business-Insights-360/blob/main/Resource/marketing%20view.png" alt="Marketing View" width="600">
</p>

### **Supply Chain View**

<p align="center">
  <img src="https://github.com/GOKUL-R18/Business-Insights-360/blob/main/Resource/supply%20chain%20view.png" alt="Supply Chain View" width="600">
</p>

### **Executive View**

<p align="center">
  <img src="https://github.com/GOKUL-R18/Business-Insights-360/blob/main/Resource/executive%20view.png" alt="Executive View" width="600">
</p>

---

## **Project Outcome**

The **Business Insights 360** dashboard provides a comprehensive view of AtliQ Hardware's key metrics across the Finance, Sales, Marketing, and Supply Chain departments. By leveraging data-driven insights, the project helps AtliQ Hardware:

- Identify areas for improvement.
- Optimize decision-making processes.
- Prevent future financial losses.
- Compete more effectively with industry leaders, such as Dell.

---
