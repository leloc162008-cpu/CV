# Portfolio CV - Nguyễn Văn An

Trang portfolio cá nhân dạng tĩnh, giới thiệu Nguyễn Văn An với vai trò Frontend Developer. Dự án trình bày thông tin cá nhân, kỹ năng, các dự án tiêu biểu và kênh liên hệ trong một trang web responsive.

## Chức năng

- Điều hướng đến các mục Giới thiệu, Kỹ năng, Dự án và Liên hệ.
- Hiển thị phần giới thiệu, ảnh đại diện, kỹ năng và danh sách dự án mẫu.
- Bố cục responsive cho màn hình điện thoại, máy tính bảng và máy tính.
- Cuộn mượt khi đi đến các mục trong trang.
- Không cần backend, cơ sở dữ liệu hoặc bước biên dịch.

> Các dự án trong trang hiện là nội dung minh họa; liên kết "Xem chi tiết" chưa được cấu hình. Phần thời tiết cũng chỉ là nội dung mô tả mẫu, chưa tích hợp API.

## Công nghệ

- HTML5: cấu trúc và nội dung trang.
- CSS3: giao diện, Flexbox, CSS Grid và responsive design.
- Nginx (tùy chọn): phục vụ trang tĩnh khi chạy bằng Docker.

Dự án không sử dụng JavaScript, framework frontend hay thư viện bên ngoài.

## Yêu cầu môi trường

Để xem trang trực tiếp:

- Trình duyệt hiện đại như Chrome, Firefox, Edge hoặc Safari.
- Không cần cài runtime hay package manager.

Để chạy bằng máy chủ cục bộ:

- Python 3 (dùng lệnh `python`, `python3` hoặc `py` tùy hệ điều hành), hoặc một máy chủ web tĩnh khác.

Để chạy bằng Docker:

- Docker Engine trên Linux, hoặc Docker Desktop trên Windows/macOS.
- Kết nối Internet lần đầu để tải image `nginx:alpine`.

## Cấu trúc thư mục

```text
CV-main/
├── index.html
├── README.md
└── assets/
	├── css/
	│   └── styles.css
	└── img/
		└── avatar.jpg
```

## Cài đặt

Tải hoặc clone mã nguồn về máy, sau đó mở terminal tại thư mục dự án (thư mục chứa `index.html`). Nếu clone từ Git, thay `<URL_REPOSITORY>` bằng địa chỉ repository thực tế:

```bash
git clone <URL_REPOSITORY>
cd CV-main
```

Nếu tải file ZIP, giải nén rồi mở terminal tại thư mục `CV-main`.

## Cấu hình

Dự án không có file cấu hình môi trường, biến môi trường hoặc khóa API.

Để cá nhân hóa nội dung, sửa trực tiếp `index.html`, bao gồm tên, phần giới thiệu, kỹ năng, dự án và thông tin liên hệ. Email hiện tại (`an.nguyen@example.com`) và các liên kết GitHub/LinkedIn là dữ liệu mẫu; hãy thay bằng thông tin thật trước khi triển khai. Thay ảnh `assets/img/avatar.jpg` nếu cần, đồng thời giữ nguyên tên file hoặc cập nhật đường dẫn ảnh trong HTML.

Để đổi giao diện, chỉnh các biến màu và quy tắc trong `assets/css/styles.css`.

## Chạy thử

### Windows

Mở PowerShell tại thư mục dự án và chạy:

```powershell
py -m http.server 8000
```

Nếu lệnh `py` không có, thử:

```powershell
python -m http.server 8000
```

### macOS

Mở Terminal tại thư mục dự án và chạy:

```bash
python3 -m http.server 8000
```

### Linux

Mở terminal tại thư mục dự án và chạy:

```bash
python3 -m http.server 8000
```

### Mở trang

Sau khi máy chủ khởi động, truy cập <http://localhost:8000> bằng trình duyệt. Dừng máy chủ bằng `Ctrl+C` trong terminal.

Có thể mở trực tiếp `index.html` trong trình duyệt để xem nhanh. Dùng máy chủ cục bộ sẽ mô phỏng cách trang tĩnh được phục vụ trên web tốt hơn.

## Chạy bằng Docker

Không cần tạo Dockerfile. Chạy container Nginx và gắn thư mục dự án vào thư mục phục vụ web.

### Windows PowerShell

Tại thư mục dự án, chạy:

```powershell
docker run --rm -p 8080:80 -v "${PWD}:/usr/share/nginx/html:ro" nginx:alpine
```

### macOS / Linux

Tại thư mục dự án, chạy:

```bash
docker run --rm -p 8080:80 -v "$(pwd):/usr/share/nginx/html:ro" nginx:alpine
```

Mở <http://localhost:8080> để xem trang. Dừng container bằng `Ctrl+C`. Nếu cổng `8080` đã được sử dụng, đổi phần `8080:80` thành một cổng trống khác, ví dụ `8081:80`, rồi truy cập cổng tương ứng.

## Thông tin liên hệ

- Tác giả hiển thị trên trang: Nguyễn Văn An
- Email mẫu: `an.nguyen@example.com`
- GitHub mẫu: `github.com/nguyenvanan`
- LinkedIn mẫu: `linkedin.com/in/nguyenvanan`

Vui lòng cập nhật các thông tin mẫu trong `index.html` trước khi sử dụng hoặc công khai dự án.
