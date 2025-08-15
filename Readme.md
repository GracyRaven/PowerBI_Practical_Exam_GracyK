# Power BI Exam Project – AdventureWorksDW2020 Analysis

## Overview

This Power BI project is developed based on the AdventureWorksDW2020 dataset. The objective was to build a complete business intelligence solution by applying data transformation, modeling, visualization, DAX calculations, and row-level security (RLS). 

## Approach

All relevant tables from the dataset were imported, including **Customers**, **Date**, **Geography**, **Product**, **Reseller**, **Sales**, and **Sales Order**. Data types were verified and corrected where necessary. Missing values were handled appropriately, and redundant or unnecessary columns were removed to streamline the model.

A calculated column for **Profit** was created in the Sales table using product cost. Customer names were split into first and last names. A custom column was added to classify sales into **High**, **Medium**, or **Low** categories based on thresholds. Data was grouped by **Year** and **Month**, and duplicate records in the Products table were removed.

A star schema was constructed with the **Date** table as the central dimension. One-to-many relationships were established between **Sales** and **Product**, **Customer**, **Date**, and **Geography**. Appropriate hierarchies were created in both the Date and Product tables. Surrogate keys were hidden, and important measures such as **Sales Amount** and **Profit** were formatted for readability.

Multiple report pages were created to present key insights through interactive visuals. These included **bar charts**, **line charts with forecasting**, **KPI cards**, **maps**, **decomposition trees**, and a **custom bullet chart** sourced from the Power BI marketplace. Features such as slicers, bookmarks, drill-through, and tooltips were added to enhance user experience. A dedicated **dashboard** was created in Power BI Service and optimized for mobile devices.

Advanced DAX measures were implemented to support business analysis, including **Year-over-Year (YoY) Growth**, **Running Total Sales**, and a dynamic **Top 5 Products** measure using `RANKX`. Row-Level Security (RLS) was configured with two roles: one for **US Managers** (filtered to the United States) and another for **Europe Managers** (filtered to European countries). Roles were tested in Power BI Service using the “View as Role” feature.

## Challenges and Solutions

Some records in the Sales table contained **zero or missing values**, which affected trend lines and forecasting visuals. These were addressed by removing null values, allowing Power BI to treat them as missing data for better forecasting results.

Building **bookmarks for different report views** was time-consuming and required attention to detail. It was easy to forget to update bookmarks after changing slicer selections or visual states, which led to confusing or broken navigation. This was resolved by developing a consistent workflow for creating and testing bookmarks.


## Repository Contents

- `August Semester Exam.pbix` – The complete Power BI report  
- `PowerBI_Report.pdf` – Exported PDF of the full report (all pages)  
- `README.md` – This documentation file  
- `/Screenshots/` – Folder with screenshots (Power Query, model view, visuals, RLS)  


![Screenshot 114](./Screenshots/Screenshot%20114.png)
![Screenshot 115](./Screenshots/Screenshot%20115.png)
![Screenshot 116](./Screenshots/Screenshot%20116.png)
![Screenshot 117](./Screenshots/Screenshot%20117.png)
![Screenshot 118](./Screenshots/Screenshot%20118.png)
![Screenshot 119](./Screenshots/Screenshot%20119.png)
![Screenshot 121](./Screenshots/Screenshot%20121.png)
![Screenshot 123](./Screenshots/Screenshot%20123.png)
![Screenshot 124](./Screenshots/Screenshot%20124.png)
![Screenshot 108](./Screenshots/Screenshot%20108.png)
![Screenshot 95](./Screenshots/Screenshot%2095.png)
![Screenshot 96](./Screenshots/Screenshot%2096.png)
![Screenshot 97](./Screenshots/Screenshot%2097.png)
![Screenshot 98](./Screenshots/Screenshot%2098.png)
![Screenshot 100](./Screenshots/Screenshot%20100.png)
![Screenshot 101](./Screenshots/Screenshot%20101.png)
![Screenshot 102](./Screenshots/Screenshot%20102.png)
![Screenshot 103](./Screenshots/Screenshot%20103.png)
![Screenshot 104](./Screenshots/Screenshot%20104.png)
![Screenshot 105](./Screenshots/Screenshot%20105.png)
![Screenshot 106](./Screenshots/Screenshot%20106.png)
![Screenshot 92](./Screenshots/Screenshot%2092.png)
![Screenshot 94](./Screenshots/Screenshot%2094.png)


## Key Insights from the Power BI Report

### Sales Performance Over Time
A consistent upward trend in total sales was observed from 2018 to early 2020, before a noticeable drop in certain months, likely due to incomplete or missing data in 2020–2021. Forecasting tools projected moderate recovery in the following months.

### Top Performing Products
The bar chart highlighted a small group of products accounting for the majority of total sales. These top 10 products were responsible for a significant portion of overall revenue, suggesting a high concentration of sales in a limited product range.

### Profitability Trends
Products with higher sales volumes didn’t always yield the highest profit margins. The scatter plot helped identify which products had both high quantity sold and strong profit margins — essential for strategic focus.

### Customer Distribution
Sales were more concentrated in specific geographic regions, particularly in the United States and key European cities. The map visualization with drill-down capability helped identify top-performing regions and cities.

### Sales Categories Analysis
Based on Sales Category segmentation (High / Medium / Low), a large portion of transactions fell under the “Medium” range, but most revenue came from “High” sales. This insight supports focusing marketing efforts on high-value transactions.

### KPI and Growth Tracking
KPI cards and gauge visuals made it clear how actual performance compared to targets, such as the 10% year-over-year growth goal and the 30% profit margin benchmark. Some months exceeded targets, while others lagged behind.

### Customer-Level Insights
The decomposition tree and customer table showed that a small percentage of customers contributed to the majority of revenue. This supports applying customer segmentation and loyalty strategies.
