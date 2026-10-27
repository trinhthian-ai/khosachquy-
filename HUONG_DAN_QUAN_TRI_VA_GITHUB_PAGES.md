# SIÊU CÂU LỆNH TẠO WEBSITE & CẨM NANG QUẢN TRỊ, XUẤT BẢN GITHUB PAGES

**Dự án:** KHO BÁU TRI THỨC – MỘT ĐỜI BIẾT ƠN (THƯ VIỆN TRI THỨC AN NHIÊN AI)

**Người sáng lập & Tác giả:** Trịnh Thị An – An Nhiên AI (TTA)

**Tri ân:** Thầy Tuấn Tử Tế Từ Tâm — Người Thầy "5T" (Tuấn – Tử – Tế – Từ – Tâm)

---

## PHẦN MỞ ĐẦU: SIÊU CÂU LỆNH TẠO WEBSITE (MASTER PROMPT ĐÃ BỔ SUNG ĐẦY ĐỦ)

> Chị 7 An có thể sao chép nguyên văn khối câu lệnh dưới đây để sử dụng hoặc lưu trữ làm chuẩn kiến tạo/nâng cấp website **Kho Báu Tri Thức – Một Đời Biết Ơn**:

```text
SIÊU PROMPT KIẾN TẠO WEBSITE THƯ VIỆN TRI THỨC TƯƠNG TÁC – AN NHIÊN AI (PHIÊN BẢN NÂNG CẤP HOÀN CHỈNH)

1. VAI TRÒ & MỆNH LỆNH TỔNG THỂ
Bạn hãy đóng vai Hội đồng chuyên gia hàng đầu thế giới về nghiên cứu sách, tổ chức tri thức, giáo dục, công nghệ AI, nghệ thuật xuất bản, thiết kế UI/UX và lập trình website Full-Stack.
Nhiệm vụ của bạn là lập trình một WEBSITE HTML5/CSS3/JAVASCRIPT THỰC TẾ, HOÀN CHỈNH, TƯƠNG TÁC SÂU VÀ CÓ GIÁ TRỊ GIÁO DỤC CAO (triển khai trực tiếp trên trình duyệt và GitHub Pages):
- Tên website: KHO BÁU TRI THỨC – MỘT ĐỜI BIẾT ƠN
- Tên phụ: THƯ VIỆN TRI THỨC AN NHIÊN AI
- Thông điệp: "Mỗi trang sách mở ra – Một chân trời tri thức."
- Người sáng lập và xây dựng: Trịnh Thị An – An Nhiên AI (TTA).
- Nguồn cảm hứng & Tri ân: Kho sách quý do Thầy Tuấn Tử Tế Từ Tâm trao tặng — Người Thầy "5T" (Tuấn – Tử – Tế – Từ – Tâm). Lưu ý: Tên "Thầy Tuấn Tử Tế Từ Tâm" viết liền mạch, trang trọng.
- Giá trị cốt lõi: "TRI THỨC ĐƯỢC TRAO TẶNG – LÒNG BIẾT ƠN ĐƯỢC LAN TỎA – GIÁ TRỊ ĐƯỢC NHÂN LÊN." Không thương mại hóa kho sách gốc, không phát tán file PDF có bản quyền, bảo vệ tuyệt đối đường dẫn Google Drive nguồn.

2. TÍCH HỢP HÌNH ẢNH CHÂN DUNG TÁC GIẢ TRỊNH THỊ AN & BỘ 4 TÁC PHẨM NGHỆ THUẬT GỐC
- Bắt buộc tích hợp trực tiếp hình chân dung thật của Tác giả & Người sáng lập Trịnh Thị An (`a1.jpg` / `assets/images/trinh-thi-an.jpg` kèm mã hóa Base64 dự phòng `window.TTA_PORTRAIT_DATA_URI` để đảm bảo hiển thị sắc nét 100%, không bao giờ bị lỗi gãy ảnh trên mọi môi trường) tại 7 vị trí trọng tâm:
  (1) Bìa sách mở đầu Tri ân,
  (2) Trang trái khi mở sách Tri ân (`#intro-author-portrait`),
  (3) Thanh điều hướng chính (Header Brand),
  (4) Khu vực A – Banner chính Trang chủ (`#hero-author-img`, khung viền vàng champagne trang trọng),
  (5) Khu vực Lời Tri Ân Thầy Tuấn Tử Tế Từ Tâm,
  (6) Khu vực 10 – Giới thiệu & Kết nối (`#founder-main-portrait`),
  (7) Chân trang (Footer).
