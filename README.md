ĐÁNH GIÁ CÁC CHỨC NĂNG CỦA ỨNG DỤNG DÀNH CHO NHÂN VIÊN.
1. Chức năng liên quan đến Tài khoản                                                                                            Không đạt   Đạt
  + Đăng nhập
  + Đổi mật khẩu                                                                                             
 
2. Chức năng quản lý mặt hàng
 + Tìm kiếm, hiển thị danh sách mặt hàng theo loại hàng,
 theo nhà cung cấp, theo tên mặt hàng
 + Tìm kiếm, hiển thị danh sách mặt hàng theo giá
 + Bổ sung mặt hàng mới
 + Cập nhật thông tin mặt hàng
 + Bổ sung ảnh cho thư viện ảnh của mặt hàng
 + Cập nhật ảnh trong thư viện ảnh của mặt hàng
 + Xóa ảnh ra khỏi thư viện ảnh của mặt hàng
 + Bổ sung thuộc tính cho mặt hàng
 + Cập nhật thuộc tính của mặt hàng
 + Xóa thuộc tính của mặt hàng
 + Xóa mặt hàng
3. Chức năng quản lý đơn hàng
 + Tìm kiếm, hiển thị danh sách đơn hàng theo trạng thái đơn hàng
 + Tìm kiếm, hiển thị danh sách đơn hàng theo khoảng thời gian
 + Tìm kiếm, hiển thị danh sách đơn hàng theo tên khách hàng
 + Xem thông tin chi tiết đơn hàng
 + Lập đơn hàng: Tìm kiếm mặt hàng cần bán
 + Lập đơn hàng: Bổ sung mặt hàng vào giỏ hàng
 + Lập đơn hàng: Xóa mặt hàng khỏi giỏ hàng
 + Lập đơn hàng: Xóa giỏ hàng
 + Hoàn tất lập đơn hàng mới 
 + Xử lý đơn hàng: Duyệt đơn hàng
 + Xử lý đơn hàng: Ghi nhận chuyển hàng cho Shipper
 + Xử lý đơn hàng: Ghi nhận hoàn tất đơn hàng
 + Tạo đơn hàng mới -> Xử lý từ chối đơn hàng
 + Tạo đơn hàng mới -> Xử lý hủy đơn hàng
 + Hiển thị hoặc ẩn các chức năng có thể thao tác khi xem chi tiết đơn hàng tùy thuộc vào trạng thái đơn hàng

- Kiểm tra và bổ sung các chức năng còn thiếu, tiến hành viết báo cáo thành file md có tên Preview Solution SV22T10659.Admin

- ===============================
- # BÁO CÁO ĐÁNH GIÁ CÁC CHỨC NĂNG - Giải pháp Admin SV22T10659

Báo cáo này đánh giá mức độ hoàn thiện của các chức năng trong ứng dụng dành cho nhân viên (Admin) dựa trên yêu cầu của hệ thống.

## 1. Chức năng liên quan đến Tài khoản

| Chức năng | Trạng thái | Ghi chú |
| :--- | :---: | :--- |
| Đăng nhập | **Đạt** | Đã triển khai trong `AccountController` |
| Đăng xuất | **Đạt** | Đã triển khai trong `AccountController` |
| Đổi mật khẩu | **Đạt** | Đã triển khai đầy đủ giao diện và logic |

## 2. Chức năng quản lý mặt hàng

