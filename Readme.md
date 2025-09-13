**IMDb BI Pipeline**

This project is an end-to-end BI implementation that involves transformation of IMDb's non-commercial datasets into actionable business insights. The pipeline ingests, profiles, cleans, models, and visualizes over 200 million records using Azure Data Factory, Snowflake, and Tableau, all orchestrated under a medallion architecture. Multi-valued fields are flattened using Snowflake’s LATERAL FLATTEN, and key insights are delivered through interactive dashboards and reports.

This solution presents transformation, staging, loading, and reporting using the following tools:
## Technologies Used

![Azure Data Factory](https://img.shields.io/badge/Azure%20Data%20Factory-0078D4?style=for-the-badge&logo=azuredatafactory&logoColor=white)
![Snowflake](https://img.shields.io/badge/Snowflake-29B5E8?style=for-the-badge&logo=snowflake&logoColor=white)
![Tableau](https://img.shields.io/badge/Tableau-E97627?style=for-the-badge&logo=tableau&logoColor=white)
![ER Studio](https://img.shields.io/badge/ER%20Studio-0071bc?style=for-the-badge)
![Python](https://img.shields.io/badge/Python-FFD43B?style=for-the-badge&logo=python&logoColor=blue)
![YData Profiling](https://img.shields.io/badge/YData%20Profiling-ffd43b?style=for-the-badge&logo=python&logoColor=white)

• ER Studio - Data Modeling
• Azure ADF - ETL & Data Pipeline Automation
• Alteryx/Python - Data Profiling & Cleaning
• Snowflake - Data Warehouse
• Power BI - Data Visualization

**Challenge** 
The IMDb dataset is extensive, unstructured, and spread across multiple files with nested or multi-valued fields. Analyzing this data directly for trends in movies, genres, cast, and crew is challenging due to inconsistencies in format and relationships between datasets.


