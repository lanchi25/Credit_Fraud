# Xây dựng mô hình xác định gian lận giao dịch thẻ tín dụng (Credit Fraud Detection)


## I. Giới thiệu
_**Đặt vấn đề**_:  
Thẻ tín dụng là một phương thức thanh toán phổ biến được sử dụng rộng rãi, những kẻ tấn công cố gắng đánh cắp thông tin thẻ tín dụng để có thể mua sắm, tiêu xài với chi phí của chủ sở hữu thẻ.  
Khi chủ sở hữu thẻ tín dụng nhìn thấy các mục trong hóa đơn mua hàng bằng thẻ tín dụng mà họ chưa bao giờ thực hiện, họ yêu cầu hoàn lại tiền, dẫn đến khoản bồi hoàn. Các doanh nghiệp, bao gồm các thương gia, công ty thẻ tín dụng, nhà cung cấp dịch vụ thanh toán và ngân hàng, đang mất hàng tỷ đô la mỗi năm do gian lận thẻ tín dụng. Người tiêu dùng có thể bị ảnh hưởng bởi điểm tín dụng thấp hơn và phí cao hơn.  
=> Cần chuẩn bị và triển khai phần mềm để phát hiện gian lận trong giao dịch thẻ tín dụng thông minh để ngăn chặn gian lận thẻ tín dụng và giảm thiểu tổn thất lớn nhất. 

_**Phát hiện gian lận thẻ tín dụng**_:  
Là quá trình sử dụng các công cụ và giải pháp phần mềm để xác định và thực hiện các biện pháp thích hợp nhằm ngăn chặn hoặc giảm thiểu tác động của việc lạm dụng thẻ tín dụng. Phần mềm phát hiện gian lận thẻ tín dụng sử dụng các công nghệ mới nhất như trí tuệ nhân tạo và học máy để phân tích một lượng lớn dữ liệu giúp đưa ra quyết định dựa trên dữ liệu.  

_**Xây dựng mô hình với bộ dữ liệu thực tế**_:  
Tiến hành xử lý tập dữ liệu và xây dựng mô hình dự đoán bằng các thuật toán học máy khác nhau. Sau đó, so sánh hiệu suất, đánh giá các chỉ số của mô hình dự đoán để đưa ra được mô hình tốt trong số các thuật toán học máy được sử dụng.  

_**Mục tiêu**_:  
    + Hiểu được sự phân bố của tập dữ liệu và nắm các kỹ thuật tiền xử lý  
    + Nhận biết được dấu hiệu bộ dữ liệu mất cân bằng và áp dụng các kỹ thuật để xử lý mẫu  
    + Áp dụng được các thuật toán phân loại sẽ sử dụng và quyết định chọn lựa thuật toán có độ chính xác cao hơn    
    + So sánh độ chính xác của mô hình được xây dựng từ hai phương pháp xử lý mẫu khác nhau  
    + Hiểu được lỗi phát sinh khi sử dụng với tập dữ liệu mất cân bằng  


## II. Phân tích
[Click here and wait a second](https://github.com/lanchi25/Credit_Fraud/blob/main/nguyenthilanchi_predict_fraud.ipynb)
### 1. Xây dựng mô hình
1. Đọc dữ liệu  
2. Thống kê dữ liệu  
3. Tiền xử lý dữ liệu  
4. Chia dữ liệu thành tập train và test  
5. Lựa chọn và huấn luyện mô hình phân lớp  
6. Đánh giá mô hình  

### 2. Cải tiến mô hình
1. Xây dựng mô hình với phương pháp xử lý mẫu Random UnderSampling kết hợp Cross-Validation đồng thời  
1.1 Huấn luyện mô hình  
1.2 Đánh giá mô hình mới  
1.3 Đánh giá hiệu suất thuật toán đã chọn  

2. Xây dựng mô hình với phương pháp xử lý mẫu SMOTE kết hợp Cross-Validation đồng thời  
2.1 Huấn luyện mô hình mới  
2.2 Đánh giá mô hình mới  

3. So sánh hai phương pháp lấy mẫu  

## III. Kết luận
Việc triển khai trên tập dữ liệu mất cân bằng để xây dựng mô hình theo các quy trình tuần tự thông thường thì dễ gây ra rủi ro mô hình bị quá khớp. Nên cần có các phương pháp lấy mẫu dưới mức hoặc lấy mẫu quá mức để mô hình được xây dựng dự đoán tốt hơn.  
Trong quá trình lấy mẫu và xác thực để xây dựng và lựa chọn được mô hình tốt thì phải thực hiện đúng cách, đó là hai việc đó phải được thực hiện đồng thời chứ không phải lấy mẫu rồi mới đi xác thực chéo như vậy mô hình sẽ bị overfitting.  

Khi triển khai SMOTE trên tập dữ liệu mất cân bằng đã giúp chúng ta giải quyết tình trạng mất cân bằng nhãn. Tuy nhiên, đôi khi việc lấy mẫu quá mức dự đoán sẽ kém chính xác hơn sơ với mô hình sử dụng trên tập dữu liệu lấy mẫu dưới mức. Và hiện tại trong bài này, thì việc xử lý ngoại lai được sử dụng trên tập dữ liệu dưới mức chứ không phải trên tập dữ liệu lấy mẫu quá mức.  
Ngoài ra, trong dữ liệu lấy mẫu dưới mức, mô hình không thể phát hiện một số lượng lớn các trường hợp giao dịch không gian lận và thay vào đó, phân loại sai các giao dịch không gian lận đó thành gian lận. Điều đó, sẽ gây phiền hà cho khách hàng sử dụng giao dịch, mặc dù không gây ra thiệt hại nhiều về tài sản cho khách hàng.  

Hướng tiếp theo của việc phân tích rút ra từ bài này sẽ là loại bỏ các ngoại lệ trên tập dữ liệu lấy mẫu quá mức và xem liệu độ chính xác trong mô hình thử nghiệm có được cải thiện hay không?

## IV. Tài liệu tham khảo
[1] Credit Card Fraud Detection Database, Anonymized credit card transactions labeled as fraudulent or genuine, https://www.kaggle.com/mlg-ulb/creditcardfraud  
[2] Principal Component Analysis, Wikipedia Page, https://en.wikipedia.org/wiki/Principal_component_analysis  
[3] ROC-AUC characteristic, https://en.wikipedia.org/wiki/Receiver_operating_characteristic#Area_under_the_curve  
[4] DEALING WITH IMBALANCED DATA: UNDERSAMPLING, OVERSAMPLING AND PROPER CROSS-VALIDATION  
[5] SMOTE explained for noobs  
[6] Machine Learning - Over-& Undersampling - Python/ Scikit/ Scikit-Imblearn by Coding-Maniac  
[7] Hands on Machine Learning with Scikit-Learn & TensorFlow by Aurélien Géron (O'Reilly). CopyRight 2017 Aurélien Géron  
[8] How to Use Statistics to Identify Outliers in Data by Jason Brownless (Machine Learning Mastery blog)  

