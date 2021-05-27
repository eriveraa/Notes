# Exam DP-900: Microsoft Azure Data Fundamentals

# Study Notes

[Exam DP-900: Microsoft Azure Data Fundamentals - Learn | Microsoft Docs](https://docs.microsoft.com/en-us/learn/certifications/exams/dp-900)



**Scott Duffy Udemy Course - DP-900 Azure Data Fundamentals Exam Prep In One Day**

[DP-900 Azure Data Fundamentals Exam Prep In One Day | Udemy](https://www.udemy.com/course/dp900-azure/?couponCode=MAY2021)

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



<img title="" src="https://www.upsolver.com/wp-content/uploads/2020/05/Screen-Shot-2020-05-26-at-17.52.58.png" alt="" width="404">



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
  
  - By default, you don´t have public access. It requires the firewall configured to allow anyone.
  
  - Supports DTUs and vCore purchasing models
  
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
  
  - Not mean to be searchable (difficult to filter and sort on non-key data)
  
  - This is how **Azure Tables** storage works
    
    <img title="" src="https://docs.microsoft.com/en-us/learn/wwl-data-ai/explore-non-relational-data-offerings-azure/media/2-row-structure.png" alt="Image showing the structure of rows in Azure Table Storage" width="296">
    
    

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
  
  - Requires an Azure Storage account
  
  - Its a key-value storage and semi-structured data, flexible data schema, JSON serialized
  
  - Now part of Azure Cosmos DB (api)
  
  - 5PB maximum limit
  
  - $0.045 per GB - cheapest data storage option in Azure
  
  - Plus pay for operations (*We charge $0.00036 per 10,000 transactions for tables. Any type of operation against the storage is counted as a transaction, including reads, writes, and deletes*.)
  
  - Can have many tables (similar to a relational database)
  
  - SLA shockingly poor (10 seconds for a query)
    
    <img src="https://docs.microsoft.com/en-us/learn/wwl-data-ai/explore-non-relational-data-offerings-azure/media/2-row-structure.png" title="" alt="Image showing the structure of rows in Azure Table Storage" width="261">
    
    ![Image of the Overview page for the storage account in the Azure portal. The user has selected Tables](https://docs.microsoft.com/en-us/learn/wwl-data-ai/explore-non-relational-data-offerings-azure/media/2-tables.png)

- Blob Storage
  
  - Requires Azure Storage account
    
    ![Diagram showing the relationship between a storage account, containers, and blobs](https://docs.microsoft.com/en-us/azure/storage/blobs/media/storage-blobs-introduction/blob1.png)
  
  - 5 PB maximum limit
  
  - $0.0208 per GB - cheapest data storage option
  
  - Allows to serve images, documents, video, audio, and any kind of file
  
  - Supports premium, hot, cool, archive access tiers
  
  - Supports "reserved capacity"
  
  - Supports blob index
  
  - Container organizes a set of blobs (similar to a directory in a file system)
  
  - Plus pay for operations
  
  - Is the **<u>absolute cheapest way </u>**to store data in Azure.
  
  - SLA shockingly poor (2 seconds per MB)

- File Storage
  
  - Requires Azure Storage account
    
    <img src="https://docs.microsoft.com/en-us/learn/wwl-data-ai/explore-non-relational-data-offerings-azure/media/4-file-shares.png" title="" alt="Image showing the relationships between a storage account, file shares, applications using the file shares, and Azure Active Directory Domain Services" width="375">
  
  - 5 PB maximum limit
  
  - File shares on Azure Storage Account
  
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
    
    - Core SQL Api: documentDB (JSON data). For new applications use this one.
    
    - MongoDB API
    
    - Cassandra Api
    
    - Azure Table API
    
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
  
  <img title="" src="https://docs.microsoft.com/en-us/azure/includes/media/cosmos-db-create-dbaccount/azure-cosmos-db-create-new-account-detail.png" alt="The new account page for Azure Cosmos DB" width="720">

- Query Cosmos DB
  
  - DB Account -> Database -> Container (table/collection/graph) -> Items
    
    ![CosmosTech_3](https://azurecomcdn.azureedge.net/mediahandler/acomblog/media/Default/blog/8d036cf9-df49-45d3-b540-00f18c4f5c31.png)
    
    <img src="https://novacontext.com/images/d/d52d335706b7fe2b07676693368945e4.jpg" title="" alt="Introduction to NoSQL in Cosmos DB" width="473">
  
  - Horizontal Partitioning
    
    <img title="" src="https://www.dotnetcurry.com/images/azure/cosmos-db/logical-parition-by-partition-key.png" alt="Azure Cosmos DB - Deep Dive | DotNetCurry" width="514">

- Use ARM Templates to manage Cosmos DB (Infrastructure as Code)
  
  - In Resource Group / Deployments, you can see the Deployment of the Cosmos DB
    
    - Can see the Cosmos DB Account deployment template and database provisioned
  
  - In Azure Cosmos DB account
    
    - Select Export template to see all Db templates generated (database, containers, etc.)

- Cosmos DB Security
  
  - Cosmos DB Keys <u>(Access Keys) </u>for Read and Write. You can regenerate them if compromised.

- Cosmos DB Geo-Replication
  
  - Can create many Read Regions by just clicking on map. It will replicate the DB in those regions and keep them in sync with the Write Database.
  
  - Every replicated database costs!!!
  
  - Can also have multi-region writes
  
  - Big powerful advantage for going GLOBAL!

- 



## Data Analytics (25-30%)

### Analytics Workloads

- **OLTP - Online Transaction Processing**
  
  - (As a place to store business transactions as they occur)
  
  - That´s your data, the database that is behind your business system.
  
  - Captures the interaction / transactions of the business
  
  - Is the backend database of your systems
  
  - Existing rows can be updated
  
  - Data can be retrieved by SQL queries
  
  - Optimized for general use
  
  - Traits / Attributes
    
    - Database normalization, schema enforced, data integrity
    
    - Heavy writes, moderate reads, updateable
    
    - Data size MBs to TBs
  
  - Azure OLTP:
    
    - Azure SQL Database, SQL Instance, SQL Server in a VM
    
    - Azure Database for MySQL / PostgreSQL

- **OLAP - Online Analytics Processing**
  
  - (As a place to hold data for complex analysis)
  
  - Pre-process your data so you can run some deep insights into it
  
  - Motivations
    
    - Data stored in transactional db can change at any time, and was not designed for complex analysis
    
    - Running complex reports can slow down a transactional database
    
    - Take time to prepare data for analysis
  
  - Traits / Attributes
    
    - No locking and no updates
    
    - Heavy reads, read-only
    
    - Multi-dimensional indexing
    
    - Data size GBs
  
  - Azure OLAP
    
    - SQL Server with Columnstore indexes
    
    - Azure Analysis Services
    
    - SQL Server Analysis Services
    
    - 

- **Data Warehouse**
  
  - (As a centralized repository for data from different sources - data warehouse)
  
  - Collects data from multiple sources and put it one database you can run reports against it
  
  - Current and historical data used for reporting and global analysis
  
  - Can rename or reformat columns to make it easier for users to create reports
  
  - Users can run reports without affecting day to day business data systems
  
  - Azure Data Warehousing
    
    - Symmetric Multiprocessing (SMP)
      
      - Azure SQL Database
      
      - SQL Server in a VM
    
    - Massively Parallel Processing (MPP)
      
      - Azure Synapse Analytics (SQL DW)
      
      - Apache Hive on HDInsight
      
      - Interactive Query (Hive LLAP) on HDInsight

- **Modern Data Warehouse**
  
  <img src="https://docs.microsoft.com/en-us/azure/architecture/solution-ideas/media/modern-data-warehouse.png" title="" alt="Modern Data Warehouse with Azure – cuteprogramming" width="560">
  
  - **Data sources**
    
    - All data comes from somewhere else
    
    - One or more data sources, **structured **(databases) or **unstructured **(csv, json, logs)
  
  - **INGEST**
    
    - **Azure Data Factory**: Hybrid data integration service that allows to create, schedule and orchestrate ETL/ELT workflows
      
      <img src="https://docs.microsoft.com/en-us/learn/wwl-data-ai/examine-components-of-modern-data-warehouse/media/3-data-factory.png" title="" alt="Screenshot of the Azure Data Factory design window, showing an example pipeline" width="502">
    
    - Moves the data from outside of Azure to inside of Azure
      
      <img src="https://docs.microsoft.com/en-us/learn/wwl-data-ai/examine-components-of-modern-data-warehouse/media/3-data-lake.png" title="" alt="Graphic showing data ingested by Azure Data Factory being sent to Azure Data Lake" width="394">
  
  - **STORE**
    
    - **Azure Blob Storage**: massively scalable object storage for any type of unstructured data
    
    - **Azure Data Lake**: type of blob storage designed to handle even larger amounts of data. 
    
    - Unprocessed data is stored here
  
  - **PREP AND TRAIN**
    
    - **Azure Databricks**: fast, easy and collaborative Apache Spark-based analytics platform.
    
    - Databricks allows you to manipulate data at large scales (big data, streaming and machine learning). It takes data from Azure Data Lake, modify/process and store it in another data source like Azure Synapse Analytics.
      
      <img src="https://docs.microsoft.com/es-es/azure/databricks/scenarios/media/what-is-azure-databricks/azure-databricks-overview.png" title="" alt="¿Qué es Azure Databricks?" width="464">
  
  - **MODEL AND SERVE**
    
    - **Azure Synapse Analytics**: fast, flexible and trusted cloud data warehouse that lets you scale, compute, and store elastically and independently, with a massive parallel processing architecture. <u>Data is optimized for read-only queries</u>. It´s a data warehouse.
    
    - **Azure Analysis Services**: an enterprise grade analytics as a service that lets you govern, deploy, test and deliver your BI solution. Data is optimized for complex queries with cubes and dimensions.
    
    - **Power BI**: a suite of BI tools that make easier for users to look at data, analyze it, and create reports / dashboards.
      
      - Can publish those reports to the organization and consume on the web or mobile devices.





### Data ingestion and processing on Azure

#### Data Engineer (What this exam is all about)

Azure data engineers are responsible for data-related implementation tasks that include:

- provisioning data storage services,

- ingesting streaming and batch data,

- transforming data,

- implementing security and data-retention policies,

- identifying performance bottlenecks and accessing external data sources



#### Azure Data Factory

<img title="" src="https://i2.wp.com/www.jamesserra.com/wp-content/uploads/2018/12/dataflows.png?w=949&ssl=1" alt="Azure Data Factory Data Flow | LaptrinhX" width="526">

- Brings data from external sources ==> apply transformations ==> send to end data store

- Similar to SQL Server Integration Services (SSIS)

- Features
  
  - Orchestration platform - data workflows from A to B
  
  - Data transformation
  
  - Create and schedule jobs
  
  - Cloud version of SSIS 
  
  - Supports existing SSIS packages

- Activities (actions to perform on data)
  
  - Data movement
  
  - Data transformation
  
  - control

- Pipelines
  
  - A logical grouping of activities to perform some task.
  
  - A data factory can contain multiple pipelines
  
  - Can perform their tasks sequentially or in parallel.
  
  - Pipeline Run (instance of a pipeline execution)
  
  - Can be run manually or started using a trigger
  
  - Trigger (event that causes a pipeline to run)
    
    - Scheduled trigger
    
    - Tumbling window
      
      - You set it up to run at a predetermined interval
      
      - Can be set to run "in the past"
      
      - Good for when the pipeline is designed to process data by the time period specified.
      
      - Non-overlapping
    
    - Event-based



### Data Visualization

This is how you view the data within your databases / reporting function

#### Types of Reports

- **Paginated Reports**
  
  - Designed to be printed and shared
  
  - Formatted to fit well on page
  
  - Contains all the data, even if it spans multiple pages: Invoice, Sales details report, etc.
  
  - **PowerBI Report Builder** creates paginated reports. (Standalone tool separated from Power BI)
  
  - Reports get published to **Power BI Service**.

- **Interactive Reports**
  
  - Reports designed to be viewed on screen
  
  - Can click for more details, drill-down on the data ---- "interactive" / "hover" logic
  
  - Very visual, not a dump of data rows
  
  - Can change design / layout based on user action
  
  - Use one or many charts
  
  - Served by Power BI Server (installed on-premises) and part of Power Bi Premium

- **Dashboards**
  
  - Typically a mixture of chart types on a single page
  
  - All the relevant data, at a glance
  
  - Can go to individual reports
  
  - Helps identify anomalies visually

#### Power BI Content Workflow

Typical workflow in Power BI

- Connect to the data source

- Pull what you need into in-memory data model

- Edit, transform the data as you require

- Build reports using **<u>Power BI Desktop</u>**

- Share the report












































