1. Project Overview

This project demonstrates a basic ETL (Extract, Transform, Load) pipeline using real-world data from the Google Mobility dataset. The primary goal is to showcase data cleaning, memory optimization, and strict data type formatting using Python and Pandas.
2. The ETL Process

    Extract:
    Loaded a large-scale raw dataset (105 MB CSV) directly into a Pandas DataFrame to initiate the data profiling and manipulation process.

    Transform:
    Conducted an initial data profiling using .info() and .isnull(). Discovered hidden null values disguised as text characters (.) which were corrupting the dataset. After replacing these anomalies with true nulls, I casted the mobility metric columns from generic strings to strict float64 data types to ensure data integrity and improve RAM efficiency.

    Load:
    Exported the cleaned DataFrame to a columnar .parquet format. This critical step preserved the strict data types and applied aggressive compression, reducing the final file size by over 83% (from 105 MB to 17.2 MB) without any data loss.