- Giữ nguyên 100% không cắt xén chữ ký T.T.An / An Nhiên AI trên 4 bức hình nghệ thuật đính kèm (`01.png`, `TRANG BÌA ĐẦU.png`, `33.jpg`, `TRANG CUỐI.jpg`) và tích hợp Lightbox phóng to sắc nét khi người dùng nhấn vào ảnh.

3. TRẢI NGHIỆM MỞ SÁCH 3D & "TRANG THƯ CỦA TRỊNH THỊ AN" TRÊN GIẤY VỞ Ô LY
- Khi truy cập, hiển thị cuốn sách lớn "KHO BÁU TRI THỨC – MỘT ĐỜI BIẾT ƠN | Tri ân Thầy Tuấn Tử Tế Từ Tâm (Người Thầy 5T)" với nút "📖 MỞ TRANG SÁCH TRI ÂN".
- Khi mở sách ra 2 trang:
  + Trang bên trái: Hình ảnh nghệ thuật "BIẾT ƠN THẦY TUẤN TỬ TẾ TỪ TÂM – TĂNG TƯƠNG TÁC – TẠO TUYỆT TÁC" và Thẻ Chân dung Tác giả Trịnh Thị An.
  + Trang bên phải: Mang tiêu đề chính thức "TRANG THƯ CỦA TRỊNH THỊ AN" (tuyệt đối sử dụng cụm từ "TRANG THƯ CỦA TRỊNH THỊ AN" thay cho cụm từ "CHỮ VIẾT TAY CỦA CÔ GIÁO LUYỆN CHỮ ĐẸP TRÊN GIẤY Ô LI").
  + Nội dung bức thư "GỬI NGƯỜI THẦY TÔI LUÔN BIẾT ƠN" được trình bày bằng phông chữ viết tay tiếng Việt mềm mại, thanh thoát, khóa chân chữ thẳng hàng và canh đều 2 bên chuẩn xác trên dòng kẻ ngang giấy vở ô ly tiểu học 4x4 (có lề đỏ đôi, hoa văn 4 góc và nút chọn màu mực: Mực Tím Truyền Thống, Mực Đỏ Nghệ Thuật, Nét Thanh Đậm).
  + Có nút "✨ BƯỚC VÀO KHO TÀNG TRI THỨC →" và tùy chọn bỏ qua màn hình giới thiệu ở lần truy cập tiếp theo.

4. TÍCH HỢP THỜI GIAN HIỆN HÀNH & Ô SỐ LƯỢNG NGƯỜI TRUY CẬP TRỰC QUAN
- Đồng hồ Thời gian hiện hành (Real-time Clock): Tự động cập nhật từng giây (`setInterval(..., 1000)`) theo múi giờ Việt Nam (GMT+7), hiển thị đầy đủ Thứ, Ngày/Tháng/Năm và Giờ:Phút:Giây (`HH:MM:SS`) tại:
  (1) Thanh công cụ đầu trang (`#topbar-live-clock`),
  (2) Màn hình bìa sách mở đầu (`#intro-live-clock`),
  (3) Ô Thời Gian Hiện Hành nổi bật tại Khu vực A – Banner chính Trang chủ (`#hero-live-time`, `#hero-live-date`),
  (4) Chân trang (`#footer-live-clock`).
