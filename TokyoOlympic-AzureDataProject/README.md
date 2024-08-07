This project uses Azure Data Factory to extract Tokyo Olympics data from an API and load it onto Azure Data Lake. Spark code is used for transformation in Azure Databricks and Synapse Analytics for analysis. 

This project is about building an end-to-end data engineering project on Azure Cloud
- Extract data from API using Azure Data Factory
- Write Spark code to transform the data and load it back onto Azure Data Lake Storage
- Use Synapse Analytics to run SQL queries on the transformed data for insights and visualization

The data set contains information about 11,000 athletes, 47 disciplines, and 743 teams participating in the Tokyo Olympics 2021.
- The data set is available on Google and in CSV format for better data processing.
- The data set includes information about athletes, coaches, gender, medals, and teams.

Extract and load data from GitHub to Azure Data Lake storage using Azure Data Factory.
- Set up a link service to establish a connection between the data source (GitHub) and Azure Data Factory
- Specify the file format and give a logical name to the property
- Create a link service to establish a connection between Azure Data Factory and Azure Data Lake storage
- Specify the target location and file path to store the data
- Validate the settings and run the pipeline to copy the file from GitHub to Azure Data Lake storage
- Verify that the file is successfully copied to the storage account

Data from GitHub is stored using Azure Data Factory
- Simple copy activity is used to load the data to a storage account
- The process involves data integration, transformation, and syncing with different files

Create a connection between Azure Databricks and Azure Data Lake Storage
- Mount Azure Data Lake Storage to the Data Factory
- Obtain client ID, tenant ID, and secret ID
- Create the configuration format for authentication
- Configure the mounting point with the source container and folder name

Successfully created connection to Azure data Factory and mounted data Lake.
- We need to give permissions to access the data stored in the data Lake.
- To give permissions, go to storage container settings and add role assignment for the app.
- Wait for a few minutes and the app will have access to the data.
- Mounting the entire data Lake to a location is successful.
- Reading a file from the mounted location is possible.
- When writing Spark code, a spark session needs to be created, but it is already assigned on Databricks.
- Column names and data types need to be properly handled when reading files.
- The print schema function can be used to check the data frame structure.

Data transformation using Apache Spark and writing data onto target location
- Apache Spark provides various functions for data transformation
- Documentation provides details of each transformation function
- The transformed data can be written to target location
- Multiple options available for writing data, including CSV format
- Data can be partitioned while writing to multiple files

Utilize Azure Synapse Analytics to generate insights from transformed data using SQL queries.
