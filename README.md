# 🚀 Dự án: Java Code Formatter & Refactor Assistant
**Loại:** SaaS Web App (Spring Boot + React)  
**Thời gian:** 6 tuần  
**Mục tiêu:** Xây dựng web app hoàn chỉnh giúp format & refactor code Java, có hệ thống thanh toán và người dùng thật.

---

## 🧱 Giai đoạn 1: Chuẩn bị & Thiết kế (Tuần 1)
### 🎯 Mục tiêu:
- Xác định yêu cầu, kiến trúc, giao diện.
- Tạo project nền Spring Boot + React.

| Ngày | Nhiệm vụ | Mô tả | Kết quả |
|------|-----------|-------|----------|
| 1 | Xác định yêu cầu chi tiết | Format, Refactor, Clean code check, Report | Tài liệu yêu cầu |
| 2–3 | Thiết kế kiến trúc hệ thống | React → Spring Boot → DB → Stripe | UML Architecture |
| 4 | Tạo project skeleton | Maven + React setup | Base chạy được |
| 5–6 | Thiết kế giao diện cơ bản | Mockup UI (Figma/React) | UI sơ khởi |
| 7 | Setup GitHub repo | Chia module backend/frontend | Repo hoàn chỉnh |

✅ **Kết quả:** Project khởi tạo chạy được với UI cơ bản.

---

## ⚙️ Giai đoạn 2: Backend (Tuần 2–3)
### 🎯 Mục tiêu:
Xây dựng API format, refactor, clean code và report.

| Ngày | Nhiệm vụ | Mô tả | Kết quả |
|------|-----------|-------|----------|
| 8–9 | Tích hợp google-java-format | API /format | Format hoạt động |
| 10–11 | Thêm refactor logic | Regex + AST | /refactor chạy |
| 12–13 | Clean Code Check | Phát hiện lỗi phổ biến | /check hoạt động |
| 14–15 | Unit test | Viết test JUnit 5 | Test pass |
| 16–17 | Báo cáo lỗi | Xuất .txt hoặc .json | Report chạy |

✅ **Kết quả:** Backend đầy đủ API + test.

---

## 💻 Giai đoạn 3: Frontend (Tuần 4)
### 🎯 Mục tiêu:
UI hoàn chỉnh, kết nối API, thêm vai trò Free/Pro giả lập.

| Ngày | Nhiệm vụ | Mô tả | Kết quả |
|------|-----------|-------|----------|
| 18–19 | Tích hợp React + Tailwind | Giao diện chính | UI layout chạy |
| 20–21 | Monaco Editor | Editor paste code | Editor hoạt động |
| 22 | Gọi API backend | Format & Refactor live | API kết nối |
| 23 | Tab Report | Hiển thị lỗi, export file | Report UI |
| 24 | Giả lập Free/Pro | Giới hạn dòng code | Role test ok |

✅ **Kết quả:** Web app hoạt động local.

---

## 💳 Giai đoạn 4: Đăng nhập & Thanh toán (Tuần 5)
### 🎯 Mục tiêu:
Tích hợp đăng nhập, JWT, thanh toán Stripe.

| Ngày | Nhiệm vụ | Mô tả | Kết quả |
|------|-----------|-------|----------|
| 25–26 | Spring Security + JWT | Login, Signup | Auth ok |
| 27 | Tạo Stripe Product | Checkout test | Thanh toán |
| 28 | Webhook Stripe | Update user.role = PRO | Role cập nhật |
| 29 | UI Pricing | Gói Free/Pro | Giao diện |
| 30 | Test E2E | Flow hoàn chỉnh | MVP sẵn sàng |

✅ **Kết quả:** SaaS hoạt động full flow.

---

## 🌍 Giai đoạn 5: Triển khai & Ra mắt (Tuần 6)
### 🎯 Mục tiêu:
Deploy sản phẩm + landing page + user thử nghiệm.

| Ngày | Nhiệm vụ | Mô tả | Kết quả |
|------|-----------|-------|----------|
| 31–32 | Deploy backend | Render / Railway | API online |
| 33 | Deploy frontend | Vercel / Netlify | Web hoạt động |
| 34 | Domain + SSL | Mua domain, https | Domain ok |
| 35 | Landing page | Viết mô tả + video demo | Trang bán |
| 36–37 | Quảng bá | ProductHunt, Reddit, FB | 20 user đầu |

✅ **Kết quả:** App online + user thật đầu tiên.

---

## 💰 Dự kiến doanh thu

| Thời gian | User | Doanh thu ước tính |
|------------|-------|--------------------|
| 1 tháng | 30 user Free | 0đ (test) |
| 2 tháng | 50 user Pro × 99k | ~5 triệu |
| 3 tháng | 100 user Pro × 99k | ~10 triệu |

---

## 🧠 Gợi ý mở rộng
- Plugin IntelliJ / Eclipse.  
- AI refactor suggestion (GPT API).  
- Clean Code Score Report.  
- Batch Maven project format.

---

## 🧾 Tác giả & Ngày tạo
- **Người lập kế hoạch:** ChatGPT (hỗ trợ User)  
- **Ngày:** 22-10-2025
