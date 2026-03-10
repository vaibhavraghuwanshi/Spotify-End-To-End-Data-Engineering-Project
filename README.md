# Spotify-End-To-End-Data-Engineering-Project

### Introduction
In this project, we will build an ETL pipeline using the Spotify API on AWS. The pipeline will retrieve data from the Spotify API, transform it into the desired format and load it into AWS Data Store.

### Architecture Diagram
<img width="1536" height="1024" alt="Architecture" src="https://github.com/user-attachments/assets/76675200-aa7b-4342-86f3-1766d89f88a1" />

### About Dataset/ API
This API contains information about music artist, albums and songs [Spotify API](https://developer.spotify.com/documentation/web-api)

### Components Used
1. Spotify API → Data source
2. Python → API calls
3. Amazon CloudWatch → Scheduled trigger
4. AWS Lambda → Extraction & transformation
5. Amazon S3 → Raw & processed storage
6. AWS Glue → Schema inference
7. AWS Glue Data Catalog → Table metadata
8. Amazon Athena → Query data

### Install Packages
```
pip install pandas
pip install numpy
pip install spotipy
```
### Project Execution Flow
Extract Data from API -> Lambda Trigger every 1 hour -> Run Extract code -> Store Raw Data -> Trigger Trasform function -> Transform Data and Load it -> Query using Athena
