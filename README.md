# DAM: Dynamic Allocation Model for Spark Execution Time Prediction

This repository provides a reproducible implementation of the **Dynamic Allocation Model (DAM)** for predicting execution time of Apache Spark applications using a deterministic, stage-based simulation framework.

---

## 🔍 Overview

The Dynamic Allocation Model (DAM) extends the Static Allocation Model (SAM) by incorporating **dynamic executor allocation**, enabling more realistic modeling of Spark execution behavior.

The model captures:

- **Backlog-based scaling**: Executors are added when tasks accumulate and cores are fully utilized  
- **Idle-time-based scaling**: Executors are removed when resources remain idle  
- **Minimum executor constraint**: Ensures baseline parallelism throughout execution  

This approach provides an interpretable and lightweight alternative to data-driven performance models.

---

## ⚙️ Key Features

- DAG-based stage execution modeling  
- Task-level simulation of Spark jobs  
- Round-robin scheduling across stages  
- Dynamic executor scaling (add/remove cores)  
- Deterministic and reproducible execution time prediction  

---

## 📓 Notebook

The complete implementation and experiment are contained in:

- **`Q52_DAM.ipynb`**

The notebook includes:
- Definition of Stage, Task, and Core classes  
- DAG construction for Query-52  
- Dynamic allocation logic (DAM)  
- Execution time simulation  
- Validation against measured results  

---

## 📊 Experimental Setup

- **Workload**: TPC-DS Query-52  
- **Data Size**: 500 GB  
- **Execution Mode**: Dynamic allocation  
- **Minimum Executor Cores**: 4  
- **Overhead Included**: Warm-up and stage transfer time  

---

## 📈 Results

The DAM model produces execution time predictions that closely match measured runtimes under selected configurations.

- Prediction error (best cases): ~2% – 9%  
- Average error (selected cases): **~4.96%**

---

## ▶️ How to Run

1. Open the notebook:

```bash
jupyter notebook Q52_DAM.ipynb
