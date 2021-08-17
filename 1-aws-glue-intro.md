### AWS Glue Basics

- AWS Glue is a system for building table definitions and performing ETL (Extract, Transform and Load)

- Data preparation is "the first mile" for doing data analytics, Business Intelligence or Machine Learning Operations. Data prep is hard for 3 reasons: - There is lots of data, - "Our" data needs customization or (brittle) hand coded scripts - and many companies are managing their own infrastructure, managing, sizing VM's and managing their lifecycle.

- Glue uses the serverless execution model, thus you don't have to manage any servers. Or pay for idle up time.

- AWS Glue is a serverless system that will find and define table definitions and schema. (Meaning, it will look at you data and learn what data type and shape it is in.)

- After defining the data and schema it will use that info and become the metadata repository for your S3 datalake.

- It can also define data located in RDS,  Redshift and most SQL databases.

### AWS Glue Components

- 1. Serverless ETL engine based on Apache Spark - that comes with an interactive UI in which you can auto generate ETL-code

- 2. AWS Glue Data Catalog - a centralized metadata store that is fully Apache Hive compatible.

- 3. AWS Crawlers that automatically scan S3 buckets, databases, Redshift and more to load the schema and data into the metadata catalog.

- 4. Workflow Management tools to create complex workflows, crawlers triggers and jobs   

### The purpose of AWS Glue is to extract structure from unstructured data

- Providing you this structure give you the ability to query the data using SQL or SQLite tools.

### AWS Glue also provides for custom ETL jobs

-These ETL jobs use serverless, fully managed Apache Spark - this is great because you don't have to manage the Spark Cluster.