- Ô Số lượng người truy cập (Visitor Counter Box): Thiết kế khung thống kê sang trọng hiển thị Tổng lượt truy cập, Lượt truy cập hôm nay và Trạng thái đang hoạt động trực tuyến tại Thanh đầu trang, Khu vực A – Banner chính (`#hero-visitor-total`, `#hero-visitor-today`, `#hero-visitor-online`) và Chân trang; tự động ghi nhận và cộng lượt truy cập qua `localStorage` an toàn (bọc `try/catch`).

5. THIẾT KẾ MỸ THUẬT & TRỢ NĂNG CHO NGƯỜI TRUNG NIÊN, LỚN TUỔI
- Phong cách: Luxury Editorial Library kết hợp Interactive Knowledge Museum.
- Bảng màu chuẩn: Trắng ngà `#FFF9EF`, Xanh lá dịu `#8BAA91`, Xanh rừng `#284C40`, Vàng champagne `#D8B66A`, Nâu mực `#4A382D`.
- Chữ lớn rõ ràng (mặc định 18px–20px), có nút chuyển đổi Cỡ chữ (Chuẩn / Lớn / Rất lớn 22px) và nút Giảm chuyển động.

6. CẤU TRÚC 10 MỤC ĐIỀU HƯỚNG & TRANG KHÁM PHÁ 12 NÚT TƯƠNG TÁC TRUNG TÂM
- Thanh điều hướng 10 mục: 1. Trang chủ | 2. Lời tri ân | 3. Kho báu sách | 4. Khám phá tri thức | 5. Sách hay nên đọc | 6. Nghiên cứu chuyên sâu | 7. Góc học tập | 8. Âm nhạc An Nhiên | 9. Website đã kiến tạo | 10. Giới thiệu – Kết nối.
- Mỗi cuốn sách mở ra Không gian Khám phá 12 nút tương tác chuyên sâu (tùy biến theo chủ đề sách), Sơ đồ tư duy 4 nhánh trực quan, Câu hỏi "Cuốn sách này giúp tôi thay đổi điều gì?", tính năng "Bạn đang muốn tìm câu trả lời cho vấn đề gì?" (7 mục trả lời thực tiễn), Góc học tập lưu ghi chú và Công cụ Quản trị thêm sách mới / xuất JSON.
```

---

## PHẦN 1. HƯỚNG DẪN XUẤT BẢN LÊN GITHUB PAGES (HIỂN THỊ CHUẨN 100% CHÂN DUNG CHỊ TRỊNH THỊ AN & 4 HÌNH NGHỆ THUẬT)

1. **Giải nén gói mã nguồn:** Giải nén tệp `kho-bau-tri-thuc-github-pages.zip` ra một thư mục trên máy tính.

2. **Tạo Kho lưu trữ (Repository) trên GitHub:**
   * Đăng nhập GitHub, nhấn **New repository**, đặt tên ví dụ: `kho-bau-tri-thuc`.
   * Chọn chế độ **Public** (để sử dụng GitHub Pages miễn phí) và nhấn **Create repository**.

3. **Tải toàn bộ file lên GitHub:**
   * Nhấn **uploading an existing file**, kéo toàn bộ `index.html`, `a1.jpg`, `trinh-thi-an.jpg`, thư mục `assets/` (bao gồm `css/`, `js/`, `data/`, `images/`) và `README.md` vào.
   * **Bảo đảm không bao giờ lỗi ảnh chân dung:** Trong gói ZIP đã được tích hợp đồng thời cả tệp ảnh vật lý (`assets/images/trinh-thi-an.jpg`, `assets/images/a1.jpg`, `a1.jpg`) **VÀ** dữ liệu ảnh Base64 nhúng trực tiếp trong `index.html` & `assets/js/app.js`. Nhờ đó, dù Chị mở trực tiếp file `index.html` trên máy hay đăng lên GitHub Pages, hình chân dung của Chị luôn hiển thị sắc nét 100%.
   * Nhấn **Commit changes**.

4. **Bật GitHub Pages:**
   * Vào mục **Settings** -> **Pages** (menu bên trái).
   * Tại phần **Build and deployment** -> **Branch**, chọn nhánh `main` (hoặc `master`), thư mục `/(root)` và nhấn **Save**.
   * Sau 1–2 phút, website của Chị sẽ hoạt động tại địa chỉ: `https://<ten-tai-khoan-github>.github.io/kho-bau-tri-thuc/`.

