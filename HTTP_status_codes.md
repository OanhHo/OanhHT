# HTTP response status codes
### 1.Information responses
-100: Continue
-101:
### 2.Successful responses
-200: Ok
-201: Created
-202: Accepted
### 3. Redirection messages
### 4.Client error responses
-400: Bad request
Server không hiểu yêu cầu do cú pháp không hợp lệ.
-401: Unauthorized
Mặc dù HTTP chỉ định "unauthorized" nhưng về ý nghĩa thì phản hồi này là "ununauthoried". Client phải tự xác thực để nhận được phản hồi đã yêu cầu.
-403: Forbiđen
Client không có quyền truy cập, vì vậy server từ chối cung cấp tài nguyên. Khác lỗi 401 là danh tính của khách hàng được server biết.
-404: Not found
Server không tìm thấy tài nguyên được yêu cầu. Trong trình duyệt, không timg thấy URL. Trong API, endpoint hợp lệ nhưng tài nguyên không tồn tại. Có thể thay phản hồi này cho phản hồi 403.
-405: Method Not Allowed
Phương thức yều cầu được biết bởi server nhưng đã bị vô hiệu hóa và không thể sử dung.
-406:Not acceptable
-407: Proxy Authentication Required
-408: Request Timeout
-409: Conflict

### 5.
