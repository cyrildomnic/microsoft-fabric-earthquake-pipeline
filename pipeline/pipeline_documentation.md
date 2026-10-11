# Microsoft Fabric Data Pipeline Documentation

## 1. Overview

This document describes the orchestration and scheduled execution of the USGS Earthquake Data Engineering Pipeline built using Microsoft Fabric.

The pipeline coordinates data ingestion and processing across the Bronze, Silver, and Gold layers of the Medallion Architecture.

## 2. Pipeline Workflow

The workflow consists of the following stages:

- **Bronze Layer:** Ingests raw earthquake data from the USGS Earthquake API into the Microsoft Fabric Lakehouse.
- **Silver Layer:** Cleans and transforms earthquake records, including timestamp conversions, and stores the processed data as Delta tables.
- **Gold Layer:** Enriches earthquake records with country information and earthquake significance classifications for analytics.

The processed Gold-layer data is used in the Power BI report through Direct Lake.

## 3. Pipeline Orchestration

The Microsoft Fabric Data Pipeline coordinates the data ingestion and processing workflow.

It orchestrates the required processing activities to move earthquake data through the Bronze, Silver, and Gold layers.

## 4. Scheduled Execution

The pipeline is configured for scheduled execution in Microsoft Fabric, allowing the workflow to run automatically according to the configured schedule.

This reduces the need to start each pipeline run manually.

## 5. Execution Monitoring and Validation

Pipeline execution can be monitored through the run history available in Microsoft Fabric.

The following checks help validate a pipeline run:

- Verify the overall pipeline execution status.
- Review individual activity results for errors.
- Confirm that the expected Lakehouse tables are created or updated.
- Check that the processed data is available for reporting.

## 6. Future Improvements

- Implement data quality checks and validation rules.
- Add error handling, logging, and failure notifications.
- Improve incremental data processing and duplicate handling.
- Monitor and optimize pipeline performance.
