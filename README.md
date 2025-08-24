# Order-to-Delivery Analytics Pipeline

Dự án này mô phỏng pipeline dữ liệu từ **Olist Kaggle dataset** để phân tích quy trình Order → Delivery.

## 🎯 Mục tiêu
- Xây dựng Data Lake (Bronze → Silver → DW)
- Chuẩn hóa dữ liệu với dbt
- Orchestrate ETL với Airflow
- Tạo dashboard phân tích bằng Metabase/BI

## 📂 Cấu trúc repo
- data/landing/ → file CSV gốc từ Kaggle
- lake/bronze/olist/ → raw CSV (Bronze layer)
- lake/silver/olist/ → Parquet chuẩn hóa (Silver layer)
- db/ddl/ → file SQL tạo schema/table
- dbt/ → dbt project (staging, marts, tests…)
- irflow/dags/ → pipeline orchestration
- i/ → dashboard (Metabase, BI tools)
- docs/ → tài liệu dự án
- scripts/ → Python ETL scripts

---
