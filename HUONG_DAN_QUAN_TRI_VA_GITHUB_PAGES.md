# CẨM NANG QUẢN TRỊ, BỔ SUNG SÁCH, XUẤT BẢN GITHUB PAGES & KẾT NỐI BACKEND
**Dự án:** KHO BÁU TRI THỨC – MỘT ĐỜI BIẾT ƠN (THƯ VIỆN TRI THỨC AN NHIÊN AI)  
**Người sáng lập:** Trịnh Thị An – An Nhiên AI — TTA  
**Tri ân:** Thầy Tuấn Tử Tế Từ Tâm

## PHẦN 1. HƯỚNG DẪN XUẤT BẢN LÊN GITHUB PAGES (HIỂN THỊ CHUẨN 100% CẢ 4 HÌNH ẢNH)

1. **Giải nén gói mã nguồn:** Giải nén tệp `kho-bau-tri-thuc-github-pages.zip` ra một thư mục trên máy tính.
2. **Tạo Kho lưu trữ (Repository) trên GitHub:**
   - Đăng nhập GitHub, nhấn **New repository**, đặt tên ví dụ: `kho-bau-tri-thuc`.
   - Chọn chế độ **Public** (để sử dụng GitHub Pages miễn phí) và nhấn **Create repository**.
3. **Tải toàn bộ file lên GitHub:**
   - Nhấn **uploading an existing file**, kéo toàn bộ `index.html`, thư mục `assets/` (bao gồm `css/`, `js/`, `data/`, `images/`) và `README.md` vào.
   - Lưu ý: Trong `assets/images/` đã có sẵn các tên file không dấu (`01.png`, `33.jpg`, `trang-bia-dau.png`, `trang-cuoi.jpg`, `trinh-thi-an.jpg`) khớp 100% với đường dẫn tương đối trong `index.html`, đảm bảo GitHub Pages tải hình nhanh và không bao giờ gặp lỗi mã hóa khoảng trắng hay tiếng Việt trên URL.
   - Nhấn **Commit changes**.
4. **Bật GitHub Pages:**
   - Vào mục **Settings** -> **Pages** (menu bên trái).
   - Tại phần **Build and deployment** -> **Branch**, chọn nhánh `main` (hoặc `master`), thư mục `/(root)` và nhấn **Save**.
   - Sau 1–2 phút, website của Chị sẽ hoạt động tại địa chỉ: `https://<ten-tai-khoan-github>.github.io/kho-bau-tri-thuc/`.

## PHẦN 2. HƯỚNG DẪN QUẢN TRỊ & BỔ SUNG HƠN 100 ĐẦU SÁCH MÀ KHÔNG CẦN SỬA CODE HTML

Chị có 2 cách rất thuận tiện để bổ sung sách mới hoặc cập nhật bài phân tích đã duyệt:

### Cách 1: Sử dụng Công cụ Quản trị ngay trên giao diện Website
1. Cuộn xuống mục **7. Góc học tập** -> Khung bên phải **"Công Cụ Quản Trị: Bổ Sung Sách Mới & Xuất JSON"**.
2. Điền **Tên sách**, **Tác giả**, chọn **Chủ đề** (1 trong 10 nhóm mục tiêu), nhập **Mô tả ngắn**, **Câu hỏi thay đổi cuộc sống** và chọn trạng thái (**Đã duyệt công khai** hoặc **Bản thảo chờ biên soạn**).
3. Nhấn **"+ Thêm Sách Vào Thư Viện"**: Sách mới sẽ xuất hiện ngay lập tức trong Kho Báu Sách và Không Gian Khám Phá 12 Nút.
4. Nhấn **"⬇ Xuất JSON Danh Mục"**: Hệ thống tự động xuất toàn bộ cấu trúc dữ liệu mới nhất ra khung văn bản và sao chép vào bộ nhớ tạm để Chị dán lưu vào file `assets/data/books.json` hoặc cập nhật biến `INITIAL_LIBRARY_DATA` trong `assets/js/app.js`.

