# Data-Engineering-and-Analysis-on-Brazilian-E-Commerce-dataset

Project Objectives:

1. Uncover e-commerce data for impactful consumer behavior patterns.
2. Examine customer data to enhance satisfaction with Brazilian E-Commerce enterprises.
3. Evaluate annual business trajectory for progression or potential downturns.
4. Explore economic patterns across diverse Brazilian regions for localized strategies.
5. Understand product demand through reviews and geolocation for targeted marketing.

Data Architecture Diagram:

<img width="617" alt="image" src="https://github.com/AnushkaDarade/Data-Engineering-and-Analysis-on-Brazilian-E-Commerce-dataset/assets/114367423/94b782b6-5a5c-4ba0-a446-68638a443056">


Implementation Description:

An overview of the implementation procedure is as follows:

1. Upon conducting Data Profiling for the Brazilian E-commerce dataset, we observed and addressed issues such as missing values, inconsistent data, and ensured alignment of data types with respect to the data dictionary. Initially, we created a data dictionary specific to the Brazilian E-commerce dataset, outlining column names and corresponding data types.

2. The files from the blob storage are imported into Azure Data Factory in the Dataset section for the Azure Cosmos Document DB implementation. The files are cleansed, integrated, transformed, aggregated as per required hierarchy and nesting and finally, sink it into the destination Azure Cosmos Document DB.
   
3. The first step in implementing Azure Graph DB is to utilize Azure Data Factory to merge the various.csv files needed for the graph implementation into a single file. We created a Python connection to our Azure Blob Storage, which is where the combined file is stored, so that it can be retrieved immediately. Next, using the Gremlin API, created a Python connection to the Azure Cosmos Graph Database. After the connection was made, we used the Gremlin API to generate the vertices and edges and ingested data into Azure Cosmos Graph DB.
