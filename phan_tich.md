Nguyên nhân gây lỗi 403 Forbidden
Thứ tự đúng phải là:
1. Lấy JWT
2. Trích xuất username
3. Load UserDetails
4. validateToken(jwt, userDetails)
5. Tạo Authentication
6. Đưa vào SecurityContextHolder
Nhưng mã hiện tại lại làm:
1. Lấy JWT
2. validateToken(jwt, null)
3. (thất bại)
4. Không load UserDetails
5. Không tạo Authentication