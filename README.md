[![Open in Visual Studio Code](https://classroom.github.com/assets/open-in-vscode-2e0aaae1b6195c2367325f4f02e2d04e9abb55f0b24a779b69b11b9e10269abc.svg)](https://classroom.github.com/online_ide?assignment_repo_id=23573989&assignment_repo_type=AssignmentRepo)
# Day 10 Lab: Data Pipeline & Data Observability

**Student Email:** bbaolongngau@gmail.com
**Name:** Ngô Gia Bảo

---

## Mo ta

Bài lab này xây dựng một ETL pipeline cơ bản gồm 4 bước:

- **Extract**: Đọc dữ liệu từ file `raw_data.json`
- **Validate**: Loại bỏ dữ liệu không hợp lệ (price <= 0 hoặc category rỗng)
- **Transform**:
  - Chuẩn hóa category (Title Case)
  - Tính discounted_price (giảm 10%)
  - Thêm timestamp `processed_at`
- **Load**: Lưu dữ liệu đã xử lý ra `processed_data.csv`

---

## Cach chay (How to Run)

### Prerequisites
```bash
pip install pandas
```

### Chay ETL Pipeline
```bash
python solution.py
```

### Chay Agent Simulation (Stress Test)
```bash
# Mo ta cach ban chay thi nghiem Clean vs Garbage data
```
Để kiểm tra ảnh hưởng của chất lượng dữ liệu đến AI Agent, tôi thực hiện 2 kịch bản:

---

### 1. Clean Data

- Sử dụng dữ liệu đã được xử lý từ ETL pipeline: `processed_data.csv`
- Dữ liệu đã:
  - Loại bỏ giá trị không hợp lệ (price <= 0)
  - Chuẩn hóa category
  - Không chứa outliers bất thường

👉 Chạy lệnh:
```bash
python agent_simulation.py
---

## Cau truc thu muc

```
├── solution.py              # ETL Pipeline script
├── processed_data.csv       # Output cua pipeline
├── experiment_report.md     # Bao cao thi nghiem
└── README.md                # File nay
```

---

## Ket qua

(Tom tat ket qua: bao nhieu records da xu ly, bao nhieu bi loai, v.v.)
Validation complete. Valid: 3, Errors: 2