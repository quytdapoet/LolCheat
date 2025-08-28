# Hướng dẫn Build LolCheat bằng GitHub Actions

## Tổng quan

Project này đã được cấu hình để build tự động trên GitHub Actions mà không cần cài đặt Visual Studio trên máy local.

## Cách sử dụng

### 1. Push code lên GitHub

```bash
git add .
git commit -m "Update code"
git push origin main
```

### 2. Kiểm tra GitHub Actions

1. Vào repository trên GitHub
2. Chuyển đến tab **Actions**
3. Chọn workflow **Build LolCheat** hoặc **Build LolCheat (Simple)**
4. Xem quá trình build

### 3. Tải artifacts

Sau khi build thành công:
1. Vào tab **Actions**
2. Chọn run build thành công
3. Cuộn xuống phần **Artifacts**
4. Tải về file DLL đã build

## Workflows có sẵn

### 1. Build LolCheat (build.yml)
- Build đầy đủ với DirectX SDK
- Tạo cả Debug và Release versions
- Hỗ trợ cả x86 và x64

### 2. Build LolCheat (Simple) (build-simple.yml)
- Build đơn giản hơn
- Chỉ tạo Release versions
- Không cần DirectX SDK

## Cấu trúc Output

```
LoL base/
├── x64/
│   ├── Release/
│   │   └── LoL base.dll
│   └── Debug/
│       └── LoL base.dll
└── Release/
    └── LoL base.dll
```

## Troubleshooting

### Lỗi DirectX SDK
Nếu gặp lỗi về DirectX SDK, hãy sử dụng workflow **Build LolCheat (Simple)** thay vì workflow đầy đủ.

### Lỗi Platform Toolset
Đảm bảo sử dụng `v143` (Visual Studio 2022) trong workflow.

### Lỗi Path
Kiểm tra đường dẫn trong file `.vcxproj` có chính xác không.

## Lưu ý

- Project này chỉ dành cho mục đích học tập
- Sử dụng cheat trong game thực có thể vi phạm ToS
- Cần cập nhật offsets khi game update
