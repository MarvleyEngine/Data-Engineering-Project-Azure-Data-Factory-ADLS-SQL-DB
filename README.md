# Project-Azure-Data-Factory-ADLS-SQL-DB
This repository contains a complete data engineering workflow built on Azure. The project demonstrates how raw hospital data is ingested, transformed, and delivered as analytics-ready datasets for reporting.

The goal is to simulate a real-world pipeline where data flows from external sources into a cloud-based architecture and is transformed into meaningful insights.

Project Architecture
<img width="1301" height="605" alt="image" src="https://github.com/user-attachments/assets/c6aa55c8-2edc-43d4-bfc9-fa2ec67171dd" />

The pipeline is built using a layered approach:

Data Source Layer
Raw CSV files are stored externally (GitHub in this case).
Ingestion Layer
Azure Data Factory pipelines pull data into the raw container in Azure Data Lake Storage Gen2.
Transformation Layer
Data Flows are used to clean, validate, and transform the raw datasets.
Storage Layer
Transformed data is written into the processed container in ADLS Gen2.
Serving Layer
Cleaned data is loaded into Azure SQL Database tables.
Visualization Layer
Power BI connects to Azure SQL Database to build dashboards and reports.
Tech Stack
Azure Data Factory – Pipeline orchestration & ingestion
Azure Data Flows – Data transformation logic
Azure Data Lake Storage Gen2 – Data storage (raw & processed layers)
Azure SQL Database – Structured data storage
Power BI – Data visualization



Datasets Used

Patients (patients.csv): Contains patient demographic details such as ID, birth date, gender, and address.


Payers (payers.csv): Includes insurance provider information and coverage details.


Encounters (encounters.csv): Tracks hospital visits, including timestamps, encounter types, and costs.


Procedures (procedures.csv) Captures medical procedures linked to each encounter.



Key Features
Automated ingestion pipeline using Azure Data Factory
Data transformation using Data Flows (no-code / low-code approach)
Layered data lake design (raw → processed)
Integration with Azure SQL Database for querying
Interactive dashboards built in Power BI
How to Run This Project
Upload datasets to your source location (e.g., GitHub or Blob Storage)
Set up Azure Data Lake Storage (create raw & processed containers)
Deploy Azure Data Factory and create linked services
Import or recreate pipelines and data flows
Run ingestion pipeline
Run transformation pipeline
Load processed data into Azure SQL Database
Connect Power BI to visualize results


Sample Outputs
<img width="1685" height="907" alt="image" src="https://github.com/user-attachments/assets/9a5513ee-f88b-4c63-bcc3-15ef6230abd2" />
<img width="1702" height="862" alt="image" src="https://github.com/user-attachments/assets/627fb04a-6478-4aac-a85c-2de60291c5de" />
<img width="1697" height="862" alt="image" src="https://github.com/user-attachments/assets/efe7440b-41f3-4d18-ba02-06cf05acde98" />
<img width="1691" height="917" alt="image" src="https://github.com/user-attachments/assets/f9633b9f-f9f1-4026-9209-518d5016cf2f" />
<img width="1715" height="910" alt="image" src="https://github.com/user-attachments/assets/6ad95db4-3817-4c8f-ae3b-5b9018a8bb0e" />
<img width="1843" height="1006" alt="image" src="https://github.com/user-attachments/assets/583fe94e-55e8-4a71-b1fc-3f9ac27ec1c3" />


Data Factory pipeline run results

Data Flow transformations

SQL tables with cleaned data

Power BI dashboard


What I Learned
Building end-to-end pipelines in Azure
Designing layered data architectures
Handling real-world data transformation challenges
Integrating multiple Azure services into one workflow


By the end of this project, the pipeline delivers:
Clean, structured data stored in a relational database
Automated data workflows using Azure Data Factory
Business-ready dashboards in Power BI for insights and reporting
