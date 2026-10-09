# Microsoft Fabric Earthquake Data Engineering Pipeline

An end-to-end data engineering project using Microsoft Fabric and the USGS Earthquake API.

## Project Overview

This project demonstrates API-based data ingestion, data transformation, enrichment, orchestration, and reporting using Microsoft Fabric.

It follows the Medallion Architecture to organize earthquake data into Bronze, Silver, and Gold layers, transforming raw earthquake records into analytics-ready datasets for reporting.

## Architecture

**USGS Earthquake API → Bronze → Silver → Gold → Power BI Direct Lake**

Microsoft Fabric Lakehouse is used for data storage and processing. Microsoft Fabric Data Pipeline handles orchestration and scheduled execution of the workflow.

## Technology Stack

* Microsoft Fabric Lakehouse
* Microsoft Fabric Notebooks
* Python and Requests
* PySpark and Delta Lake
* Medallion Architecture (Bronze, Silver, Gold)
* Reverse Geocoder
* Microsoft Fabric Data Factory
* Power BI Direct Lake

## Implementation

### Bronze — Data Ingestion

* Fetch earthquake data from the USGS Earthquake API using Python and Requests.
* Store raw earthquake data in the Bronze layer of the Microsoft Fabric Lakehouse.

### Silver — Data Transformation

* Clean and structure raw earthquake records.
* Convert timestamps into appropriate datetime formats.
* Transform the data and store it in Delta tables for downstream processing.

### Gold — Data Enrichment

* Enrich earthquake records with geographic information, including country codes using the Reverse Geocoder library.
* Classify earthquakes based on their significance.
* Prepare analytics-ready datasets for reporting and analysis.

### Reporting — Power BI

* Connect the Gold-layer data to Power BI using Direct Lake.
* Build interactive reports to explore earthquake records and their attributes.

### Orchestration and Scheduling — Microsoft Fabric Data Pipeline

* Created a data pipeline in Microsoft Fabric to orchestrate the end-to-end data ingestion and processing workflow.
* Configured scheduled execution to automate pipeline runs.
* Orchestrated the processing workflow across the Bronze, Silver, and Gold layers.

## Repository Contents

* `notebooks/` — Exported Microsoft Fabric notebook files.
* `pipeline/` — Pipeline workflow and execution documentation.
* `reports/` — Power BI report screenshots.
* `docs/` — Architecture diagrams and supporting documentation.

## Data Source

[USGS Earthquake API](https://earthquake.usgs.gov/fdsnws/event/1/)

## Reference Tutorial

This project was developed as a guided learning exercise based on the following tutorial:

[End-to-End Microsoft Fabric Earthquake Data Engineering Tutorial — YouTube](https://youtu.be/Av44Nrhl05s?si=zQKzm7g5LpC8nvGC)

## Learning Outcomes

* Implementing API-based data ingestion using Python.
* Applying Medallion Architecture in Microsoft Fabric.
* Cleaning and transforming data using Fabric notebooks and PySpark.
* Storing structured datasets using Delta Lake.
* Enriching datasets for analytical use cases.
* Building Power BI reports using Direct Lake.
* Orchestrating and scheduling data engineering workflows using Microsoft Fabric Data Factory.
