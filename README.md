# Sentiment Analysis on IMDB Dataset

## Mô tả dự án

Dự án này nhằm phân loại cảm xúc của các đánh giá phim trên IMDB thành hai loại: **Tích cực** và **Tiêu cực**. Chúng ta sử dụng các phương pháp xử lý ngôn ngữ tự nhiên (NLP) để làm sạch dữ liệu, sau đó áp dụng các mô hình học máy như Decision Tree và Random Forest để dự đoán nhãn cảm xúc.

## Các bước xử lý

### 1. Xử lý dữ liệu:
- **Loại bỏ các đánh giá trùng lặp**: Để đảm bảo dữ liệu sạch và không bị lặp lại.
- **Mở rộng viết tắt**: Sử dụng thư viện `contractions` để mở rộng các từ viết tắt như `can't` thành `cannot`.
- **Loại bỏ thẻ HTML**: Sử dụng BeautifulSoup để xóa các thẻ HTML khỏi văn bản.
- **Loại bỏ biểu tượng cảm xúc và ký tự đặc biệt**: Xóa biểu tượng cảm xúc và các ký tự đặc biệt không liên quan.
- **Lemmatization**: Sử dụng WordNet Lemmatizer để đưa các từ về dạng nguyên mẫu (vd: "running" thành "run").
- **Loại bỏ stopwords**: Loại bỏ các từ không mang nhiều ý nghĩa như "the", "is",...

### 2. Trực quan hóa dữ liệu:
- **Biểu đồ tròn**: Biểu diễn tần suất của các nhãn cảm xúc tích cực và tiêu cực.
- **Biểu đồ phân bố từ**: Trực quan hóa độ dài của các đánh giá theo từng loại cảm xúc.
- **Biểu đồ phân phối hạt nhân (KDE)**: Hiển thị phân phối từ ngữ của các đánh giá.

### 3. Mô hình hóa:
- **Chia dữ liệu**: Sử dụng `train_test_split` để chia dữ liệu thành tập huấn luyện (80%) và tập kiểm tra (20%).
- **Tính năng TF-IDF**: Chuyển đổi văn bản thành vector số sử dụng phương pháp TF-IDF.
- **Decision Tree**: Xây dựng mô hình cây quyết định để dự đoán nhãn cảm xúc.
- **Random Forest**: Áp dụng mô hình rừng ngẫu nhiên để cải thiện độ chính xác.

## Cách sử dụng

### 1. Cài đặt các gói cần thiết:
Trước khi chạy dự án, bạn cần cài đặt các thư viện cần thiết:

    pip install 
    contractions 
    beautifulsoup4 
    nltk scikit-learn 
    seaborn 
    matplotlib 
    pandas

### 2. Tải dữ liệu:
Đảm bảo rằng bạn đã tải xuống và lưu file dữ liệu IMDB dưới tên IMDB-Dataset.csv.

### 3. Chạy dự án:
Chạy file Python chính để thực hiện các bước xử lý và huấn luyện mô hình:
    
    python main.py

### 4. Kết quả
Dự án sẽ hiển thị các biểu đồ trực quan hóa và kết quả dự đoán của các mô hình như Decision Tree và Random Forest. Độ chính xác của mô hình sẽ được tính toán và hiển thị cuối cùng.

Yêu cầu hệ thống
    
    Python 3.x
    Các thư viện như:  
    nltk, beautifulsoup4, scikit-learn, seaborn,  matplotlib, pandas

