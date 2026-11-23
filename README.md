# Aptis Speaking Studio

Ứng dụng luyện thi **Aptis Speaking General**, không liên kết chính thức với British Council.

## Mở ứng dụng
Nếu đã bật GitHub Pages (Settings → Pages → Deploy from branch → main / root):
https://longduydinh1809-png.github.io/aptis-speaking-studio/

## Nội dung
- 11 thẻ từ [Google Docs nguồn](https://docs.google.com/document/d/18B36GRG5vX45-CnnmzCz7mj5pYDmGdkiytGZxpcgX5c/edit), 33 ảnh, bài mẫu B2 Thẻ 1–10
- Thi thử 4 phần với đồng hồ, tự chuyển câu, ghi âm trực tiếp trên trình duyệt và tải file sau khi thi.
- Chế độ thi: Part 1 3×30s, Part 2 3×45s, Part 3 3×45s, Part 4 chuẩn bị 60s rồi nói 120s liên tục.
- Chế độ luyện cá nhân: Part 4 tách câu 60s/20s/40s.
- Mẫu B2 và keywords hiện sau bài thi, không tự chấm điểm.
- Không tải ghi âm lên máy chủ.

## Tệp mã nguồn
Để giảm số lần tải qua kết nối GitHub, bản snapshot gồm website + ảnh hiện được lưu trong thư mục `bundle/` thành các phần nhị phân. `index.html` giải nén và khởi chạy website tại trình duyệt. Mã nguồn đọc được nằm trong [bộ zip đầy đủ ở Google Drive](https://drive.google.com/file/d/1w4UA3u15UHemx5mCJKNJfjvmE0RkBO_b/view). Hãy tải ZIP để sửa app.js, app.css, build_data.py hay Apps Script.

## Đồng bộ Google Docs — cần thiết lập một lần
1. Tải bộ ZIP đầy đủ, mở `google-apps-script/Code.gs`.
2. Trong [Google Apps Script](https://script.google.com/home/projects/create), tạo project và dán Code.gs. Tài khoản triển khai phải có quyền đọc Google Docs.
3. Deploy → New deployment → Web app → Execute as Me, Who has access Anyone. Sao chép URL /exec.
4. Trong bộ ZIP sửa `config.js` thành `window.APTIS_SYNC_URL = 'URL /exec';`, đóng gói lại và cập nhật website.
5. Website kiểm tra thay đổi 60 giây một lần khi đang mở, không cập nhật giữa lượt thi.

**Chưa kích hoạt đồng bộ**: cấu hình hiện đang để trống; website sử dụng snapshot tại 23/11/2026. Không có quyền truy cập Apps Script trên tài khoản người dùng để tự tạo deployment.

**Lưu ý:** Deploy Apps Script công khai sẽ làm nội dung đề có thể được đọc bởi bất cứ ai biết URL endpoint. Đừng dùng cách này với tài liệu bí mật.

## Xuất bản qua GitHub Pages
Repository → Settings → Pages → Build and deployment → Deploy from a branch → Branch main, Folder /(root) → Save.
