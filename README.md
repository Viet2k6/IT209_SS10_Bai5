\# Session 10 - Bài 5: Docker Compose và File .env



\## 1. Mục tiêu



Sử dụng Docker Compose v2 để quản lý dịch vụ PostgreSQL và giao diện web quản trị database. Các thông tin cấu hình được lưu trong file `.env`.



\## 2. Các file nộp bài



\- `docker-compose.yml`: khai báo hai service, network và volume.

\- `.env.example`: cung cấp mẫu biến môi trường.

\- `.gitignore`: loại file `.env` khỏi Git.

\- `README.md`: hướng dẫn chạy và kiểm tra bài.



\## 3. Khởi chạy dịch vụ



```bash

docker compose up -d

```



\## 4. Kiểm tra trạng thái



```bash

docker compose ps

```



Kết quả: hai service `backend` và `database` ở trạng thái đang chạy.



\## 5. Truy cập giao diện web



Mở trình duyệt tại `http://localhost:8083`.



Thông tin kết nối PostgreSQL:

\- Server: `database`

\- Database: `appdb`

\- Username: `appuser`



Mật khẩu được khai báo trong file `.env`.



\## 6. Xem log dịch vụ



```bash

docker compose logs -f

```



Nhấn `Ctrl + C` để dừng theo dõi log.



\## 7. Dừng dịch vụ



```bash

docker compose down

```



Lệnh này dừng và xóa các container cùng network do Compose tạo; named volume vẫn được giữ lại.



\## 8. Kết luận



Đã kiểm tra thành công việc khởi chạy các dịch vụ bằng Docker Compose, truy cập giao diện web và kết nối tới PostgreSQL qua network nội bộ.



