# Sentiment Analysis for Film Reviews

## Mục tiêu dự án

Dự án này nhằm tối ưu hóa tiết kiệm thời gian và chi phí trong ngành công nghiệp điện ảnh bằng cách tự động hóa quá trình phân tích cảm xúc (sentiment analysis) từ các đánh giá, bình luận phim. Mục tiêu chính là phân loại các đánh giá thành tích cực hoặc tiêu cực, giúp các nhà làm phim và nhà phân phối nắm bắt nhanh chóng phản hồi của khán giả.

## Tổng quan về dự án

- **Xử lý ngôn ngữ tự nhiên (NLP):** Làm sạch, token hóa, loại bỏ stopwords, stemming/lemmatization cho dữ liệu đánh giá phim.
- **Vector hóa văn bản:** Sử dụng CountVectorizer và TfidfVectorizer để chuyển đổi văn bản thành các vector số học.
- **Huấn luyện mô hình:** Áp dụng các mô hình phân loại như Logistic Regression, SGDClassifier, Multinomial Naive Bayes, và Support Vector Classifier (SVC).
- **Đánh giá mô hình:** Sử dụng các chỉ số accuracy, classification report, confusion matrix để đánh giá hiệu suất.
- **Phân tích cảm xúc với TextBlob:** Tính toán điểm polarity và subjectivity cho từng đánh giá.
- **Trực quan hóa dữ liệu:** Vẽ biểu đồ phân phối cảm xúc, word cloud, và các biểu đồ thống kê khác.

## Các bước thực hiện chính

1. **Import thư viện**
   - Sử dụng các thư viện như numpy, pandas, seaborn, matplotlib, nltk, scikit-learn, spacy, TextBlob, wordcloud.
2. **Load dữ liệu**
   - Đọc dữ liệu đánh giá phim (ví dụ: 50.000 mẫu, mỗi mẫu có nhãn cảm xúc 0/1 tương ứng tiêu cực/tích cực).
   - Thêm trường review_length để phân tích độ dài đánh giá.
3. **Tiền xử lý dữ liệu**
   - Làm sạch văn bản, token hóa, loại bỏ stopwords, stemming/lemmatization.
4. **Vector hóa văn bản**
   - Sử dụng CountVectorizer và TfidfVectorizer để chuyển đổi văn bản thành vector.
5. **Huấn luyện mô hình**
   - Áp dụng các mô hình phân loại: Logistic Regression, SGDClassifier, MultinomialNB, SVC.
6. **Đánh giá mô hình**
   - Sử dụng các chỉ số accuracy, classification report, confusion matrix.
7. **Phân tích cảm xúc với TextBlob**
   - Tính điểm polarity, subjectivity cho từng đánh giá.
8. **Trực quan hóa dữ liệu**
   - Vẽ biểu đồ phân phối cảm xúc, word cloud, và các biểu đồ thống kê khác.

## Cách sử dụng

1. **Chạy notebook:**  
   - Mở file `sentiment_analysis.ipynb` trên Jupyter Notebook hoặc Google Colab.
   - Chạy lần lượt các cell để thực hiện các bước phân tích từ đầu đến cuối.
2. **Tùy chỉnh dữ liệu:**  
   - Thay đổi đường dẫn file dữ liệu nếu cần thiết.
3. **Tùy chỉnh mô hình:**  
   - Có thể thử nghiệm với các mô hình phân loại khác hoặc điều chỉnh tham số cho phù hợp.

## Các thư viện chính

- **numpy, pandas:** Xử lý dữ liệu
- **seaborn, matplotlib:** Trực quan hóa dữ liệu
- **nltk, spacy:** Xử lý ngôn ngữ tự nhiên
- **scikit-learn:** Vector hóa văn bản và huấn luyện mô hình
- **TextBlob:** Phân tích cảm xúc
- **wordcloud:** Tạo word cloud

## Dữ liệu đầu vào

- **File dữ liệu:** Chứa các cột `review` (nội dung đánh giá) và `sentiment` (nhãn cảm xúc: 0 = tiêu cực, 1 = tích cực).
- **Ví dụ:**  
  - `review`: "My family and I normally do not watch local movies..."  
  - `sentiment`: 1

## Kết quả đầu ra

- **Phân loại cảm xúc:** Mỗi đánh giá được gán nhãn tích cực hoặc tiêu cực.
- **Biểu đồ phân phối cảm xúc:** Trực quan hóa phân bố nhãn cảm xúc.
- **Word cloud:** Trực quan hóa các từ xuất hiện nhiều nhất trong đánh giá.
- **Đánh giá mô hình:** Các chỉ số accuracy, classification report, confusion matrix.
