# Data Warehouse Concepts in Modern Data Architecture

## Big Data
- Volume, velocity, variety and veracity of data that exceeds traditional data processing capabilities
- Requires distributed processing and storage systems
- Examples: IoT sensor data, web logs, social media feeds
- **Explanation**: Big Data refers to datasets that are so large or complex that traditional data processing applications are inadequate. It encompasses the challenges of storing, processing, and analyzing vast amounts of data.

## OLTP vs OLAP
### Online Transaction Processing (OLTP)
- Handles day-to-day transactions
- Optimized for quick updates and inserts
- Examples: Order processing, banking transactions
- Row-oriented storage

### Online Analytical Processing (OLAP) 
- Used for complex analysis and reporting
- Optimized for read operations and aggregations
- Examples: Sales analysis, forecasting
- Column-oriented storage
- **Explanation**: OLTP systems are designed for managing transaction-oriented applications, while OLAP systems are optimized for querying and reporting, allowing for complex calculations and data analysis.

## Data Warehouse (DWH)
- Central repository for integrated data from multiple sources
- Optimized for analytics and reporting
- Contains historical and current data
- Implements dimensional modeling
- **Explanation**: A Data Warehouse is a system used for reporting and data analysis, serving as a central repository of integrated data from various sources, structured for query and analysis.

## Data Lake
- Storage repository that holds raw data in native format
- Supports structured, semi-structured and unstructured data
- Highly scalable and cost effective
- Enables schema-on-read approach
- **Explanation**: A Data Lake allows for the storage of vast amounts of raw data in its native format until it is needed for analysis, providing flexibility in data management.

## Delta Lake
- Open source storage layer that brings ACID transactions to data lakes
- Provides versioning and time travel capabilities
- Supports batch and streaming data
- Enables lakehouse architecture
- **Explanation**: Delta Lake enhances data lakes by adding ACID transaction capabilities, allowing for reliable data management and enabling features like time travel for data versioning.

## Data Models

### Star Schema
Pros:
- Simple to understand and query
- Good query performance
- Widely supported by BI tools

Cons:
- Data redundancy
- Less flexible for complex relationships

Use cases:
- Sales analysis
- Financial reporting
- **Explanation**: The Star Schema is a type of database schema that is optimized for data warehousing and business intelligence, characterized by a central fact table connected to dimension tables.

### Snowflake Schema
Pros:
- Reduces data redundancy
- Better data integrity
- More flexible for complex relationships

Cons:
- More complex queries
- Slower query performance
- More joins required

Use cases:
- Complex business domains
- Highly normalized data requirements
- **Explanation**: The Snowflake Schema is a more complex version of the Star Schema, where dimension tables are normalized into multiple related tables, which can improve data integrity but may complicate queries.

## ETL vs ELT

### Extract, Transform, Load (ETL)
- Traditional approach
- Transforms data before loading to target
- Better for smaller datasets
- Used with data warehouses

### Extract, Load, Transform (ELT)
- Modern approach
- Loads raw data first, transforms as needed
- Better for large datasets
- Used with data lakes
- More flexible and scalable
- **Explanation**: ETL is a traditional data integration process that transforms data before loading it into a data warehouse, while ELT allows for raw data to be loaded first and transformed later, making it more suitable for big data environments.
