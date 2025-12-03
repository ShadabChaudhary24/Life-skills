# Data Warehousing
**A Data warehouse (DWH)** is a **centralized storage system** that holds 
huge amounts of historical data, specifically built to help 
companies make smart decisions this is 
called Business Intelligence (BI). It gathers information from all the
different system like sales records, inventory, and website logs,
giving a complete picture of the business in the past few days or months.

# Essential Components and Architecture
![ETL Process Diagram](https://upload.wikimedia.org/wikipedia/commons/c/c7/Extract%2C_Transform%2C_Load_Data_Flow_Diagram.svg)
### 1. The ETL Process: Data Preparation Pipeline
Before information can be trusted, it must be prepared through
a crucial three-step process called **ETL (Extract, Transform, Load)**:
* **Extract (Pull):** Data is first pulled out of the various source 
systems (like transactional databases).
* **Transform (Clean & Fix):** Data is then cleaned up, 
fixed, and standardized. This step is important for ensuring the data 
is integrated-meaning all inconsistent formats, names, 
and codes matches the warehouse's structure.
* **Load (Store):** Finally, the clean, ready-to-use data is placed 
into the final warehouse tables.

### 2. Post-ETL: Analysis and Delivery
Once the data is successfully Loaded into the Data Warehouse, 
it is immediately ready to be used. This involves 
two main activities:
* **Querying and Reporting:** Analysts, data scientists, 
and managers use specialized tools (BI tools like Tableau or 
Power BI) and complex SQL queries to retrieve the specific 
data they need. The huge dataset to answer 
business questions, such as "What was the sales trend for this 
product in the South region last quarter?"
* **Data Delivery:** For faster, more focused analysis, 
data relevant to a specific team (like Finance or Marketing) is 
often copied into a smaller, simpler Data Mart. 
This ensures that departments can access their required history 
quickly without searching through the entire corporate warehouse.

## 3. Dimensional Modeling: The Blueprint for Analysis
![Star Schema Diagram illustrating Dimensional Modeling](https://media.geeksforgeeks.org/wp-content/uploads/20211002145356/starskema.png)
The final structure of the warehouse is the most critical technical 
detail that enables fast reporting. This is achieved through 
Dimensional Modeling, where data is organized into simple tables:
* **Fact Tables:** Contain the data that needs to be counted or added
up like total sales.
* **Dimension Tables:** Hold the context the details like Customer Name, 
Product Type, or Date. This structure makes the data organized by business topic rather than operational 
function, and ensures it is kept forever and never 
changed, making it ideal for historical comparison.

This entire architecture provides a necessary single source of truth
that allows managers to confidently discover historical patterns, 
track performance over time, and accurately plan future strategy.

# References
### 1. Wikipedia: Data warehouse
* https://en.wikipedia.org/wiki/Data_warehouse
### 2. Oracle: What is a Data Warehouse?
* https://www.oracle.com/in/database/what-is-a-data-warehouse/
### 3. What is ETL?
* https://aws.amazon.com/what-is/etl/
### 4. Star Schema
* https://www.geeksforgeeks.org/data-analysis/designing-the-star-schema-in-data-warehousing/
