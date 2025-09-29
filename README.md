# NguyenLeTuongVi_LAB02
NHẬP MÔN CÔNG NGHỆ PHẦN MỀM

Lab 02 – Phân tích yêu cầu & Thiết kế Use Case (Hotel Booking System)
Mục tiêu
Sinh viên học cách mô tả yêu cầu và thiết kế hệ thống đặt phòng khách sạn bằng UML,
thiết kế cơ sở dữ liệu, và triển khai quy trình Agile-Scrum trên Jira, đồng bộ với GitHub.

1. Thiết kế Mini Project: Hệ thống quản lý đặt phòng khách sạn
1.1 Entity (6 bảng dữ liệu chính)
• Guest (Khách hàng)
• RoomType (Loại phòng)
• Room (Phòng cụ thể)
• Reservation (Đặt phòng)
• Payment (Thanh toán)
• Staff (Nhân viên/Lễ tân/Quản lý)
Mối quan hệ:
• Guest 1–N Reservation
• Reservation 1–N Payment
• RoomType 1–N Room
• Room 1–N Reservation
• Staff 1–N Reservation (lễ tân quản lý)

1.2 Use Case UML
Các tác nhân chính:
• Guest (Khách hàng)
• Receptionist (Lễ tân)
• Manager (Quản lý)
• Payment Gateway
• Housekeeping (Buồng phòng)
Use Case chính:
• Tìm phòng, Xem chi tiết phòng
• Đặt phòng online (Booking)
• Thanh toán online
• Check-in / Check-out

• Quản lý phòng & giá
• Quản lý đặt phòng (cho lễ tân)
• Công việc buồng phòng
• Báo cáo doanh thu

1.3 Sequence UML
a) Luồng Đặt phòng online
1. Guest chọn phòng → hệ thống giữ phòng (hold).
2. Guest nhập thông tin → thực hiện thanh toán.
3. Cổng thanh toán trả kết quả → xác nhận & gửi email.
b) Luồng Check-in/Check-out (Lễ tân)
1. Receptionist tra cứu mã đặt phòng.
2. Check-in: gán phòng thực tế, cập nhật trạng thái.
3. Check-out: tổng hợp chi phí, thu tiền, cập nhật buồng phòng.

1.4 Thiết kế cơ sở dữ liệu (ERD)
• Guest(GuestID, Name, Phone, Email, Address)
• RoomType(TypeID, Name, Price, Capacity, Description)
• Room(RoomID, TypeID, Status, Floor)
• Reservation(ResvID, GuestID, RoomID, StaffID, CheckInDate, CheckOutDate,
Status)
• Payment(PaymentID, ResvID, Amount, Method, Status, Date)
• Staff(StaffID, Name, Role, Username, PasswordHash)
ERD thể hiện các quan hệ 1-N, PK, FK rõ ràng.

2. Triển khai chi tiết trên Jira (Agile Scrum)
• Product Backlog (ví dụ):
o Đăng ký/Đăng nhập khách hàng
o Tìm phòng & Xem chi tiết phòng
o Đặt phòng & thanh toán online
o Check-in/Check-out (Lễ tân)
o Quản lý phòng & giá (Manager)

o Báo cáo doanh thu
o Công việc buồng phòng
• Sprint Plan:
o Sprint 1: Auth, Tìm phòng, Xem chi tiết phòng
o Sprint 2: Đặt phòng & giữ chỗ
o Sprint 3: Thanh toán & Check-in/out
o Sprint 4: Báo cáo, housekeeping, tối ưu & release
• Board:
o To Do → In Progress → Code Review → Testing → Done

3. Đồng bộ GitHub
• Mỗi sinh viên tạo repo riêng (public).
• Upload các artefact:
o Use Case Diagram (.png/.drawio)
o Sequence Diagram
o ERD
o README.md mô tả dự án
• Đồng bộ Jira ↔ GitHub (có thể dùng Smart Commit để gắn issue key vào commit).
• Mỗi commit: #JIRA-123 Add: Booking use case diagram
