# lake/bronze/olist

Thư mục này chứa dữ liệu **raw Olist dataset** sau khi copy từ data/landing.

## 📌 Đặc điểm
- Định dạng: **CSV**
- Dữ liệu giữ nguyên từ Kaggle, **chưa qua xử lý/chuẩn hóa**
- Đây là **Bronze layer** trong Data Lake (Raw Zone)

## 📂 Quy trình
1. CSV từ data/landing/ được load sang đây.
2. Lưu trữ dữ liệu nguyên bản để đảm bảo tính toàn vẹn.
3. Sau đó chuyển sang **Silver layer** để chuẩn hóa.