### Cách 2: Cập nhật trực tiếp cấu trúc dữ liệu chuẩn (`books.json` / `app.js`)
Mỗi hồ sơ sách tuân theo cấu trúc chuẩn gồm:
- `id`: Mã định danh duy nhất (ví dụ: `"dac-nhan-tam"`).
- `code`: Mã ký hiệu kệ sách (ví dụ: `"TTA-BK-01"`).
- `title`, `author`, `category`, `categoryName`.
- `processStatus`: `"verified"` (Đã biên soạn & kiểm duyệt) hoặc `"pending"` (Chờ biên soạn).
- `sharePermission`: `"analysis_only"` (Chỉ công khai bài phân tích, bảo vệ bản quyền sách gốc).
- `mindmap`: Tâm điểm (`center`) và 4 nhánh (`branches`).
- `nodes`: Mảng 12 đối tượng tương ứng với 12 nút khám phá theo đặc thù chủ đề sách (`id`, `label`, `title`, `summary`, `points`, `example`, `application`).
- `researchProblems`: Mảng các câu hỏi thực tế người đọc quan tâm (7 mục trả lời chuẩn).

## PHẦN 3. QUY TRÌNH XỬ LÝ HƠN 100 SÁCH PDF BẰNG AI & CHI PHÍ DỊCH VỤ DỰ KIẾN

Để xử lý kho hơn 100 đầu sách PDF từ Google Drive riêng của Thầy Tuấn Tử Tế Từ Tâm một cách an toàn, đúng bản quyền và không lộ đường dẫn nguồn:

1. **Quy trình chạy công cụ AI nội bộ (Offline / Private Script):**
   - Đặt thư mục PDF ở máy tính cá nhân của Quản trị viên hoặc Google Drive riêng (tuyệt đối không bật chia sẻ công khai link Drive lên web).
   - Sử dụng script Python nội bộ gọi Gemini API (`gemini-2.5-flash` hoặc `gemini-2.5-pro`) thực hiện **10 bước phân tích**:
     - Bước 1–3: Nhận diện thông tin xuất bản, trích xuất mục lục và thông điệp tổng quan.
     - Bước 4–8: Phân tích từng chương, rút ra 10 bài học, phân tích đa chiều, tạo tình huống thực tế và sơ đồ tư duy 4 nhánh.
     - Bước 9: Biên tập thành bài giới thiệu giáo dục độc lập (không tái tạo nguyên văn sách gốc).
     - Bước 10: Xuất ra file nháp `draft_books.json` để Chị Trịnh Thị An đọc duyệt trước khi đưa lên website.
2. **Dịch vụ cần cấu hình & Chi phí phát sinh dự kiến:**
   - **Lưu trữ giao diện công khai (GitHub Pages / Cloudflare Pages):** **0đ (Miễn phí hoàn toàn)**.
   - **Xử lý bản thảo 100 sách PDF bằng AI API (Gemini API):**
     - Nếu dùng gói miễn phí (Google AI Studio Free tier) xử lý lần lượt từng cuốn: **0đ**.
     - Nếu dùng gói trả phí theo lượng token (Pay-as-you-go với Gemini Flash) cho 100 cuốn sách (~15–25 triệu token đầu vào): Chi phí một lần khoảng **5 USD – 15 USD** (tương đương 125.000đ – 380.000đ cho toàn bộ 100 cuốn).
   - **Hệ thống Thành viên & Cơ sở dữ liệu đám mây (Supabase hoặc Firebase):**
     - Gói khởi đầu (Free Tier của Supabase/Firebase) hỗ trợ tới **50.000 người dùng hoạt động/tháng** và **500MB cơ sở dữ liệu**: **0đ/tháng**.
     - Khi cộng đồng phát triển lớn (trên 50.000 thành viên hoặc cần lưu trữ lớn): Gói Pro khoảng **25 USD/tháng**.

## PHẦN 4. HƯỚNG DẪN KẾT NỐI BACKEND THỰC TẾ (SUPABASE / FIREBASE) & BẢO VỆ KHO SÁCH THẦY TUẤN TỬ TẾ TỪ TÂM

Khi muốn nâng cấp từ phiên bản Lưu trữ Trình duyệt (LocalStorage) sang Hệ thống Tài khoản Thành viên Đồng bộ Đám mây:

1. **Thiết lập xác thực (Authentication):**
   - Tạo dự án trên **Supabase** (hoặc **Firebase Authentication**).
   - Bật đăng nhập bằng Email/Mật khẩu hoặc Google OAuth.
   - Tuyệt đối chỉ dùng `anon public key` kèm **Row Level Security (RLS)** ở phía trình duyệt; mọi `service_role secret key` hoặc thông tin kết nối Google Drive API phải đặt trên biến môi trường máy chủ (Cloudflare Workers / Supabase Edge Functions).
2. **Thiết lập Bảng phân quyền (Database Tables & RLS):**
   - Bảng `profiles`: Lưu `user_id`, `role` (`member`, `editor`, `admin`).
   - Bảng `member_notes` & `member_favorites`: Áp dụng chính sách RLS `auth.uid() = user_id` để mỗi thành viên chỉ đọc/sửa được sổ tay của chính mình.
   - Bảng `books_catalog`: Công khai các bài phân tích có `process_status = 'verified'`; ẩn các bản thảo `pending` chỉ cho phép `role = 'admin'` duyệt.
