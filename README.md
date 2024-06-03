# testing-with-JMeter
## Giới thiệu
Trong báo cáo này, chúng tôi sẽ trình bày quá trình kiểm thử hiệu năng của một trang web trường học sử dụng công cụ Apache JMeter. Mục tiêu của kiểm thử là đánh giá khả năng chịu tải và hiệu năng của trang web dưới các điều kiện tải khác nhau.


## Công cụ sử dụng
JMeter là một công cụ mã nguồn mở mạnh mẽ, được sử dụng để kiểm thử tải và hiệu năng của các ứng dụng web.
Mục tiêu kiểm thử
Đánh giá khả năng chịu tải của trang web phenikaa uni.
Kiểm tra hiệu năng của các trang chính trên website dưới các điều kiện tải khác nhau.
Xác định ngưỡng chịu tải của trang web trước khi bắt đầu gặp lỗi.
Thiết lập 
Mô tả: Thiết lập số lượng người dùng ảo và chu kỳ kiểm thử.
Cấu hình: 100 người dùng, thời gian chờ là 20 giây, số lần lặp là 10.


![]()
## Kết quả kiểm thử
Sau khi chạy kiểm thử , kết quả có thể biểu diễn qua các loại report như: biểu đồ, dạng báo cáo, dạng cây v.v.
Kết quả theo dạng cây

Hình 6.2 kết quả hiển thị theo dạng cây
kết quả cho thấy một yêu cầu HTTP cụ thể mất 23759 ms để hoàn thành với thời gian kết nối là 8 ms và độ trễ là 63 ms. Kích thước phản hồi là 1619583 bytes và mã phản hồi là 200. Thời gian tải dài và kích thước phản hồi lớn chỉ ra rằng cần phải tối ưu hóa để giảm thời gian phản hồi và kích thước dữ liệu, nhằm cải thiện hiệu suất trang web.
Kết quả hiển thị theo dạng báo cáo tổng hợp

Hình 6.3 kết quả hiển thị theo dạng báo cáo tổng hợp
Kết quả kiểm thử cho thấy server có thể xử lý 1100 yêu cầu với thời gian phản hồi trung bình là 6929.96 ms. Tỉ lệ lỗi 0.36% là khá thấp, cho thấy hệ thống hoạt động ổn định dưới tải. Thông lượng 4.02 yêu cầu/giây và tốc độ truyền tải dữ liệu cũng cho thấy server có khả năng xử lý tốt. Tuy nhiên, thời gian phản hồi trung bình khá cao, cần xem xét tối ưu hóa để cải thiện tốc độ phản hồi của hệ thống.
Kết quả hiển thị theo dạng bảng

Hình 6.4 kết quả hiển thị theo dạng bảng
Trong quá trình kiểm thử tải trang web, các yêu cầu HTTP được gửi và tất cả đều thành công với mã phản hồi 200. Thời gian tải trung bình là khoảng 1068 ms, với thời gian nhanh nhất là 754 ms và chậm nhất là 1979 ms. Kích thước phản hồi chủ yếu là 1619583 bytes, ngoại trừ một trường hợp đặc biệt. Độ trễ trung bình là 29 ms, với mức thấp nhất là 5 ms và cao nhất là 73 ms. Thời gian kết nối trung bình là 5 ms, với nhiều yêu cầu có thời gian kết nối là 0 ms. Kết quả cho thấy trang web hoạt động ổn định dưới tải hiện tại, nhưng có thể cần tối ưu hóa thêm để cải thiện hiệu suất.
Kết quả hiển thị theo dạng biểu đồ

Hình 6.5 kết quả hiển thị theo dạng biểu đồ
Biểu đồ cho thấy trang web có khả năng xử lý trung bình 240.965 yêu cầu/phút với thời gian phản hồi trung bình là 18029 ms và thời gian phản hồi trung vị là 21078 ms. Độ lệch chuẩn cao (6929 ms) chỉ ra sự biến động lớn trong thời gian phản hồi, với thời gian tải lâu nhất là 20616 ms. Kết quả này cho thấy trang web có thể xử lý nhiều yêu cầu nhưng cần tối ưu hóa để giảm thời gian xử lý và đảm bảo hiệu suất ổn định hơn.
## Kết luận
Trang web có khả năng xử lý một lượng lớn yêu cầu với thông lượng cao, tuy nhiên, thời gian phản hồi trung bình dài và sự biến động lớn trong thời gian phản hồi chỉ ra rằng cần có sự tối ưu hóa để cải thiện hiệu suất. Việc giảm thời gian xử lý và đảm bảo tính nhất quán trong hiệu suất sẽ nâng cao trải nghiệm người dùng và độ tin cậy của trang web. Cần tập trung vào các yếu tố gây ra thời gian phản hồi dài để tiến hành các biện pháp cải thiện hiệu quả.
