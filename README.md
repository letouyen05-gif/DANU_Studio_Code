# DANU_Studio_Code

# TrustFlow AI – Smart Escrow & Financial Monitoring System

TrustFlow AI là một nền tảng web mô phỏng hệ thống **Escrow thông minh** kết hợp AI nhằm hỗ trợ:
- Đối soát tài chính  
- Giám sát giao dịch  
- Quản lý uy tín người dùng  
- Xử lý tình huống rủi ro  

Hệ thống hướng tới việc tăng **minh bạch, an toàn và tin cậy** trong các giao dịch nhóm.

---

## Mục tiêu dự án

- Ứng dụng AI vào kiểm tra hóa đơn và đối soát tài chính  
- Mô phỏng hệ thống Escrow minh bạch  
- Quản lý Leader / Member trong giao dịch  
- Tăng độ tin cậy thông qua đánh giá & voting  
- Hỗ trợ xử lý rủi ro bằng Panic Button  

---

## Các chức năng chính

### 1. Đăng ký tài khoản (Register)

Người dùng có thể tạo tài khoản mới bằng cách nhập:
- Họ tên  
- Email  
- Mật khẩu  

Hệ thống hỗ trợ:
- Kiểm tra email trùng  
- Hiển thị thông báo lỗi / thành công  
- Chuyển đổi ngôn ngữ Việt – Anh  

Mục tiêu: Tạo cơ sở dữ liệu người dùng cho hệ thống.

---

### 2. Đăng nhập (Login)

Người dùng đăng nhập bằng:
- Email  
- Mật khẩu  

Hệ thống sẽ:
- So khớp với `users.json`  
- Phân quyền tự động:
  - Leader  
  - Member  

Tính năng:
- Quên mật khẩu  
- Chuyển ngôn ngữ  

Mục tiêu: Đảm bảo bảo mật và phân quyền chính xác.

---

### 3. Dashboard (Bảng điều khiển)

Dashboard hiển thị:
- Tên người dùng  
- Vai trò (Leader / Member)  
- Điểm uy tín  
- Cấp độ SBT  
- Số Pool đã hoàn thành  

Cho phép truy cập nhanh:
- AI Đối soát  
- Smart Monitor  
- Panic Button  

Mục tiêu: Quản lý và theo dõi trạng thái người dùng.

---

### 4. Đối soát hóa đơn bằng AI  
*(AI_AGENT_QUETHOADON.html)*

Người dùng:
- Nhập Leader ID  
- Upload ảnh hóa đơn  

Hệ thống AI sẽ:
1. Phân tích hình ảnh (OCR)  
2. So sánh dữ liệu với Google Sheets  
3. Đưa ra kết luận  

Kết quả hiển thị:
- Approved / Rejected  
- Lý do cụ thể  

Mục tiêu: Giảm gian lận tài chính, tăng minh bạch.

---

### 5. Smart Monitor (Giám sát thông minh)

Chức năng:

#### a. Theo dõi dòng tiền
- Hiển thị số tiền escrow  
- Trạng thái giao dịch  

#### b. Theo dõi tiến độ
- Thanh progress thể hiện mức hoàn thành  

#### c. AI Flow
- Mô phỏng luồng xử lý giao dịch  
- AI đóng vai trò trung gian  

#### d. Chat AI
- Người dùng trao đổi với AI  
- AI hỗ trợ tư vấn  

#### e. Voting
- Người dùng vote đồng thuận / phản đối  
- Tăng minh bạch  

Mục tiêu: Tạo môi trường giao dịch công khai, minh bạch.

---

### 6. Panic Button (Xử lý khẩn cấp)

#### Leader:
- Kích hoạt trạng thái khẩn cấp  
- Dừng giao dịch
- Cảnh báo hệ thống  

#### Member:
- Báo cáo sự cố  
- Gửi cảnh báo  

Mục tiêu: Giảm rủi ro, xử lý tranh chấp.

---

### 7. Quên mật khẩu (Forgot Password)

Người dùng có thể:
- Nhập email  
- Đặt mật khẩu mới  

Hệ thống cập nhật lại trong `users.json`.

Mục tiêu: Tăng trải nghiệm người dùng.

---

### 8. Hệ thống quản lý người dùng (users.json)

Dữ liệu gồm:

| Trường | Ý nghĩa |
|--------|--------|
| user_id | Mã người dùng |
| name | Tên |
| role | Leader / Member |
| reputation_score | Điểm uy tín |
| completed_pools | Số giao dịch |
| sbt_level | Cấp độ |
| email | Email |
| password_hash | Mật khẩu |

Đây là **database giả lập** phục vụ mục đích học tập.

---

### 9. Đa ngôn ngữ (VI / EN)

Hệ thống hỗ trợ:
- Chuyển đổi ngôn ngữ realtime  
- Áp dụng cho:
  - Login  
  - Register  
  - Dashboard  
  - AI Portal  

Mục tiêu: Phù hợp môi trường quốc tế.

---

### Cấu trúc thư mục
├── Login.html
├── Register.html
├── forgot-password.html
├── Dashboard.html
├── AI_AGENT_QUETHOADON.html
├── PanicButton_Leader.html
├── PanicButton_member.html
├── users.json
└── README.md

##Cách chạy project

1. Tải toàn bộ source code  
2. Mở `Login.html` bằng trình duyệt  
3. Đăng nhập bằng tài khoản mẫu trong user.json:
- Tên đăng nhập: minhanh@gmail.com
- Mật khẩu: trustU001
