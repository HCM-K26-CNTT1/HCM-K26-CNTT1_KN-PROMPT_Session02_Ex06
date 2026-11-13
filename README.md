**BÀI 6: LOẠI BỎ "LỜI CHÀO VÔ NGHĨA" BẰNG KỸ THUẬT STRUCTURED OUTPUT**

---

### PHẦN 1. PHÂN TÍCH NGUYÊN NHÂN LỖI

* **Vì sao AI hay thêm lời chào/kết luận?**
* Do AI được huấn luyện theo mô hình giao tiếp tự nhiên với con người (xu hướng thân thiện, lịch sự).
* Prompt trước đó chưa có lệnh cấm nghiêm ngặt (Negative Constraint) và chưa yêu cầu định dạng đầu ra thuần túy (raw output), khiến AI tưởng đây là cuộc trò chuyện thông thường thay vì một tác vụ API tự động hóa.



---

### PHẦN 2. HOÀN THIỆN PROMPT ÉP CẤU TRÚC

```text
[CONTEXT]
Bạn là module AI chuyển đổi dữ liệu bảo hành tự động cho hệ thống ERP của TechShop.

[REQUEST]
Đọc biên bản bảo hành dạng text và trích xuất thành định dạng JSON gồm các trường: customer_name, device, issue.

[NEGATIVE CONSTRAINT]
- Tuyệt đối không thêm lời chào mở đầu (VD: "Dạ em chào...").
- Tuyệt đối không thêm lời chúc kết luận hay giải thích thừa ở cuối.

[TYPE OF OUTPUT]
Chỉ trả về đúng một chuỗi JSON thuần túy hợp lệ, không dùng markdown block (như ```json), bắt đầu bằng ký tự { và kết thúc bằng ký tự }.

```
