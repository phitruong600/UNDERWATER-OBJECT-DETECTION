## 1. GIỚI THIỆU VỀ ĐỀ TÀI
Bài toán tập trung vào **ứng dụng học sâu** để nhận diện và định vị các sinh vật biển (cá, sứa, chim cánh cụt, chim nhạn biển, cá mập, sao biển, cá đuối) thông qua các bounding box và phân loại chúng. Phương pháp chính sử dụng hai mô hình tiên tiến: **YOLO** (cho thời gian thực) và **Faster R-CNN** (cho độ chính xác cao).

## 2. PHƯƠNG PHÁP & THỰC NGHIỆM
- **Thu thập dữ liệu**: 637 ảnh, chia thành tập huấn luyện, kiểm định và kiểm thử.  
- **Tăng cường dữ liệu**: Thay đổi kích thước, ánh sáng, lật ảnh, v.v.  
- **Huấn luyện mô hình**:
  - **Faster R-CNN**: Backbone ResNet50, RPN để tìm vùng đối tượng.  
  - **YOLOv8**: Triển khai qua Ultralytics, tối ưu để xử lý thời gian thực.  
- **Đánh giá**: Dùng mAP, Recall, Precision; so sánh hiệu suất hai mô hình.

## 3. KẾT QUẢ CHÍNH
- **YOLO** đạt mAP cao hơn (0.79 so với 0.5 của Faster R-CNN) và tốc độ nhanh hơn.  
- **Faster R-CNN** có khả năng định vị chính xác hơn khi đối tượng có bounding box rõ ràng, nhưng huấn luyện và dự đoán chậm hơn.  
- **Tăng cường ảnh** giúp tăng đáng kể mAP, đặc biệt ở điều kiện ánh sáng yếu.

## 4. KẾT LUẬN & HƯỚNG PHÁT TRIỂN
- **Faster R-CNN** và **YOLO** đều có ưu, nhược điểm riêng; tuỳ mục đích (thời gian thực hay độ chính xác cao) để lựa chọn.  
- Cải thiện hơn nữa bằng **ensemble modeling** hoặc áp dụng thêm nhiều kỹ thuật **tăng cường dữ liệu**.  
- Kết quả khả quan trong **nghiên cứu và bảo tồn sinh thái biển**, mở rộng tiềm năng cho các dự án tương tự.
