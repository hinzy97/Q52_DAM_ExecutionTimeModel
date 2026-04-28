# DAM: Dynamic Allocation Model for Spark Execution Time Prediction

This repository provides a reproducible implementation of the Dynamic Allocation Model (DAM) used for predicting execution time of Spark applications under dynamic resource allocation.

## 🔍 Overview
The model extends the Static Allocation Model (SAM) by dynamically adjusting executor cores based on:

- Backlog timeout (scale up)
- Idle timeout (scale down)
- Minimum executor cores constraint

## ⚙️ Key Features
- DAG-based stage execution
- Task-level simulation
- Dynamic executor scaling
- Deterministic prediction framework

## 📊 Experiment
- Query: TPC-DS Query-52
- Dataset size: 500 GB
- Minimum cores: 4
- Warm-up + transfer time included

## ▶️ How to Run

## 📓 Notebook

The primary implementation and experiment can be found in:

- `Q52_DAM.ipynb`

This notebook contains:
- Stage and task modeling
- Dynamic executor allocation logic
- Execution time simulation for Query-52
- Result validation against measured execution times
