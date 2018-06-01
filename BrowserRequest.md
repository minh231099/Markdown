# *Điều gì xảy ra khi trình duyệt của bạn truy cập vào một trang web ?*

## *Cách thức truy cập của một trình duyệt:*  

- Có một vài bước xảy ra cùng lúc khi bạn truy cập vào một trang web đến khi nó hiện lên màn hình:  
  1. Tra cứu DNS
  2. Gửi truy cập HTTP
  3. Máy chủ phản hồi và gửi lại tệp yêu cầu
  4. Thông dịch thành HTML
  5. Gửi yêu cầu bổ sung trong các đối tượng được nhúng trong file HTML (các file CSS, ảnh, javascript, ...)

### *Tra cứu DNS*
---  
- Bước đầu tiên khi yêu cầu 1 trang web là **chuyển tên miền thành một địa chỉ IP**.  
- Chúng ta có xu hướng vào một trang web nhiều lần, nên những địa chỉ IP của trang web sẽ được lưu lại trong bộ nhớ cache.  
- Danh sách thiết bị lưu trữ bộ nhớ cache theo thứ tự được chọn:  
  - Bộ nhớ cache của trình duyệt (Browser cache)  
  - Bộ nhớ cache của hệ điều hành (Operating system cache)  
  - Bộ nhớ cache định tuyến (Router cache)
  - Bộ nhớ cache ISP DNS (Internet Service Provider Domain Name Server cache)  

>*Việc tra cứu DNS trong máy chủ gốc (root server) không tốn nhiều thời gian nhưng sẽ nhanh hơn nếu nó được lưu trữ trong cache. Vì vậy, ta có thể cải thiện được việc tra cứu DNS bằng cách lưu trữ các ánh xạ trong bộ nhớ cache lâu hơn.*

### *Trình duyệt gửi yêu cầu*
---  
- Sau khi tra cứu DNS xong, trình duyệt sẽ **truy cập HTTP đến máy chủ thích hợp**. Không bắt buộc phải là HTTP, còn có thể là HTPPS hoặc HTTP/2. Để yêu cầu một file cụ thể nào đó, thường là HTML.  

### *Máy chủ phản hồi*
---  
- Khi máy chủ nhận được yêu cầu, nó sẽ phản hồi lại, kết quả phản hồi sẽ phụ thuộc vào một vài vấn đề. 
>*Ví dụ: khi tệp tin không còn sẽ trả lại 404 (file not found) error, 200 OK nghĩa là truy cập thành công, ...* 

### *Trình duyệt hiện thị trang*
---  
- Sau khi nhận được file HTML trình duyệt sẽ hiện thị trang, sau khi trải qua một vài bước được gọi là **đường dẫn hiển thi**:
  - Xử lý đánh dấu file HTML và xây dựng giao diện DOM (Dom tree).  
  - Xử lý đánh dấu CSS và xây dựng mô hình đối tượng CSS (CSSMD tree).
  - Kết hợp DOM và CSSMD thành một cây kết xuất.
  - Chạy tổng thể để tính toán tương thích từng mắt cây (node).
  - Vẽ lại từng node lên màn hình.

Tham khảo tại : [What Happens When Your Browser Requests a Web Page?](https://vanseodesign.com/web-design/browser-requests/)
# END!
