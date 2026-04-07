# Logistic Regression Models to Predict Diabetes

## 📋 Mô Tả Dự Án
Dự án này xây dựng các mô hình **Logistic Regression** để dự đoán khả năng mắc bệnh tiểu đường dựa trên các thông số y tế. Sử dụng Jupyter Notebook để khám phá dữ liệu, xây dựng mô hình, và đánh giá hiệu suất.

---

## 🎯 Mục Tiêu
* **Phân tích dữ liệu y tế:** Liên quan đến bệnh tiểu đường.
* **Thuật toán Hồi quy Logistic:** Tự triển khai các hàm `sigmoid`, `compute_cost`, `predict` và 3 phương pháp tối ưu hóa Gradient Descent:
    * **Batch Gradient Descent (BGD):** Tối ưu hóa trên toàn bộ tập dữ liệu.
    * **Mini-Batch Gradient Descent (MBGD):** Tối ưu hóa trên các tập dữ liệu con (batch size = 32).
    * **Stochastic Gradient Descent (SGD):** Tối ưu hóa trên từng mẫu dữ liệu ngẫu nhiên.
* **Đánh giá mô hình:** Sử dụng Accuracy Score, Classification Report (Precision, Recall, F1-score) và Confusion Matrix.

---

## 📊 Dữ Liệu
Diabetes Dataset lấy từ Kaggle bao gồm các thông số y tế:
* Mức glucose, Huyết áp, Độ dày da, Insulin.
* Chỉ số BMI, Lịch sử gia đình, Tuổi.
* Kết quả xét nghiệm tiểu đường.

---

## 🛠️ Công Nghệ & Thư Viện
* **Ngôn ngữ:** Python 3.x
* **Môi trường:** Jupyter Notebook
* **Thư viện:** * `NumPy`, `Pandas` (Xử lý dữ liệu)
    * `Scikit-learn` (Machine Learning)
    * `Matplotlib`, `Seaborn` (Trực quan hóa)

---

## 📈 Quy Trình Dự Án
1.  **Khám Phá Dữ Liệu (EDA):** Tải dữ liệu, phân tích thống kê và trực quan hóa tương quan.
2.  **Tiền Xử Lý:** Xử lý giá trị thiếu, chuẩn hóa dữ liệu và chia tập Train/Test.
3.  **Huấn Luyện:** Xây dựng 4 biến thể Logistic Regression, tối ưu Hyperparameters.
4.  **Đánh Giá:** Phân tích Accuracy, Precision, Recall, F1-score, Confusion Matrix và ROC Curve.

---

## 📊 Kết Quả Mô Hình

### 📈 Tóm Tắt Kết Quả
| Mô Hình | Accuracy | Precision (Class 1) | Recall (Class 1) | F1-Score (Class 1) |
| :--- | :---: | :---: | :---: | :---: |
| **Logistic Regression (sklearn)** | **75.32%** ⭐ | **0.65** | **0.67** | **0.66** |
| Mini-batch Gradient Descent | 74.68% | 0.64 | 0.65 | 0.65 |
| SGD (Stochastic GD) | 73.38% | 0.62 | 0.64 | 0.63 |
| Batch Gradient Descent | 73.38% | 0.62 | 0.64 | 0.63 |

---

### 1️⃣ Logistic Regression - sklearn (Tốt Nhất ⭐)
**Accuracy:** `75.32%`

**Classification Report:**
| Class | Precision | Recall | F1-Score | Support |
| :--- | :---: | :---: | :---: | :---: |
| Class 0 | 0.81 | 0.80 | 0.81 | 99 |
| Class 1 | 0.65 | 0.67 | 0.66 | 55 |
| **Average** | **0.76** | **0.75** | **0.75** | **154** |

> **Nhận xét:** Độ chính xác cao nhất. Cân bằng tốt giữa Precision và Recall. Độ nhạy (Recall) tốt trong việc phát hiện bệnh.

---

### 2️⃣ Mini-batch Gradient Descent
**Accuracy:** `74.68%`

| Class | Precision | Recall | F1-Score | Support |
| :--- | :---: | :---: | :---: | :---: |
| Class 0 | 0.81 | 0.80 | 0.80 | 99 |
| Class 1 | 0.64 | 0.65 | 0.65 | 55 |

> **Nhận xét:** Hiệu suất rất gần với sklearn. Phù hợp cho dữ liệu lớn, tốc độ hội tụ nhanh hơn Batch GD.

---

### 3️⃣ & 4️⃣ SGD & Batch Gradient Descent
**Accuracy:** `73.38%`

| Class | Precision | Recall | F1-Score | Support |
| :--- | :---: | :---: | :---: | :---: |
| Class 0 | 0.80 | 0.79 | 0.79 | 99 |
| Class 1 | 0.62 | 0.64 | 0.63 | 55 |

> **Nhận xét:** Hiệu suất thấp hơn. SGD có độ dao động cao do cập nhật từng mẫu. Batch GD hội tụ chậm nhất trên dữ liệu lớn.

---

## 🔍 Phân Tích Chi Tiết

### 📌 Diễn Giải Các Chỉ Số
* **Accuracy:** Tỷ lệ dự đoán chính xác trên toàn bộ dữ liệu.
* **Precision:** Trong những ca dự đoán là bệnh, bao nhiêu % thực sự bệnh.
* **Recall:** Trong những ca thực sự bệnh, mô hình phát hiện được bao nhiêu %.
* **F1-Score:** Trung bình điều hòa giữa Precision và Recall.

## 🎯 Kết Luận
1.  **Mô hình tốt nhất:** Sklearn Logistic Regression (`75.32%`).
2.  **Khả năng phát hiện:** Mô hình phát hiện được khoảng 2/3 bệnh nhân thực tế (`Recall = 0.67`).
3.  **Cảnh báo sai:** Tỷ lệ báo động nhầm là khoảng `35%`.
4.  **Khuyến nghị:** Sử dụng **Mini-batch GD** khi làm việc với các bộ dữ liệu quy mô lớn để cân bằng tốc độ và hiệu suất.
