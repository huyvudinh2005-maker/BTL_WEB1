# HỆ THỐNG QUẢN LÍ NHÀ HÀNG

## 1. Giới thiệu đề tài

Đề tài xây dựng **website quản lí nhà hàng/quán cà phê** theo mô hình hệ thống gồm **khách hàng**, **nhân viên/quản trị viên**, **bàn ăn** và **khu vực quản lí món ăn - đơn hàng - thanh toán**.  
Hệ thống cho phép khách hàng quét **mã QR tại từng bàn** để truy cập vào trang gọi món của chính bàn đó, lựa chọn sản phẩm, đặt món trực tiếp trên web, theo dõi trạng thái đơn hàng; đồng thời phía quản trị có thể quản lí bàn, thực đơn, đơn hàng, người dùng, khuyến mãi và doanh thu.

Mục tiêu của hệ thống là hỗ trợ số hóa quy trình phục vụ trong nhà hàng, giảm thao tác thủ công, tăng tốc độ phục vụ và nâng cao trải nghiệm khách hàng.

---

## 2. Mục tiêu xây dựng hệ thống

- Xây dựng một hệ thống quản lí nhà hàng hoạt động trên nền tảng web.
- Cho phép **khách hàng gọi món bằng QR theo từng bàn**.
- Cho phép **quản trị viên/nhân viên** quản lí thực đơn, đơn hàng, bàn, thanh toán và báo cáo.
- Hỗ trợ quản lí trạng thái đơn hàng theo thời gian thực.
- Hỗ trợ lưu trữ dữ liệu tập trung trong cơ sở dữ liệu để dễ thống kê và mở rộng.

---

## 3. Phạm vi bài toán

Hệ thống tập trung giải quyết các nghiệp vụ chính sau:

### 3.1. Đối với khách hàng
- Quét mã QR tại bàn để vào đúng trang đặt món của bàn đó.
- Xem danh sách món ăn/đồ uống.
- Xem chi tiết món: tên, giá, mô tả, hình ảnh, size, topping.
- Thêm món vào giỏ hàng.
- Đặt món trực tiếp từ bàn đang ngồi.
- Theo dõi trạng thái đơn hàng.
- Có thể gọi thêm món nhiều lần trong cùng một bàn.

### 3.2. Đối với quản trị viên / nhân viên
- Quản lí danh mục món ăn.
- Quản lí sản phẩm/món ăn.
- Quản lí bàn ăn.
- Sinh mã QR cho từng bàn.
- Theo dõi đơn hàng theo thời gian thực.
- Cập nhật trạng thái đơn hàng: chờ xác nhận, đang chuẩn bị, đang phục vụ, đã thanh toán, đã hủy.
- Quản lí tài khoản người dùng và phân quyền.
- Quản lí thanh toán.
- Quản lí khuyến mãi.
- Xem thống kê doanh thu và số lượng đơn hàng.

---

## 4. Mô hình hoạt động tổng quát

Hệ thống hoạt động theo quy trình sau:

1. Quản trị viên tạo bàn trong hệ thống.
2. Mỗi bàn được gán một mã định danh riêng và sinh ra một mã QR tương ứng.
3. Khách hàng đến quán, ngồi tại bàn và quét QR.
4. Hệ thống mở trang đặt món tương ứng với bàn đó.
5. Khách hàng chọn món, thêm vào giỏ và gửi đơn.
6. Đơn hàng được chuyển đến trang quản trị để nhân viên tiếp nhận.
7. Nhân viên cập nhật trạng thái đơn hàng trong quá trình xử lí.
8. Sau khi phục vụ xong, hệ thống tiến hành thanh toán và lưu lịch sử đơn hàng.

---

## 5. Các tác nhân trong hệ thống

### 5.1. Khách hàng
Là người trực tiếp quét QR tại bàn và tạo đơn hàng.

### 5.2. Nhân viên
Là người tiếp nhận đơn hàng, theo dõi trạng thái và hỗ trợ phục vụ.

### 5.3. Quản trị viên
Là người quản lí toàn bộ hệ thống: món ăn, bàn, tài khoản, đơn hàng, thanh toán, báo cáo.

