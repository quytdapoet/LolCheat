# LoL Cheat Injector

Injector đơn giản để inject DLL vào League of Legends.

## ⚠️ Cảnh báo

**CHỈ SỬ DỤNG CHO MỤC ĐÍCH HỌC TẬP!**
- Sử dụng cheat trong game thực có thể vi phạm ToS
- Có thể bị ban tài khoản
- Chỉ test trên môi trường offline

## 🔧 Cách build

### Sử dụng CMake:
```bash
mkdir build
cd build
cmake ..
cmake --build . --config Release
```

### Sử dụng Visual Studio:
1. Mở file `.cpp` tương ứng
2. Build project
3. Chạy file `.exe`

## 🎮 Cách sử dụng

### Bước 1: Chuẩn bị
1. Build DLL từ project chính
2. Build injector này
3. Đặt file `LoL base.dll` cùng thư mục với injector

### Bước 2: Inject

#### **SimpleInjector (Console):**
1. **Chạy League of Legends**
2. **Chạy SimpleInjector.exe** với quyền Administrator
3. **Nhấn Enter** để inject

#### **GUIInjector (Basic GUI):**
1. **Chạy League of Legends**
2. **Chạy GUIInjector.exe** với quyền Administrator
3. **Click "Browse"** để chọn file DLL
4. **Click "INJECT DLL"** để inject

#### **ModernInjector (Advanced GUI):**
1. **Chạy League of Legends**
2. **Chạy ModernInjector.exe** với quyền Administrator
3. **Click "Browse"** để chọn file DLL
4. **Chọn process** từ danh sách
5. **Click "INJECT DLL"** hoặc bật **Auto Inject**

### Bước 3: Sử dụng
- Nhấn **Space** để bật/tắt orbwalking
- Nhấn **X** để last hit
- Các tính năng khác sẽ hiển thị trong game

## 🛠️ Troubleshooting

### Lỗi "Không tìm thấy process"
- Đảm bảo League of Legends đang chạy
- Kiểm tra tên process có đúng không

### Lỗi "Không thể mở process"
- Chạy injector với quyền Administrator
- Tắt antivirus tạm thời

### Lỗi "Inject thất bại"
- Kiểm tra file DLL có tồn tại không
- Đảm bảo DLL được build đúng platform (x86/x64)

## 📁 Cấu trúc file

```
injector/
├── SimpleInjector.cpp     # Console injector
├── GUIInjector.cpp        # Basic GUI injector
├── ModernInjector.cpp     # Advanced GUI injector
├── CMakeLists.txt         # Build configuration
├── README.md             # Hướng dẫn này
└── build/                # Thư mục build
    └── bin/
        ├── SimpleInjector.exe
        ├── GUIInjector.exe
        └── ModernInjector.exe
```

## 🆚 So sánh các injector

| Tính năng | SimpleInjector | GUIInjector | ModernInjector |
|-----------|----------------|-------------|----------------|
| Giao diện | Console | Basic GUI | Advanced GUI |
| Chọn file DLL | ❌ | ✅ | ✅ |
| Process list | ❌ | ✅ | ✅ |
| Auto refresh | ❌ | ❌ | ✅ |
| Auto inject | ❌ | ❌ | ✅ |
| Log system | ❌ | ❌ | ✅ |
| Status bar | ❌ | ✅ | ✅ |

## 🔍 Các injector khác

Nếu injector này không hoạt động, thử:

1. **Process Hacker** - GUI injector
2. **Xenos** - Command line injector  
3. **Extreme Injector** - Popular injector
4. **GH Injector** - Modern injector

## 📝 Lưu ý

- Luôn chạy với quyền Administrator
- Tắt Windows Defender tạm thời
- Backup tài khoản trước khi test
- Chỉ test trên custom games
