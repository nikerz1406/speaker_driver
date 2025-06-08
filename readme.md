# Dự án Driver Loa Thông Minh

## Mô tả
Dự án này triển khai một mô-đun loa thông minh sử dụng chip ESP32, hỗ trợ ghi âm rõ ràng, phát nhạc, kết nối không dây và điều khiển qua các nút vật lý. Thiết bị hướng tới các ứng dụng IoT với khả năng giao tiếp với máy chủ đám mây và điện thoại di động.

## Tính năng
- Ghi âm bằng micro chất lượng cao.
- Phát âm thanh qua loa.
- Sử dụng nguồn điện 12V.
- 5 nút điều khiển:
  - 1 nút reset.
  - 2 nút tăng/giảm âm lượng.
  - 1 nút bật/tắt nguồn.
  - 1 nút dự phòng.
- Kết nối WiFi và Bluetooth:
  - Kết nối với máy chủ đám mây (VM Cloud).
  - Kết nối với điện thoại.
- Đèn LED 7 màu báo trạng thái hoạt động.
- Sử dụng chip ESP32.

## Công nghệ sử dụng (Stacks)
- Phần cứng: ESP32, micro, loa, LED RGB, nút nhấn vật lý.
- Phần mềm: ESP-IDF, giao tiếp MQTT/HTTPS với cloud, Bluetooth, WiFi.

## Luồng kết đăng ký loa IOT lên server

1. **Khởi động thiết bị:** Đèn báo xanh, âm thanh báo hiệu bluetooth hoạt động
2. **kết nối điện thoại** Kết nối loa với điện thoại với điện thoại, âm thanh báo kết nối thành công
3. **Kết nối wifi** điện thoại cấu hình mạng wifi cho loa thông qua bluetooth, âm thanh báo kết nối mạng thành công
4. **Giao tiếp với cloud:**
   - Thiết bị gửi dữ liệu trạng thái (âm lượng, trạng thái nguồn, v.v.) lên máy chủ đám mây qua MQTT hoặc HTTPS.
   - Nhận lệnh điều khiển từ cloud (ví dụ: thay đổi âm lượng, bật/tắt loa).

**Giao tiếp với điện thoại:**
   - Kết nối Bluetooth để nhận lệnh trực tiếp hoặc cấu hình các key, thông số kỹ thuật
**Phản hồi trạng thái:**
   - LED RGB thay đổi màu sắc để báo hiệu trạng thái (kết nối, lỗi, ghi âm, v.v.).
   - Gửi thông báo trạng thái về cloud để đồng bộ.

---
