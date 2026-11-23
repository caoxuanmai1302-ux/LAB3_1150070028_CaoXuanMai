# LAB 3 – MÃ HÓA KHÓA CÔNG KHAI

## 1. Thông tin sinh viên

- **Họ và tên:** Cao Xuân Mai
- **MSSV:** 1150070028
- **Lớp:** 11_TTMT
- **Môn học:** An toàn và Bảo mật Thông tin

## 2. Giới thiệu

LAB 3 xây dựng ứng dụng mã hóa và giải mã sử dụng các thuật toán mật mã khóa công khai, bao gồm RSA, ECC và mã hóa lai RSA kết hợp AES.

Ứng dụng được xây dựng bằng Java với giao diện đồ họa Swing trên NetBeans IDE, hỗ trợ quản lý khóa, mã hóa, giải mã và lưu lịch sử thao tác vào SQL Server.

## 3. Mục tiêu

- Tìm hiểu nguyên lý hoạt động của mã hóa khóa công khai.
- Thực hành thuật toán RSA và ECC.
- Tìm hiểu mô hình mã hóa lai RSA kết hợp AES.
- Thực hiện tạo, lưu và nạp cặp khóa.
- Tích hợp ứng dụng Java với cơ sở dữ liệu SQL Server.
- Kiểm tra kết quả mã hóa, giải mã và xử lý lỗi.

## 4. Công nghệ sử dụng

| Công nghệ    | Mô tả                       |
| ------------ | --------------------------- |
| Java         | Ngôn ngữ lập trình          |
| Java Swing   | Xây dựng giao diện đồ họa   |
| NetBeans IDE | Môi trường phát triển       |
| RSA          | Mã hóa khóa công khai       |
| AES-GCM      | Mã hóa dữ liệu              |
| ECC          | Mật mã đường cong elliptic  |
| SQL Server   | Lưu trữ lịch sử thao tác    |
| JDBC         | Kết nối Java với SQL Server |

## 5. Các chức năng

- Tạo cặp khóa công khai và khóa riêng.
- Hiển thị khóa dưới dạng Base64.
- Lưu khóa vào tệp và nạp khóa từ tệp.
- Mã hóa và giải mã dữ liệu bằng RSA.
- Mã hóa và giải mã bằng ECC.
- Mã hóa lai RSA kết hợp AES.
- Lưu lịch sử thao tác mã hóa và giải mã vào SQL Server.
- Hiển thị trạng thái xử lý và thông báo lỗi.
- Kiểm tra trường hợp dữ liệu không hợp lệ hoặc sai khóa.

## 6. Cấu hình cơ sở dữ liệu SQL Server

### 6.1. Chuẩn bị

Cài đặt và khởi động:

- Microsoft SQL Server.
- SQL Server Management Studio (SSMS).

### 6.2. Tạo cơ sở dữ liệu

1. Mở SQL Server Management Studio.
2. Kết nối đến SQL Server.
3. Mở file SQL đi kèm project.
4. Thực thi script để tạo database và các bảng cần thiết.
5. Kiểm tra database đã được tạo thành công.

### 6.3. Cấu hình kết nối

Kiểm tra cấu hình kết nối SQL Server trong source code và cập nhật theo máy đang sử dụng:

- **Server Name:** Tên máy chủ SQL Server.
- **Database:** Tên database của LAB 3.
- **Authentication:** Phương thức xác thực.
- **Username/Password:** Thông tin đăng nhập nếu sử dụng SQL Server Authentication.

Đảm bảo SQL Server đang hoạt động và cho phép kết nối trước khi chạy chương trình.

### 6.4. Kiểm tra

Sau khi kết nối, thực hiện các thao tác mã hóa và giải mã trên giao diện. Kiểm tra dữ liệu lịch sử thao tác được ghi vào SQL Server.

## 7. Hướng dẫn chạy chương trình

### Bước 1: Tải project

Clone repository hoặc tải source code về máy và giải nén.

### Bước 2: Mở project

1. Mở NetBeans IDE.
2. Chọn **File → Open Project**.
3. Chọn thư mục project LAB 3.

### Bước 3: Cấu hình SQL Server

Thực hiện các bước cấu hình cơ sở dữ liệu được trình bày tại mục 6.

### Bước 4: Chạy chương trình

Mở project trong NetBeans và nhấn **Run Project (F6)** hoặc chạy class giao diện chính của chương trình.

### Bước 5: Thực hiện chức năng

1. Chọn chức năng mã hóa tương ứng.
2. Nhấn Generate Keys để tạo cặp khóa hoặc Load Keys để nạp khóa.
3. Nhập dữ liệu cần xử lý vào ô Plaintext.
4. Nhấn Encrypt để mã hóa.
5. Kiểm tra dữ liệu Ciphertext.
6. Nhấn Decrypt để giải mã và đối chiếu kết quả.
7. Kiểm tra thông báo trạng thái và lịch sử thao tác.

## 8. Kiểm thử

Các chức năng được kiểm tra thông qua việc tạo khóa, lưu/nạp khóa, mã hóa, giải mã và kiểm tra dữ liệu đầu ra.

| STT | Nội dung kiểm thử               | Kết quả |
| --- | ------------------------------- | ------- |
| 1   | Tạo cặp khóa                    | PASS    |
| 2   | Lưu và nạp khóa                 | PASS    |
| 3   | Mã hóa dữ liệu                  | PASS    |
| 4   | Giải mã dữ liệu                 | PASS    |
| 5   | Kiểm tra dữ liệu sau giải mã    | PASS    |
| 6   | Kiểm tra nhập dữ liệu rỗng      | PASS    |
| 7   | Ghi lịch sử thao tác SQL Server | PASS    |

## 9. Kết luận

Thông qua LAB 3, chương trình đã thực hiện các chức năng mật mã khóa công khai RSA, ECC và mã hóa lai RSA kết hợp AES. Bài thực hành giúp củng cố kiến thức về quản lý khóa, mã hóa dữ liệu, giải mã và tích hợp cơ sở dữ liệu trong ứng dụng Java.

