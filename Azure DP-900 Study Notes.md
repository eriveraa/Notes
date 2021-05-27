# Exam DP-900: Microsoft Azure Data Fundamentals

# Study Notes

[Exam DP-900: Microsoft Azure Data Fundamentals - Learn | Microsoft Docs](https://docs.microsoft.com/en-us/learn/certifications/exams/dp-900)



## Skills measured

- The content of this exam was updated on April 23, 2021. Please download the exam skills outline below to see what changed.
- Describe core data concepts (15-20%)
- Describe how to work with relational data on Azure (25-30%)
- Describe how to work with non-relational data on Azure (25-30%)
- Describe an analytics workload on Azure (25-30%)



## Core Concepts (15-20%)

### Data Workloads

1. **Batch Data**
   Static data like CSV, JSON (row-based), XML, text files, Apache Parquet files (Column-based),  blob files, database in another location (SQL Server, Oracle, ..).

2. **Stream Data**
   Data always generating that never has a beginning and never has an end. Examples: Sensor data, Event hub, IoT Hub, Log processing, Live video (Netflix, YouTube) 



<img src="https://www.upsolver.com/wp-content/uploads/2020/05/Screen-Shot-2020-05-26-at-17.52.58.png" title="" alt="" width="479">



### Characteristics of Relational Data

- Tables

- Views

- Primary Keys

- Relationships between tables (Orders --> Order Details)

- Referential integrity

### Data Visualization

#### Too much data

- Easier and cheaper to collect data

- Hard to see trends and insights from raw numbers

- Data visualization let´s you distill thousands/millions of data into an easily digestible format.

#### Chart Types

Comparison, Change over time, Ranking, Spatial, Flow, Distribution, Correlation....

### Analytics Techniques

We got 5 types of analytics:

1. **<u>Descriptive</u>**
   
   . What happened?
   
   . Today´s sales, Service appointments booked, net margins
   
   . Existing data records together and organized, and displayed in a useful way --> Hindsight
   
   . Reports.

2. **<u>Diagnostic </u>**
   
   - Why did it happen?
   
   - Drill down into the data -> Sales per location
   
   - Comparing data against another over time, i.e. Sales per region against another region.

3. **<u>Predictive</u>**
   
   - Why will likely happen in the future?
   
   - Based on past trends and forecast
   
   - Projected sales report, azure portal predicts your bill, weather prediction

4. **<u>Prescriptive</u>**
   
   - What should I do?
   
   - Try to advise on best approach for maximum success
   
   - Google maps navigation (traffic), movie recommendations (Netflix), SEO tools

5. **<u>Cognitive</u>**
   
   - Use of Artificial intelligence and machine learning
   
   - Analyzes data to come up with a "model" of how the world works
   
   - Makes prediction based on that model and learn and improve over time
   
   - Self-driving car, understand human language, 

### ELT and ETL

- E: Extract (how to get the data)

- L: Load (getting the data into a database)

- T: Transform (apply transforms and rules on data)

### Data Processing Core Concepts

- Batch processing
  
  | Data Sources                 | Data Storage                                                 | Batch Processing                  | Analytical data store                            | Analytics and reporting    |
  | ---------------------------- | ------------------------------------------------------------ | --------------------------------- | ------------------------------------------------ | -------------------------- |
  | Data sources<br>Data storage | Blob Storage<br>Data Lake Store<br>SQL Database<br>Cosmos DB | U-SQL<br>Hive<br>Pig<br>Spark<br> | SQL Data Warehouse<br>Spark SQL<br>HBase<br>Hive | Analytics, Power BI, Excel |

- Stream processing
  
  | Data Sources                 | Ingestion                       | Stream Processing                            | Analytical data store                            | Analytics and reporting    |
  | ---------------------------- | ------------------------------- | -------------------------------------------- | ------------------------------------------------ | -------------------------- |
  | Data sources<br>Data storage | Event Hubs<br>IOT Hub<br> Kafka | Stream analytics<br>Storm<br>Spark Streaming | SQL Data Warehouse<br>Spark SQL<br>HBase<br>Hive | Analytics, Power BI, Excel |

## 

## Relational Data (25-30%)

### Relational DB Services in Azure:

- <u>**SQL Server in a VM**</u>
  
  - IaaS offering
  
  - SQL Server in a Virtual Machine Linux or Windows
  
  - SQL Server 2008, 2012, 2016 are available for Windows, and 2017 and 2019 are available for Windows or Linux
  
  - Tiers - Express, Developer, Web, Standard, Enterprise
  
  - 100% Compatibility with SQL Server on premises
  
  - You manage everything: OS updates, software, backups, replication
  
  - Push maximum performance
  
  - No limitations
  
  - Pay for the server and licensing, not per DB

- **<u>SQL Managed Instance</u>**
  
  - Fully managed (you are not managing hardware, OS, bug-fixes)
  
  - Close to 100% compatibility to SQL Server on premises
  
  - You choose: vCores (4 to 80), memory, storage
  
  - 32GB to 8TB storage

- **<u>Azure SQL Database</u>**
  
  - Fully managed
  
  - Close to 98% compatibility to SQL Server on premises - uses SQL Server engine underneath
  
  - Lots of options for provisioned and serverless databases - designed to work in the cloud
  
  - Easy to grow to larger plans as your needs grow, additional tools like advisors
  
  - Pay for performance or pay for hardware
  
  - You choose: vCores (2 to 80), memory, storage
  
  - 5GB to 4TB storage
  
  - Starting at $5 per month
  
  - **Types of databases**
    
    - Single Database: allocate resources to a specific database (# of cpus, memory)
    
    - Elastic Database: allocate shared resources (cpu, memory) to a group/pool of databases

- **<u>Azure Database for MySQL, PostgreSQL or MariaDB</u>**
  
  - Managed versions of MySQL, PostgreSQL and MariaDB
  
  - Community versions
  
  - Fully managed
  
  - Compatible with your legacy systems and support migration of existing solutions

- **<u>Azure Synapse Analytics (SQL DW)</u>**
  
  - Used to be called SQL Data Warehouse
  
  - Serverless on-demand or provisioned
  
  - Database designed for store and query large amounts of data and reporting / analytics

### Relational Data Structures

#### How is data stored?

- Relational data is stored in "tables"

- Tables have rows and columns

- Like an "excel" spreadsheet

- Columns of a table define an schema

#### Tables

- They are intended to store a single "type" of data: Employees, Orders, Products.

- Best practice is for every table to have a PK (primary key), also called index.

- Have fields, primary keys, foreign keys, unique fields/keys

#### Indexes

- Used to improve the performance of queries

- The PK is by default an index

- The data of the table is physically stored by PK sorted order

- You can define other indexes if it´s common to query on them

#### Views

- A view is like a table - you can a query on it

- The data it returns is from another table

- It can be a simplified view of a table or a more complex one

### Relational Query Tools

- Query Editor (Portal)
  
  - Built into the Azure portal
  
  - Access from the SQL Database module
  
  - Execute queries

- Azure Data Studio
  
  - Cross-platform software to work with SQL Server relational data (Windows, Mac, Linux)
  
  - Can connect to local SQL Server of Azure SQL Database
  
  - Intellisense, code snippets, source control, integrated terminal
  
  - Charting of query results
  
  - Not for managing databases
  
  - Open source, free

- SQL Server Management Studio (SSMS)
  
  - Classic tool and with full set of features (you can do anything)
  
  - Support any kind of queries
  
  - Enterprise grade SQL Server management
  
  - Supports database administration tasks (user management, performance tuning, import/export)

- sqlcmd
  
  - Command line utility
  
  - Execute T-SQL statements, stored procedures and scripts
  
  - Windows and Linux options. MacOS in preview
  
  - Can run in a docker container

- Columns of a table define an schema

### Structured Query Language (SQL)

- DDL (Data Definition Language)
  
  - Data management SQL commands around database structures
  
  - CREATE, ALTER, DROP, TRUNCATE, COMMENT, RENAME

- DML (Data Manipulation Language)
  
  - SQL commands around data manipulation
  
  - SELECT, INSERT, UPDATE, DELETE, LOCK TABLE

- DCL (Data Control Language)
  
  - Granting rigths and permissions to others
  
  - GRAND, REVOKE

- SQL (Structured Query Language)
  
  - Developed in the early 1970s
  
  - SQL Standard first formalized in 1986 as SQL-86, now up to SQL:2019

- Vendors
  
  - Each database engine has its own version of SQL that extends the standard for its own purpose.
  
  - Most vendors are not 100% compatible with the standard
  
  - SQL Server uses T-SQL, Oracle uses PL/SQL, MySQL uses SQL/PSM, PostgreSQL uses PL/pgSQL





## Non-Relational Database Concepts (25-30%)

### What is Non-Relational Database?

- Is any database that is not based on tables, rows and columns

- Often, the way the data is stored better supports the application´s use



### Non-Relational Data Types

- Document or JSON document
  
  - Javascript object notation

- Column-Family Data
  
  - Similar to table structure but it stores the ID field and another field for nested data 
  
  - It is like a nested tables system
  
  - Used in Cassandra database (invented by Facebook)

- Key-Value Data
  
  - Used for cache / Redis and similar to a hash-table
  
  - Not mean to be searchable
  
  - This is how Azure table storage works

- Graph Data
  
  - Graph database deals with nodes and relationships

- Time Series Data
  
  - Data is really optimized around timestamps (like IOT data)

- Object Data / File storage / Blob storage
  
  - Has a path, blob and metadata fields

- Azure Search document
  
  - Has an ID, and search-document (json) field
  
  - Searching natural language recognition, query scoring, point system relevance



### Choose a Database

- Benefits of Relational Database
  
  - Normalization
  
  - Data relationships, data integrity, constraints and fixed schema
  
  - Established products  for decades
  
  - BI tools like Power BI

- Benefits of NoSQL Databases
  
  - Optimized for specific data types
  
  - Can be designed for performance at internet scales
  
  - Might not require massive hardware, reduced expense
  
  - Open Source



### Non-Relational DB Services in Azure:

- Cosmos DB
  
  - Enterprise-grade non-relational database
  
  - Supports many data models: graph, document, table, column-family
  
  - Compatible with established APIs (Cassandra, MongoDB, Gremlin, etc)
  
  - Select the data consistency you need
  
  - Easy to scale worldwide
  
  - Sub-10ms latency
  
  - SLA for throughput, latency, availability and consistency

- Table Storage
  
  - Azure Storage account
  
  - 5PB maximum limit
  
  - $0.045 per GB - cheapest data storage option in Azure
  
  - Plus pay for operations
  
  - SLA shockingly poor (10 seconds for a query)

- Blob Storage
  
  - Azure Storage account
  
  - 5 PB maximum limit
  
  - $0.0208 per GB - cheapest data storage option
  
  - Supports premium, hot, cool, archive access tiers
  
  - Supports "reserved capacity"
  
  - Supports blob index
  
  - Plus pay for operations
  
  - SLA shockingly poor (2 seconds per MB)

- File Storage
  
  - Azure Storage account
  
  - 5 PB maximum limit
  
  - $0.06 per GB - cheapest data storage option
  
  - Supports standard and premium options
  
  - SLA shockingly poor (2 seconds per MB)



### Managing Non-Relational Databases:

- Creation Azure Cosmos Account (Provisioning)
  
  - Can create a maximum of 50 Azure Cosmos accounts under an Azure Subscription
  
  - Choose Azure Cosmos DB Account in Azure Portal
  
  - Requires a Subscription, Resource Group and Storage Account first
  
  - Requires a Instance Details: Account Name (Server), an API (Core SQL) and Location (region)
  
  -  Available APIS / Database Model (choose one)
    
    - Core SQL: documentDB (JSON data)
    
    - Azure Cosmos DB for MongoDB API
    
    - Cassandra
    
    - Azure Table
    
    - Gremlin (graph)
  
  - Can´t have multiple database models in the same DB Account.
  
  - Choose Account Type: Production / Non-Production
  
  - Choose Geo-Redundancy
  
  - Choose Multi-Region Writes
  
  - Choose Networking / Connectivity method
    
    - All networks
    
    - Public endpoint
    
    - Private endpoint
  
  - Encrypted by default (Service-managed key)
  
  - Specify tags required
  
  <img src="https://docs.microsoft.com/en-us/azure/includes/media/cosmos-db-create-dbaccount/azure-cosmos-db-create-new-account-detail.png" title="" alt="The new account page for Azure Cosmos DB" width="590">

- Query Cosmos DB
  
  - DB Account -> Database -> Container (table/collection/graph) -> Items
    
    <img src="https://docs.microsoft.com/en-us/azure/cosmos-db/media/account-databases-containers-items/hierarchy.png" title="" alt="Hierarchy of an Azure Cosmos account" width="227">
    
    <img title="" src="https://docs.microsoft.com/en-us/azure/cosmos-db/media/account-databases-containers-items/cosmos-entities.png" alt="Azure Cosmos account entities" width="692">
  
  - Compatible wi
