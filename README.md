Process and Ingest the daily flight data into the Redshift data warehouse fact table

# Tech Stack


### Extract:

S3
Glue Crawler

### Transform:

Glue Low Code ETL

### Load:

Redshift

### Alerting:

Event Bridge
SNS
S3 CloudTrail Notification

### Orchestration:

Step Function

# S3

Directory Structure:


Create a crawler for the S3 input file:

Run the above crawler and check the catalog table created for the S3 input file - table_name:

# Redshift

Now create the dimenstion and fact tables in redshift using the commands redshift_create_table_commands.txt

Create JDBC connection for Glue crawler to get the data catalog tables for fact and dimenstion tables present in Redshift:


# Glue Low Code ETL
