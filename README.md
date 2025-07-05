# Dynamic Data‑Driven Insights for Blinkit 🛒

**Power BI dashboard showcasing quick‑commerce analytics for Blinkit.**

---

## 🚀 Project Overview
Interactive Power BI dashboard built to provide Blinkit’s stakeholders with real‑time insights into sales trends, outlet performance, product mix, and customer ratings.

---

## 📊 Features
- **Top‑level KPIs**: Total Sales, Avg. Sales, Total Items Sold, Avg. Rating  
- **Interactive visuals**: Time series, bar charts, donut charts, stacked column chart, line chart, pie charts, matrix cards,funnel map and slicers  
- **Dynamic metric selector** using DAX   
- **Category analysis**: By item type, fat content, outlet size, and city tier  
- **Time Intelligence**: YoY and MoM growth using `SAMEPERIODLASTYEAR`, `DATEADD`

---
## 🗂️ Data Model
- **Fact Table**: `SalesTransactions` with `SalesAmount`, `Quantity`, `Rating`  
- **Dimensions**: `Item`, `FatContent`, `Outlet`, `Date`  
- Star schema relationships enable efficient slicer filtering and drill‑down interactivity

---

## 🛠️ DAX & Measures

```DAX
Total Sales= SUM('BlinkIT Grocery Data'[Sales])
Avg Sales= AVERAGE('BlinkIT Grocery Data'[Sales])
No of Items= COUNTROWS('BlinkIT Grocery Data')
Avg Rating= AVERAGE('BlinkIT Grocery Data'[Rating])


metrics = {
    ("Total Sales", NAMEOF('BlinkIT Grocery Data'[Total Sales]), 0),
    ("Average Sales", NAMEOF('BlinkIT Grocery Data'[Average Sales]), 1),
    ("Avg Rating", NAMEOF('BlinkIT Grocery Data'[Avg Rating]), 2),
    ("No of Items", NAMEOF('BlinkIT Grocery Data'[No of Items]), 3)
}
```

## 🎨 **Dashboard Structure**

- **Landing Page**: Overview

- **Trend Analysis**: Total sales over Outlet Establishment

- **Category & Outlet Insights**: Performance by item type, fat content, outlet size, outlet type

- **Ratings & Customer Insights**: Avg. ratings across segments

------
## 📊**Charts Done**
- **Donut Chart**: Total sales by Fat Content
  
- **Bar Chart**: Total sales by item type

- **Stacked column chart**: Fat content by outlet for total sales

- **Line Chart**: Total sales by outlet establishment

- **Pie Chart**: Sales by outlet size

- **Funnel Chart**:Sales by outlet type

- **Matrix Card**: All metrics by outlet type

---
## 📌 How to Use
- Open the .pbix file in Power BI Desktop

- Refresh or connect to your dataset

- Toggle metrics via slicers (e.g., Total Sales / Avg Rating)

- Apply filters for outlet size, tier, fat content, or date range

- Download reports as needed (PDF/PowerPoint)

---
## 🧠 Business Value
- Product push: Identified high‑margin item segments (e.g., regular‑fat)

- Outlet strategy: Highlighted Tier 3 & medium outlets for expansion

- Category targeting: Identified top‑sellers for focused promotions

- Performance tracking: Monitor newer outlets with strong growth trajectories

---
## 🛠️ Technical Notes

- Entirely built in Power BI Desktop

- No external tools used—data modeling, transformations, and calculations are native to Power BI

- Designed with an efficient star schema to minimize DAX complexity and maximize performance

---
## 📞 Contact

- For questions, feedback, or collaboration, feel free to reach out:
  
Email: devikishore18@gmail.com

LinkedIn: https://www.linkedin.com/in/devikishore18/