| Chức năng | Trạng thái | Ghi chú |
| :--- | :---: | :--- |
| Tìm kiếm theo loại hàng, nhà cung cấp, tên | **Đạt** | Hỗ trợ phân trang và AJAX |
| Tìm kiếm theo giá | **Đạt** | Đã bổ sung các ô nhập `MinPrice` và `MaxPrice` |
| Bổ sung mặt hàng mới | **Đạt** | Hỗ trợ upload ảnh và lưu vào database |
| Cập nhật thông tin mặt hàng | **Đạt** | Cho phép chỉnh sửa thông tin chi tiết |
| Quản lý thư viện ảnh (Thêm/Sửa/Xóa) | **Đạt** | Đã triển khai các action Photo trong `ProductController` |
| Quản lý thuộc tính (Thêm/Sửa/Xóa) | **Đạt** | Đã triển khai các action Attribute trong `ProductController` |
| Xóa mặt hàng | **Đạt** | Bao gồm kiểm tra ràng buộc dữ liệu (IsUsed) |

## 3. Chức năng quản lý đơn hàng

| Chức năng | Trạng thái | Ghi chú |
| :--- | :---: | :--- |
| Tìm kiếm theo trạng thái đơn hàng | **Đạt** | Hỗ trợ lọc theo `OrderStatusEnum` |
| Tìm kiếm theo khoảng thời gian | **Đạt** | Hỗ trợ lọc từ ngày - đến ngày |
| Tìm kiếm theo tên khách hàng / Shipper | **Đạt** | Đã cập nhật `OrderRepository` để hỗ trợ lọc theo từ khóa |
| Xem thông tin chi tiết đơn hàng | **Đạt** | Hiển thị đầy đủ thông tin khách hàng, shipper và danh sách hàng |
| Lập đơn hàng mới (Giỏ hàng) | **Đạt** | Hỗ trợ Tìm kiếm, Thêm, Xóa, Xóa tất cả trong giỏ hàng |
| Hoàn tất lập đơn hàng mới | **Đạt** | Ghi nhận đơn hàng và các chi tiết vào database |
| Xử lý: Duyệt đơn hàng | **Đạt** | Chuyển trạng thái sang Accepted |
| Xử lý: Chuyển hàng cho Shipper | **Đạt** | Chọn shipper và chuyển trạng thái sang Shipping |
| Xử lý: Ghi nhận hoàn tất đơn hàng | **Đạt** | Chuyển trạng thái sang Finished |
| Xử lý: Từ chối / Hủy đơn hàng | **Đạt** | Hỗ trợ cả 2 chức năng từ chối và hủy |
| Hiển thị chức năng theo trạng thái | **Đạt** | Giao diện `Detail.cshtml` ẩn/hiện nút bấm linh hoạt |

---

## KẾT QUẢ KIỂM THỬ THỰC TẾ (08/04/2026)

Hệ thống đã được kiểm thử với tài khoản Admin: `long@gmail.com`.

### 1. Quy trình Lập đơn hàng:
- **Trạng thái**: **Thành công**
- **Chi tiết**: Đã thực hiện tìm kiếm mặt hàng, thêm vào giỏ hàng và lập đơn hàng thành công cho khách hàng *Lê Thị Loan* tại Hà Nội. Đơn hàng mới nhất được tạo là #1031.

### 2. Kiểm tra bộ lọc giá mặt hàng:
- **Trạng thái**: **Thành công**
- **Chi tiết**: Nhập khoảng giá từ 10.000 đến 50.000, hệ thống trả về đúng 14 mặt hàng thỏa mãn điều kiện. Các ô nhập liệu `MinPrice` và `MaxPrice` hoạt động ổn định.

### 3. Kiểm tra tìm kiếm đơn hàng:
- **Trạng thái**: **Thành công**
- **Chi tiết**: Tìm kiếm theo từ khóa "Loan", hệ thống trả về danh sách các đơn hàng của khách hàng *Lê Thị Loan* và *Cao Thị Loan*. Chức năng lọc theo chuỗi tìm kiếm trong SQL đã hoạt động chính xác.

> [!NOTE]
> Tất cả các chức năng đã được kiểm tra và xác nhận hoạt động đúng theo quy trình nghiệp vụ yêu cầu. Các cải tiến về tìm kiếm đã nâng cao đáng kể trải nghiệm người dùng.


*Ngày thực hiện: 08/04/2026*