3. **Nguyên tắc Bảo vệ Kho sách Thầy Tuấn Tử Tế Từ Tâm:**
   - Không bao giờ nhúng Folder ID hay link Google Drive gốc vào mã nguồn frontend.
   - Lưu ý bảo mật trung thực: Mọi nội dung văn bản và hình ảnh khi đã hiển thị công khai trên trình duyệt đều có thể được người xem đọc hoặc chụp màn hình; vì vậy việc ẩn liên kết kho nguồn giúp **bảo vệ tuyệt đối thư mục PDF gốc của Thầy Tuấn Tử Tế Từ Tâm**, đồng thời chỉ xuất bản các bài phân tích giáo dục đã được kiểm duyệt.

## PHẦN 5. DANH SÁCH TÍNH NĂNG ĐÃ HOÀN THÀNH & LỘ TRÌNH MỞ RỘNG MINH BẠCH

| Hạng mục tính năng | Trạng thái hiện tại | Ghi chú kỹ thuật |
| :--- | :--- | :--- |
| **1. Trải nghiệm Mở Sách Tri Ân 3D & Bức thư viết tay** | **Đã hoàn thành 100%** | Hiệu ứng mở sách mượt mà, đúng nguyên văn bức thư tri ân Thầy Tuấn Tử Tế Từ Tâm, có tùy chọn bỏ qua lần sau. |
| **2. Tích hợp 4 bức hình nghệ thuật gốc của Chị Trịnh Thị An** | **Đã hoàn thành 100%** | Giữ nguyên 100% ảnh gốc, chữ ký T.T.An / An Nhiên AI, đúng 4 vị trí yêu cầu, có Lightbox phóng to. |
| **3. Thiết kế Luxury Editorial Library & Hỗ trợ người lớn tuổi** | **Đã hoàn thành 100%** | Bảng màu chuẩn (`#FFF9EF`, `#8BAA91`, `#284C40`, `#D8B66A`, `#4A382D`), nút chỉnh cỡ chữ Lớn/Rất lớn, nút Giảm chuyển động. |
| **4. Thanh điều hướng 10 mục & Cấu trúc Trang chủ (A, B, C, D, E)** | **Đã hoàn thành 100%** | Responsive trên điện thoại, máy tính bảng và máy tính. |
| **5. Hệ thống Danh mục Kho sách, Tìm kiếm & Bộ lọc 10 chủ đề** | **Đã hoàn thành 100%** | Đầy đủ các đầu sách xác thực từ danh mục ban đầu + mẫu tương tác Đắc Nhân Tâm + trạng thái chờ biên soạn minh bạch. |
| **6. Không gian Khám phá 12 Nút tương tác & Sơ đồ tư duy** | **Đã hoàn thành 100%** | 12 nút tùy biến sát chủ đề thực tế của từng sách, hiển thị ngay tại chỗ không chuyển trang trống. |
| **7. Tính năng Chọn vấn đề nghiên cứu & Tra cứu đối chiếu** | **Đã hoàn thành 100%** | Hiển thị đủ 7 mục giải đáp thực tiễn và công cụ đối chiếu dữ liệu đã duyệt (không bịa nội dung). |
| **8. Góc Học tập: Lưu ghi chú, Sách yêu thích & Tiến độ đọc** | **Đã hoàn thành 100%** | Hoạt động ngay trên trình duyệt với cơ chế lưu trữ an toàn. |
| **9. Công cụ Quản trị thêm sách mới & Xuất JSON danh mục** | **Đã hoàn thành 100%** | Cho phép thêm sách, thêm website và xuất JSON không cần sửa HTML. |
| **10. Góc Âm nhạc An Nhiên & Kết nối mạng xã hội (FB, YT, Zalo)** | **Đã hoàn thành 100%** | Có trình phát nhạc đọc sách (không tự phát), kết nối đúng kênh YouTube, Facebook và Zalo `0834 133 344`. |
| **11. Xác thực Thành viên Server-side & Worker AI đọc 100+ PDF** | **Cần cấu hình dịch vụ Backend khi triển khai mở rộng** | Đã thiết kế sẵn kiến trúc dữ liệu và hướng dẫn chi tiết kết nối Supabase/Firebase & Gemini API tại Phần 3 & Phần 4 tài liệu này. |
