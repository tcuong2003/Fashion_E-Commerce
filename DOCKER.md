# 🐳 Docker Setup Guide

Hướng dẫn build và push Docker image lên Docker Hub cho Fashion E-Commerce project.

## 📋 Yêu cầu

- Docker đã được cài đặt trên máy
- Tài khoản Docker Hub (username: `tcuong2003`)

## 🚀 Các bước thực hiện

### 1. Đăng nhập vào Docker Hub

```bash
docker login
```

Nhập username và password của Docker Hub khi được yêu cầu.

### 2. Build Docker image

```bash
docker build -t tcuong2003/fashion_e-commerce:latest .
```

Hoặc với tag cụ thể:

```bash
docker build -t tcuong2003/fashion_e-commerce:v1.0.0 .
```

### 3. Kiểm tra image đã build

```bash
docker images | grep fashion_e-commerce
```

### 4. Test chạy image locally (tùy chọn)

```bash
docker run -p 3000:3000 tcuong2003/fashion_e-commerce:latest
```

Sau đó mở trình duyệt tại `http://localhost:3000` để kiểm tra.

### 5. Push image lên Docker Hub

```bash
docker push tcuong2003/fashion_e-commerce:latest
```

Hoặc với tag cụ thể:

```bash
docker push tcuong2003/fashion_e-commerce:v1.0.0
```

## 📝 Lưu ý

- Thay `latest` hoặc `v1.0.0` bằng tag bạn muốn sử dụng
- Đảm bảo đã cấu hình biến môi trường (nếu cần) trước khi build
- Image sẽ được push lên: `https://hub.docker.com/r/tcuong2003/fashion_e-commerce`

## 🔧 Environment Variables

Nếu ứng dụng cần biến môi trường, bạn có thể:

1. Tạo file `.env` trong project
2. Hoặc truyền khi chạy container:

```bash
docker run -p 3000:3000 \
  -e DATABASE_URL="your-database-url" \
  -e NEXTAUTH_SECRET="your-secret" \
  tcuong2003/fashion_e-commerce:latest
```

## 📦 Pull và chạy image từ Docker Hub

Sau khi push, bạn hoặc người khác có thể pull và chạy:

```bash
docker pull tcuong2003/fashion_e-commerce:latest
docker run -p 3000:3000 tcuong2003/fashion_e-commerce:latest
```
