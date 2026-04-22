# Big Data Analysis with Scala and Spark Lab (ENSP359)

**Author:** Aditya Shibu  
**Roll Number:** 2401201047  
**Course:** BCA (AI & DS)  

## Overview
This repository contains the complete laboratory experiments for the "Big Data Analysis with Scala and Spark" course. The work is implemented in a Jupyter Notebook using PySpark, specifically configured to run on modern Linux environments (Arch/glibc) with Java 17 compatibility.

## Experiments Included
1. Scala/Python Basics (Variables, Control Flow)
2. Functions for Collections (Lists, Maps)
3. RDD Transformations (map, filter, flatMap)
4. Word Count via Map-Reduce
5. RDD Actions (collect, count, aggregate)
6. Multiple RDD Operations (union, intersection)
7. DataFrame Basics (select, filter)
8. Nested JSON & Explode
9. Missing Data Handling (fillna, dropna)
10. DataFrame Aggregations (groupBy, sum, avg)
11. Spark SQL (Temporary Views)
12. Joins (Inner, Left, Right, Outer)
13. Spark SQL Column Functions
14. File Formats (Read/Write Parquet with Zstd)
15. End-to-End Housing Dataset Project

## Setup & Compatibility
- **Language:** Python (PySpark)
- **Engine:** Apache Spark 3.x
- **Java:** OpenJDK 17 (Targeted via `JAVA_HOME` environment variables in-notebook)
- **Compression:** Zstd (Configured to avoid snappy/musl compatibility issues)

## How to Run
1. Ensure Java 17 is installed on your system.
2. Open `ADITYA_SHIBU_2401201047_BIG_DATA_LAB.ipynb` in Jupyter or Google Colab.
3. Run the first cell to initialize the Spark session.
