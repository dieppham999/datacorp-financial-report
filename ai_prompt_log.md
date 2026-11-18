# AI Prompt Log – DataCorp Financial Report

### Prompt 01 – Phân tích dữ liệu Legacy

**Prompt:**

> Tôi đang thực hiện bài tập chuyển đổi báo cáo tài chính DataCorp Quý 1/2026 từ văn bản thô thành bảng HTML. Hãy hướng dẫn tôi phân loại dữ liệu thành phần tiêu đề, nội dung chi tiết và tổng kết. Không viết mã HTML hoàn chỉnh.

**Mục đích:** Hiểu cấu trúc dữ liệu trước khi triển khai.

**Kiến thức cần rút ra:** Phân biệt vai trò của `thead`, `tbody` và `tfoot`.

### Prompt 02 – Xác định cấu trúc lưới HTML

**Prompt:**

> Với bảng báo cáo gồm khu vực, hạng mục sản phẩm và doanh thu của ba tháng, hãy giải thích cách xác định tổng số cột và số hàng cần thiết. Tôi muốn hiểu cách trình duyệt phân bố các ô trên lưới HTML.

**Mục đích:** Nắm nguyên tắc tổ chức các hàng và cột.

**Kiến thức cần rút ra:** Bảng cần 5 cột, gồm 2 hàng tiêu đề, 3 hàng dữ liệu và 1 hàng tổng kết.

### Prompt 03 – Phân biệt thẻ th và td

**Prompt:**

> Giải thích sự khác nhau giữa thẻ `th` và `td` trong HTML Table. Trong báo cáo DataCorp, những ô nào nên sử dụng `th` thay vì `td` để đảm bảo ngữ nghĩa và khả năng truy cập?

**Mục đích:** Lựa chọn thẻ HTML phù hợp.

**Kiến thức cần rút ra:** `th` thể hiện ô tiêu đề, `td` thể hiện ô dữ liệu. Có thể kết hợp thuộc tính `scope` để xác định phạm vi tiêu đề.

### Prompt 04 – Tìm hiểu nguyên lý colspan

**Prompt:**

> Tôi muốn tạo tiêu đề "Quý 1/2026" bao trùm ba cột Tháng 1, Tháng 2 và Tháng 3. Hãy giải thích nguyên lý hoạt động của `colspan="3"` bằng sơ đồ lưới, đồng thời chỉ ra các lỗi thường gặp khi tính sai số cột. Không viết toàn bộ bảng HTML.

**Mục đích:** Hiểu cách gộp nhiều cột mà không làm vỡ bảng.

**Kiến thức cần rút ra:** Một ô có `colspan="3"` chiếm ba vị trí cột trong cùng một hàng.

### Prompt 05 – Tìm hiểu nguyên lý rowspan

**Prompt:**

> Trong báo cáo DataCorp, khu vực Châu Á có hai hạng mục Phần cứng và Phần mềm. Tôi muốn dùng `rowspan="2"` để hiển thị tên khu vực một lần. Hãy giải thích cách ô này chiếm vị trí trên hai hàng và ảnh hưởng đến số ô cần khai báo trong hàng tiếp theo.

**Mục đích:** Hiểu cơ chế gộp hàng.

**Kiến thức cần rút ra:** Hàng tiếp theo không được tạo thêm ô tại vị trí đã bị `rowspan` chiếm.

### Prompt 06 – Kiểm tra logic bù trừ số ô

**Prompt:**

> Giả sử bảng của tôi có 5 cột. Nếu hàng đầu tiên của tbody chứa một ô `rowspan="2"` tại cột Khu vực, thì hàng thứ hai cần khai báo bao nhiêu ô mới? Hãy giải thích bằng cách đếm từng vị trí trong lưới, không cung cấp code hoàn chỉnh.

**Mục đích:** Tránh lỗi dư hoặc thiếu ô sau khi gộp hàng.

**Kiến thức cần rút ra:** Hàng thứ hai chỉ cần khai báo 4 ô mới vì một vị trí đã được ô từ hàng trước chiếm.

### Prompt 07 – Thiết kế Wireframe