---

## 6. Đặc tả nghiệp vụ chi tiết

## 6.1. Nghiệp vụ quản lí tài khoản

### Mô tả
Hệ thống cho phép quản lí tài khoản người dùng để phục vụ đăng nhập và phân quyền.

### Chức năng
- Đăng ký tài khoản.
- Đăng nhập / đăng xuất.
- Phân quyền người dùng (Admin, Nhân viên, Khách hàng nếu có).
- Cập nhật thông tin cá nhân.
- Khóa / mở khóa tài khoản.

### Kết quả
Giúp hệ thống xác định đúng vai trò người dùng khi truy cập các chức năng khác nhau.

---

## 6.2. Nghiệp vụ quản lí danh mục

### Mô tả
Danh mục dùng để phân loại món ăn/đồ uống như: Cà phê, Trà sữa, Nước ép, Đồ ăn nhanh, Món chính, Tráng miệng...

### Chức năng
- Thêm danh mục.
- Sửa danh mục.
- Xóa danh mục.
- Hiển thị danh sách danh mục.

### Kết quả
Giúp thực đơn được tổ chức rõ ràng, dễ tìm kiếm và dễ quản lí.

---

## 6.3. Nghiệp vụ quản lí sản phẩm / món ăn

### Mô tả
Quản trị viên quản lí toàn bộ món ăn, đồ uống hiển thị trên website.

### Chức năng
- Thêm món mới.
- Cập nhật thông tin món.
- Xóa món.
- Upload hình ảnh món ăn.
- Thiết lập giá bán.
- Thiết lập mô tả món ăn.
- Gắn danh mục cho món.
- Thiết lập size cho món (S, M, L...).
- Thiết lập topping đi kèm.
- Bật / tắt trạng thái kinh doanh của món.

### Kết quả
Đảm bảo thực đơn trên website luôn đồng bộ với thực tế kinh doanh.

---

## 6.4. Nghiệp vụ quản lí bàn ăn

### Mô tả
Mỗi bàn trong nhà hàng được lưu trong hệ thống để phục vụ việc gọi món và quản lí trạng thái phục vụ.

### Chức năng
- Thêm bàn mới.
- Cập nhật tên/số bàn.
- Xóa bàn.
- Cập nhật trạng thái bàn (trống, đang phục vụ, đã đặt trước, đang chờ thanh toán...).
- Sinh mã QR cho từng bàn.
- In hoặc tải QR để dán tại bàn.

### Kết quả
Mỗi bàn có một mã truy cập riêng, giúp khách hàng vào đúng trang gọi món của bàn mình.

---

## 6.5. Nghiệp vụ khách hàng quét QR và gọi món

### Mô tả
Đây là nghiệp vụ trung tâm của hệ thống. Khách hàng sử dụng điện thoại quét mã QR trên bàn để truy cập website đặt món.

### Chức năng
- Nhận diện bàn thông qua mã QR.
- Hiển thị thực đơn theo bàn đang hoạt động.
- Chọn món, chọn size, chọn topping.
- Nhập số lượng.
- Thêm vào giỏ hàng.
- Gửi đơn hàng.
- Gọi thêm món sau khi đã có đơn trước đó.

### Kết quả
Khách hàng có thể tự đặt món mà không cần nhân viên ghi order thủ công.

---

## 6.6. Nghiệp vụ quản lí giỏ hàng

### Mô tả
Giỏ hàng là nơi lưu tạm các món mà khách hàng lựa chọn trước khi gửi đơn.

### Chức năng
- Thêm món vào giỏ.
- Tăng / giảm số lượng.
- Xóa món khỏi giỏ.
- Tính tạm tính cho từng món.
- Tính tổng tiền đơn hàng.
- Gửi đơn hàng từ giỏ hàng.

### Kết quả
Hỗ trợ khách hàng dễ dàng kiểm tra món đã chọn trước khi xác nhận order.

---

## 6.7. Nghiệp vụ quản lí đơn hàng

### Mô tả
Sau khi khách gửi order, hệ thống tạo một đơn hàng tương ứng với bàn.