---

## PHẦN 2. HƯỚNG DẪN QUẢN TRỊ & BỔ SUNG HƠN 100 ĐẦU SÁCH MÀ KHÔNG CẦN SỬA CODE HTML

Chị có 2 cách rất thuận tiện để bổ sung sách mới hoặc cập nhật bài phân tích đã duyệt:

### Cách 1: Sử dụng Công cụ Quản trị ngay trên giao diện Website

1. Cuộn xuống mục **7. Góc học tập** -> Khung bên phải **"Công Cụ Quản Trị: Bổ Sung Sách Mới & Xuất JSON"**.
2. Điền **Tên sách**, **Tác giả**, chọn **Chủ đề** (1 trong 10 nhóm mục tiêu), nhập **Mô tả ngắn**, **Câu hỏi thay đổi cuộc sống** và chọn trạng thái (**Đã duyệt công khai** hoặc **Bản thảo chờ biên soạn**).
3. Nhấn **"+ Thêm Sách Vào Thư Viện"**: Sách mới sẽ xuất hiện ngay lập tức trong Kho Báu Sách và Không Gian Khám Phá 12 Nút.
4. Nhấn **"⬇ Xuất JSON Danh Mục"**: Hệ thống tự động xuất toàn bộ cấu trúc dữ liệu mới nhất ra khung văn bản và sao chép vào bộ nhớ tạm để Chị dán lưu vào file `assets/data/books.json` hoặc cập nhật biến `INITIAL_LIBRARY_DATA` trong `assets/js/app.js`.

### Cách 2: Cập nhật trực tiếp cấu trúc dữ liệu chuẩn (`books.json` / `app.js`)

Mỗi hồ sơ sách tuân theo cấu trúc chuẩn gồm:
* `id`: Mã định danh duy nhất (ví dụ: `"dac-nhan-tam"`).
* `code`: Mã ký hiệu kệ sách (ví dụ: `"TTA-BK-01"`).
* `title`, `author`, `category`, `categoryName`.
* `processStatus`: `"verified"` (Đã biên soạn & kiểm duyệt) hoặc `"pending"` (Chờ biên soạn).
* `sharePermission`: `"analysis_only"` (Chỉ công khai bài phân tích, bảo vệ bản quyền sách gốc).
* `mindmap`: Tâm điểm (`center`) và 4 nhánh (`branches`).
* `nodes`: Mảng 12 đối tượng tương ứng với 12 nút khám phá theo đặc thù chủ đề sách (`id`, `label`, `title`, `summary`, `points`, `example`, `application`).
* `researchProblems`: Mảng các câu hỏi thực tế người đọc quan tâm (7 mục trả lời chuẩn).

---

## PHẦN 3. QUY TRÌNH XỬ LÝ HƠN 100 SÁCH PDF BẰNG AI & CHI PHÍ DỊCH VỤ DỰ KIẾN

Để xử lý kho hơn 100 đầu sách PDF từ Google Drive riêng của **Thầy Tuấn Tử Tế Từ Tâm** (Người Thầy "5T") một cách an toàn, đúng bản quyền và không lộ đường dẫn nguồn:

