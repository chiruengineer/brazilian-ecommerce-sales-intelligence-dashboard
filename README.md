# Brazilian E-Commerce Sales Analysis Dashboard

## 📊 Project Overview

This project analyzes Brazilian e-commerce sales data to understand sales performance, customer behavior, product performance, payment methods, and delivery performance.

The project combines **Python/Jupyter Notebook**, **Power BI**, and **GitHub** to demonstrate an end-to-end data analytics workflow, from data cleaning and analysis to dashboard creation and documentation.

## 🎯 Project Objectives

The main objectives of this project are to:

* Analyze overall e-commerce sales performance
* Track revenue and order trends over time
* Understand customer distribution across Brazilian states
* Identify product categories contributing to revenue
* Analyze payment methods used by customers
* Examine order status and delivery performance
* Build an interactive Power BI dashboard for business insights

## 🛠️ Tools & Technologies

* **Python** – Data cleaning and preparation
* **Pandas** – Data manipulation and analysis
* **Jupyter Notebook** – Exploratory data analysis
* **Power BI** – Interactive dashboard and visualization
* **DAX** – Measures and calculations in Power BI
* **Git & GitHub** – Version control and project sharing

## 📁 Project Structure

```text
ecommerce-sales-powerbi/
│
├── data/
│   ├── raw/
│   │   └── ecommerce_sales.csv
│   └── cleaned/
│       └── Sales.csv
│
├── notebooks/
│   └── ecommerce_sales_analysis.ipynb
│
├── powerbi/
│   └── ecommerce_sales_dashboard.pbix
│
├── screenshots/
│   ├── executive_dashboard.png
│   ├── sales_analysis.png
│   └── delivery_analysis.png
│
└── README.md
```

## 📌 Dataset

The dataset contains Brazilian e-commerce order information, including:

* Orders
* Customers
* Products
* Product categories
* Sellers
* Payment methods
* Prices
* Freight values
* Order status
* Purchase dates
* Delivery dates
* Estimated delivery dates
* Customer locations

The dataset contains approximately **113,000 records** and covers orders from **2016 to 2018**.

## 🧹 Data Preparation

The data was cleaned and prepared using Python and Pandas.

The main preparation steps included:

* Removing unnecessary columns
* Converting date columns into appropriate datetime formats
* Handling date-based calculations
* Creating revenue-related fields
* Creating year, month, quarter, and year-month fields
* Calculating delivery duration
* Calculating delivery variance compared with estimated delivery
* Preparing the cleaned dataset for Power BI

### Important calculated fields

Some of the additional fields created during preparation include:

* `revenue`
* `order_year`
* `order_month`
* `order_month_name`
* `order_quarter`
* `year_month`
* `delivery_days`
* `delivery_delay_days`

## 📈 Power BI Dashboard

The Power BI report contains three main pages.

### 1. Executive Overview

This page provides a high-level view of the business.

Key metrics include:

* Total Revenue
* Total Orders
* Total Customers
* Total Products
* Average Order Value
* Total Freight

Visualizations include:

* Monthly Revenue Trend
* Revenue by Product Category
* KPI cards
* Interactive filters

### 2. Sales & Product Analysis

This page focuses on sales, products, customers, and payment behavior.

Visualizations include:

* Revenue by Customer State
* Orders by Payment Type
* Revenue by Product Category
* Orders by Order Status
* Interactive filters

### 3. Delivery & Customer Analysis

This page focuses on order fulfillment and delivery performance.

Key metrics include:

* Average Delivery Days
* Average Delivery Variance
* Orders Delivered

Visualizations include:

* Orders by Order Status
* Delivery performance metrics
* Customer and order analysis

## 🔢 Key Power BI Measures

Some of the main DAX measures created for the dashboard are:

```DAX
Total Revenue =
SUM(Sales[revenue])
```

```DAX
Total Orders =
DISTINCTCOUNT(Sales[order_id])
```

```DAX
Total Customers =
DISTINCTCOUNT(Sales[customer_unique_id])
```

```DAX
Total Products =
DISTINCTCOUNT(Sales[product_id])
```

```DAX
Average Order Value =
DIVIDE(
    [Total Revenue],
    [Total Orders],
    0
)
```

```DAX
Total Freight =
SUM(Sales[freight_value])
```

Additional delivery measures were created to analyze average delivery time and delivery performance.

## 💡 Key Findings

The analysis provides several useful observations about the e-commerce business:

* The dataset contains approximately **95K unique orders** and **92K unique customers**.
* Total revenue in the cleaned dataset is approximately **19.5 million**.
* The average order value is approximately **205**.
* Most orders in the dataset were successfully delivered.
* Revenue and order activity can be analyzed across different Brazilian states and product categories.
* Payment method analysis shows how customers completed their purchases.
* Delivery analysis allows comparison between actual delivery time and estimated delivery dates.

These findings can help understand sales performance, customer behavior, and operational efficiency.

## 📸 Dashboard Screenshots

### Executive Overview

![Executive Overview](screenshots/executive_dashboard.png)

### Sales & Product Analysis

![Sales & Product Analysis](screenshots/sales_analysis.png)

### Delivery & Customer Analysis

![Delivery & Customer Analysis](screenshots/delivery_analysis.png)

## 🚀 Project Workflow

The project followed this workflow:

```text
Raw Dataset
     ↓
Python / Pandas
     ↓
Data Cleaning & Transformation
     ↓
Exploratory Analysis
     ↓
Cleaned CSV
     ↓
Power BI
     ↓
DAX Measures
     ↓
Interactive Dashboard
     ↓
GitHub Portfolio Project
```

## 📚 What I Learned

Through this project, I practiced:

* Data cleaning with Pandas
* Working with dates and time-based data
* Exploratory data analysis
* Creating calculated columns
* Creating DAX measures
* Designing interactive Power BI dashboards
* Using slicers and KPI cards
* Creating business-focused visualizations
* Organizing a data analytics project
* Using Git and GitHub for version control

## 🔮 Future Improvements

Possible future improvements include:

* Adding customer segmentation
* Creating a more detailed seller performance analysis
* Adding customer retention and repeat-purchase analysis
* Adding advanced time-series analysis
* Improving dashboard design and navigation
* Adding automated data refresh
* Creating additional business KPIs

## 👤 Author

**Sayash**

This project was created as part of my data analytics portfolio to demonstrate practical skills in **Python, Pandas, Power BI, DAX, and GitHub**.
