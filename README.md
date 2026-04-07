# Logistic Regression Models to Predict Diabetes

## 📋 Mô Tả Dự Án

Dự án này xây dựng các mô hình **Logistic Regression** để dự đoán khả năng mắc bệnh tiểu đường dựa trên các thông số y tế. Sử dụng Jupyter Notebook để khám phá dữ liệu, xây dựng mô hình, và đánh giá hiệu suất.

## 🎯 Mục Tiêu

- Phân tích dữ liệu y tế liên quan đến bệnh tiểu đường
- Thuật toán Hồi quy Logistic: Tự triển khai các hàm sigmoid, compute_cost, predict và ba phương pháp tối ưu hóa Gradient Descent:
+ Batch Gradient Descent (BGD): Tối ưu hóa trên toàn bộ tập dữ liệu.
+ Mini-Batch Gradient Descent (MBGD): Tối ưu hóa trên các tập dữ liệu con (batch size = 32), cải thiện hiệu quả tính toán và độ hội tụ.
+ Stochastic Gradient Descent (SGD): Tối ưu hóa trên từng mẫu dữ liệu ngẫu nhiên, giúp thoát khỏi các cực tiểu cục bộ.
- Đánh giá mô hình: Sử dụng các chỉ số Accuracy Score, Classification Report (Precision, Recall, F1-score) và Confusion Matrix.
## 📊 Dữ Liệu

Diabetes Dataset lấy từ kaggle được sử dụng trong dự án bao gồm các thông số y tế như:
- Mức glucose
- Huyết áp
- Độ dày da
- Insulin
- Chỉ số BMI
- Lịch sử gia đình
- Tuổi
- Kết quả xét nghiệm tiểu đường

## 🛠️ Công Nghệ & Thư Viện

- **Python 3.x**
- **Jupyter Notebook** - Môi trường phát triển tương tác
- **NumPy** - Xử lý mảng số học
- **Pandas** - Phân tích và xử lý dữ liệu
- **Scikit-learn** - Machine Learning library
- **Matplotlib/Seaborn** - Trực quan hóa dữ liệu

