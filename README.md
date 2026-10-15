# Dựng file IPA cho MINICRAFT SURVIVAL (để ký bằng eSign)

Mình không tạo được file .ipa trực tiếp (cần máy Mac có Xcode). Bộ này nhờ GitHub dựng giúp, miễn phí, không cần Mac.

## Các bước
1. Tạo tài khoản GitHub, tạo một kho mới (repository). Chọn **Public** để dùng macOS miễn phí không giới hạn phút (kho Private bị tính phút macOS gấp 10 lần).
2. Tải toàn bộ thư mục `ipa-kit` này lên kho (cả thư mục ẩn `.github`).
3. Vào tab **Actions** -> **Build MINICRAFT SURVIVAL IPA (chua ky)** -> **Run workflow**.
4. Chờ khoảng 10-15 phút. Xong, vào lần chạy đó, mục **Artifacts** tải `MINICRAFT-SURVIVAL-ipa` (file zip chứa `MINICRAFT-SURVIVAL.ipa`).
5. Giải nén lấy file `.ipa`, đưa vào **eSign** để ký và cài như bình thường.

## Ghi chú
- Tên ứng dụng: MINICRAFT SURVIVAL. Mã gói: `com.minicraft.survival` (eSign có thể đổi khi ký).
- Game chạy ngoại tuyến hoàn toàn: thư viện 3D được gói sẵn trong app (không cần mạng, trừ khi chơi online).
- App xoay ngang, toàn màn hình. Biểu tượng là biểu tượng mặc định của Capacitor, muốn đổi thì thay ảnh trong `ios/App/App/Assets.xcassets` sau khi tạo dự án.
- Chơi online: cần chạy máy chủ trong thư mục `server` (xem `server/README.md`), nhập `wss://...` ở nút **Chơi online**.

## Thật thà về độ tin cậy
Mình chưa chạy thử quy trình này, vì môi trường của mình không có Mac, Xcode hay mạng. Quy trình viết theo cách Capacitor 6 thường dựng, nhưng lỗi nhỏ có thể xảy ra ở bước dựng. Nếu lỗi, copy dòng đỏ trong tab Actions gửi cho mình để sửa.