**Prompt:**

> Hãy hướng dẫn tôi tự phác thảo bảng báo cáo DataCorp bằng sơ đồ ASCII gồm 5 cột. Đánh dấu những vị trí cần sử dụng rowspan và colspan, sau đó chỉ ra cách kiểm tra sự liên kết giữa các hàng và cột.

**Mục đích:** Hình dung cấu trúc bảng trước khi lập trình.

**Kiến thức cần rút ra:** Sử dụng sơ đồ lưới để xác minh các ô gộp.

### Prompt 08 – Kiểm tra cấu trúc HTML Semantic

**Prompt:**

> Tôi đã tự viết bảng HTML sử dụng table, caption, thead, tbody, tfoot, tr, th và td. Hãy đưa ra checklist kiểm tra cấu trúc ngữ nghĩa, thứ tự các thành phần và những lỗi lồng thẻ thường gặp. Không viết lại toàn bộ code của tôi.

**Mục đích:** Tự kiểm tra tính hợp lệ của mã nguồn.

**Kiến thức cần rút ra:** Các hàng và ô phải nằm trong cấu trúc bảng hợp lệ, không chèn div hoặc văn bản tùy ý trực tiếp giữa các thành phần bảng.

### Prompt 09 – Kiểm thử lỗi vỡ bảng

**Prompt:**

> Khi sử dụng đồng thời rowspan và colspan, bảng HTML có thể bị lệch cột hoặc xuất hiện ô dư. Hãy đóng vai QA Tester, liệt kê các tình huống kiểm thử và hướng dẫn tôi xác định hàng nào đang chiếm sai số vị trí trong lưới.

**Mục đích:** Phát hiện lỗi hiển thị và lỗi cấu trúc.

**Kiến thức cần rút ra:** Đếm tổng số vị trí cột thực tế của từng hàng, bao gồm cả những vị trí bị ô gộp từ hàng trước chiếm.

### Prompt 10 – Kiểm thử dữ liệu tài chính

**Prompt:**

> Hãy giúp tôi kiểm tra phép cộng dữ liệu doanh thu của DataCorp. Châu Á có Phần cứng 500, 600, 550 USD và Phần mềm 1000, 1200, 1100 USD; Châu Âu có Phần mềm 800, 900, 950 USD. Hãy xác minh tổng từng tháng và chỉ ra sự khác biệt về ý nghĩa giữa doanh thu và lợi nhuận.

**Mục đích:** Kiểm tra tính chính xác của dữ liệu trước khi bàn giao.

**Kiến thức cần rút ra:** Tổng lần lượt là 2.300 USD, 2.700 USD và 2.600 USD. Doanh thu và lợi nhuận là hai chỉ tiêu tài chính khác nhau.

### Prompt 11 – Kiểm tra khả năng hiển thị

**Prompt:**

> Hãy đề xuất các bước kiểm thử bảng HTML DataCorp khi thay đổi mức zoom trình duyệt từ 75% đến 200%. Những dấu hiệu nào cho thấy bảng bị lỗi cấu trúc và những trường hợp nào chỉ là vấn đề hiển thị do kích thước màn hình?

**Mục đích:** Đánh giá giao diện khi thay đổi mức thu phóng.

**Kiến thức cần rút ra:** Phân biệt lỗi cấu trúc lưới với hiện tượng tràn ngang hoặc xuống dòng do không đủ không gian.

### Prompt 12 – Chuẩn bị vấn đáp với CFO

**Prompt:**

> Hãy đóng vai CFO của DataCorp và chất vấn tôi về lý do sử dụng tfoot thay vì đặt dòng tổng kết trong tbody, nguyên tắc bù trừ ô khi dùng rowspan="2" và mục đích của colspan="3". Hãy đánh giá câu trả lời của tôi dựa trên tính chính xác của HTML Semantic.

**Mục đích:** Chuẩn bị bảo vệ mã nguồn trước giảng viên.

**Kiến thức cần rút ra:** Hiểu được lý do thiết kế bảng và có thể giải thích từng quyết định kỹ thuật.

