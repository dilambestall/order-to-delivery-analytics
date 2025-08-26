# 🚀 Order-to-Delivery Analytics Pipeline
Dự án Data Engineering mô phỏng pipeline phân tích dữ liệu **Order → Delivery** từ bộ dữ liệu **[Olist (Kaggle)](https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce)**.  
Mục tiêu: xây dựng Data Lake (Bronze/Silver), chuẩn hoá với dbt, orchestration bằng Airflow, và trực quan hoá với Metabase.

## 🎯 Mục tiêu
- Xây dựng Data Lake (Bronze → Silver → Data Warehouse)  
- Chuẩn hoá dữ liệu với dbt  
- Orchestrate ETL với Airflow  
- Tạo dashboard phân tích bằng Metabase/BI  

## 🏗️ Kiến trúc hệ thống
Kaggle CSV
↓
Data Lake (Bronze → Silver)
↓
Data Warehouse (Postgres)
↓
dbt models (staging, marts, KPIs)
↓
Airflow DAGs (orchestration)
↓
Metabase Dashboard

## 📂 Cấu trúc repo
data/landing/ # CSV gốc từ Kaggle
lake/bronze/olist/ # raw CSV (Bronze layer)
lake/silver/olist/ # Parquet chuẩn hoá (Silver layer)
db/ddl/ # file SQL tạo schema/table
dbt/ # dbt project (staging, marts, tests…)
airflow/dags/ # pipeline orchestration
bi/ # dashboard (Metabase, BI tools)
docs/ # tài liệu dự án
scripts/ # Python ETL scripts



## ⚙️ Cài đặt (Setup)
### Yêu cầu
- Python 3.10+  
- PostgreSQL 15+ (DB: `ecommerce_dw`)  
- Virtualenv / venv  

### Các bước
```bash
# Clone repo
git clone https://github.com/dilambestall/order-to-delivery-analytics.git
cd order-to-delivery-analytics

# Tạo môi trường ảo
python -m venv venv
venv\Scripts\activate   # Windows
source venv/bin/activate # Linux/Mac

# Cài thư viện
pip install -r requirements.txt
pip install -r dev-requirements.txt

# Tạo database trong Postgres
createdb ecommerce_dw



## 📊 Dataset
Nguồn: [Olist Brazilian E-Commerce Public Dataset](https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce)  
Sau khi tải về, giải nén vào thư mục: `data/landing/`

## 👥 Contributors
- [@dilambestall](https://github.com/dilambestall)  
- [@hovngnvm](https://github.com/hovngnvm)



## 📜 License
This project is licensed under the MIT License - see the [LICENSE](./LICENSE) file for details.

