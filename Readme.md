**IMDb BI Pipeline**

This project is an end-to-end BI implementation that involves transformation of IMDb's non-commercial datasets into actionable business insights. The pipeline ingests, profiles, cleans, models, and visualizes over 200 million records using Azure Data Factory, Snowflake, and Tableau, all orchestrated under a medallion architecture. Multi-valued fields are flattened using Snowflake’s LATERAL FLATTEN, and key insights are delivered through interactive dashboards and reports.

This solution presents transformation, staging, loading, and reporting using the following tools:
## Technologies Used

<!-- Badge Row: Each badge on the same line with proper Markdown! -->
![Azure Data Factory](https://img.shields.io/badge/Azure%20Data%20Factory-0078D4?style=for-the-badge&logo=azuredatafactory&logoColor=white)
![Snowflake](https://img.shields.io/badge/Snowflake-29B5E8?style=for-the-badge&logo=snowflake&logoColor=white)
![Power BI](https://img.shields.io/badge/Power%20BI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)
![ER Studio](https://img.shields.io/badge/ER%20Studio-0071bc?style=for-the-badge)
![YData Profiling](https://img.shields.io/badge/YData%20Profiling-ffd43b?style=for-the-badge&logo=python&logoColor=white)


**Challenge** 
The IMDb dataset is extensive, unstructured, and spread across multiple files with nested or multi-valued fields. Analyzing this data directly for trends in movies, genres, cast, and crew is challenging due to inconsistencies in format and relationships between datasets

To address these challenges, the project implements:

1]Data Profiling using ydata-profiling and Alteryx to assess data quality
2]Schema Design via ER/Studio to build normalized structures
3]Data Cleaning through ADF Data Flows for data file
4]Data Flattening using LATERAL FLATTEN in Snowflake for nested fields
    Medallion Architecture:
    Bronze: raw ingestion using ADF
    Silver: transformation pipelines and flattening
    Gold: fact/dimension models with surrogate keys and derived metrics
5]Dashboards in Power BI to answer business requirements on professions, genres, titles, languages, regions, and trends

**Data Source**
Dataset was sourced from IMDb's official non-commercial repository
https://developer.imdb.com/non-commercial-datasets/

Additional Metadata:
Language codes: ISO 639 language codes
Region codes: IMDb’s official country code listings

| File Name                  | Description                                                     | Approx. Row Count |
|----------------------------|-----------------------------------------------------------------|-------------------|
| `name.basics.tsv.gz`       | Details about cast and crew members (name, professions, known titles)      | 14,195,120        |
| `title.basics.tsv.gz`      | Title data (title type, primary title, release year, runtime, genres) | 11,464,895        |
| `title.akas.tsv.gz`        | Title aliases (international titles and translations)            | 51,409,880        |
| `title.crew.tsv.gz`        | List of directors and writers associated with titles             | 11,464,885        |
| `title.episode.tsv.gz`     | Details about TV series episodes                                 | 8,815,771         |
| `title.principals.tsv.gz`  | Key cast and crew per title                                     | 90,984,102        |
| `title.ratings.tsv.gz`     | IMDb ratings and number of votes per title                      | 1,536,010         |