### Chức năng
- Tạo đơn hàng mới.
- Lưu danh sách món trong đơn.
- Gắn đơn hàng với bàn.
- Gắn đơn hàng với khách hàng (nếu có tài khoản).
- Hiển thị đơn hàng trên trang quản trị.
- Cập nhật trạng thái đơn hàng.
- Tìm kiếm và lọc đơn hàng.

### Các trạng thái đơn hàng có thể gồm
- Chờ xác nhận.
- Đã xác nhận.
- Đang chuẩn bị.
- Đang phục vụ.
- Hoàn thành.
- Đã thanh toán.
- Đã hủy.

### Kết quả
Giúp nhân viên theo dõi tiến độ xử lí món ăn một cách rõ ràng và chính xác.

---

## 6.8. Nghiệp vụ cập nhật đơn hàng theo thời gian thực

### Mô tả
Đơn hàng sau khi khách gửi cần được chuyển ngay đến giao diện quản trị để nhân viên xử lí.

### Chức năng
- Tự động đẩy đơn hàng mới lên trang admin.
- Cập nhật trạng thái đơn theo thời gian thực.
- Đồng bộ trạng thái để khách hàng và admin cùng nhìn thấy.

### Gợi ý kỹ thuật
Có thể sử dụng **Socket.IO / WebSocket** để gửi dữ liệu đơn hàng từ bàn lên hệ thống quản trị theo thời gian thực.

### Kết quả
Giảm độ trễ trong việc nhận order và nâng cao hiệu quả phục vụ.

---

## 6.9. Nghiệp vụ thanh toán

### Mô tả
Sau khi khách sử dụng dịch vụ xong, nhân viên tiến hành thanh toán cho bàn.

### Chức năng
- Tính tổng tiền đơn hàng.
- Áp dụng khuyến mãi nếu có.
- Lưu hình thức thanh toán.
- Cập nhật trạng thái đã thanh toán.
- Lưu lịch sử thanh toán.

### Hình thức thanh toán có thể hỗ trợ
- Tiền mặt.
- Chuyển khoản.
- Ví điện tử.
- Thẻ ngân hàng.

### Kết quả
Đảm bảo việc thanh toán minh bạch và dễ kiểm soát.

---

## 6.10. Nghiệp vụ khuyến mãi

### Mô tả
Hệ thống hỗ trợ tạo chương trình giảm giá để áp dụng cho đơn hàng hoặc sản phẩm.

### Chức năng
- Tạo mã khuyến mãi.
- Thiết lập phần trăm giảm giá hoặc số tiền giảm.
- Quy định thời gian áp dụng.
- Áp dụng theo điều kiện đơn hàng.
- Bật / tắt chương trình khuyến mãi.

### Kết quả
Hỗ trợ hoạt động marketing và thu hút khách hàng.

---

## 6.11. Nghiệp vụ đặt bàn trước (nếu mở rộng)

### Mô tả
Ngoài việc khách đến trực tiếp và quét QR, hệ thống có thể mở rộng thêm chức năng đặt bàn trước.

### Chức năng
- Khách chọn ngày giờ đặt bàn.
- Chọn số lượng người.
- Nhập thông tin liên hệ.
- Nhân viên xác nhận hoặc từ chối yêu cầu đặt bàn.

### Kết quả
Hỗ trợ nhà hàng quản lí lượng khách tốt hơn trong giờ cao điểm.

---

## 6.12. Nghiệp vụ thống kê - báo cáo

### Mô tả
Quản trị viên cần theo dõi hiệu quả kinh doanh thông qua các chỉ số tổng hợp.

### Chức năng
- Thống kê doanh thu theo ngày/tháng/năm.
- Thống kê số lượng đơn hàng.
- Thống kê món bán chạy.
- Thống kê bàn hoạt động nhiều.
- Thống kê hình thức thanh toán.

### Kết quả
Giúp quản trị viên đưa ra quyết định kinh doanh chính xác hơn.

---

## 7. Yêu cầu chức năng

Hệ thống cần đáp ứng các yêu cầu chức năng sau:

