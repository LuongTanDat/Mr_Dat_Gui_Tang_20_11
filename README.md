# Sự thức giấc của Dany — mã nguồn tách file

Đây là bản tách từ **file HTML được lưu bằng trình duyệt** do người dùng cung cấp, không phải kho mã nguồn nguyên gốc phía máy chủ.

## Cấu trúc

- `index.html`: Cấu trúc trang và thứ tự tải CSS/JavaScript, được giữ nguyên như bản HTML đã lưu.
- `styles/`: Các khối CSS nội tuyến được tách thành từng file (đánh số để giữ nguyên thứ tự).
- `scripts/`: Các khối JavaScript nội tuyến được tách thành từng file (đánh số để giữ nguyên thứ tự thực thi).
- `assets/`: Những file hình ảnh, âm thanh và video từng nhúng dạng base64 đã được giải mã ra tệp thông thường.
- `asset_manifest.json`: Danh sách tài nguyên đã được trích xuất.

## Chạy thử

1. Giải nén toàn bộ ZIP.
2. Mở thư mục này trong VS Code.
3. Dùng tiện ích Live Server hoặc chạy `python -m http.server 8000` trong thư mục.
4. Truy cập `http://localhost:8000/index.html`.

## Giới hạn và lưu ý

- Bản lưu **không kèm** hai tài nguyên được dẫn theo đường dẫn địa phương của Chrome:
  - `./Sự thức giấc của Dany - Ngày 20_10_files/css2` (stylesheet phông chữ).
  - `./Sự thức giấc của Dany - Ngày 20_10_files/saved_resource.html` (HTML dự phòng của iframe hoa; JavaScript gốc có tạo `srcdoc` để thay thế khi kích hoạt cảnh hoa trên máy tính).
  Nếu muốn khôi phục toàn bộ tài nguyên như lúc tải trực tuyến, cần bổ sung các file gốc; riêng phần cảnh hoa có mã HTML/CSS được JavaScript nhúng sẵn nên có thể hoạt động mà không cần file iframe phụ.
- Chỉ khôi phục được frontend và tài nguyên gửi xuống trình duyệt; không bao gồm backend/database nếu có.
- Mã JavaScript, thuộc tính `src`, cấu trúc DOM và CSS được giữ ở thứ tự gốc, nhưng đây là bản chuyển đổi tự động; **chưa xác minh toàn bộ hoạt cảnh bằng kiểm thử trình duyệt**.
- Cảnh "Liệu cậu có thể..." được chuyển thành lời hỏi dành cho người thương.
- Nút "Nhận nhé" chỉ kích hoạt hoạt cảnh máy bay và lời nhắn cuối; **không sao chép liên kết, không mở trang khác và không chia sẻ gì**.
- Lời kết: "cậu biết không... cậu là một điều rất đặc biệt trong lòng tớ. ♡".
- Nếu nhúng nhạc/hình/video có bản quyền, hãy xác minh quyền sử dụng trước khi tái xuất bản.

## Đưa lên GitHub Pages

Upload **nội dung trong thư mục này** (index.html, styles/, scripts/, assets/, ...), không upload file ZIP làm trang web. Trong Settings → Pages chọn nhánh main, /(root).
