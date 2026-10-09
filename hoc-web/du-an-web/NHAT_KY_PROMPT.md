# NHẬT KÝ PROMPT
- Họ tên: Nguyễn Khã Minh
- MSSV: 25810130
- Công cụ AI: Gemini
 
## Lần 1 - Ngày 1, 08:30
- Mục đích: Viết bản đặc tả cho website đồ án (bán sách).
- Prompt đã dùng: Prompt mẫu 0 (Khung ngữ cảnh) và Prompt mẫu 1 (AI phỏng vấn để viết đặc tả)[cite: 1]. Đã sửa tên website thành "Doctor Book"[cite: 4].
- Kết quả: AI đã đóng vai người phỏng vấn và chốt được bản đặc tả gồm 4 trang: Trang chủ (index.html), Cửa hàng (cua-hang.html), Chi tiết (chi-tiet.html) và Liên hệ (lien-he.html)[cite: 2, 3, 4, 5].
- Vấn đề gặp phải: AI ban đầu gợi ý thêm tính năng đăng nhập và giỏ hàng thanh toán phức tạp.
- Điều tôi học được: Cần giới hạn rõ ràng với AI rằng đây là đồ án trang tĩnh cho người mới học, chỉ tối đa 4 trang cơ bản[cite: 1].
 
## Lần 2 - Ngày 1, 08:50
- Mục đích: Dựng bố cục và code cho trang chủ `index.html` cùng file `style.css`[cite: 4, 6].
- Prompt đã dùng: Prompt mẫu 3 (Dựng trang chủ từ bản đặc tả)[cite: 1].
- Kết quả: AI tạo ra mã HTML cho phần đầu trang, banner chào mừng, các khu vực sách bán chạy, sách mới nổi bật và chân trang[cite: 4].
- Vấn đề gặp phải: AI viết luôn CSS vào thẻ `<style>` bên trong file HTML thay vì tách riêng.
- Điều tôi học được: Phải yêu cầu rõ "Hãy tách CSS ra file riêng public/css/style.css" để quản lý code tốt hơn theo chuẩn bài thực hành[cite: 1].
 
## Lần 3 - Ngày 1, 09:15
- Mục đích: Chỉnh sửa màu sắc chủ đạo và cách hiển thị của thanh menu[cite: 6].
- Prompt đã dùng: Prompt mẫu 4 (Chỉnh sửa giao diện) - Mô tả cụ thể: "Trang chủ đang hiển thị như ảnh chụp. Hãy đổi màu chủ đạo ở đầu trang, chân trang và các nút bấm thành màu xanh lá (mã #2e7d32). Trên điện thoại menu đang bị tràn, hãy cho xuống dòng và canh giữa"[cite: 1, 6].
- Kết quả: AI cập nhật file `style.css`, sử dụng biến `:root { --mau-chu-dao: #2e7d32; }` để đồng bộ màu sắc và thêm đoạn `@media (max-width: 768px)` để xử lý menu trên di động[cite: 6].
- Vấn đề gặp phải: Chép code mới vào nhưng trình duyệt không đổi màu.
- Điều tôi học được: Cần lưu file (Ctrl+S hoặc bật Auto Save) và nhấn Ctrl+F5 để xóa cache trình duyệt[cite: 1].
 
## Lần 4 - Ngày 1, 09:40
- Mục đích: Thêm các trang phụ gồm `cua-hang.html` và `chi-tiet.html` dùng chung giao diện CSS[cite: 2, 3].
- Prompt đã dùng: Prompt mẫu 5 (Thêm một trang mới dùng chung giao diện)[cite: 1].
- Kết quả: Có thêm trang Cửa hàng với bộ lọc bên trái, danh sách sách bên phải[cite: 3] và trang Chi tiết sách với ảnh bên trái, thông tin giá bên phải[cite: 2]. Cả 2 đều nạp chung `css/style.css`[cite: 2, 3].
- Vấn đề gặp phải: Khi nhấp vào các liên kết ở menu trên trang mới, trình duyệt báo lỗi không tìm thấy file.
- Điều tôi học được: Tên file thực tế và tên file trong thuộc tính `href="chi-tiet.html"` phải khớp nhau từng ký tự, không được viết hoa hay có dấu[cite: 1, 2]. Phải đồng bộ menu trên tất cả các trang[cite: 1].

## Lần 5 - Ngày 1, 10:15
- Mục đích: Tạo trang `lien-he.html` với form điền thông tin[cite: 5].
- Prompt đã dùng: "Dựa vào style.css hiện tại, hãy tạo trang lien-he.html gồm 2 cột: Cột trái là thông tin liên hệ và bản đồ giả lập, Cột phải là form nhập nội dung (Họ tên, Email, Lời nhắn) có nút gửi. Giữ nguyên header và footer"[cite: 5].
- Kết quả: Hoàn thiện HTML trang liên hệ với cấu trúc thẻ `<form>` rõ ràng và thêm CSS cho các trường nhập liệu (`.truong-nhap`)[cite: 5, 6].
- Vấn đề gặp phải: Form bị tràn khung trên màn hình nhỏ.
- Điều tôi học được: Khi làm form, nên set thuộc tính `width: 100%;` cho các ô input để nó tự động co giãn theo khung chứa[cite: 5, 6].
 
## Lần 6 - Ngày 1, 10:35
- Mục đích: Nhờ AI đóng vai người kiểm thử (tester) để rà soát toàn bộ dự án[cite: 1].
- Prompt đã dùng: Prompt mẫu 6 (AI đóng vai người kiểm thử). Đã copy toàn bộ nội dung các file gộp vào một tin nhắn[cite: 1].
- Kết quả: AI phát hiện một số ảnh thiếu thuộc tính `alt` và padding ở khu vực Lý do chọn Doctor Book bị lệch trên thiết bị di động.
- Vấn đề gặp phải: AI đề xuất sửa nhiều thứ cùng lúc bằng cách tự động viết lại cả file dài.
- Điều tôi học được: Chỉ yêu cầu AI sửa từng lỗi một (ví dụ: "Sửa vấn đề số 1 trước") để dễ kiểm soát mã nguồn và kiểm chứng bằng DevTools (F12)[cite: 1].