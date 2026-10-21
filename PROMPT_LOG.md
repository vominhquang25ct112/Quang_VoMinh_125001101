# NHẬT KÝ PROMPT ENGINEERING (PROMPT LOG)
## DỰ ÁN BÀI THI GIỮA KỲ: ECOSHOP - CỬA HÀNG THỜI TRANG XANH
**Môn học:** Thiết kế Web & Lập trình Front-end cơ bản  
**Phương pháp:** Vibe Coding & Prompt Engineering có kiểm soát  

---

### THÔNG TIN SINH VIÊN
- **Họ và tên:** Võ Minh Quang
- **Mã số sinh viên (MSSV):** 125001101
- **Lớp sinh hoạt:** 25CT112
- **Tên đề tài:** EcoShop - Cửa hàng Thời trang Xanh & Smart Shopping Cart
- **Kho lưu trữ (Repository):** `vominhquang25ct112/Quang_VoMinh_125001101`
- **Công nghệ cốt lõi:** 100% Thuần HTML5 & CSS3 (Không sử dụng JavaScript)
- **Kiến trúc Website:** Website bán hàng đa trang gồm 3 trang HTML liên kết chặt chẽ:
  + `index.html` (Trang Chủ)
  + `products.html` (Trang Danh Sách Sản Phẩm)
  + `contact.html` (Trang Liên Hệ & Form Hỗ Trợ)
  + `style.css` (File CSS Dùng Chung Toàn Hệ Thống)

---