1. **Quy trình chạy công cụ AI nội bộ (Offline / Private Script):**
   * Đặt thư mục PDF ở máy tính cá nhân của Quản trị viên hoặc Google Drive riêng (tuyệt đối không bật chia sẻ công khai link Drive lên web).
   * Sử dụng script Python nội bộ gọi Gemini API (`gemini-2.5-flash` hoặc `gemini-2.5-pro`) thực hiện **10 bước phân tích**:
     * Bước 1–3: Nhận diện thông tin xuất bản, trích xuất mục lục và thông điệp tổng quan.
     * Bước 4–8: Phân tích từng chương, rút ra 10 bài học, phân tích đa chiều, tạo tình huống thực tế và sơ đồ tư duy 4 nhánh.
     * Bước 9: Biên tập thành bài giới thiệu giáo dục độc lập (không tái tạo nguyên văn sách gốc).
     * Bước 10: Xuất ra file nháp `draft_books.json` để Chị Trịnh Thị An đọc duyệt trước khi đưa lên website.

2. **Dịch vụ cần cấu hình & Chi phí phát sinh dự kiến:**
   * **Lưu trữ giao diện công khai (GitHub Pages / Cloudflare Pages):** **0đ (Miễn phí hoàn toàn)**.
   * **Xử lý bản thảo 100 sách PDF bằng AI API (Gemini API):**
     * Nếu dùng gói miễn phí (Google AI Studio Free tier) xử lý lần lượt từng cuốn: **0đ**.
     * Nếu dùng gói trả phí theo lượng token (Pay-as-you-go với Gemini Flash) cho 100 cuốn sách (~15–25 triệu token đầu vào): Chi phí một lần khoảng **5 USD – 15 USD** (tương đương 125.000đ – 380.000đ cho toàn bộ 100 cuốn).
   * **Hệ thống Thành viên & Cơ sở dữ liệu đám mây (Supabase hoặc Firebase):**
     * Gói khởi đầu (Free Tier của Supabase/Firebase) hỗ trợ tới **50.000 người dùng hoạt động/tháng** và **500MB cơ sở dữ liệu**: **0đ/tháng**.

---

## PHẦN 4. DANH SÁCH TÍNH NĂNG ĐÃ HOÀN THÀNH 100% TRONG BẢN CẬP NHẬT MỚI NHẤT

| Hạng mục tính năng | Trạng thái hiện tại | Ghi chú kỹ thuật |
| ----- | ----- | ----- |
| **1. Tích hợp ảnh chân dung thật của Chị Trịnh Thị An (`a1.jpg`)** | **Đã hoàn thành 100%** | Nhúng trực tiếp Base64 + file vật lý trong gói GitHub Pages tại 7 vị trí, hiển thị sắc nét, không bao giờ lỗi ảnh. |
| **2. Đổi tiêu đề thành "TRANG THƯ CỦA TRỊNH THỊ AN"** | **Đã hoàn thành 100%** | Thay thế hoàn toàn cụm từ cũ trên cả trang mở sách 3D và mục Lời Tri Ân, giữ nguyên chữ viết tay thẳng hàng trên giấy ô ly. |
| **3. Đồng hồ Thời gian hiện hành (Real-time Clock)** | **Đã hoàn thành 100%** | Cập nhật từng giây theo múi giờ Việt Nam (Thứ, Ngày/Tháng/Năm, Giờ:Phút:Giây) tại Thanh đầu trang, Bìa sách, Banner chính và Chân trang. |
| **4. Ô Số lượng người truy cập (Visitor Counter Box)** | **Đã hoàn thành 100%** | Hiển thị Tổng lượt truy cập, Lượt truy cập hôm nay và Trạng thái trực tuyến; tự động lưu và cộng lượt truy cập qua LocalStorage. |
| **5. Tri ân Thầy Tuấn Tử Tế Từ Tâm (Người Thầy "5T")** | **Đã hoàn thành 100%** | Hiển thị đồng bộ, trang trọng tên Thầy Tuấn Tử Tế Từ Tâm (Người Thầy "5T") xuyên suốt toàn bộ website. |
| **6. Không gian Khám phá 12 Nút tương tác, Sơ đồ tư duy & Góc học tập** | **Đã hoàn thành 100%** | Đầy đủ 12 nút khám phá chuyên sâu, tra cứu vấn đề thực tế, nhạc đọc sách An Nhiên và công cụ quản trị xuất JSON. |
