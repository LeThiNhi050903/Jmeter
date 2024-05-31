# Jmeter

Kết quả của thử nghiệm hiệu suất trên trang web Dân trí bằng Apache JMeter. Thử nghiệm bao gồm ba nhánh: Dantri, Thegioi, và Xahoi, với kết quả được hiển thị trong bảng "View Results in Table": 
![Screenshot 2024-05-31 074708](https://github.com/LeThiNhi050903/Jmeter/assets/124944063/5219c63b-6277-4636-a012-9407eb9cc412)

# Chi tiết các tham số và kết quả:

1. Cấu trúc Kế hoạch thử nghiệm (Test Plan)
- Test Plan: Test Plan
  + Thread Group: Dan tri
    * Sampler: Dantri
    * Sampler: Thegioi
    * Sampler: Xahoi 
- Listeners: View Results in Table, View Results Tree

2. Bảng kết quả thử nghiệm (View Results in Table)
- Các cột:
  + Sample #: Số thứ tự mẫu thử nghiệm.
  + Start Time: Thời gian bắt đầu mẫu thử nghiệm.
  + Thread Name: Tên luồng thử nghiệm.
  + Label: Nhãn của sampler, thể hiện tên từng sampler.
  + Sample Time (ms): Thời gian mẫu thử nghiệm (ms).
  + Status: Trạng thái của mẫu thử nghiệm (màu xanh lá cây biểu thị thành công).
  + Bytes: Số byte dữ liệu được nhận.
  + Sent Bytes: Số byte dữ liệu được gửi.
  + Latency: Độ trễ (ms).
  + Connect Time (ms): Thời gian kết nối (ms).
- Các mẫu thử nghiệm:
+ Mẫu 1:
  * Sample #: 1
  * Start Time: 07:46:05.699
  * Thread Name: Dan tri 1-1
  * Label: Dantri
  * Sample Time (ms): 951
  * Status: Thành công
  * Bytes: 591174
  * Sent Bytes: 230
  * Latency: 258
  * Connect Time (ms): 226
+ Mẫu 2:
  * Sample #: 2
  * Start Time: 07:46:06.651
  * Thread Name: Dan tri 1-1
  * Label: Thegioi
  * Sample Time (ms): 108
  * Status: Thành công
  * Bytes: 348952
  * Sent Bytes: 254
  * Latency: 14
  * Connect Time (ms): 0
+ Mẫu 3:
  * Sample #: 3
  * Start Time: 07:46:06.759
  * Thread Name: Dan tri 1-1
  * Label: Xahoi
  * Sample Time (ms): 230
  * Status: Thành công
  * Bytes: 374169
  * Sent Bytes: 250
  * Latency: 9
  * Connect Time (ms): 0
  *  
3. Phân tích
- Thời gian mẫu thử nghiệm (Sample Time): Thời gian thử nghiệm của các sampler khác nhau. Sampler "Dantri" có thời gian dài nhất (951 ms), trong khi "Thegioi" và "Xahoi" có thời gian ngắn hơn, lần lượt là 108 ms và 230 ms. Điều này có thể phản ánh độ phức tạp và dung lượng dữ liệu của từng trang.
- Độ trễ (Latency): Độ trễ của các mẫu thử nghiệm là khá thấp, đặc biệt với "Thegioi" (14 ms) và "Xahoi" (9 ms), cho thấy khả năng phản hồi nhanh. Độ trễ của "Dantri" cao hơn (258 ms), có thể do tải trang hoặc kích thước dữ liệu lớn hơn.
- Thời gian kết nối (Connect Time): Thời gian kết nối cho thấy "Dantri" mất 226 ms để thiết lập kết nối, trong khi "Thegioi" và "Xahoi" không mất thời gian kết nối, điều này có thể là do các kết nối đã được thiết lập sẵn từ trước đó.
- Số byte dữ liệu: Dữ liệu nhận được và gửi đi của từng sampler khác nhau. "Dantri" nhận được nhiều dữ liệu nhất (591174 bytes), trong khi "Thegioi" và "Xahoi" nhận được ít hơn, lần lượt là 348952 bytes và 374169 bytes.
4. Kết luận
- Hiệu suất: Kết quả cho thấy trang "Dantri" có thời gian tải lâu hơn và độ trễ cao hơn so với "Thegioi" và "Xahoi", có thể do kích thước và độ phức tạp của trang lớn hơn.
- Thành công: Tất cả các mẫu thử nghiệm đều thành công, không có lỗi nào xảy ra.
- Đề xuất cải tiến:
  + Tối ưu hóa thời gian tải: Cần tối ưu hóa thời gian tải của trang "Dantri" bằng cách giảm kích thước dữ liệu hoặc cải thiện mã nguồn.
  + Kiểm tra kết nối: Nghiên cứu thêm về thời gian kết nối của trang "Dantri" để giảm thiểu độ trễ ban đầu.