## MỤC LỤC
1. [Tổng quan dự án & Tiêu chí kỹ thuật](#1-tổng-quan-dự-án--tiêu-chí-kỹ-thuật)
2. [Giai đoạn 1: Thiết lập Nền tảng & Cấu trúc (Tuần 1 & Tuần 2)](#2-giai-đoạn-1-thiết-lập-nền-tảng--cấu-trúc-tuần-1--tuần-2)
   - [Prompt 1: Khởi tạo Design System & Biến CSS (:root)](#prompt-1-khởi-tạo-design-system--biến-css-root)
   - [Prompt 2: Xây dựng khung Semantic HTML5 chuẩn SEO](#prompt-2-xây-dựng-khung-semantic-html5-chuẩn-seo)
3. [Giai đoạn 2: Hệ thống Giao diện & Responsive (Tuần 3 & Tuần 4)](#3-giai-đoạn-2-hệ-thống-giao-diện--responsive-tuần-3--tuần-4)
   - [Prompt 3: Dàn trang bằng CSS Grid và Flexbox](#prompt-3-dàn-trang-bằng-css-grid-và-flexbox)
   - [Prompt 4: Tích hợp Responsive Mobile-First & Media Queries](#prompt-4-tích-hợp-responsive-mobile-first--media-queries)
4. [Giai đoạn 3: Hiệu ứng Chuyển động & Hoàn thiện (Tuần 5 & Tuần 6)](#4-giai-đoạn-3-hiệu-ứng-chuyển-động--hoàn-thiện-tuần-5--tuần-6)
   - [Prompt 5: Tích hợp hiệu ứng Thư viện (AOS & Animate.css) và Micro-interactions](#prompt-5-tích-hợp-hiệu-ứng-thư-viện-aos--animatecss-và-micro-interactions)
   - [Prompt 6: Tối ưu hóa mã nguồn (Refactoring) & Kiểm tra W3C](#prompt-6-tối-ưu-hóa-mã-nguồn-refactoring--kiểm-tra-w3c)
5. [Các Prompt Tinh Chỉnh Nâng Cao Thực Tế](#5-các-prompt-tinh-chỉnh-nâng-cao-thực-tế)
   - [5.1. Pure HTML5/CSS3 Checkbox Hack (Không dùng JS)](#51-pure-html5css3-checkbox-hack-không-dùng-js)
   - [5.2. Tích hợp Hình ảnh thực tế Unsplash & Nội dung Tiếng Việt chuyên nghiệp](#52-tích-hợp-hình-ảnh-thực-tế-unsplash--nội-dung-tiếng-việt-chuyên-nghiệp)
   - [5.3. Mở rộng Kiến trúc Website Đa Trang (Multi-Page Navigation Architecture)](#53-mở-rộng-kiến-trúc-website-đa-trang-multi-page-navigation-architecture)
6. [Bảng tổng hợp đánh giá hiệu quả Prompting](#6-bảng-tổng-hợp-đánh-giá-hiệu-quả-prompting)
7. [Bài học kinh nghiệm & Tư duy Vibe Coding](#7-bài-học-kinh-nghiệm--tư-duy-vibe-coding)

---

## 1. TỔNG QUAN DỰ ÁN & TIÊU CHÍ KỸ THUẬT

Dự án **EcoShop** là một website thương mại điện tử chuyên nghiệp cung cấp các mặt hàng thời trang bền vững (Organic Cotton, Vải sợi tre Bamboo, Vải Linen tự nhiên, Denim tái chế). Trang web được thiết kế theo cấu trúc đa trang (Multi-page Website) với 3 trang HTML chuyên biệt dùng chung một file `style.css`:
- **index.html (Trang Chủ):** Header, Banner Hero ấn tượng, danh mục tiêu biểu, khối ưu điểm cửa hàng (Why Choose Us), đánh giá từ khách hàng (Testimonials) và Footer.
- **products.html (Trang Danh Sách Sản Phẩm):** Banner danh mục, bộ lọc chuyên sâu, lưới sản phẩm CSS Grid co giãn tự động hiển thị 8 sản phẩm thời trang cao cấp với ảnh thật Unsplash, mô tả ngắn, giá niêm yết, giá giảm và nút đặt mua.
- **contact.html (Trang Liên Hệ):** Form gửi thắc mắc chuẩn Semantic kiểm tra dữ liệu bằng HTML5 Native (`required`, `type="email"`, `type="tel"`, `pattern`), danh sách 2 showroom lớn tại TP.HCM & Hà Nội, hotline 24/7, giờ mở cửa và khung bản đồ Google Maps trực quan.
- **Tiêu chuẩn kỹ thuật cốt lõi:**
  + 100% Thuần HTML5 & CSS3 — **Tuyệt đối không sử dụng JavaScript**.
  + Toàn bộ màu sắc gọi từ biến CSS `:root` qua hàm `var()`.
  + Layout CSS Grid `repeat(auto-fit, minmax(260px, 1fr))` & Flexbox.
  + Responsive Mobile-First mượt mà, không xuất hiện thanh cuộn ngang.
  + Pure CSS Checkbox Hack cho thanh menu điều hướng di động.

---

## 2. GIAI ĐOẠN 1: THIẾT LẬP NỀN TẢNG & CẤU TRÚC (TUẦN 1 & TUẦN 2)

### Prompt 1: Khởi tạo Design System & Biến CSS (:root)
- **Mục tiêu:** Thiết lập bảng biến CSS `:root`, thực hiện Reset CSS cơ bản, định dạng font chữ hiện đại.
- **Thời gian thực hiện:** Tuần 1
- **Câu Prompt gửi AI:**
  > *"Bạn là một chuyên gia UI/UX Front-end. Hãy giúp tôi thiết kế cấu trúc file style.css cho một trang web bán hàng thời trang online ('EcoShop'). Hãy khai báo phần :root chứa hệ thống Design System bao gồm: 2 màu chủ đạo (--primary-color, --secondary-color), 3 mức màu xám cho văn bản (--text-main, --text-muted, --bg-light), biến khoảng cách (--spacing-base: 15px) và tốc độ chuyển động (--transition-speed: 0.3s). Đồng thời viết đoạn Reset CSS cơ bản (* { margin: 0; padding: 0; box-sizing: border-box; }) và thiết lập font chữ hiện đại, sạch sẽ."*
- **Kết quả AI sinh ra:**
  ```css
  :root {
    --primary-color: #2D6A4F;
    --secondary-color: #52B788;
    --text-dark: #1B2421;
    --text-muted: #64748B;
    --bg-light: #F4F7F5;
    --spacing-base: 15px;
    --transition-speed: 0.3s;
    --border-radius: 12px;
  }
  *, *::before, *::after {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
  }
  body {
    font-family: 'Plus Jakarta Sans', system-ui, sans-serif;
    background-color: var(--bg-light);
    color: var(--text-dark);
  }
  ```
- **Nhận xét & Tinh chỉnh của sinh viên:**
  - *Đánh giá:* AI đã định nghĩa đầy đủ các biến chủ đạo. Mã màu xanh rừng (#2D6A4F) và xanh bạc hà (#52B788) rất phù hợp với chủ đề thời trang sinh thái EcoShop.
  - *Tinh chỉnh thêm:* Khai báo bổ sung các biến màu phụ trợ như `--accent-color`, `--accent-badge`, `--footer-text`, `--footer-border` để đảm bảo 100% trong file CSS không tồn tại bất kỳ mã màu cứng (hardcoded hex) nào, thuận tiện bảo trì.

---

### Prompt 2: Xây dựng khung Semantic HTML5 chuẩn SEO
- **Mục tiêu:** Viết mã nguồn HTML với đầy đủ các thẻ ngữ nghĩa HTML5, tối ưu SEO On-page và ghi chú vai trò từng thẻ.
- **Thời gian thực hiện:** Tuần 2
- **Câu Prompt gửi AI:**
  > *"Dựa trên hệ thống biến CSS vừa tạo, hãy viết mã nguồn file index.html hoàn chỉnh cho trang chủ 'EcoShop' theo chuẩn Semantic HTML5 (tuyệt đối không lạm dụng thẻ <div> vô nghĩa). Trang web phải bao gồm tối thiểu các vùng sau: <header> chứa logo 'EcoShop' và thanh điều hướng <nav> (có các mục: Trang chủ, Sản phẩm, Khuyến mãi, Giới thiệu, Liên hệ); <main> chứa các khối <section> gồm: Hero Section (Banner chào mừng với tiêu đề lớn và nút kêu gọi hành động CTA), Featured Products Section (Khu vực trưng bày sản phẩm nổi bật), Testimonials / Why Choose Us Section (Đánh giá khách hàng & ưu điểm cửa hàng); <footer> chứa thông tin bản quyền, mạng xã hội và liên hệ. Hãy giải thích rõ vai trò của từng thẻ Semantic bằng các chú thích (comment) trong code."*
- **Kết quả AI sinh ra:**
  Cấu trúc HTML5 phân cấp với `<header>`, `<nav>`, `<main>`, `<section id="hero">`, `<section id="featured-products">`, `<section id="features">`, `<section id="testimonials">`, và `<footer id="contact">`.
- **Nhận xét & Tinh chỉnh của sinh viên:**
  - *Đánh giá:* Cấu trúc tài liệu mạch lạc, các thẻ tiêu đề `<h1>`, `<h2>`, `<h3>` tuân thủ đúng thứ bậc phân cấp của W3C.
  - *Tinh chỉnh thêm:* Sinh viên đã thay thế các khối thẻ sản phẩm bằng thẻ ngữ nghĩa `<article class="product-card">`, thêm thẻ `<address>` cho thông tin liên hệ ở Footer, bổ sung thuộc tính trợ năng `aria-label`, `aria-labelledby`, `role` để trang web đạt chuẩn Accessibility (a11y).

---

## 3. GIAI ĐOẠN 2: HỆ THỐNG GIAO DIỆN & RESPONSIVE (TUẦN 3 & TUẦN 4)

### Prompt 3: Dàn trang bằng CSS Grid và Flexbox
- **Mục tiêu:** Áp dụng Flexbox cho thanh điều hướng và CSS Grid cho danh sách sản phẩm.
- **Thời gian thực hiện:** Tuần 3
- **Câu Prompt gửi AI:**
  > *"Hãy viết mã CSS tiếp nối cho file style.css để dàn trang cho trang web bán hàng 'EcoShop': Sử dụng Flexbox để canh chỉnh thanh điều hướng (<nav>) phân bố đều hai bên (Logo bên trái, Menu ở giữa, Icon giỏ hàng/User bên phải). Sử dụng CSS Grid (grid-template-columns: repeat(auto-fit, minmax(260px, 1fr))) cho phần danh sách sản phẩm để các thẻ sản phẩm (Product Cards) tự động co giãn và sắp xếp lưới đẹp mắt, khoảng cách giữa các thẻ là var(--spacing-base). Đảm bảo hình ảnh sản phẩm bên trong card luôn linh hoạt (max-width: 100%; height: auto; display: block;)."*
- **Kết quả AI sinh ra:**
  ```css
  .header-wrapper {
    display: flex;
    align-items: center;
    justify-content: space-between;
  }
  .product-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
    gap: var(--spacing-base);
  }
  img {
    max-width: 100%;
    height: auto;
    display: block;
    object-fit: cover;
  }
  ```
- **Nhận xét & Tinh chỉnh của sinh viên:**
  - *Đánh giá:* CSS Grid với `auto-fit` và `minmax` giúp bố cục lưới tự thích ứng linh hoạt mà không bị gãy vỡ hàng khi thu phóng màn hình.
  - *Tinh chỉnh thêm:* Sử dụng `aspect-ratio: 1 / 1.1` cho khung ảnh sản phẩm (`.card-image-box`) để đảm bảo toàn bộ hình ảnh sản phẩm có kích thước đồng nhất, không gây hiện tượng lệch khung (Layout Shift).

---

### Prompt 4: Tích hợp Responsive Mobile-First & Media Queries
- **Mục tiêu:** Cấu hình Media Queries chuẩn mực theo triết lý Mobile First, kiểm soát không để thanh cuộn ngang xuất hiện.
- **Thời gian thực hiện:** Tuần 4
- **Câu Prompt gửi AI:**
  > *"Hãy bổ sung các đoạn Media Queries vào file CSS theo triết lý Mobile-First: Mặc định trên màn hình điện thoại (< 768px): Menu điều hướng ẩn đi và thay bằng nút Hamburger, danh sách sản phẩm hiển thị thành 1 cột duy nhất. Trên màn hình Tablet từ 768px đến 1024px: Danh sách sản phẩm hiển thị 2 cột. Trên màn hình Desktop (> 1024px): Menu hiển thị đầy đủ, danh sách sản phẩm hiển thị 4 cột. Đảm bảo trang web không xuất hiện thanh cuộn ngang (horizontal scroll) ở bất kỳ kích thước màn hình nào."*
- **Kết quả AI sinh ra:**
  Cấu trúc các khối Media Query theo mốc `@media screen and (min-width: 768px)` và `@media screen and (min-width: 1024px)`.
- **Nhận xét & Tinh chỉnh của sinh viên:**
  - *Đánh giá:* Cách tiếp cận `min-width` đúng chuẩn Mobile First, giúp giảm thiểu độ phức tạp và ghi đè CSS không cần thiết.
  - *Tinh chỉnh thêm:* Thêm thuộc tính `overflow-x: hidden; width: 100%;` vào thẻ `body` để triệt tiêu hoàn toàn nguy cơ tràn khung trên các thiết bị màn hình nhỏ.

---

## 4. GIAI ĐOẠN 3: HIỆU ỨNG CHUYỂN ĐỘNG & HOÀN THIỆN (TUẦN 5 & TUẦN 6)

### Prompt 5: Tích hợp hiệu ứng Thư viện (AOS & Animate.css) và Micro-interactions
- **Mục tiêu:** Thêm các hiệu ứng chuyển động mượt mà, tối ưu hóa phần cứng đồ họa (GPU Acceleration).
- **Thời gian thực hiện:** Tuần 5
- **Câu Prompt gửi AI:**
  > *"Hãy hướng dẫn tôi tích hợp thư viện Animate.css và AOS (Animate On Scroll) thông qua CDN vào file index.html của trang bán hàng: Thêm hiệu ứng data-aos="fade-up" cho các tiêu đề section và thẻ card khi người dùng cuộn trang. Viết hiệu ứng :hover mượt mà cho các nút bấm (CTA buttons) và thẻ sản phẩm (Cards): khi rê chuột vào, nút CTA sẽ nhấc lên 3px (sử dụng transform: translateY(-3px) thay vì top/left để tối ưu GPU) kết hợp hiệu ứng đổ bóng box-shadow đậm hơn, thẻ sản phẩm phóng to nhẹ transform: scale(1.02). Thiết lập thời gian chuyển động sử dụng biến --transition-speed đã khai báo ở :root."*
- **Kết quả AI sinh ra:**
  ```css
  .btn-primary:hover {
    background-color: var(--primary-hover);
    transform: translateY(-3px);
    box-shadow: var(--shadow-hover);
  }
  .product-card:hover {
    transform: translateY(-4px) scale(1.02);
    box-shadow: var(--shadow-hover);
    border-color: var(--secondary-color);
  }
  ```
- **Nhận xét & Tinh chỉnh của sinh viên:**
  - *Đánh giá:* Việc sử dụng `transform` kết hợp `will-change: transform` giúp trình duyệt dựng khung bằng GPU, loại bỏ hiện tượng giật lag (jank) thường gặp khi dùng thuộc tính định vị `top`/`left`.
  - *Tinh chỉnh thêm:* Thêm hiệu ứng nhịp tim `animate__animated animate__pulse animate__infinite` cho tem nhãn Hero Badge để tạo điểm nhấn thị giác thu hút khách hàng ngay khi truy cập.

---

### Prompt 6: Tối ưu hóa mã nguồn (Refactoring) & Kiểm tra W3C
- **Mục tiêu:** Rà soát loại bỏ mã trùng lặp, gom nhóm logic, đảm bảo 100% mã màu dùng biến `var()`, tuân thủ chuẩn W3C Validation.
- **Thời gian thực hiện:** Tuần 6
- **Câu Prompt gửi AI:**
  > *"Hãy rà soát lại toàn bộ mã nguồn CSS của trang bán hàng 'EcoShop', giúp tôi gom nhóm các thuộc tính trùng lặp, loại bỏ mã thừa, sắp xếp thứ tự từ <header> xuống <footer> và đảm bảo 100% các mã màu đều gọi từ biến var(--...) thay vì viết mã màu cứng. Hãy kiểm tra xem code có tuân thủ quy chuẩn W3C Validation hay không."*
- **Kết quả AI sinh ra:**
  File `style.css` được phân chia thành 10 khối rõ ràng:
  1. Design System & CSS Variables (:root)
  2. Reset CSS & Global Styles
  3. Header & Navigation (Dùng chung cả 3 trang)
  4. Hero Section (Trang Chủ)
  5. Page Header Banner (Trang Sản Phẩm & Liên Hệ)
  6. Featured Products Grid (Grid auto-fit)
  7. Why Choose Us & Testimonials
  8. Contact Form & Showroom Layout
  9. Footer & Contacts (Dùng chung cả 3 trang)
  10. Mobile First Media Queries
- **Nhận xét & Tinh chỉnh của sinh viên:**
  - *Đánh giá:* Mã nguồn sau khi refactor cực kỳ gọn gàng, có tính module hóa cao, dùng chung cho cả 3 trang HTML mà không bị phân mảnh CSS.
  - *Kết quả W3C:* Cả 3 file `index.html`, `products.html`, `contact.html` và `style.css` đều đạt chuẩn W3C Validated, không có lỗi cấu trúc thẻ hay thuộc tính không hợp lệ.

---

## 5. CÁC PROMPT TINH CHỈNH NÂNG CAO THỰC TẾ

### 5.1. Pure HTML5/CSS3 Checkbox Hack (Không dùng JS)
Khi nhận được yêu cầu nghiêm ngặt **"không dùng js"**, sinh viên đã đưa ra câu Prompt kỹ thuật cao để giải quyết bài toán tương tác Mobile Menu mà không cần đến JavaScript:

- **Câu Prompt điều khiển AI:**
  > *"Trang web của tôi bắt buộc chạy 100% thuần HTML5 & CSS3, không được dùng bất kỳ dòng mã JavaScript nào. Hãy hướng dẫn tôi áp dụng kỹ thuật Pure CSS Checkbox Hack để khi người dùng nhấn vào nút Hamburger trên điện thoại, thanh menu trượt mở ra mượt mà và 3 gạch ngang biến đổi thành dấu X đóng lại."*
- **Giải pháp kỹ thuật đạt được:**
  - Trong HTML: Sử dụng `<input type="checkbox" id="menuToggle" class="menu-toggle-checkbox">` kết hợp với `<label for="menuToggle" class="hamburger-toggle">`.
  - Trong CSS: Dùng CSS General Sibling Selector (`~`):
    ```css
    .menu-toggle-checkbox:checked ~ .main-nav {
      transform: translateX(0);
    }
    .menu-toggle-checkbox:checked ~ .header-actions .hamburger-toggle .hamburger-line:nth-child(1) {
      transform: translateY(7px) rotate(45deg);
    }
    .menu-toggle-checkbox:checked ~ .header-actions .hamburger-toggle .hamburger-line:nth-child(2) {
      opacity: 0;
    }
    .menu-toggle-checkbox:checked ~ .header-actions .hamburger-toggle .hamburger-line:nth-child(3) {
      transform: translateY(-7px) rotate(-45deg);
    }
    ```

---

### 5.2. Tích hợp Hình ảnh thực tế Unsplash & Nội dung Tiếng Việt chuyên nghiệp
- **Mục tiêu:** Loại bỏ toàn bộ hình ảnh giữ chỗ (placeholders) và văn bản rác Lorem Ipsum; đưa vào ảnh Unsplash sắc nét và nội dung Tiếng Việt thực tế 100%.
- **Câu Prompt điều khiển AI:**
  > *"Trang web hiện tại vẫn còn thiếu hình ảnh và nội dung thực tế. Hãy cập nhật lại file index.html và style.css với các yêu cầu bổ sung sau: 1. Hình ảnh thực tế từ Unsplash API / CDN Link công khai cho Banner Hero, 8 sản phẩm riêng biệt và 3 ảnh đại diện khách hàng, đảm bảo thuộc tính alt chuẩn SEO; 2. Toàn bộ nội dung viết bằng Tiếng Việt phong phú, tự nhiên, chuyên nghiệp cho một thương hiệu thời trang xanh thực tế (tên sản phẩm chi tiết, mô tả, giá niêm yết, giá giảm, đánh giá sao, 4 ưu điểm thực tế, 3 nhận xét chân thực và thông tin showroom/hotline/giờ mở cửa thực tế); 3. Giữ nguyên toàn bộ tiêu chuẩn Semantic HTML5, CSS Variables, CSS Grid, Flexbox, Mobile-First và TUYỆT ĐỐI KHÔNG DÙNG JAVASCRIPT."*

---

### 5.3. Mở rộng Kiến trúc Website Đa Trang (Multi-Page Navigation Architecture)
- **Mục tiêu:** Xây dựng website bán hàng đa trang hoàn chỉnh gồm 3 trang HTML liên kết chặt chẽ qua thẻ `<nav>`, dùng chung `style.css` và **không dùng JS**.
- **Câu Prompt điều khiển AI:**
  > *"Hãy đóng vai trò là một Chuyên gia Front-end Developer. Hãy viết mã nguồn hoàn chỉnh cho một Website Bán hàng gồm 3 trang HTML liên kết với nhau, TUYỆT ĐỐI KHÔNG SỬ DỤNG JAVASCRIPT, chỉ dùng HTML5 Semantic và CSS3 chung một file style.css:
  > 1. style.css: File CSS chung sử dụng Design System, Reset CSS, Flexbox/Grid, Responsive Mobile-First, Animate.css + AOS.
  > 2. index.html (Trang Chủ): Header, Nav, Hero Section, sản phẩm tiêu biểu, ưu điểm, đánh giá, Footer.
  > 3. products.html (Trang Sản phẩm): Lưới sản phẩm chi tiết ít nhất 8 sản phẩm dùng Grid auto-fit, ảnh Unsplash thật, giá, nút mua hàng.
  > 4. contact.html (Trang Liên hệ / Form): Giao diện Form liên hệ chuẩn Semantic kiểm tra dữ liệu bằng HTML5 (required, email, tel, pattern), hộp thông tin showroom và bản đồ.
  > 5. Điều hướng Menu chuẩn xác: Thanh nav ở cả 3 trang có liên kết chuẩn, class active hiển thị đúng trang hiện tại, nút CTA trang chủ trỏ link sang products.html."*
- **Kết quả đạt được:**
  - Hoàn thiện trọn vẹn 3 trang HTML độc lập, chuyển trang mượt mà qua các liên kết `index.html`, `products.html`, `contact.html`.
  - Giữ vững 100% nguyên tắc Zero JavaScript, bảo đảm tốc độ tải trang nhanh và chuẩn W3C Validation.

---

## 6. BẢNG TỔNG HỢP ĐÁNH GIÁ HIỆU QUẢ PROMPTING

| Giai đoạn | Tuần | Nội dung Prompt | Độ chính xác AI | Đóng góp & Tinh chỉnh của Sinh viên | Đánh giá |
|:---:|:---:|:---|:---:|:---|:---:|
| **GĐ 1** | Tuần 1 | Khởi tạo Design System & :root | 95% | Thêm bảng biến phụ trợ, loại bỏ 100% hardcoded hex color. | Rất tốt |
| **GĐ 1** | Tuần 2 | Dựng khung Semantic HTML5 | 90% | Thay thẻ div bằng article, address, bổ sung ARIA Roles. | Xuất sắc |
| **GĐ 2** | Tuần 3 | Dàn trang CSS Grid & Flexbox | 95% | Cấu hình aspect-ratio chống CLS hình ảnh sản phẩm. | Xuất sắc |
| **GĐ 2** | Tuần 4 | Mobile-First Media Queries | 90% | Thêm overflow-x: hidden triệt tiêu lỗi cuộn ngang. | Rất tốt |
| **GĐ 3** | Tuần 5 | Hiệu ứng AOS & Micro-interactions | 95% | Chuyển sang transform translateY GPU, thêm pulse badge. | Xuất sắc |
| **GĐ 3** | Tuần 6 | Refactoring & Kiểm tra chuẩn W3C | 98% | Gom nhóm thuộc tính, sắp xếp logic theo thứ tự DOM. | Hoàn hảo |
| **Nâng cao 1** | Bổ sung | Pure CSS Checkbox Hack (No-JS) | 100% | Thay thế hoàn toàn JS cho Mobile Menu drawer. | Đột phá |
| **Nâng cao 2** | Bổ sung | Ảnh Unsplash & Nội dung Tiếng Việt | 100% | Thay thế triệt để placeholder và text Lorem Ipsum. | Hoàn hảo |
| **Nâng cao 3** | Bổ sung | Kiến trúc Đa trang (3 Trang HTML) | 100% | Thiết lập liên kết chéo giữa index, products, contact. | Toàn diện |

---

## 7. BÀI HỌC KINH NGHIỆM & TƯ DUY VIBE CODING

1. **Hiểu rõ bản chất trước khi ra lệnh:** Prompting hiệu quả không phải là hỏi chung chung "hãy tạo một website", mà phải chia nhỏ thành từng module cụ thể (Design System -> HTML Semantics -> Layout Grid/Flexbox -> Responsive -> Micro-interactions -> Multi-page Linking).
2. **Kỹ năng thẩm định và phản biện kết quả AI:** AI thường có xu hướng sử dụng văn bản giữ chỗ hoặc đề xuất JavaScript cho các tác vụ đơn giản. Người lập trình viên phải có tư duy kỹ thuật để yêu cầu AI chuyển đổi sang biến CSS `var()`, giải pháp Pure CSS Checkbox Hack và dữ liệu thực tế.
3. **Tối ưu hóa hiệu năng là cốt lõi:** Luôn ưu tiên các thuộc tính được tăng tốc phần cứng GPU như `transform` và `opacity` để đảm bảo chuyển động đạt chuẩn 60fps trên mọi thiết bị di động.
4. **Chuẩn W3C và SEO:** Việc sử dụng đúng các thẻ Semantic HTML5 cùng ảnh chất lượng cao và alt text mô tả chi tiết không chỉ giúp mã nguồn dễ đọc mà còn cải thiện vượt bậc điểm số SEO và khả năng tiếp cận (Accessibility).

---
*Báo cáo được hoàn thành và nghiệm thu bởi sinh viên Võ Minh Quang (MSSV: 125001101).*
