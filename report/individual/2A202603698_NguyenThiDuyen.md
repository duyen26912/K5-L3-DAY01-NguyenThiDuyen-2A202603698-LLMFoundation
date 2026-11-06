# LAB DAY 1 - AI Foundation & LLM - VIN - 20K

## 1. Giới thiệu

Đây là bài thực hành thuộc **AICB – Phase 1 – Day 1: AI Foundation & LLM**.

Dự án tập trung giải quyết bài toán phân loại tin nhắn SMS thành hai nhóm:

- **Spam:** Tin nhắn rác, quảng cáo hoặc lừa đảo.
- **Ham:** Tin nhắn bình thường, hợp lệ.

Bài thực hành sử dụng cùng một bộ dữ liệu để triển khai và so sánh 4 phương pháp tiếp cận AI: Machine Learning, Deep Learning, Embedding và Large Language Model (LLM).

## 2. Mục tiêu

- Hiểu quy trình xây dựng một mô hình phân loại văn bản.
- Thực hành xử lý và phân tích dữ liệu.
- Tự xây dựng Logistic Regression bằng NumPy.
- Xây dựng mạng Neural Network bằng PyTorch.
- Tìm hiểu Text Embedding và thuật toán K-Nearest Neighbors (kNN).
- Sử dụng LLM API để phân loại văn bản bằng Zero-shot và Few-shot Prompting.
- So sánh các mô hình dựa trên F1-score, độ trễ, tốc độ xử lý và chi phí.

## 3. Công nghệ sử dụng

| Công nghệ | Mục đích |
|---|---|
| Python | Ngôn ngữ lập trình chính |
| NumPy | Xử lý dữ liệu và tính toán |
| Pandas | Phân tích và xử lý dữ liệu |
| Matplotlib | Trực quan hóa kết quả |
| PyTorch | Xây dựng và huấn luyện MLP |
| Sentence Transformers | Tạo Text Embedding |
| LLM API | Phân loại văn bản bằng mô hình ngôn ngữ lớn |
| Google Colab | Môi trường thực thi notebook |

## 4. Nội dung thực hành

### Part 0 – Data Exploration
- Tải bộ dữ liệu SMS Spam Collection.
- Khám phá dữ liệu, kiểm tra tin nhắn trùng lặp.
- Làm sạch và chia dữ liệu thành Train, Validation và Test.
- Phân tích vấn đề Data Leakage và mất cân bằng dữ liệu.

### Part 1 – Machine Learning
- Xây dựng Bag of Words (BoW).
- Vector hóa văn bản.
- Cài đặt Sigmoid và Logistic Regression bằng NumPy.
- Huấn luyện bằng Gradient Descent.
- Đánh giá Accuracy, Precision, Recall và F1-score.

### Part 2 – Deep Learning
- Xây dựng Multi-Layer Perceptron (MLP) bằng PyTorch.
- Huấn luyện mô hình với Backpropagation.
- Theo dõi Train Loss và Validation Loss.
- Phân tích hiện tượng Overfitting.

### Part 3 – Text Embedding
- Sử dụng Sentence Transformer (MiniLM) để tạo Embedding.
- Tính Cosine Similarity.
- Tìm kiếm các câu có ý nghĩa tương đồng.
- Xây dựng mô hình kNN, Logistic Regression và MLP trên Embedding.

### Part 4 – Large Language Model (LLM)
- Kết nối LLM API.
- Xây dựng Prompt phân loại Spam/Ham.
- Thử nghiệm Zero-shot và Few-shot Prompting.
- Xây dựng hàm xử lý kết quả trả về.
- Đo lường độ trễ và ước tính chi phí API.
- Thử nghiệm Prompt Injection và Prompt phòng thủ.

### Part 5 – Model Comparison & Evaluation
- So sánh các phương pháp dựa trên F1-score và độ trễ.
- Phân tích biểu đồ Pareto.
- Thực hiện Stress Test với các trường hợp khó.
- Đề xuất hệ thống kết hợp nhiều mô hình (Router).
- Thực hiện thử thách cá nhân.

## 5. Dataset

**SMS Spam Collection Dataset**

- Nguồn: UCI / Kaggle.
- Link: https://www.kaggle.com/datasets/uciml/sms-spam-collection-dataset
- Tổng dữ liệu ban đầu: 5.572 tin nhắn.
- Hai nhãn phân loại: `spam` và `ham`.

Dữ liệu được loại bỏ các tin nhắn trùng lặp trước khi chia thành các tập Train, Validation và Test.

## 6. Cách chạy dự án

**Bước 1:** Mở file `day1_lab.ipynb` bằng Google Colab.

**Bước 2:** Điền mã sinh viên vào biến `STUDENT_ID` để tạo cách chia dữ liệu riêng.

**Bước 3:** Chạy lần lượt các cell từ trên xuống dưới hoặc chọn `Runtime → Run all`.

**Bước 4:** Đối với phần LLM, thiết lập API Key trong Colab Secrets. Notebook hỗ trợ các provider như OpenAI, Gemini, Groq, Anthropic, OpenRouter và Ollama.

**Bước 5:** Hoàn thành các TODO, thí nghiệm, câu hỏi và thử thách cá nhân.

**Bước 6:** Chạy báo cáo cuối để tổng hợp kết quả và tạo file `lab1_report.json`.

## 7. Kết quả và đánh giá

Các mô hình được đánh giá bằng:

- Accuracy
- Precision
- Recall
- F1-score
- Training Time
- Inference Latency (p50, p95)
- API Cost

Kết quả cho thấy mỗi phương pháp có ưu điểm riêng. Các mô hình BoW có tốc độ xử lý nhanh, Embedding giúp khai thác thông tin ngữ nghĩa, trong khi LLM có khả năng xử lý những trường hợp phức tạp tốt hơn nhưng thường có độ trễ và chi phí API cao hơn.

## 8. Cấu trúc bài nộp

report/
└── individual/
    ├── 2A202603698_NguyenThiDuyen.md
    ├── day01_lab.ipynb
    ├── lab1_report.json
    ├── hand_calc_1.jpg
    └── hand_calc_2.jpg

