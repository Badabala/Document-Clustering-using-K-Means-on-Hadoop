# 📂 Document Clustering using K-Means on Hadoop

## 📌 Project Overview
This project implements **document clustering** using the **K-Means algorithm** on a **Hadoop MapReduce** framework. The goal is to group similar documents into clusters based on term frequency-inverse document frequency (**TF-IDF**) values.

## 👥 Team
- **Team Size**: 5 members
- **Duration**: March 2025

## 🏗️ Technologies Used
- **Hadoop MapReduce** – Distributed processing of large-scale document data
- **Java** – Implementation of MapReduce jobs
- **TF-IDF** – Feature extraction for document representation
- **K-Means Clustering** – Algorithm for grouping similar documents
- **HDFS** – Storage for input/output data

## 🚀 Features
- **Preprocessing of document data** (tokenization, stop-word removal, and TF-IDF computation)
- **Parallel execution of the K-Means algorithm** using Hadoop MapReduce
- **Convergence detection for optimal clustering results**
- **Scalability to handle large datasets**

## 📜 Folder Structure
```
Document-Clustering-using-K-Means-on-Hadoop/
  │── 1.1/  # Task 1.1 implementation
  │── 1.2/  # Task 1.2 implementation
  │── 1.3/  # Task 1.3 implementation
      │── input/  # Input files (e.g., output_1_2.mtx)
      │── output/ # Output files (e.g., task_1_3.txt)
      │── source/ # Source code (e.g., Task1_3.java)
  │── 1.4/  # Task 1.4 implementation
  │── 1.5/  # Task 1.5 implementation (Final clustering output)
  │── 2.1/  # Task 2.1 implementation
  │── 2.2/  # Task 2.2 implementation
  │── 2.3/  # Task 2.3 implementation
  │── README.md  # Project documentation
```

## 🚀 How to Run
### 1. Clone the Repository
```sh
git clone https://github.com/Badabala/Document-Clustering-using-K-Means-on-Hadoop.git
cd Document-Clustering-using-K-Means-on-Hadoop
```

### 2. Set Up Hadoop Environment
- Ensure **Hadoop** is installed and configured.
- Start HDFS and YARN:
  ```sh
  start-dfs.sh
  start-yarn.sh
  ```

### 3. Upload Data to HDFS
```sh
hdfs dfs -mkdir -p /user/hadoop/input
hdfs dfs -put dataset.txt /user/hadoop/input/
```

### 4. Compile and Run the MapReduce Job for Task 1.3
```sh
hadoop jar Task1_3.jar Task1_3 /user/hadoop/input/output_1_2.mtx /user/hadoop/output/task_1_3.txt
```

### 5. Retrieve Output
```sh
hdfs dfs -cat /user/hadoop/output/task_1_3.txt
```

## 📌 Notes
- Modify **K value** in the configuration for different numbers of clusters.
- Ensure **Java** and **Hadoop** are properly set up in your environment.
- The **output folder must not exist** before running the job (delete if necessary):
  ```sh
  hdfs dfs -rm -r /user/hadoop/output
  ```
