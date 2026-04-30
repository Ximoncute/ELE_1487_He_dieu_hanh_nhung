# 🚀 ELE_1487 - Hệ điều hành nhúng

## 📌 Giới thiệu
Đây là repository cho học phần **Hệ điều hành nhúng (Embedded Operating System)**.

Dự án tập trung vào:
- Xây dựng và cấu hình hệ điều hành nhúng
- Làm việc với driver, kernel và user space
- Tích hợp ứng dụng vào hệ thống nhúng
- Tự động hóa quá trình khởi động (autostart service)

---

## 🎯 Mục tiêu
- Hiểu rõ cách hoạt động của hệ điều hành nhúng
- Xây dựng hệ thống Linux nhúng bằng Buildroot / Yocto
- Viết driver cơ bản trong Linux
- Giao tiếp giữa kernel space và user space
- Triển khai ứng dụng thực tế trên board

---

## 🏗️ Kiến trúc hệ thống
```
+----------------------+
|   User Application   |
+----------------------+
|     System Call      |
+----------------------+
|    Kernel Space      |
|  (Driver / Module)   |
+----------------------+
|    Hardware Layer    |
+----------------------+
```

---

## 🧰 Công nghệ sử dụng
- Ngôn ngữ: C / C++
- Hệ điều hành: Embedded Linux
- Build system: Buildroot / Yocto
- Giao tiếp: GPIO / I2C / SPI / UART

---

## 📂 Cấu trúc thư mục
```
.
├── driver/
├── app/
├── buildroot/
├── scripts/
├── docs/
└── README.md
```

---

## ⚙️ Cài đặt môi trường

### Clone repository
```bash
git clone https://github.com/Ximoncute/ELE_1487_He_dieu_hanh_nhung.git
cd ELE_1487_He_dieu_hanh_nhung
```

---

## 🔧 Build

### Build driver
```bash
cd driver
make
```

### Build application
```bash
cd app
gcc main.c -o app
```

---

## ▶️ Chạy

### Load driver
```bash
insmod driver.ko
```

### Kiểm tra
```bash
dmesg | tail
```

### Run app
```bash
./app
```

---

## 🔄 Autostart
Tạo script trong:
```
/etc/init.d/
```

---

## 📊 Chức năng
- Giao tiếp kernel ↔ user
- Đọc dữ liệu từ driver
- Tự động chạy khi boot

---

## 👨‍💻 Tác giả
- Ximon Cute

---

## 📄 License
Educational purpose only
