# Bài 2 — Biên dịch đóng gói .jar với Gradle và lưu Artifacts

## Nội dung bổ sung vào Job `test`

```yaml
- name: Đóng gói tệp JAR với Gradle
  run: gradle bootJar

- name: Lưu trữ thành phẩm JAR Artifact
  uses: actions/upload-artifact@v4
  with:
    name: app-jar
    path: build/libs/*.jar
```

## Kiểm tra trên GitHub

1. Push lên nhánh `main`.
2. Tab **Actions** → chọn workflow CI đã chạy.
3. Phần **Summary** / **Artifacts** phải có **app-jar** (tải được file `.jar` từ `build/libs/`).

## Ảnh nộp bài

Chụp màn hình Summary tab Actions hiển thị artifact `app-jar`.