- Quản lí tài khoản và phân quyền.
- Quản lí danh mục sản phẩm.
- Quản lí món ăn/đồ uống.
- Quản lí bàn ăn.
- Sinh mã QR cho từng bàn.
- Khách hàng gọi món theo bàn.
- Quản lí giỏ hàng.
- Tạo và cập nhật đơn hàng.
- Cập nhật trạng thái theo thời gian thực.
- Thanh toán đơn hàng.
- Quản lí khuyến mãi.
- Thống kê và báo cáo.

---

## 8. Yêu cầu phi chức năng

### 8.1. Hiệu năng
- Hệ thống phản hồi nhanh khi khách hàng truy cập menu và đặt món.
- Hạn chế độ trễ khi đồng bộ đơn hàng giữa khách và admin.

### 8.2. Bảo mật
- Mật khẩu cần được mã hóa.
- Phân quyền rõ ràng giữa admin, nhân viên và khách hàng.
- Kiểm soát truy cập API.

### 8.3. Khả năng mở rộng
- Dễ dàng thêm món, thêm bàn, thêm chi nhánh trong tương lai.
- Có thể mở rộng sang mô hình nhà hàng nhiều cơ sở.

### 8.4. Tính dễ sử dụng
- Giao diện thân thiện với điện thoại vì khách hàng chủ yếu quét QR bằng mobile.
- Giao diện quản trị rõ ràng, dễ thao tác.

---

## 9. Tác nhân và use case chính

| Tác nhân | Use case |
|----------|----------|
| Khách hàng | Quét QR, xem menu, chọn món, đặt món, xem trạng thái đơn |
| Nhân viên | Nhận đơn, cập nhật trạng thái, hỗ trợ thanh toán |
| Quản trị viên | Quản lí món ăn, danh mục, bàn, người dùng, doanh thu, khuyến mãi |

---

## 10. Dữ liệu chính của hệ thống

Các bảng dữ liệu chính có thể gồm:

- `roles`: phân quyền người dùng.
- `users`: thông tin tài khoản.
- `categories`: danh mục món.
- `products`: thông tin món ăn/đồ uống.
- `product_sizes`: các size của món.
- `toppings`: topping đi kèm.
- `coffee_tables` hoặc `restaurant_tables`: thông tin bàn.
- `orders`: thông tin đơn hàng.
- `order_items`: chi tiết từng món trong đơn.
- `payments`: thông tin thanh toán.
- `promotions`: chương trình khuyến mãi.
- `reservations`: đặt bàn trước (nếu có).

---

## 11. Công nghệ dự kiến sử dụng

### Frontend
- Next.js / React.js
- HTML, CSS, JavaScript
- Có thể dùng Bootstrap hoặc CSS thuần nếu không dùng Tailwind

### Backend
- FastAPI hoặc Node.js/Express
- RESTful API
- Socket.IO / WebSocket cho realtime order

### Database
- MySQL
- ORM: Prisma hoặc SQLAlchemy tùy theo backend

### Khác
- QR code generator để tạo mã cho từng bàn
- Git/GitHub để quản lí source code
- Docker nếu muốn triển khai bằng container

---

## 12. Hướng phát triển mở rộng

Trong tương lai, hệ thống có thể mở rộng thêm:

- Đăng nhập bằng số điện thoại hoặc Google.
- Tích hợp thanh toán online.
- In hóa đơn tự động.
- Quản lí kho nguyên liệu.
- Quản lí nhiều chi nhánh.
- Gợi ý món ăn theo lịch sử order.
- Tích hợp AI chatbot hỗ trợ khách hàng.

---

## 13. Kết luận

Hệ thống quản lí nhà hàng là một bài toán thực tế, phù hợp để xây dựng thành website quản lí hoàn chỉnh. Điểm nổi bật của đề tài là kết hợp giữa **quản lí nội bộ** và **gọi món trực tuyến bằng QR theo từng bàn**, giúp số hóa toàn bộ quy trình phục vụ từ gọi món đến thanh toán.

Đây là nền tảng tốt để phát triển thành một sản phẩm thực tế với các công nghệ web hiện đại như **React/Next.js, FastAPI, MySQL, WebSocket**.
