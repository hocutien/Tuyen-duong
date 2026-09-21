# Công cụ lập tuyến phát quà

Trang web một file, chạy thẳng trong trình duyệt. Không có máy chủ, không gửi dữ liệu đi đâu —
toàn bộ danh sách khách nằm trong bộ nhớ trình duyệt trên máy của người dùng.

## Dùng thế nào

1. Mở trang (địa chỉ GitHub Pages của repo này)
2. **📗 Nạp Excel** — chọn file danh sách khách, chọn sheet
3. **📇 Cập nhật danh bạ** — nạp file `.csv` hoặc `.vcf` xuất từ Google Danh bạ để lấy toạ độ
4. **🏭 Kho** — đặt điểm xuất phát của xe tải
5. **🚚 Sắp tuyến xe tải** — máy tính thứ tự giao tối ưu
6. **💾 Lưu tiến độ** — xuất file `.json` để sao lưu hoặc mang sang máy khác

## Vì sao nên chạy trên địa chỉ https thay vì mở file từ bộ nhớ máy

Mở file trực tiếp trên Android (đường dẫn `content://`) thì Chrome chặn:

- gọi máy chủ dẫn đường → không có cự ly đường bộ thật, phải đo đường chim bay
- lấy GPS → không lấy được vị trí hiện tại
- tải file → không xuất được CSV/KML

Chạy qua `https://` thì cả ba đều hoạt động.

## ⚠ KHÔNG ĐƯỢC đưa dữ liệu khách lên đây

Repo này là **công khai**. Chỉ để mã nguồn, tuyệt đối không commit:

- file Excel danh sách khách
- file `.json` lưu tiến độ
- file `.csv` danh bạ hoặc file xuất ra từ công cụ

Các file đó chứa họ tên, số điện thoại, địa chỉ và **số dư tiền gửi** của khách hàng.
File `.gitignore` đã chặn sẵn, nhưng vẫn phải tự kiểm trước khi commit.
