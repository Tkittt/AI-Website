# AI trong cuộc sống — Website tĩnh responsive

Tác giả: **Phan Thế Kiệt**  
MSSV: **2531540443**

Bản nâng cấp của bài tập 1: tám trang HTML độc lập, CSS dùng chung, không dùng JavaScript, framework hoặc backend.

## Bản vá văn bản — 03/10/2026

- Khôi phục 328 chỗ chữ tiếng Việt bị thay nhầm trong toàn bộ tám trang, kể cả menu, tiêu đề, mô tả ảnh và thông tin trang.
- Giữ nguyên các từ “bạn” dùng đúng nghĩa; không thay từ theo ranh giới ASCII nữa.
- Giữ nguyên CSS, màu sắc, bố cục và các đường dẫn.
- Chỉnh nét minh họa quyển sách SVG để không bị tô thành các mảng đen.
- Đã đối chiếu toàn bộ văn bản, kiểm tra cấu trúc HTML, ảnh, liên kết nội bộ và tính toàn vẹn ZIP.
- Việc cập nhật lên GitHub Pages vẫn cần thực hiện với mã đã sửa.

## Xem thử trên máy

1. Giải nén ZIP bằng **Extract All / Giải nén tất cả**. Không mở HTML trực tiếp từ trong ZIP.
2. Vào thư mục `AI-Website-Responsive`, mở `index.html` bằng Chrome hoặc Edge.
3. Bấm menu để xem đủ tám trang.
4. Mở bằng VS Code: **File → Open Folder → chọn AI-Website-Responsive**.
5. Khi sửa, lưu bằng **Ctrl + S**, sau đó tải lại trình duyệt.

CSS và ảnh dùng đường dẫn tương đối nên xem offline được. Chỉ các liên kết bên ngoài cần Internet.

## Các trang

| Tệp | Nội dung |
| --- | --- |
| `index.html` | Trang chủ, hero, nội dung nổi bật |
| `khai-niem.html` | AI, học máy, học sâu, AI tạo sinh |
| `ung-dung.html` | Sáu lĩnh vực ứng dụng và ví dụ ôn tập |
| `loi-ich-rui-ro.html` | Lợi ích, rủi ro, checklist an toàn |
| `cong-cu-ai.html` | Công cụ, nguồn chính thức, cách viết yêu cầu |
| `thu-vien-anh.html` | Bảy ảnh/minh họa có chú thích và nguồn |
| `tai-lieu.html` | Tài liệu, nguồn ảnh và ghi chú biên soạn |
| `lien-he.html` | Tác giả, dự án và giải đáp |

## Thư mục và tệp khác

- `css/style.css`: toàn bộ CSS, biến màu, bố cục và media queries.
- `images/ai-home.jpg`: ảnh trang chủ giữ từ bài cũ.
- `images/*.svg`: sáu minh họa tạo bằng mã cho bản nâng cấp.
- `link-website.txt`: thông tin sinh viên, URL website và kho GitHub.

Tám trang HTML phải cùng cấp với `index.html`; không di chuyển CSS hay ảnh mà không sửa đường dẫn.

## Components và responsive

Header, Navigation, Hero, Section, Grid, Card, Button/Link và Footer có trên website.
Grid nội dung dùng CSS Grid; các hàng nút và chi tiết dùng Flexbox. FAQ dùng thẻ HTML `details` và `summary`, không cần JavaScript.

| Kích thước CSS | Grid | Menu | Hero/nội dung đôi |
| --- | --- | --- | --- |
| Trên 960 px | 3 cột (khối đôi: 2) | 8 cột | 2 cột |
| 701–960 px | 2 cột | 4 cột | 2 cột |
| 601–700 px | 2 cột | 4 cột | 1 cột |
| 600 px trở xuống | 1 cột | 2 cột | 1 cột |

Ảnh co theo vùng chứa, giữ tỷ lệ; các card dùng `object-fit`.
Cột dùng `minmax(0, 1fr)`, phần tử con có `min-width: 0`, liên kết dài xuống dòng.
Không dùng `overflow-x: hidden` để che lỗi bố cục.

Hỗ trợ tiếp cận: `lang="vi"`, alt ảnh, skip link, focus bàn phím và `aria-current="page"` cho mục menu hiện tại.

## Nguồn và sự hỗ trợ của AI

Trang `tai-lieu.html` ghi nguồn IBM, OECD, UNESCO, NIST, các nhà cung cấp công cụ và ảnh Steve A Johnson / Unsplash.
Sáu SVG được tạo bằng mã riêng với hỗ trợ AI, không lấy từ kho ảnh bên ngoài.

Mã và nội dung được xây dựng với sự hỗ trợ của AI. Sinh viên cần đọc hiểu, kiểm tra và chỉnh sửa trước khi nộp theo quy định môn học.
Trang liên hệ không có biểu mẫu giả; HTML/CSS không tự gửi hoặc lưu dữ liệu.

## Cập nhật GitHub Pages

**ZIP này là bản nâng cấp để xem thử, chưa được tải lên GitHub trong lần làm này.**
URL bên dưới đang dùng cho bài cũ; có thể giữ nguyên sau khi cập nhật thành công.

Kho: https://github.com/Tkittt/AI-Website  
Website: https://tkittt.github.io/AI-Website/

1. Vào kho → **Add file → Upload files**.
2. Tải các HTML mới và các thư mục `css`, `images` từ **bên trong** thư mục dự án. Giữ `index.html` ở gốc kho, không lồng thêm `AI-Website-Responsive`.
3. Giữ chính xác tên và chữ hoa-thường. Các tệp trùng tên là bản thay thế bài cũ.
4. Tải `README.md` và `link-website.txt` cùng mã nếu muốn. Không tải ZIP thay cho mã HTML.
5. Chọn **Commit changes**.
6. **Settings → Pages**: nếu dùng nhánh, chọn **Deploy from a branch → main → /(root) → Save**. Nếu bài cũ đã cấu hình đúng, chỉ cần kiểm tra.
7. Theo dõi triển khai tại Pages hoặc Actions; khi hoàn tất, mở URL và tải lại mạnh bằng **Ctrl + F5**.
8. Kiểm tra bản mới, rồi đổi dòng trạng thái trong TXT thành “Đã triển khai và kiểm tra bản nâng cấp”.

Hướng dẫn chính thức:
https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site

## Checklist trước khi nộp

Kiểm tra mã đã thực hiện: đủ 8 HTML; 199 tham chiếu nội bộ có tệp/đích tồn tại; cấu trúc thẻ HTML cân bằng; SVG hợp lệ và CSS có các breakpoint responsive.
Chưa kiểm tra hiển thị bằng trình duyệt trong môi trường tạo bản này vì địa chỉ chạy cục bộ bị chặn. Bạn cần mở trên máy để kiểm tra giao diện thực tế ở các kích thước dưới đây.

- [ ] Đủ tám HTML, `index.html` ở gốc dự án.
- [ ] Menu, các liên kết và hình ảnh đều hoạt động.
- [ ] Xem ở 1440 px, 768 px, 375 px; thêm 320 px nếu có thể.
- [ ] Grid đổi cột, menu vừa màn hình, không cuộn ngang.
- [ ] Đã cập nhật mã nguồn lên GitHub và kiểm tra bản mới trên Pages.
- [ ] TXT có URL đúng và trạng thái đã triển khai.
- [ ] ZIP cuối chứa toàn bộ HTML, CSS, ảnh, README và TXT.
