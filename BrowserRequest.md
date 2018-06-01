# *Điều gì xảy ra khi trình duyệt của bạn truy cập vào một trang web ?*

## *Cách truy cập của một trình duyệt:*  
---

- Có một vài bước xảy ra cùng lúc khi bạn truy cập vào một trang web đến khi nó hiện lên màn hình:  
  1. Tra cứu DNS
  2. Gửi yêu cầu đến HTTP
  3. Máy chủ phản hồi và gửi lại tệp HTTP yêu cầu
  4. Trình duyệt thông dịch thành HTML
  5. Trình duyệt gửi yêu cầu bổ sung trong các đối tượng được nhúng trong file HTML (các file CSS, ảnh, javascript, ...)

### *Tra cứu DNS*
---  
- Bước đầu tiên khi yêu cầu 1 trang web là chuyển tên miền thành một địa chỉ IP.  
- Chúng ta có xu hướng vào một trang web nhiều lần, nên những địa chỉ IP của trang web sẽ được lưu lại trong bộ nhớ cache.  
- Danh sách thiết bị lưu trữ bộ nhớ cache theo thứ tự được chọn:  
  - Bộ nhớ cache của trình duyệt (Browser cache)  
  - Bộ nhớ cache của hệ điều hành (Operating system cache)  
  - Bộ nhớ cache định tuyến (Router cache)
  - Bộ nhớ cache ISP DNS (Internet Service Provider Domain Name Server cache)  

>*Việc tra cứu DNS trong máy chủ gốc (root server) không tốn nhiều thời gian nhưng sẽ nhanh hơn nếu nó được lưu trữ trong cache. Vì vậy, ta có thể cải thiện được việc tra cứu DNS bằng cách lưu trữ các ánh xạ trong bộ nhớ cache lâu hơn.*

### *Trình duyệt gửi yêu cầu*
---
