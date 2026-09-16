# 🚚 Courier Delivery & Logistics Analytics (2024–2026)

### Python | Pandas | SQL | Power BI | Tableau | Looker Studio | Neo4j

An end-to-end courier and logistics analytics project designed to analyze shipment performance, delivery operations, customer segments, shipping modes, and logistics trends using data analytics and business intelligence tools.

---

## 📌 Project Overview

This project focuses on analyzing courier shipment data from 2024 to 2026 to understand delivery operations and identify meaningful business insights.

The project demonstrates the complete analytics workflow:

**Raw Data → Data Cleaning → Data Modeling → SQL Analysis → BI Dashboards → Graph Analytics**

The dataset is synthetically generated for educational and portfolio purposes.

---

## 🎯 Business Objectives

* Analyze total shipment volume and shipment trends.
* Understand delivery status and delivery performance.
* Compare Standard, Express, and Same Day shipping modes.
* Analyze shipment activity across origin and destination zones.
* Understand customer segments and package types.
* Analyze shipping cost patterns.
* Explore customer-to-shipment and shipment-to-zone relationships using Neo4j.

---

## 📂 Dataset Information

| Attribute   | Details                       |
| ----------- | ----------------------------- |
| Domain      | Courier & Logistics           |
| Data Period | 2024–2026                     |
| Raw Records | 2,000                         |
| Raw Columns | 10                            |
| Data Format | CSV                           |
| Data Type   | Synthetic Dataset             |
| Source      | Self-generated                |
| Purpose     | Analytics & Portfolio Project |

### Raw Dataset

The raw dataset was created using Python and uploaded to Kaggle.

**Kaggle Dataset:** [Add your Kaggle dataset link here]

### Raw Dataset Columns

| Column           | Description                              |
| ---------------- | ---------------------------------------- |
| Shipment_ID      | Unique shipment identifier               |
| Order_Date       | Date when the shipment was booked        |
| Delivery_Date    | Shipment delivery date                   |
| Customer_Type    | Individual or Business                   |
| Origin_Zone      | Shipment origin zone                     |
| Destination_Zone | Shipment destination zone                |
| Package_Type     | Type of package                          |
| Shipping_Mode    | Standard, Express, or Same Day           |
| Shipping_Cost    | Shipping charge                          |
| Delivery_Status  | Delivered, Delayed, Cancelled, or Failed |

---

## 🧹 Data Cleaning & Transformation

Data cleaning and transformation were performed using Python and Pandas.

### Key Activities

* Loaded the raw CSV dataset.
* Checked dataset dimensions and data types.
* Checked missing values.
* Checked duplicate shipment IDs.
* Converted date columns to datetime format.
* Cleaned text values.
* Validated shipping costs.
* Created a customer identifier for graph modeling.
* Created analytical date columns.
* Calculated delivery days.
* Created delivery performance classification.
* Exported a separate cleaned dataset.

### Analytical Columns

| Column               | Purpose                                |
| -------------------- | -------------------------------------- |
| Customer_ID          | Customer identifier for graph modeling |
| Year                 | Order year                             |
| Month                | Order month                            |
| Quarter              | Order quarter                          |
| Delivery_Days        | Days between order and delivery        |
| Delivery_Performance | On Time / Not On Time                  |

---

## 🗃️ Project Structure

```text
Courier-Delivery-Logistics-Analytics/
│
├── data/
│   ├── courier_raw_data_2024_2026.csv
│   ├── courier_cleaned_data_2024_2026.csv
│   ├── customers.csv
│   ├── shipments.csv
│   └── zones.csv
│
├── notebooks/
│   └── courier_data_cleaning.ipynb
│
├── dashboards/
│   ├── PowerBI/
│   ├── Tableau/
│   └── Looker/
│
├── neo4j/
│   └── courier_graph_queries.cypher
│
├── assets/
│   ├── powerbi.png
│   ├── tableau.png
│   └── looker.png
│
└── README.md
```

---

## 🧠 Data Modeling

The project uses separate data files for relational analytics and graph modeling.

### Neo4j Graph Model

```text
(Customer)
    |
    | BOOKED
    v
(Shipment)
    |
    | ORIGINATES_FROM
    v
(Zone)

(Shipment)
    |
    | DELIVERED_TO
    v
(Zone)
```

### Neo4j Tables

#### customers.csv

Contains customer information.

* Customer_ID
* Customer_Type

#### shipments.csv

Contains shipment-level information.

