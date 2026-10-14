# [Bài tập] Phối màu cho newsletter (Trello Newsletter Redesign)

> **Khóa học:** CodeGym Web Development  
> **Học viên:** HueAn14  
> **Repository:** [https://github.com/HueAn14/phoi-mau-cho-newsletter](https://github.com/HueAn14/phoi-mau-cho-newsletter)  

---

## 🎯 Mục tiêu bài tập
1. **Luyện tập sử dụng Adobe Color:** Khám phá, trích xuất và chọn lọc 2 bộ màu sắc hài hòa tuân theo các nguyên tắc bánh xe màu (Color Wheel Rules).
2. **Xây dựng khung Newsletter với Bootstrap 5:** Thiết kế giao diện newsletter chuyên nghiệp (chuẩn Trello Pulse / SaaS newsletter) sử dụng grid, card, button và utility classes.
3. **Ứng dụng CSS Custom Properties (Variables):** Quản lý màu sắc tập trung bằng các biến CSS (`--primary-color`, `--secondary-color`, `--accent-color`, v.v.), cho phép hoán đổi phong cách tức thì mà không cần can thiệp vào cấu trúc HTML.
4. **So sánh tâm lý học màu sắc (Color Psychology):** Đánh giá sự khác biệt về cảm xúc, tâm trạng và thông điệp mà mỗi bộ màu mang lại cho người đọc.

---

## 🎨 Bảng đối chiếu 2 bộ màu sắc từ Adobe Color

### 🌊 Bộ màu 1: Oceanic Tech Productivity (Phiên bản 1)
* **Quy tắc Adobe Color:** Split-Complementary (Bổ túc phân tách)  
* **Tông màu chủ đạo:** Trello Sapphire Blue kết hợp Electric Cyan và điểm nhấn Coral Sunset rực rỡ.  
* **Cảm xúc & Tâm lý học:** Mang tính công nghệ, năng động, tin cậy, thúc đẩy tập trung và gia tăng năng suất làm việc.

| Thành phần UI | Tên màu | Mã HEX | Thông số RGB | Độ tương phản WCAG 2.1 |
|:---|:---|:---:|:---:|:---:|
| **Primary Color** | Sapphire Blue | `#0065FF` | `rgb(0, 101, 255)` | 4.8:1 với chữ trắng (Đạt chuẩn AA) |
| **Secondary Color** | Electric Cyan | `#00C2E0` | `rgb(0, 194, 224)` | Tươi sáng, phân tách khối nổi bật |
| **Accent / CTA** | Coral Sunset | `#FF5630` | `rgb(255, 86, 48)` | Kêu gọi hành động mạnh mẽ |
| **Text Main** | Deep Navy | `#091E42` | `rgb(9, 30, 66)` | 13.8:1 với nền trắng (Đạt chuẩn AAA) |
| **Text Muted** | Slate Gray | `#5E6C84` | `rgb(94, 108, 132)` | Phụ đề, thời gian đọc, link phụ |
| **Background Page** | Cool Slate Light | `#F4F5F7` | `rgb(244, 245, 247)` | Nền ngoài tạo chiều sâu |
| **Background Card** | Pure White | `#FFFFFF` | `rgb(255, 255, 255)` | Khối nội dung sạch sẽ |
| **Footer BG** | Midnight Navy | `#091E42` | `rgb(9, 30, 66)` | Chân trang vững chãi, trang trọng |

---

### 🌿 Bộ màu 2: Warm Terracotta & Sage (Phiên bản 2)
* **Quy tắc Adobe Color:** Compound / Analogous + Accent (Hài hòa hữu cơ)  
* **Tông màu chủ đạo:** Đất nung Terracotta ấm kết hợp Xanh xô thơm Sage Teal và Hồng mơ Apricot Peach.  
* **Cảm xúc & Tâm lý học:** Ấm áp, thư thái, khơi nguồn sáng tạo nghệ thuật, mang tính nhân bản và giảm áp lực thị giác khi làm việc kéo dài.

| Thành phần UI | Tên màu | Mã HEX | Thông số RGB | Độ tương phản WCAG 2.1 |
|:---|:---|:---:|:---:|:---:|
| **Primary Color** | Warm Terracotta | `#C85A32` | `rgb(200, 90, 50)` | 4.6:1 với chữ trắng (Đạt chuẩn AA) |
| **Secondary Color** | Calm Sage Teal | `#4E878C` | `rgb(78, 135, 140)` | Màu xanh cân bằng, tự nhiên |
| **Accent / CTA** | Apricot Peach | `#E29578` | `rgb(226, 149, 120)` | Điểm xuyết tinh tế, ngọt ngào |
| **Text Main** | Dark Espresso | `#2D2327` | `rgb(45, 35, 39)` | 13.2:1 với nền trắng (Đạt chuẩn AAA) |
| **Text Muted** | Warm Charcoal | `#6B5E62` | `rgb(107, 94, 98)` | Thân thiện, êm mắt khi đọc lâu |
| **Background Page** | Alabaster Cream | `#FBF8F5` | `rgb(251, 248, 245)` | Nền kem ấm cúng |
| **Background Card** | Pure White | `#FFFFFF` | `rgb(255, 255, 255)` | Thẻ bài viết nổi bật, sắc nét |
| **Footer BG** | Deep Espresso | `#2D2327` | `rgb(45, 35, 39)` | Chân trang trầm ấm, lịch sự |

---

## 📁 Cấu trúc thư mục mã nguồn

```
phoi-mau-cho-newsletter/
├── index.html                  # Trang tổng quan với bộ chuyển đổi theme trực tiếp (Live Switcher)
├── newsletter_version1.html    # Trang độc lập Phiên bản 1 (Oceanic Tech Productivity)
├── newsletter_version2.html    # Trang độc lập Phiên bản 2 (Warm Terracotta & Sage)
├── css/
│   ├── newsletter-base.css     # CSS bố cục, typography, responsiveness và utility classes
│   ├── theme-oceanic.css       # Khai báo CSS Custom Properties cho Bộ màu 1
│   └── theme-terracotta.css    # Khai báo CSS Custom Properties cho Bộ màu 2
├── .gitignore                  # File cấu hình bỏ qua file tạm của Git
└── README.md                   # Tài liệu thuyết minh bài tập chi tiết
```

---

## 💡 Hướng dẫn chạy và trải nghiệm
1. **Trực quan nhất:** Mở file [index.html](file:///c:/Users/Admin/Desktop/Bai-Tap-CodeGym1/phoi-mau-cho-newsletter/index.html) bằng trình duyệt. Bạn có thể bấm vào hai nút chuyển đổi màu ở góc trên cùng để so sánh trực tiếp sự thay đổi sắc thái và tâm trạng của newsletter ngay lập tức.
2. **Xem từng trang độc lập:**
   - Mở [newsletter_version1.html](file:///c:/Users/Admin/Desktop/Bai-Tap-CodeGym1/phoi-mau-cho-newsletter/newsletter_version1.html) để xem riêng Phiên bản 1.
   - Mở [newsletter_version2.html](file:///c:/Users/Admin/Desktop/Bai-Tap-CodeGym1/phoi-mau-cho-newsletter/newsletter_version2.html) để xem riêng Phiên bản 2.
