# 📄 Requirements Document: Java Code Formatter & Refactor Assistant
**Ngày tạo:** 22-10-2025

---

## 1. Giới thiệu dự án
**Tên:** Java Code Formatter & Refactor Assistant  
**Mô tả:**  
Ứng dụng web giúp developer format, refactor và kiểm tra chất lượng code Java tự động theo chuẩn Google Style.  
Hỗ trợ gói Free và Pro, có hệ thống đăng nhập, thanh toán và xuất báo cáo clean code.

**Mục tiêu:**  
- Giúp lập trình viên tiết kiệm thời gian khi định dạng và dọn dẹp code.  
- Cải thiện chất lượng mã nguồn, giảm lỗi tiềm ẩn.  
- Cung cấp tool nhẹ, online, dễ dùng.

---

## 2. Đối tượng sử dụng (Actors)
| Loại người dùng | Mô tả | Nhu cầu chính |
|------------------|--------|----------------|
| 👨‍💻 Developer (Free User) | Người dùng thử miễn phí | Format code nhanh |
| 💎 Pro User | Người trả phí | Refactor, batch format, report |
| 👨‍💼 Admin | Quản trị hệ thống | Quản lý user, gói dịch vụ, logs |

---

## 3. Use Cases
### Developer
1. Đăng ký / Đăng nhập tài khoản.  
2. Paste code và format.  
3. Refactor code tự động.  
4. Clean code check.  
5. Xuất báo cáo.  
6. Thanh toán để nâng cấp gói Pro.

---

## 4. Yêu cầu chức năng (Functional Requirements)
| Mã | Tên chức năng | Mô tả | Actor |
|----|----------------|-------|--------|
| FR-01 | Đăng nhập/Đăng ký | Người dùng tạo tài khoản, xác thực JWT | Developer |
| FR-02 | Format Code | Nhận input code → chạy google-java-format → trả output | Developer |
| FR-03 | Refactor | Đổi tên biến, xóa import thừa, remove println | Pro User |
| FR-04 | Clean Code Check | Quét code tìm lỗi, TODO, biến không dùng | Pro User |
| FR-05 | Export Report | Xuất file .txt hoặc .json | Pro User |
| FR-06 | Quản lý gói dịch vụ | Phân biệt Free/Pro qua role | Admin |
| FR-07 | Thanh toán Stripe | Gọi API checkout, cập nhật role | Developer |
| FR-08 | Giới hạn Free User | Giới hạn 100 dòng/lần format | System |

---

## 5. Yêu cầu phi chức năng (Non-Functional Requirements)
| Mã | Loại | Mô tả |
|----|-------|--------|
| NFR-01 | Hiệu năng | Format code ≤ 1s cho 200 dòng |
| NFR-02 | Bảo mật | Token mã hóa, không lưu code người dùng |
| NFR-03 | Sẵn sàng | Uptime ≥ 99% |
| NFR-04 | Mở rộng | Dễ thêm ngôn ngữ khác |
| NFR-05 | Bảo trì | Tách module format, refactor, auth, billing |
| NFR-06 | Giao diện | UI responsive, thân thiện |
| NFR-07 | API | RESTful, JSON rõ ràng |
| NFR-08 | Log & Audit | Ghi log thao tác, billing |

---

## 6. API chính
| Endpoint | Method | Input | Output | Quyền |
|-----------|---------|--------|---------|--------|
| /api/format | POST | code: string | formattedCode | All |
| /api/refactor | POST | code: string | refactoredCode, report | Pro |
| /api/check | POST | code: string | warnings[] | Pro |
| /api/export | POST | code, options | file | Pro |
| /api/auth/login | POST | email, password | jwt | Public |
| /api/stripe/webhook | POST | payload | 200 OK | System |

---

## 7. Giao diện (UI Wireframe)
| Trang | Mô tả |
|-------|--------|
| /login | Form đăng nhập |
| /formatter | Editor + nút Format |
| /refactor | Code Editor + Report panel |
| /pricing | Gói Free/Pro |
| /dashboard | Thống kê lịch sử |

---

## 8. Rủi ro & Giải pháp
| Rủi ro | Mức độ | Giải pháp |
|--------|----------|-----------|
| Xử lý code lớn | Trung bình | Giới hạn dung lượng input |
| Lỗi format | Thấp | Dùng google-java-format |
| Stripe không hỗ trợ VN | Trung bình | LemonSqueezy/Gumroad |
| Spam API | Cao | Rate limit theo IP/JWT |

---

## 9. Tiêu chí bàn giao (Acceptance Criteria)
- Đăng ký, đăng nhập hoạt động.  
- Format & Refactor code thành công.  
- Xuất báo cáo clean code.  
- Thanh toán gói Pro thành công.  
- App chạy ổn định, UI đẹp, log đầy đủ.

---

## 10. Tài liệu tham chiếu
- [Google Java Format](https://github.com/google/google-java-format)  
- [Stripe API Docs](https://stripe.com/docs/api)  
- [Spring Boot Security JWT](https://spring.io/guides/tutorials/spring-boot-oauth2/)  
- [Monaco Editor React](https://github.com/suren-atoyan/monaco-react)

---

## ✅ Kết quả mong muốn
Tạo file requirements.md hoàn chỉnh để làm chuẩn thiết kế và code.