* Shipment_ID
* Customer_ID
* Order_Date
* Delivery_Date
* Origin_Zone
* Destination_Zone
* Package_Type
* Shipping_Mode
* Shipping_Cost
* Delivery_Status
* Delivery_Days
* Delivery_Performance

#### zones.csv

Contains zone master data.

* Zone_ID
* Zone_Name

---

## 📊 Business Intelligence Dashboards

The project is designed to support dashboard development in Power BI, Tableau, and Looker Studio.

### Power BI

Planned analysis:

* Total Shipments
* Shipping Revenue
* Average Delivery Days
* Delivery Status Distribution
* Shipment Trends
* Shipping Mode Analysis
* Zone Performance
* Package Type Analysis

**Power BI Dashboard:** Coming Soon

### Tableau

Planned analysis:

* Shipment Trend Analysis
* Delivery Performance
* Shipping Mode Comparison
* Origin vs Destination Zones
* Package Type Distribution

**Tableau Dashboard:** Coming Soon

### Looker Studio

Planned analysis:

* Shipment KPIs
* Delivery Status
* Shipping Cost Analysis
* Customer Type Analysis
* Shipping Mode Performance

**Looker Studio Dashboard:** Coming Soon

---

## 🕸️ Neo4j Graph Analytics

Neo4j is used to explore relationships between customers, shipments, and zones.

### Example Business Questions

1. Which customers have booked the most shipments?
2. Which zones receive the highest shipment volume?
3. Which customers use Express shipping most frequently?
4. Which origin-destination routes have the most shipments?
5. Which zones have higher delayed shipment activity?
6. How are customers connected to shipment operations?

### Technologies

* Neo4j Desktop
* Cypher Query Language
* Graph Data Modeling
* Nodes & Relationships
* Aggregation
* Graph Traversal

---

## 🛠️ Tools & Technologies

| Tool          | Purpose                                   |
| ------------- | ----------------------------------------- |
| Python        | Data generation and processing            |
| Pandas        | Data cleaning and transformation          |
| NumPy         | Synthetic data generation                 |
| SQL           | Data analysis                             |
| Power BI      | Business intelligence dashboards          |
| Tableau       | Visual analytics                          |
| Looker Studio | Reporting and dashboards                  |
| Neo4j         | Graph database and relationship analytics |
| GitHub        | Version control and portfolio             |
| Kaggle        | Dataset publishing                        |

---

## 📈 Key Metrics

| Metric                 | Description                         |
| ---------------------- | ----------------------------------- |
| Total Shipments        | Count of shipment records           |
| Total Shipping Revenue | Sum of shipping costs               |
| Average Delivery Days  | Average delivery duration           |
| Delivered Shipments    | Shipments with Delivered status     |
| Delayed Shipments      | Shipments with Delayed status       |
| Cancellation Rate      | Cancelled shipments as a percentage |
| Failure Rate           | Failed shipments as a percentage    |
| On-Time Delivery Rate  | On-time shipments as a percentage   |

---

## 🚀 Project Workflow

1. Created a synthetic courier dataset using Python.
2. Uploaded the raw dataset to Kaggle.
3. Performed data cleaning and transformation using Pandas.
4. Created a separate cleaned CSV file.
5. Created separate CSV tables for Neo4j.
6. Built a graph model using Customers, Shipments, and Zones.
7. Performed SQL-based analysis.
8. Developed Power BI, Tableau, and Looker Studio dashboards.
9. Documented the complete project on GitHub.

---

## 📁 Dataset Files

| File                               | Description                     |
| ---------------------------------- | ------------------------------- |
| courier_raw_data_2024_2026.csv     | Original raw dataset            |
| courier_cleaned_data_2024_2026.csv | Cleaned and transformed dataset |
| customers.csv                      | Customer master table           |
| shipments.csv                      | Shipment transaction table      |
| zones.csv                          | Zone master table               |

---

## ⚠️ Disclaimer

This project uses synthetically generated data for educational, portfolio, and analytics practice purposes.

It does not represent the actual operations, customers, or performance of any courier or logistics company.

---

## 👤 Author

**Ajit Jha**

Data Analyst | Research Analyst | Business Intelligence Enthusiast

### Skills Demonstrated

Python • SQL • Pandas • Power BI • Tableau • Looker Studio • Neo4j • Data Cleaning • Data Modeling • Business Analytics

---

⭐ If you find this project useful, feel free to explore the repository and share feedback.
