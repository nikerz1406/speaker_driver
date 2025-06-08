# Tóm tắt phần cứng cho kỹ sư thiết kế

## 1. Thành phần chính
- **Vi điều khiển:** ESP32 (hỗ trợ WiFi, Bluetooth, xử lý âm thanh)
- **Micro:** Loại chất lượng cao để ghi âm rõ ràng
- **Loa:** Phát âm thanh
- **LED RGB (7 màu):** Báo hiệu trạng thái thiết bị (kết nối, lỗi, ghi âm...)
- **Nút nhấn vật lý (5 nút):**
  - 1 nút reset
  - 2 nút tăng/giảm âm lượng
  - 1 nút bật/tắt nguồn
  - 1 nút dự phòng
- **Nguồn:** 12V đầu vào

## 2. Chức năng & Tương tác chính
- **WiFi:** Kết nối cloud để trao đổi dữ liệu (MQTT/HTTPS)
- **Bluetooth:** Nhận lệnh hoặc phát nhạc từ điện thoại
- **MQTT:** Gửi trạng thái thiết bị, nhận lệnh điều khiển, gửi dữ liệu âm thanh dạng chunk
- **Xử lý âm thanh:** Ghi âm, chia nhỏ thành các chunk (1 giây hoặc vài trăm ms), mã hóa (PCM/WAV/MP3, base64/nhị phân), gửi lên server
- **Báo trạng thái:** LED RGB đổi màu theo trạng thái thiết bị

## 3. Yêu cầu phần cứng
- Đảm bảo ESP32 dễ tiếp cận để nạp firmware và debug
- Micro và loa bố trí tối ưu cho chất lượng âm thanh
- Nút nhấn bền, rõ chức năng
- LED RGB đặt vị trí dễ quan sát
- Mạch nguồn ổn định 12V, có mạch chuyển đổi phù hợp cho ESP32 và các linh kiện

## 4. Bảo mật & Độ tin cậy
- Sử dụng WiFi bảo mật WPA2
- Hỗ trợ TLS cho MQTT nếu cần
- Đảm bảo chống nhiễu nút nhấn và quản lý nguồn hợp lý

---

