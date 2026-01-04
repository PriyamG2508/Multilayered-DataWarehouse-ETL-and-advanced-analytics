# Multilayered Data Warehouse ETL & Advanced Analytics

[![SQL Server](https://img.shields.io/badge/SQL_Server-CC2927?style=for-the-badge&logo=microsoft-sql-server&logoColor=white)](https://www.microsoft.com/sql-server)
[![Data Engineering](https://img.shields.io/badge/Data_Engineering-4285F4?style=for-the-badge&logo=databricks&logoColor=white)](https://github.com/PriyamG2508)
[![ETL](https://img.shields.io/badge/ETL_Pipeline-FF6F00?style=for-the-badge&logo=apache-airflow&logoColor=white)](https://github.com/PriyamG2508)
![T-SQL](https://img.shields.io/badge/T--SQL-CC2927?style=for-the-badge&logo=microsoft-sql-server&logoColor=white)
![Data Quality](https://img.shields.io/badge/Data_Quality_Checks-4CAF50?style=for-the-badge&logo=checkmarx&logoColor=white)
![Validation Framework](https://img.shields.io/badge/Data_Validation-673AB7?style=for-the-badge)


> A production-grade end-to-end data warehouse implementation following the **Medallion Architecture** (Bronze → Silver → Gold) with advanced SQL-based analytics and reporting capabilities.

## Table of Contents

- [Overview](#overview)
- [Architecture](#architecture)
- [Key Features](#key-features)
- [Project Structure](#project-structure)
- [Tech Stack](#tech-stack)
- [Getting Started](#getting-started)
- [Analytics & Insights](#analytics--insights)
- [Data Quality](#data-quality)
- [Skills Demonstrated](#skills-demonstrated)
- [Connect](#connect)

## Overview

This project showcases a complete **modern data warehouse solution** designed to handle enterprise-level data integration, transformation, and analytics. Built with industry best practices, it demonstrates proficiency in data engineering, ETL pipeline development, and SQL-based analytical reporting.

### Business Objectives

- **Unified Data Platform**: Integrate ERP and CRM source systems into a single analytical repository
- **Data Quality Assurance**: Implement robust validation and cleansing processes
- **Business Intelligence**: Enable data-driven decision-making through advanced analytics
- **Scalable Architecture**: Design for future growth and complexity
- **Documentation Excellence**: Provide comprehensive technical and business documentation

## Architecture

### Medallion Architecture Implementation

```
┌─────────────────────────────────────────────────────────────┐
│                     SOURCE SYSTEMS                          │
│              ERP Systems  │  CRM Systems                    │
│              (CSV Files)  │  (CSV Files)                    │
└─────────────────┬───────────────────────────────────────────┘
                  │
                  ▼
┌─────────────────────────────────────────────────────────────┐
│  BRONZE LAYER - Raw Data Ingestion                          │
│  -  Raw data stored as-is                                   │
│  -  Minimal transformation                                  │
│  -  Full audit trail                                        │
└─────────────────┬───────────────────────────────────────────┘
                  │
                  ▼
┌─────────────────────────────────────────────────────────────┐
│  SILVER LAYER - Cleaned & Validated                         │
│  -  Data cleansing & standardization                        │
│  -  Schema validation                                       │
│  -  Business rules applied                                  │
│  -  Data quality checks                                     │
└─────────────────┬───────────────────────────────────────────┘
                  │
                  ▼
┌─────────────────────────────────────────────────────────────┐
│  GOLD LAYER - Business-Ready Analytics                      │
│  -  Star Schema modeling                                    │
│  -  Fact & Dimension tables                                 │
│  -  Aggregated metrics                                      │
│  -  Optimized for reporting                                 │
└─────────────────────────────────────────────────────────────┘
```

### Data Flow

1. **Bronze Layer**: Raw data ingestion from source systems  
2. **Silver Layer**: Data cleansing, validation, and integration  
3. **Gold Layer**: Star schema dimensional modeling for analytics  
4. **Reports Layer**: Business insights and KPI dashboards  

## Key Features

### Data Engineering
- Complete ETL pipeline implementation  
- Medallion architecture (Bronze → Silver → Gold)  
- Automated data quality validation  
- Incremental data loading capabilities  
- Error handling and logging mechanisms  

### Data Modeling
- Star schema dimensional model  
- Fact and dimension table design  
- Surrogate key management  
- Slowly Changing Dimensions (SCD) ready  
- Optimized indexes and partitioning  

### Analytics
- Customer behavior analysis  
- Product performance metrics  
- Sales trend analysis  
- Advanced SQL analytics  
- Business KPI reporting

### Documentation
- Architecture diagrams (DrawIO)  
- Data flow documentation  
- Data catalog and dictionary  
- Naming conventions guide  
- Technical specifications  

## Project Structure

```
Multilayered-DataWarehouse-ETL-and-advanced-analytics/
│
├── datasets/                       # Source data files
│   ├── erp/                        # ERP system data
│   └── crm/                        # CRM system data
│
├── scripts/                        # SQL scripts
│   ├── init_database.sql           # Database initialization
│   ├── bronze/                     # Raw data ingestion
│   ├── silver/                     # Data cleansing & validation
│   ├── gold/                       # Star schema & aggregations
│   ├── eda/                        # Exploratory data analysis
│   ├── advanced_analytics/         # Advanced analytics queries
│   └── reports/                    # Business reporting queries
│
├── docs/                           # Documentation
│   ├── data_catalog.md             # Data dictionary
│   └── naming-conventions.md       # Naming standards
│
├── tests/                          # Data quality tests
│   ├── bronze_validation.sql       # Bronze layer tests
│   ├── silver_validation.sql       # Silver layer tests
│   └── gold_validation.sql         # Gold layer tests
│
├── README.md                       # Project documentation
├── LICENSE                         # MIT License
├── .gitignore                      # Git ignore rules
└── requirements.txt                # Project dependencies
```

## Tech Stack

- SQL Server (T-SQL)
- Data Warehousing & ETL
- Medallion Architecture
- Star Schema Modeling
- Git & Version Control
  
## Getting Started

### Prerequisites

- **SQL Server Express (2019 or later)**  
- **SQL Server Management Studio (SSMS)**  
- **Git**  
- **DrawIO** *(optional, for viewing diagrams)*  

### Installation

1. **Clone the Repository**
   ```bash
   git clone https://github.com/PriyamG2508/Multilayered-DataWarehouse-ETL-and-advanced-analytics.git
   cd Multilayered-DataWarehouse-ETL-and-advanced-analytics
   ```

2. **Set Up Database**
   ```sql
   :r scripts/init_database.sql
   ```

3. **Load Bronze Layer**
   ```sql
   :r scripts/bronze/ddl_bronze.sql
   :r scripts/bronze/proc_bronze_load.sql
   ```

4. **Transform to Silver Layer**
   ```sql
   :r scripts/silver/ddl_silver.sql
   :r scripts/silver/proc_silver_load.sql
   :r tests/quality_checks_silver.sql
   ```

5. **Build Gold Layer**
   ```sql
   :r scripts/gold/ddl_gold.sql
   :r tests/quality_checks_gold.sql
   ```

6. **Run Analytics**
   ```sql
   :r scripts/reports/report_customers.sql
   :r scripts/reports/report_products.sql
   ```

## Analytics & Insights

### Customer Analytics
- Segmentation  
- LTV analysis  
- Churn indicators  
- Purchase behavior  

### Product Performance
- Top sellers  
- Profitability metrics  
- Inventory turnover  

### Sales Trends
- Time-series analysis  
- Seasonal patterns  
- Regional performance  

#### Example Query

```sql
SELECT TOP 10
    c.customer_name,
    SUM(f.sales_amount) AS total_revenue,
    COUNT(DISTINCT f.sale_key) AS order_count,
    AVG(f.sales_amount) AS avg_order_value
FROM gold.fact_sales f
JOIN gold.dim_customer c 
  ON f.customer_key = c.customer_key
WHERE f.date_key >= 20240101
GROUP BY c.customer_name
ORDER BY total_revenue DESC;
```

## Data Quality

### Validation Framework

**Bronze**
- Row counts  
- File completeness  
- Schema drift detection  

**Silver**
- Null handling  
- Data type validation  
- Referential integrity  
- Duplicate detection  

**Gold**
- Dimensional integrity  
- Aggregation validation  
- Performance benchmarks  

## Skills Demonstrated

### Technical
- SQL (CTEs, Window Functions, Stored Procedures)  
- ETL & ELT Pipeline Design  
- Dimensional Modeling / Star Schema  
- Medallion Architecture  
- Performance Tuning & Optimization  
- Git & Version Control  

### Business
- Requirements Understanding  
- Data Quality Management  
- Documentation & Communication  

## Connect

**Priyam Gupta**  
*Data Engineer | Analytics Enthusiast*

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/priyamg2508)
[![GitHub](https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white)](https://github.com/PriyamG2508)
[![Email](https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:priyamgupta2508@gmail.com)

---
<div align="center">

**⭐ Star this repository if you found it helpful!**

Made with ❤️ by **Priyam Gupta**

</div>
