# Big Data Analysis with Scala and Spark Lab (ENSP359)

**Author:** Aditya Shibu  
**Roll Number:** 2401201047  
**Course:** BCA (AI & DS)  
**University:** K.R. Mangalam University  
**Submitted To:** Mr. Nikhil Sharma  

## Overview
This repository contains the complete laboratory experiments for the "Big Data Analysis with Scala and Spark" course (ENSP359). Experiments 1–3 are implemented in native Scala via `spark-shell`, demonstrating real Scala syntax for variables, collections, and RDD transformations. Experiments 4–15 use PySpark (Python), configured to run on Arch Linux with Java 17 compatibility.

## Experiments

| No. | Title | Language |
|-----|-------|----------|
| 1 | Variables, Data Types, Arithmetic, Conditionals, Loops, Functions | Scala |
| 2 | Collections — Array, List, Vector, Map | Scala |
| 3 | RDD Transformations — map, filter, flatMap | Scala |
| 4 | Word Count via Map-Reduce (reduceByKey) | PySpark |
| 5 | RDD Actions — collect, count, aggregate, mapValues, partitioning | PySpark |
| 6 | Multiple RDD Operations — union, intersection, subtract, cartesian | PySpark |
| 7 | DataFrame Basics — CSV & JSON load, printSchema, select, filter | PySpark |
| 8 | Nested JSON & explode() — flatten arrays, filter on exploded data | PySpark |
| 9 | Missing Data — fillna, dropna, dataset cleaning | PySpark |
| 10 | Aggregations — groupBy, agg, sum, avg, sorting (DataFrame + SQL) | PySpark |
| 11 | Spark SQL — temp views, SELECT, WHERE, GROUP BY, HAVING, ORDER BY | PySpark |
| 12 | Joins — inner, left, right, full outer (DataFrame API + SQL) | PySpark |
| 13 | PySpark SQL Functions — string, numeric, date, conditional, cast | PySpark |
| 14 | File Formats — CSV, JSON, Parquet with explicit schema and partitioning | PySpark |
| 15 | End-to-End Project — Housing Dataset (load, clean, transform, SQL, agg, optimize) | PySpark |

> **Note on Ex 14:** The spec references Databricks Volumes. This lab runs locally on Arch Linux, so equivalent operations use local filesystem paths (`/tmp`). All Spark read/write operations and schema concepts are identical — only the storage backend differs.

## Environment

| Component | Version |
|-----------|---------|
| Apache Spark | 4.1.1 |
| Scala | 2.13.17 |
| Python | 3.14 |
| Java | OpenJDK 17.0.19 |
| OS | Arch Linux |

## How to Run
1. Ensure **Java 17** is installed (`/usr/lib/jvm/java-17-openjdk`).
2. Ensure **PySpark** is installed: `pip install pyspark --break-system-packages`
3. Open `ADITYA_SHIBU_2401201047_BIG_DATA_LAB.ipynb` in Jupyter.
4. Run the **Setup cell** first — it forces Java 17 via `JAVA_HOME` and initializes the Spark session.
5. For Ex 15, place `housing.csv` at `~/Downloads/housing.csv` before running.

## Notes
- Scala experiments (Ex 1–3) run via `spark-shell` invoked through Python's `subprocess` module using a `run_scala()` helper defined in the notebook.
- Java 26 may be the system default on some setups — the setup cell explicitly overrides `JAVA_HOME` and `PATH` to target Java 17, which is required for Spark compatibility.
- Zstd compression is configured for Parquet output to avoid `snappy`/`musl` native library conflicts on Arch Linux.
