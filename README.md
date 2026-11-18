# Chiến dịch Giải cứu Báo cáo Tài chính Đa quốc gia

## 1. Giới thiệu

Dự án thực hành HTML Table tại CodeGym, mô phỏng nhiệm vụ tái cấu trúc báo cáo doanh thu Quý 1/2026 của tập đoàn DataCorp.

Mục tiêu là chuyển đổi dữ liệu tài chính dạng văn bản thô (Legacy Data) thành bảng HTML có cấu trúc phân cấp, dễ đọc, dễ so sánh và đúng ngữ nghĩa.

## 2. Mục tiêu học tập

- Sử dụng các thẻ HTML Table: `table`, `caption`, `thead`, `tbody`, `tfoot`, `tr`, `th`, `td`.
- Phân biệt dữ liệu tiêu đề, dữ liệu chi tiết và dữ liệu tổng kết.
- Sử dụng `colspan` để gộp nhiều cột.
- Sử dụng `rowspan` để gộp nhiều hàng.
- Hiểu nguyên tắc bù trừ ô khi gộp để tránh vỡ cấu trúc bảng.
- Kiểm tra tính hợp lệ và khả năng hiển thị của bảng HTML.

## 3. Yêu cầu chức năng

**Cấu trúc bảng:**

- `caption`: Tiêu đề báo cáo Quý 1/2026.
- `thead`: Tiêu đề khu vực, hạng mục và doanh thu theo tháng.
- `tbody`: Doanh thu chi tiết của Châu Á và Châu Âu.
- `tfoot`: Tổng số liệu toàn cầu theo từng tháng.

**Yêu cầu kỹ thuật:**

- Có ít nhất một thuộc tính `rowspan="2"`.
- Có ít nhất một thuộc tính `colspan="3"`.
- Không có ô dư, ô thiếu hoặc sai vị trí.
- Chỉ sử dụng HTML, không sử dụng JavaScript.

## 4. Phân tích dữ liệu

| Khu vực | Hạng mục | Tháng 1 | Tháng 2 | Tháng 3 |
|---|---|---:|---:|---:|
| Châu Á | Phần cứng | $500 | $600 | $550 |
| Châu Á | Phần mềm | $1,000 | $1,200 | $1,100 |
| Châu Âu | Phần mềm | $800 | $900 | $950 |
| **Tổng toàn cầu** | | **$2,300** | **$2,700** | **$2,600** |

**Thiết kế lưới:**

- Tổng số cột: 5.
- Phần tiêu đề: 2 hàng.
- Phần nội dung: 3 hàng.
- Phần tổng kết: 1 hàng.
- Gộp 3 cột tháng bằng `colspan="3"`.
- Gộp 2 hàng Châu Á bằng `rowspan="2"`.

## 5. Cấu trúc dự án

```text
datacorp-financial-report/
├── financial_table.html
├── design_sketch.png
├── ai_prompt_log.md
└── README.md
```

## 6. Hướng dẫn chạy

1. Clone repository về máy.
2. Mở thư mục dự án bằng VS Code.
3. Mở `financial_table.html` bằng trình duyệt hoặc Live Server.
4. Kiểm tra cấu trúc bảng và thử thay đổi mức thu phóng trình duyệt.

## 7. Kiến thức vấn đáp

### Tại sao sử dụng `tfoot` thay vì `tbody`?

`tfoot` biểu diễn dữ liệu tổng kết, giúp phân biệt rõ phần tổng hợp với các dòng dữ liệu chi tiết trong `tbody`, qua đó cải thiện cấu trúc ngữ nghĩa và khả năng bảo trì.

### Khi sử dụng `rowspan="2"` cần lưu ý gì?

Một ô chiếm vị trí trên hai hàng liên tiếp. Vì vậy, hàng thứ hai không được khai báo thêm ô tại cột đã bị chiếm, tránh làm lệch cấu trúc bảng.

### `colspan="3"` hoạt động như thế nào?

Một ô chiếm chiều rộng của ba cột. Khi sử dụng, phải tính tổng số cột được chiếm trong hàng để không vượt quá cấu trúc lưới đã thiết kế.

## 8. Sản phẩm bàn giao

- `financial_table.html`: Báo cáo HTML hoàn chỉnh.
- `design_sketch.png`: Bản phác thảo cấu trúc bảng (khuyến khích).
- `ai_prompt_log.md`: Nhật ký trao đổi với AI.
- `README.md`: Tài liệu mô tả dự án.

## 9. Công nghệ sử dụng

- HTML5
- CSS cơ bản (nếu cần)
- Visual Studio Code
- Git & GitHub

---

**Dự án thực hành tại CodeGym – HTML Table & Semantic Structure.**