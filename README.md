# Simple ETL Pipeline Project

## Overview

This project is to demonstrate ETL pipelining using only python and pandas. The datasets, sourced from Kaggle, consist of multiple CSV files that are cleaned, transformed, and merged into a single CSV file using Python and the pandas library. The resulting dataset is structured and ready for further analysis.

## Technology Used
- **Python**
- **Pandas**
- **Shell Script**

## Feature
- **Multiple Data Extraction**
- **Data Transformation from wide to long format**
- **Dynamic Configuration of path and data sources**
- **Scalable merge algorithm**
- **System Process Logger**

## Contents
- **Task Description**: Details of the ETL process and goals.
- **Data Extraction Process**: Available in the [Jupyter Notebook](https://github.com/ramadhantaAkmal/etl-pipeline-capstone-project/blob/main/Extraction.ipynb).
- **Data Transformation Process**: Available in the [Jupyter Notebook](https://github.com/ramadhantaAkmal/etl-pipeline-capstone-project/blob/main/Transformation.ipynb).
- **Summary**: Key findings and outcomes.

## Task Description

This project demonstrates the creation of an ETL pipeline to process multiple CSV datasets from Kaggle. Using Python and pandas, the data is cleaned, transformed, and consolidated into a single analysis-ready CSV file. All of the program process will be recorded into log files. The exercise was conducted as part of the Purwadhika School Data Engineering curriculum.

## Architecture
```mermaid
    flowchart TD
      datasource[Source Data #40;Kaggle#41;]
      extract[Extract]
      transform[Transform]
      load[Load]
      logger[Logger]
      dwh[Data Warehouse #40;local directory#41;]
      log[Log Directory]

      datasource --> extract
      extract -->|csv to dataframe| transform
      transform -->|wide to long format| load
      load -->  dwh
      extract --> logger
      transform --> logger
      load --> logger
      logger --> log
