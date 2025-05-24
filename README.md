1. Quá trình Ký số (Máy khách):

Tạo hash SHA-256 từ file.

Mã hóa hash bằng private key RSA-2048 với padding PSS → thành chữ ký số.

Gửi file + chữ ký đến máy chủ.

2. Quá trình Xác minh (Máy chủ):

Tính lại hash SHA-256 của file nhận.

Dùng public key để giải mã chữ ký lấy hash gốc.

So sánh hai hash:

Trùng → file nguyên vẹn, nguồn tin cậy.

Khác → báo lỗi tính toàn vẹn hoặc giả mạo.

3. Bảo mật chính:

RSA 2048-bit + PSS padding

SHA-256

Giao diện đồ họa trực quan cho phép ký & xác minh dễ dàng.