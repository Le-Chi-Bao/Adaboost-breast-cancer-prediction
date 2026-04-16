# 🧠 Dự đoán khối u vú bằng AdaBoost

## 📌 Giới thiệu
Dự án này xây dựng mô hình **AdaBoost từ đầu (from scratch)** để dự đoán khối u vú thuộc hai nhóm:

- 🟢 Lành tính (Benign)  
- 🔴 Ác tính (Malignant)

Sử dụng bộ dữ liệu Breast Cancer Wisconsin với 30 đặc trưng.

---

## 🎯 Mục tiêu
- Hiểu và cài đặt thuật toán AdaBoost
- So sánh với mô hình sklearn
- Phân tích sâu hành vi của mô hình
- Xây dựng giao diện web bằng Gradio

---

## 📂 Cấu trúc project
```
AdaBoost/
│
├── notebook.ipynb
├── app.py
├── saved_models/
│   ├── custom_model_state.pkl
│   ├── sklearn_adaboost.pkl
│   └── scaler.pkl
├── requirements.txt
└── README.md
```

---

## ⚙️ Phương pháp

### AdaBoost (tự cài đặt)
- Huấn luyện weak learner (decision stump)
- Tính error
- Tính alpha
- Cập nhật trọng số mẫu
- Tổng hợp dự đoán

### AdaBoost (sklearn)
Sử dụng `AdaBoostClassifier` để so sánh kết quả.

---

## 📊 Kết quả
- Độ chính xác ~ **98%**
- Mô hình tự xây dựng ≈ mô hình sklearn
- Không có false positive
- Có một số false negative

---

## 📈 Phân tích mô hình
- Alpha giảm dần theo từng vòng boosting
- Entropy giảm → mô hình tập trung vào mẫu khó
- Decision score phân tách rõ hai lớp

---

## 🌐 Demo Web (Gradio)

Chạy ứng dụng:
```
python app.py
```

Chức năng:
- Dự đoán một mẫu
- Dự đoán hàng loạt bằng file CSV
- Chọn giữa 2 mô hình

---

## 💾 Lưu mô hình
- Custom model: lưu dạng state (alphas, trees, M)
- Sklearn model: lưu bằng joblib
- Scaler: lưu để dùng lại khi dự đoán

---

## 🚀 Hướng phát triển
- Giảm lỗi false negative
- Thử các mô hình mạnh hơn (XGBoost, Gradient Boosting)
- Triển khai web thực tế

---

## ⚠️ Lưu ý
Dự án mang tính học tập, không dùng cho chẩn đoán y khoa thực tế.

---

## 👨‍💻 Tác giả
Sinh viên ngành Machine Learning
