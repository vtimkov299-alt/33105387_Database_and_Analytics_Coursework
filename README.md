# 33105387_Database_and_Analytics_Coursework
# Northstar Data Analysis Project

##  Overview
This project focuses on analysing the **Northstar logistics dataset** using multiple technologies, including **SQL, R, Python, and MongoDB**. The aim is to extract insights related to delivery performance, operational efficiency, and customer experience.

---

##  Objectives
- Analyse delivery patterns across different pickup zones
- Identify areas with high failure rates
- Evaluate complaint trends and severity
- Optimise database queries for performance
- Compare relational and NoSQL approaches

---

##  Technologies Used
- **SQL** – Data querying and aggregation  
- **R (dplyr, sqldf, ggplot2)** – Data manipulation and visualisation  
- **Python (pandas, pymongo)** – Data processing and MongoDB integration  
- **MongoDB Atlas** – NoSQL database storage and aggregation  

---

##  Dataset
The dataset includes:
- Orders
- Deliveries
- Complaints
- Drivers
- Vehicles
- Incidents

---

##  Key Analysis

### 1. Delivery Distribution
- Highest deliveries observed in:
  - **East (156)**
  - **South (139)**
  - **North (135)**

---

### 2. Failure Rate by Pickup Zone
- Highest failure rates:
  - **Central (20%)**
  - **CTR (17%)**
  - **North (16%)**

---

### 3. Complaint Analysis
- Most frequent complaint:
  - **Delay (101 cases)**
- High severity complaints:
  - **77 total**
- Highest compensation:
  - **Damage (~24.0)**
  - **Billing (~23.9)**

---

### 4. Delivery Status Breakdown
- **On-time:** 616  
- **Delayed:** 202  
- **Failed:** 132  

---

### 5. Service Type Analysis
- Longest average delivery window:
  - **Parcel (~8.30 hours)**
- Shortest:
  - **Business (~6.93 hours)**

---

##  Visualisations
- Failure rate by pickup zone (bar chart using ggplot2)
- Aggregated delivery statistics

---

##  MongoDB Implementation
- Data imported into MongoDB collections:
  - `orders`, `deliveries`, `complaints`
- Aggregation pipelines used:
  - `$lookup` (join operations)
  - `$group` (aggregation)
  - `$avg`, `$sum` (metrics)
- Query optimisation:
  - Indexes created on `order_id`

---

##  Query Optimisation
Indexes were created to improve performance:
```python
db.orders.create_index("order_id")
db.deliveries.create_index("order_id")
db.complaints.create_index("order_id")
