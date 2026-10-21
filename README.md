# ECOSHOP - CỬA HÀNG THỜI TRANG XANH & SMART SHOPPING
> **BÀI THI GIỮA KỲ: THIẾT KẾ WEB & LẬP TRÌNH FRONT-END**  
> **Sinh viên:** Võ Minh Quang | **MSSV:** 125001101 | **Lớp:** 25CT112  
> **Kho lưu trữ:** `vominhquang25ct112/Quang_VoMinh_125001101`  

---

## 🌿 GIỚI THIỆU DỰ ÁN
**EcoShop** là website thương mại điện tử đa trang (Multi-Page Website) chuyên về thời trang sinh thái bền vững, được phát triển theo triết lý **Vibe Coding** với các tiêu chuẩn kỹ thuật Front-end hiện đại nhất:
- **100% Thuần HTML5 & CSS3** — Tuyệt đối không phụ thuộc vào JavaScript.
- **Kiến trúc Website 3 trang liên kết chặt chẽ:**
  1. `index.html`: Trang Chủ giới thiệu thương hiệu, banner Hero lớn, sản phẩm tiêu biểu, cam kết sinh thái và đánh giá khách hàng.
  2. `products.html`: Trang Danh sách sản phẩm chi tiết với 8 sản phẩm thời trang cao cấp (ảnh Unsplash thật, mô tả, giá, đánh giá sao, nút mua hàng).
  3. `contact.html`: Trang Liên hệ chuẩn Semantic với Form xác thực dữ liệu bằng HTML5 Native, danh sách showroom, hotline và khung bản đồ vị trí.
- **Pure CSS Checkbox Hack** cho thanh điều hướng trên thiết bị di động (Mobile Menu).
- **Hệ thống Design System & Biến CSS (:root)** chuẩn chỉnh, 100% màu sắc sử dụng biến `var()`.
- **Bố cục CSS Grid & Flexbox:** Lưới sản phẩm co giãn tự động `repeat(auto-fit, minmax(260px, 1fr))` chống tràn khung.
- **Responsive Mobile First:** Tối ưu mượt mà từ màn hình điện thoại (320px) đến máy tính bảng và màn hình máy tính lớn (>1024px).
- **Tối ưu hóa GPU 60fps:** Mọi hiệu ứng hover nút bấm và thẻ sản phẩm dùng `transform` và `opacity`.

---

## 📁 CẤU TRÚC THƯ MỤC NỘP BÀI
```text
Quang_VoMinh_125001101/
│
├── index.html          # Trang Chủ (Home Page)
├── products.html       # Trang Danh sách Sản phẩm (Catalog Page)
├── contact.html        # Trang Liên hệ & Form Hỗ trợ (Contact Page)
├── style.css           # File CSS dùng chung cho cả 3 trang HTML
├── prompt_log.md       # Nhật ký Prompt Engineering (Quy định đề thi)
└── README.md           # Giới thiệu dự án & Hướng dẫn sử dụng
```

---

## 🚀 HƯỚNG DẪN TRẢI NGHIỆM TRANG WEB
1. Clone kho lưu trữ về máy tính:
   ```bash
   git clone https://github.com/vominhquang25ct112/Quang_VoMinh_125001101.git
   ```
2. Mở trực tiếp file `index.html` bằng bất kỳ trình duyệt web hiện đại nào (Google Chrome, Microsoft Edge, Mozilla Firefox, Safari).
3. Sử dụng thanh Menu điều hướng ở đầu trang hoặc các nút CTA để di chuyển qua lại giữa **Trang chủ**, **Sản phẩm** và **Liên hệ** mượt mà.

---

## 📋 HỒ SƠ PROMPT ENGINEERING
Chi tiết toàn bộ các câu lệnh Prompt qua 3 giai đoạn (6 tuần) và các phần nhận xét, tinh chỉnh kỹ thuật của sinh viên được trình bày đầy đủ tại file [prompt_log.md](prompt_log.md).
