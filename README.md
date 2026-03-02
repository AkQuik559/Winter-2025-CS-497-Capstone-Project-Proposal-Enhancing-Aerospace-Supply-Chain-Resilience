# Winter-2025-CS-497-Capstone-Project-Proposal-Enhancing-Aerospace-Supply-Chain-Resilience
A Predictive Analytics Approach to Mitigate Lead-Time Volatility

# Aerospace Supply Chain Volatility – Databricks Pipeline

## Overview
This repository contains the Databricks notebook/script used to ingest, clean, align, and merge three monthly time-series datasets:
- FRED Aerospace Production Index (IPG3361T3S)
- FRED Freight Transportation Index (TSIFRGHTC)
- NY Fed Global Supply Chain Pressure Index (GSCPI)

The pipeline creates a unified monthly dataset and engineers volatility features to support downstream analysis and Power BI dashboards.

## Outputs
- `final_aerospace_dataset.csv` (generated in Databricks)
- Engineered features:
  - Production_Volatility_3mo
  - Freight_Volatility_3mo
  - Pressure_Change

## How it was built
1. Upload raw files into a Unity Catalog volume.
2. Read CSV inputs in Databricks.
3. Clean metadata rows in GSCPI file and normalize schema.
4. Align all datasets to a monthly key (`Month`).
5. Merge datasets and compute rolling volatility features.
6. Export curated dataset for Power BI.

## Repo Contents
- `notebooks/databricks_pipeline.py` – pipeline code exported from Databricks
- `data/` – optional sample output for quick preview
