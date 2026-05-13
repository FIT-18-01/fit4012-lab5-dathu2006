# Logs / Minh chứng

Thư mục này dùng để lưu các minh chứng chạy bài lab (build, chạy mẫu, kết quả test).

Ví dụ file minh chứng mong đợi:

- `sample-run.log` — output khi chạy ví dụ (stdout/stderr)
- `test-output.log` — output khi chạy test (ví dụ `make test`)
- ảnh chụp màn hình hoặc bản ghi terminal (nếu cần)

Hướng dẫn tạo log (ví dụ):

```bash
# Chạy encrypt và decrypt, lưu output mẫu
printf "hello FIT4012 AES\n" | ./encrypt > logs/sample-run.log 2>&1
./decrypt >> logs/sample-run.log 2>&1

# Chạy toàn bộ test và lưu output
make test > logs/test-output.log 2>&1
```

An toàn dữ liệu:

- KHÔNG lưu hoặc commit khóa thật (file `keyfile` với khóa production) vào repository.
- KHÔNG lưu dữ liệu nhạy cảm hoặc thông tin cá nhân trong logs.

English — Notes for logs

This directory is used to store build/run/test evidence for the lab. Expected files:

- `sample-run.log` — sample execution output
- `test-output.log` — output of the test suite
- screenshots or terminal recordings

Example commands to produce logs (same as above):

```bash
printf "hello FIT4012 AES\n" | ./encrypt > logs/sample-run.log 2>&1
./decrypt >> logs/sample-run.log 2>&1
make test > logs/test-output.log 2>&1
```

Security reminder: do not commit real keys or sensitive data into the repository.

