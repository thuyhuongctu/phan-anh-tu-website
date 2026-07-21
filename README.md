# Phan Anh Tu — Personal Academic Website

Website cá nhân của PGS. Phan Anh Tu — Phó Hiệu trưởng Trường Kinh tế, Đại học Cần Thơ.

Đây là một website tĩnh (static website) gồm một file `index.html` duy nhất, chứa toàn bộ các trang: Home, Research, Teaching, CV, Events, Me Blog, Photos, Aphorisms, 3L Learning, và Contact. Việc chuyển trang được xử lý bằng JavaScript (điều hướng theo hash `#research`, `#cv`, …), có hỗ trợ chế độ sáng/tối (dark mode) và giao diện responsive cho điện thoại.

## Cách chạy website

### 1. Chạy thử trên máy tính (local)

Chỉ cần mở file `index.html` bằng trình duyệt (nhấp đúp vào file), hoặc chạy một web server đơn giản:

```bash
# Nếu có Python:
python3 -m http.server 8000
# Sau đó mở trình duyệt tại: http://localhost:8000
```

### 2. Đưa website lên mạng bằng GitHub Pages (miễn phí)

Repository này đã có sẵn workflow tự động triển khai (`.github/workflows/deploy.yml`). Chỉ cần làm các bước sau **một lần duy nhất**:

1. Vào repository trên GitHub → **Settings** → **Pages**.
2. Ở mục **Build and deployment** → **Source**, chọn **GitHub Actions**.
3. Merge pull request vào nhánh `main` (hoặc push code lên nhánh `main`).
4. Đợi khoảng 1–2 phút, website sẽ chạy tại địa chỉ:
   `https://<tên-tài-khoản>.github.io/phan-anh-tu-website/`

Sau đó, mỗi lần cập nhật nội dung và push lên nhánh `main`, website sẽ tự động được cập nhật.

### 3. Gắn tên miền riêng (tùy chọn)

Nếu muốn dùng tên miền riêng (ví dụ `phananhtu.com`):

1. Vào **Settings** → **Pages** → **Custom domain**, nhập tên miền.
2. Trỏ DNS của tên miền về GitHub Pages theo hướng dẫn của GitHub.

## Những việc cần làm trước khi công bố chính thức

- [ ] **Ảnh chân dung**: thay ảnh placeholder (chữ "PAT") trong `index.html` bằng ảnh chân dung thật (khung vuông).
- [ ] **Logo trường**: thay logo placeholder "CTU" bằng logo chính thức của Đại học Cần Thơ.
- [ ] **File CV**: đặt file PDF vào thư mục `assets/` với tên `Phan_Anh_Tu_CV_May2026.pdf` (nút "Download CV" đang trỏ tới đường dẫn này).
- [ ] **Form liên hệ**: hiện tại form sẽ mở trình email của người dùng (mailto). Có thể kết nối dịch vụ như Formspree hoặc Basin nếu muốn nhận tin nhắn trực tiếp.

## Cấu trúc thư mục

```
├── index.html              # Toàn bộ website (HTML + CSS + JavaScript)
├── assets/                 # Chứa file CV PDF, hình ảnh, …
└── .github/workflows/
    └── deploy.yml          # Tự động triển khai lên GitHub Pages
```
