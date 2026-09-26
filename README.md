

<div align="center">

<img width="738" height="506" alt="image" src="https://github.com/user-attachments/assets/ed1c76d2-e159-4029-b717-adff78f7e47a" />
<img width="396" height="434" alt="image" src="https://github.com/user-attachments/assets/79071488-0eb6-4397-abf7-351ff8e67ac3" />


# 🚚 Courier Delivery & Logistics Analytics (2024–2026)


###  Data Sources → Extraction → Cleaning → Storage → Visualization → Graph DB  → Graph Query 

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/pandas-%23150458.svg?style=for-the-badge&logo=pandas&logoColor=white)
![SQL](https://img.shields.io/badge/SQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white)
![Power BI](https://img.shields.io/badge/Power%20BI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)
![DAX](https://img.shields.io/badge/DAX-KPI%20Measures-5E5E5E?style=for-the-badge)
![Data Modeling](https://img.shields.io/badge/Data%20Modeling-Relationships-2F855A?style=for-the-badge)
![Looker Studio](https://img.shields.io/badge/Looker%20Studio-4285F4?style=for-the-badge)
![Neo4j](https://img.shields.io/badge/Neo4j-Graph%20DB-008CC1?style=for-the-badge)
![Cypher](https://img.shields.io/badge/Cypher-Query%20Language-2F855A?style=for-the-badge)
![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white)



> A complete end-to-end analyst portfolio project built across three industry-standard BI platforms and a graph database layer.
> Python (Data Extraction) → Raw Data → Cleaning → Modeling → Power BI · Tableau · Looker Studio → Neo4j → Cypher

</div>

---
## Live Demos


| Platform | Link |
|---|---|
| Power BI | See `/Dashboard` folder (`.pbix` file) |
| Tableau Public | [Courier Delivery & Logistics Intelligence](https://public.tableau.com/app/profile/ajit.jha/viz/CourierDeliveryLogisticsIntelligence/Dashboard1)|
| Looker Studio | [Live Report](https://datastudio.google.com/s/kjA5soPoloY)|
| GitHub Repo | [Grocery Store Sales Analytics](Courier-Delivery-Logistics-Analytics-Dataset-2024-2026-) |



A multi-platform analytics portfolio project focused on **courier shipment performance, delivery operations, customer segmentation, and logistics intelligence**.

The project combines **Python/Pandas, SQL, Power BI, Tableau, Looker Studio, and Neo4j** to demonstrate an end-to-end analytics workflow — from raw data preparation to BI reporting and graph analytics.



---


# 📑 Table of Contents

- [Project Overview](#-project-overview)
- [Business Objective](#-business-objective)
- [Key Business Questions](#-key-business-questions)
- [Dataset Overview](#-dataset-overview)
- [Data Preparation](#-data-preparation)
- [Data Model](#-data-model)
- [Power BI Dashboard](#-power-bi-dashboard)
- [Power BI DAX Measures](#-power-bi-dax-measures)
- [Tableau Dashboard](#-tableau-dashboard)
- [Tableau Calculations](#-tableau-calculations)
- [Looker Studio Dashboard](#-looker-studio-dashboard)
- [Looker Studio Calculated Fields](#-looker-studio-calculated-fields)
- [Neo4j Graph Analytics](#️-neo4j-graph-analytics)
- [Neo4j Cypher Queries](#-neo4j-cypher-queries)
- [Business Insights](#-business-insights)
- [Project Workflow](#-project-workflow)
- [Repository Structure](#-repository-structure)
- [Tools & Technologies](#️-tools--technologies)
- [Skills Demonstrated](#-skills-demonstrated)
- [Future Enhancements](#-future-enhancements)
- [How to Run](#-how-to-run--setup)
- [Disclaimer](#️-disclaimer)
- [Author](#-author)
- [License](#license)

---

# 📌 Project Overview

This project analyzes **2,000 courier shipments from 2024 to 2026** to understand shipment volume, delivery status, delivery performance, shipping modes, destination-zone activity, and delayed shipments.

The same analytical dataset was implemented across three BI platforms:

- **Power BI**
- **Tableau**
- **Looker Studio**

A separate **Neo4j graph model** was created to analyze relationships between customers, shipments, and geographical zones.

The objective is to demonstrate how the same business problem can be analyzed through **relational, BI, and graph-based approaches**.

---

# 🎯 Business Objective

The project is designed to answer operational and management questions such as:

- How many shipments are being processed?
- What is the total shipping revenue/cost represented in the dataset?
- How many shipments were delivered?
- What percentage of shipments met the project-defined on-time SLA?
- What is the average delivery time?
- Which shipping modes handle the highest shipment volume?
- Which destination zones receive the most shipments?
- Which destination zones have the highest number of delayed shipments?
- How does shipment volume change over time?
- What is the distribution of delivery statuses?
- How can customer–shipment–zone relationships be represented as a graph?

---

# ❓ Key Business Questions

### Shipment Performance
1. What is the total shipment volume?
2. How does shipment volume change month by month?
3. Which shipping mode handles the highest number of shipments?

### Delivery Performance
4. How many shipments were delivered?
5. What is the on-time delivery percentage?
6. What is the average delivery time?
7. What is the distribution of Delivered, Delayed, Cancelled and Failed shipments?

### Geographic / Operational Analysis
8. Which destination zones receive the most shipments?
9. Which destination zones have the highest delayed shipment volume?

### Graph Analytics
10. Which customers are connected to the highest number of shipments?
11. Which zones are connected to the highest number of shipments?
12. How can customer → shipment → zone relationships be explored using Neo4j?

---

# 📊 Dataset Overview

| Attribute | Details |
|---|---|
| Records | **2,000 shipments** |
| Period | **2024–2026** |
| Domain | Courier / Logistics |
| Data Type | Synthetic project dataset |
| Granularity | Shipment-level |
| Raw Columns | 10 |
| Analytical Columns | Added during transformation |

---

# 🧾 Raw Dataset Columns

| Column | Description |
|---|---|
| `Shipment_ID` | Unique shipment identifier |
| `Order_Date` | Shipment booking/order date |
| `Delivery_Date` | Shipment delivery date |
| `Customer_Type` | Individual or Business |
| `Origin_Zone` | Shipment origin zone |
| `Destination_Zone` | Shipment destination zone |
| `Package_Type` | Type/category of package |
| `Shipping_Mode` | Standard, Express or Same Day |
| `Shipping_Cost` | Shipping amount associated with shipment |
| `Delivery_Status` | Delivered, Delayed, Cancelled or Failed |

---

# 🧹 Data Preparation

The raw dataset was processed using **Python and Pandas**.

### Main preparation steps

- Loaded the raw CSV dataset
- Inspected data types and structure
- Checked missing values
- Checked duplicate shipment IDs
- Standardized text fields
- Converted date columns
- Validated delivery dates
- Validated shipping cost values
- Added customer identifiers for graph modelling
- Created analytical date fields
- Calculated delivery duration
- Created project-defined delivery-performance classification
- Exported the cleaned analytical dataset

### Analytical columns

| Column | Purpose |
|---|---|
| `Customer_ID` | Customer-level analysis and Neo4j modelling |
| `Delivery_Days` | Number of days between order and delivery |
| `Year` | Year-level filtering |
| `Month` | Monthly trend analysis |
| `Quarter` | Quarterly analysis |
| `Delivery_Performance` | On-time vs not-on-time classification |

### Project-defined On-Time SLA

For this portfolio project:

> A shipment is classified as **On Time** when `Delivery_Status = Delivered` and `Delivery_Days <= 3`.

This is a **project-defined analytical assumption**, not an external courier-company SLA.

---

# 🧩 Data Model

The analytical dataset is used across the BI tools.

The Neo4j model separates the data into:

### Customers
`customers.csv`

- Customer_ID
- Customer_Type

### Shipments
`shipments.csv`

- Shipment_ID
- Customer_ID
- Order_Date
- Delivery_Date
- Origin_Zone
- Destination_Zone
- Package_Type
- Shipping_Mode
- Shipping_Cost
- Delivery_Status
- Delivery_Days
- Delivery_Performance

### Zones
`zones.csv`

- Zone_ID
- Zone_Name

---

# 📊 Power BI Dashboard

The Power BI dashboard provides a one-page executive and operational overview.

### Dashboard KPIs

- Total Shipments
- Total Revenue / Shipping Amount
- Delivered Shipments
- On-Time Delivery %
- Average Delivery Days

### Dashboard Visuals

- Shipment Volume Trend
- Delivery Status Distribution
- Shipments by Shipping Mode
- Shipments by Destination Zone
- Delayed Shipments by Destination Zone

### Filters

- Year
- Shipping Mode

---

# 🧮 Power BI DAX Measures

Only the measures used in the dashboard are documented below.

### 1. Total Shipments

```DAX
Total Shipments =
DISTINCTCOUNT(Courier[Shipment_ID])
```

### 2. Total Revenue

```DAX
Total Revenue =
SUM(Courier[Shipping_Cost])
```

### 3. Delivered Shipments

```DAX
Delivered Shipments =
CALCULATE(
    [Total Shipments],
    Courier[Delivery_Status] = "Delivered"
)
```

### 4. On-Time Shipments

```DAX
On-Time Shipments =
CALCULATE(
    [Total Shipments],
    Courier[Delivery_Performance] = "On Time"
)
```

### 5. On-Time Delivery %

```DAX
On-Time Delivery % =
DIVIDE(
    [On-Time Shipments],
    [Total Shipments],
    0
)
```

### 6. Average Delivery Days

```DAX
Average Delivery Days =
AVERAGE(Courier[Delivery_Days])
```

### 7. Delayed Shipments

```DAX
Delayed Shipments =
CALCULATE(
    [Total Shipments],
    Courier[Delivery_Status] = "Delayed"
)
```

---

# 📈 Tableau Dashboard

The Tableau dashboard provides the same business analysis using Tableau visual analytics.

### Dashboard KPIs

- Total Shipments
- Total Revenue
- Delivered Shipments
- On-Time Delivery %
- Average Delivery Days

### Dashboard Visuals

- Shipment Volume Trend
- Delivery Status
- Shipments by Shipping Mode
- Shipments by Destination Zone
- Delayed Shipments by Destination Zone

### Filters

- Year
- Shipping Mode

---

# 🧮 Tableau Calculations

The Tableau dashboard uses calculated fields corresponding to the business metrics shown in the dashboard.

### Total Shipments

```text
COUNTD([Shipment_ID])
```

### Total Revenue

```text
SUM([Shipping_Cost])
```

### Delivered Shipments

```text
SUM(
    IF [Delivery_Status] = "Delivered"
    THEN 1
    ELSE 0
    END
)
```

### On-Time Shipments

```text
SUM(
    IF [Delivery_Performance] = "On Time"
    THEN 1
    ELSE 0
    END
)
```

### On-Time Delivery %

```text
SUM(
    IF [Delivery_Performance] = "On Time"
    THEN 1
    ELSE 0
    END
)
/
COUNTD([Shipment_ID])
```

### Average Delivery Days

```text
AVG([Delivery_Days])
```

### Delayed Shipments

```text
SUM(
    IF [Delivery_Status] = "Delayed"
    THEN 1
    ELSE 0
    END
)
```

---

# 📊 Looker Studio Dashboard

Looker Studio provides a web-based implementation of the same courier analytics model.

### Dashboard KPIs

- Total Shipments
- Total Revenue
- Delivered Shipments
- On-Time Delivery %
- Average Delivery Days

### Dashboard Visuals

- Shipment Volume Trend
- Delivery Status
- Shipments by Shipping Mode
- Shipments by Destination Zone
- Delayed Shipments by Destination Zone

### Filters

- Year
- Shipping Mode

---

# 🧮 Looker Studio Calculated Fields

### Total Shipments

```text
COUNT_DISTINCT(Shipment_ID)
```

### Total Revenue

```text
SUM(Shipping_Cost)
```

### Delivered Shipments

```text
SUM(
  CASE
    WHEN Delivery_Status = "Delivered" THEN 1
    ELSE 0
  END
)
```

### On-Time Shipments

```text
SUM(
  CASE
    WHEN Delivery_Performance = "On Time" THEN 1
    ELSE 0
  END
)
```

### On-Time Delivery %

```text
SUM(
  CASE
    WHEN Delivery_Performance = "On Time" THEN 1
    ELSE 0
  END
)
/
COUNT_DISTINCT(Shipment_ID)
```

### Average Delivery Days

```text
AVG(Delivery_Days)
```

### Delayed Shipments

```text
SUM(
  CASE
    WHEN Delivery_Status = "Delayed" THEN 1
    ELSE 0
  END
)
```

---

# 🕸️ Neo4j Graph Analytics

The project also models courier data as a graph to analyze relationships that are not naturally represented by standard BI charts.

## Graph Model

```text
(Customer)
     |
     | BOOKED
     v
 (Shipment)
    /   \
   /     \
  v       v
(Zone)   (Zone)
Origin   Destination
```

### Relationships

```text
Customer ──[:BOOKED]──> Shipment

Shipment ──[:ORIGINATES_FROM]──> Zone

Shipment ──[:DELIVERED_TO]──> Zone
```

---

# 🧠 Neo4j Cypher Queries

### Find all customers

```cypher
MATCH (c:Customer)
RETURN c
LIMIT 20;
```

### Find all shipments

```cypher
MATCH (s:Shipment)
RETURN s
LIMIT 20;
```

### Find all zones

```cypher
MATCH (z:Zone)
RETURN z;
```

### Customer → Shipment relationship

```cypher
MATCH (c:Customer)-[:BOOKED]->(s:Shipment)
RETURN c.Customer_ID AS Customer,
       s.Shipment_ID AS Shipment
LIMIT 20;
```

### Customers with the highest shipment count

```cypher
MATCH (c:Customer)-[:BOOKED]->(s:Shipment)
RETURN c.Customer_ID AS Customer,
       count(s) AS TotalShipments
ORDER BY TotalShipments DESC
LIMIT 10;
```

### Shipments by destination zone

```cypher
MATCH (s:Shipment)-[:DELIVERED_TO]->(z:Zone)
RETURN z.Zone_Name AS DestinationZone,
       count(s) AS TotalShipments
ORDER BY TotalShipments DESC;
```

### Delayed shipments by destination zone

```cypher
MATCH (s:Shipment)-[:DELIVERED_TO]->(z:Zone)
WHERE s.Delivery_Status = "Delayed"
RETURN z.Zone_Name AS DestinationZone,
       count(s) AS DelayedShipments
ORDER BY DelayedShipments DESC;
```

### Customer → Shipment → Destination traversal

```cypher
MATCH (c:Customer)-[:BOOKED]->(s:Shipment)-[:DELIVERED_TO]->(z:Zone)
RETURN c.Customer_ID AS Customer,
       s.Shipment_ID AS Shipment,
       z.Zone_Name AS DestinationZone
LIMIT 20;
```

---

# 💡 Business Insights

The dashboards and graph model are designed to highlight:

- Overall shipment volume and trend
- Delivery-status composition
- Delivery performance against the project-defined SLA
- Shipping-mode utilization
- Destination-zone shipment concentration
- Destination zones associated with delayed shipments
- Customer shipment activity
- Relationships between customers, shipments and zones

The exact metrics dynamically change with filters in the BI dashboards.

---

# 🔄 Project Workflow

```text
Raw Dataset
     ↓
Python / Pandas
     ↓
Data Cleaning & Validation
     ↓
Analytical Dataset
     ↓
 ┌───────────────┬────────────────┬─────────────────┐
 ↓               ↓                ↓
Power BI       Tableau       Looker Studio
 ↓               ↓                ↓
Executive & Operational BI Dashboards

     +

Analytical CSVs
     ↓
Neo4j
     ↓
Graph Model
     ↓
Cypher Queries & Relationship Analysis
```

---

# 📁 Repository Structure

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
│   └── data_cleaning.ipynb
│
├── Dashboard/
│   └── Courier_Delivery_Logistics.pbix
│   └── Courier_Delivery_Logistics.twbx
│
├── neo4j/
│   ├── queries/
│   └── graph_screenshot.png
│
├── assets/
│   ├── powerbi_dashboard.png
│   ├── tableau_dashboard.png
│   ├── looker_dashboard.png
│   └── neo4j_graph.png
│
└── README.md
│
└── License
```

---

# 🛠️ Tools & Technologies

| Tool / Technology | Purpose |
|---|---|
| **Python** | Data generation, cleaning and transformation |
| **Pandas** | Data preprocessing and analytical column creation |
| **SQL** | Data analysis and business queries |
| **Power BI** | Interactive BI dashboard and DAX measures |
| **Tableau** | Interactive visual analytics dashboard |
| **Looker Studio** | Web-based BI reporting |
| **Neo4j** | Graph database and relationship analysis |
| **Cypher** | Graph querying and traversal |
| **Kaggle** | Dataset publishing |
| **GitHub** | Project version control and documentation |

---

## 💻 Skills Demonstrated

### Data Analytics
- Data cleaning
- Data validation
- Data transformation
- Exploratory analysis
- KPI development

### Python
- Pandas
- CSV processing
- Date transformation
- Data quality checks

### SQL
- Aggregation
- Filtering
- Grouping
- Business analysis

### Business Intelligence
- Power BI
- DAX
- Tableau
- Looker Studio
- Dashboard design
- Interactive filtering
- KPI visualization

### Graph Analytics
- Neo4j
- Cypher
- Nodes
- Relationships
- Graph traversal
- Aggregation
- Relationship-based analysis

---

# 🚀 Future Enhancements

Potential future improvements include:

- Predictive delivery-delay modelling
- Customer shipment segmentation
- Route-level optimization
- Carrier-level performance analysis
- Advanced graph centrality analysis
- Automated data refresh
- Real-time shipment tracking integration

---

# ⚠️ Disclaimer

This project uses a **synthetic dataset created for portfolio and learning purposes**.

The dataset does not represent actual courier-company operational records.

The **3-day on-time delivery threshold is a project-defined analytical assumption** and should not be interpreted as an actual industry SLA.

---

## 🚀 How to Run / Setup

You can set up and run this project locally on your system using any of the options below:

### 🔹 Option 1: Direct Download (Easiest)
If you do not have Git installed, you can download the project as a ZIP file:
1. Scroll to the top of this GitHub repository page and click the green **Code** button.
2. Select **Download ZIP** from the dropdown menu.
3. Once downloaded, extract (unzip) the file to a folder on your computer.

---

### 🔹 Option 2: Clone the Repository (Recommended)
If you have Git installed, open your Terminal or Command Prompt (CMD) and run the following commands:

```bash
# 1. Clone the repository
git clone https://github.com

# 2. Navigate into the project directory
cd Courier-Delivery-Logistics-Analytics-Dataset-2024-2026-
```

---

### 🛠️ Post-Download Setup

#### 1. Running Python & Pandas (Data Cleaning)
To execute the data cleaning steps or run the Jupyter Notebook, install the required dependencies first:
```bash
pip install pandas numpy jupyter
```
After installation, navigate to the `notebooks/` folder and open `courier_data_cleaning.ipynb` using Jupyter Notebook.

#### 2. Running Neo4j Graph Analytics
1. Open **Neo4j Desktop** and create a new Local DBMS.
2. Place the CSV files (`customers.csv`, `shipments.csv`, and `zones.csv`) from the `data/` folder into the `import/` directory of your Neo4j database.
3. Open the `neo4j/courier_graph_queries.cypher` file, copy the queries, and run them directly in the Neo4j Browser interface.


# 👤 Author

**Ajit Jha**

Analytics Professional | Research & Business Intelligence

### Core Areas

`Data Analytics` • `Business Intelligence` • `Python` • `SQL` • `Power BI` • `Tableau` • `Looker Studio` • `Neo4j` • `Graph Analytics`

---

⭐ **If you find this project useful, feel free to explore the dashboards, data model, and Neo4j graph implementation.**
- **GitHub:** [Ajitjha3095](https://github.com/Ajitjha3095)
- **LinkedIn:** [Ajit Jha](https://www.linkedin.com/in/ajitjha01/)

## License

This project is licensed under the **MIT License**.  
See the [LICENSE](LICENSE) file for details.
