# Pharmaceutical-Sales-Performance-Dashboard
A comprehensive Data Analysis & Business Intelligence project created using Power BI. This project analyzes real-world Egyptian pharmaceutical sales and distribution data covering pharmacies, distribution companies, and medical product lines across Egyptian territories over a 3-month period (Q1: January, February, and March).

🎥 Project Demo (Video Presentation)

📌 Note: Click the image above to watch the full interactive dashboard demo on YouTube. Source data and Power BI .pbix files are kept confidential due to privacy and data protection guidelines.

📋 Table of Contents

Project Overview

Dataset Architecture

Data Transformation & DAX Modeling

Key Performance Indicators (KPIs)

Dashboard Architecture & Interactive Views

Advanced Power BI Features & UX Concepts

Business Insights Summary

🎯 Project Overview

The main objective of this project is to provide actionable commercial insights for pharmaceutical sales leadership and regional managers in Egypt. By monitoring revenue patterns, channel performance (Store, Retail, Tender), distributor volume shares, and individual product line dynamics, decision-makers can identify market opportunities and address sales bottlenecks.

Data Volume: 135,668 Rows

Geographic Coverage: Regions and Territories across Egypt (e.g., Cairo, Giza, Alex, Delta, Upper Egypt)

Time Horizon: Q1 Full Quarter (January, February, March)

Primary Tool: Power BI Desktop (Power Query, DAX Data Modeling, Data Visualization)

🗃️ Dataset Architecture

The underlying dataset captures granular B2B sales operations containing key dimensions and metrics:

Field Name

Description

Customer Code & Customer Name

Unique identifiers for pharmacies, hospitals, and clients

Distributor

Name of the pharmaceutical distribution entity (e.g., Stores, POS, Ibn Sina, EGY, Sofico)

Product Name & Product Key

Specific pharmaceutical product SKU and its database key

Line Name

Product classification/business line (e.g., Line 1, Line 2, CVM, Tender)

Sales Month

Transaction month (January, February, March)

Unit Price

Price per unit sold

Units Sold

Volume of products sold in a single transaction

Channel / Sales Type

Distribution pathway (Store, Retail, Tender)

Region & Territory

Egyptian geographical boundaries and local coverage units

Sales Value

Total monetary value generated per sales transaction

⚙️ Data Transformation & DAX Modeling

1. Data Cleaning (Power Query)

Raw Data Validation: Cleaned and structured 135k+ rows of real transaction logs.

Data Type Corrections: Set precise numerical formats for unit counts, financial transactions, and geographical texts.

Handling Missing/Null Values: Cleaned records to maintain accurate channel and regional aggregation.

2. Custom DAX Measures

Several custom Data Analysis Expressions (DAX) were crafted to measure business performance:

Total Sales Value:

Total Sales = SUM('SalesData'[Sales Value])


Total Units Sold:

Total Units Sold = SUM('SalesData'[Units Sold])


Total Customers Count:

Total Customers = DISTINCTCOUNT('SalesData'[Customer Code])


Total Products & Distributors:

Total Products = DISTINCTCOUNT('SalesData'[Product Key])
Total Distributors = DISTINCTCOUNT('SalesData'[Distributor])


Average Transaction Value (ATV):

Avg Transaction Value = DIVIDE([Total Sales], COUNT('SalesData'[Customer Code]), 0)


Average Sales Value per Product:

Avg Sales Per Product = DIVIDE([Total Sales], [Total Products], 0)


📊 Key Performance Indicators (KPIs)

The header metrics tracked across the executive views include:

💰 Total Sales: 108.91M EGP

📦 Total Units Sold: 3M Units

👥 Total Customers: 43K Accounts

💊 Total Active Products: 47 Items

🚚 Total Distributors: 15 Partners

💳 Avg Transaction Value: 802.78 EGP

🖼️ Dashboard Architecture & Interactive Views

The report is structured into dedicated analytical views connected by seamless custom navigation:

1. Home Page (Navigation Hub)

Serves as the main landing screen, providing clear visual pathways to Executive Summaries, Product Portfolio Analysis, and Regional Sales Trends.

2. Executive Performance Summary

High-level dashboard overview showing main KPIs, channel performance breakdown (Store vs. Retail vs. Tender), product line contribution, and monthly trend curves.

3. Product Portfolio & Pricing Analysis (Dynamic Bookmarks View)

Detailed product catalog performance allowing toggle navigation between Top 10 Products and Bottom 10 Products by revenue.

🔝 Top 10 Products View

⬇️ Bottom 10 Products View

4. Sales Trend & Regional Distribution Performance

Geographical analysis breaking down sales by Egyptian regions, territories, distributor contribution, and line-level pricing dynamics.

5. Detailed Breakdown Table (Drill-through & Pop-up View)

Granular data matrix providing line-by-line figures for product SKUs against specific Egyptian territories.

💡 Advanced Power BI Features & UX Concepts

To maintain a clean layout while processing large data points, modern Power BI visual techniques were incorporated:

Custom Bookmarks & Selection Panes: Enabled interactive toggling between views (e.g., Top 10 vs Bottom 10 products and detail modal overlays) without cluttering page space.

Report Page Tooltips: Implemented hover-over visual tooltips showing real-time distributor performance metrics when mouse-overing specific product rows.

Slicers & Cross-filtering: Dynamic slicing by Month (Jan, Feb, Mar), Channel Type (Retail, Store, Tender), and Territory (Cairo, Alex, Giza, etc.).

Custom Theme & Typography: Cohesive pharmaceutical color palette (medical green and deep charcoal) for maximum visual clarity and corporate presentation.

📈 Key Insights & Business Findings

Monthly Momentum: Peak revenue was observed in February (~44M EGP), followed by high stability across March and January.

Channel Dominance: Store and Retail channels drive over 68% of total unit volume distribution.

Top Regional Contributors: Cairo, Alexandria, and Giza territories lead in revenue contribution, while specific Delta territories show high growth potential in direct sales lines.

Line Concentration: Line 2 and Line 1 represent the majority of total revenues among the product lines portfolio.

👩‍💻 Developed By

Habiba Ahmed

Data Analyst | Power BI Specialist
