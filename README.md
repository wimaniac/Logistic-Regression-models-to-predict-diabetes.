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
  
📈 Quy Trình Dự Án
1️⃣ Khám Phá Dữ Liệu (EDA)
Tải và kiểm tra dữ liệu
Phân tích các thông số thống kê
Trực quan hóa phân phối dữ liệu và mối quan hệ
2️⃣ Tiền Xử Lý Dữ Liệu
Xử lý các giá trị thiếu
Chuẩn hóa/Tiêu chuẩn hóa dữ liệu
Chia dữ liệu thành train set và test set
3️⃣ Xây Dựng & Huấn Luyện Mô Hình
4 mô hình Logistic Regression với các thuật toán tối ưu khác nhau
Tối ưu các tham số (learning rate, số lần lặp, etc.)
4️⃣ Đánh Giá Mô Hình
Tính toán Accuracy, Precision, Recall, F1-score
Vẽ Confusion Matrix
Phân tích ROC Curve
📊 Kết Quả Mô Hình
Dự án so sánh 4 mô hình Logistic Regression với 3 thuật toán tối ưu khác nhau:

📈 Tóm Tắt Kết Quả
Mô Hình	Accuracy	Precision (Class 1)	Recall (Class 1)	F1-Score (Class 1)
Logistic Regression (sklearn)	75.32% ⭐	0.65	0.67	0.66
Mini-batch Gradient Descent	74.68%	0.64	0.65	0.65
SGD (Stochastic GD)	73.38%	0.62	0.64	0.63
Batch Gradient Descent	73.38%	0.62	0.64	0.63
1️⃣ Logistic Regression - sklearn (Mô Hình Tốt Nhất) ⭐
Code
Accuracy: 75.32%

Classification Report:
┌─────────┬───────────┬────────┬──────────┬─────────┐
│ Class   │ Precision │ Recall │ F1-Score │ Support │
├─────────┼───────────┼────────┼──────────┼─────────┤
│ Class 0 │   0.81    │  0.80  │   0.81   │   99    │
│ Class 1 │   0.65    │  0.67  │   0.66   │   55    │
├─────────┼───────────┼────────┼──────────┼─────────┤
│ Average │   0.76    │  0.75  │   0.75   │   154   │
└─────────┴───────────┴────────┴──────────┴─────────┘
✨ Nhận xét:

Độ chính xác cao nhất (75.32%)
Cân bằng tốt giữa Precision (0.81) và Recall (0.80) cho Class 0
Độ nhạy tốt (Recall = 0.67) cho việc phát hiện bệnh tiểu đường
2️⃣ Mini-batch Gradient Descent
Code
Accuracy: 74.68%

Classification Report:
┌─────────┬───────────┬────────┬──────────┬─────────┐
│ Class   │ Precision │ Recall │ F1-Score │ Support │
├─────────┼───────────┼────────┼──────────┼─────────┤
│ Class 0 │   0.81    │  0.80  │   0.80   │   99    │
│ Class 1 │   0.64    │  0.65  │   0.65   │   55    │
├─────────┼───────────┼────────┼──────────┼─────────┤
│ Average │   0.75    │  0.75  │   0.75   │   154   │
└─────────┴───────────┴────────┴──────────┴─────────┘
💡 Nhận xét:

Hiệu suất rất gần với sklearn (chỉ kém 0.64%)
Phù hợp cho dữ liệu lớn nhất
Thời gian tính toán nhanh hơn Batch GD
3️⃣ SGD (Stochastic Gradient Descent)
Code
Accuracy: 73.38%

Classification Report:
┌─────────┬───────────┬────────┬──────────┬─────────┐
│ Class   │ Precision │ Recall │ F1-Score │ Support │
├─────────┼───────────┼────────┼──────────┼─────────┤
│ Class 0 │   0.80    │  0.79  │   0.79   │   99    │
│ Class 1 │   0.62    │  0.64  │   0.63   │   55    │
├─────────┼───────────┼────────┼──────────┼─────────┤
│ Average │   0.73    │  0.73  │   0.73   │   154   │
└─────────┴───────────┴────────┴──────────┴─────────┘
⚠️ Nhận xét:

Hiệu suất giảm so với các mô hình trước (73.38%)
Độ dao động cao do cập nhật dựa trên từng mẫu
Recall cho Class 1 thấp hơn (0.64)
4️⃣ Batch Gradient Descent
Code
Accuracy: 73.38%

Classification Report:
┌─────────┬───────────┬────────┬──────────┬─────────┐
│ Class   │ Precision │ Recall │ F1-Score │ Support │
├─────────┼───────────┼────────┼──────────┼─────────┤
│ Class 0 │   0.80    │  0.79  │   0.79   │   99    │
│ Class 1 │   0.62    │  0.64  │   0.63   │   55    │
├─────────┼───────────┼────────┼──────────┼─────────┤
│ Average │   0.73    │  0.73  │   0.73   │   154   │
└─────────┴───────────┴────────┴──────────┴─────────┘
⚠️ Nhận xét:

Kết quả giống hệt SGD (73.38%)
Hội tụ chậm hơn Mini-batch GD
Cần nhiều thời gian tính toán nhất
🔍 Phân Tích Chi Tiết
📌 Diễn Giải Các Chỉ Số
Chỉ Số	Ý Nghĩa
Accuracy	Tỷ lệ dự đoán chính xác trên toàn bộ dữ liệu
Precision	Trong những trường hợp được dự đoán là bệnh, bao nhiêu % thực sự bệnh
Recall	Trong những trường hợp thực sự bệnh, mô hình phát hiện được bao nhiêu %
F1-Score	Trung bình điều hòa giữa Precision và Recall
Support	Số lượng mẫu thực tế trong tập test
🎯 Kết Luận
Mô hình tốt nhất: Logistic Regression (sklearn) với độ chính xác 75.32%
Tỷ lệ phát hiện bệnh: 67% (Recall = 0.67) - mô hình phát hiện được 2/3 bệnh nhân mắc tiểu đường
Độ cảnh báo sai: 35% (1 - Precision) - trong những bệnh nhân được dự đoán bệnh, 35% thực tế không bệnh
Mini-batch GD là lựa chọn tốt nếu cần cân bằng giữa hiệu suất và tốc độ
