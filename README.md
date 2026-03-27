# 🎯 2D Object Tracker & Trajectory Analyzer

![Language](https://img.shields.io/badge/Language-Python-blue.svg)
![Computer Vision](https://img.shields.io/badge/Domain-Computer%20Vision-orange.svg)
![Algorithm](https://img.shields.io/badge/Algorithm-Template%20Matching-success.svg)

## 📌 Tổng quan (Overview)
Đây là một chương trình Thị giác máy tính (Computer Vision) ứng dụng thuật toán **Template Matching** (Khớp mẫu) thông qua phép **Tương quan chéo 2D (2D Cross-Correlation)**. Chương trình cho phép người dùng chọn một vùng vật thể (ROI) bất kỳ trên khung hình đầu tiên của video, sau đó tự động theo dõi vị trí của vật thể đó xuyên suốt video và trích xuất ra biểu đồ quỹ đạo chuyển động.

## 🚀 Tính năng chính (Key Features)
* **Tương tác trực quan:** Cho phép người dùng dùng chuột quét chọn vùng vật thể (ROI - Region of Interest) trực tiếp trên khung hình đầu tiên bằng `matplotlib.widgets`.
* **Thuật toán bám sát độ chính xác cao:** Sử dụng `scipy.signal.correlate2d` kết hợp chuẩn hóa (trừ đi giá trị trung bình) để tăng độ ổn định của thuật toán khi độ sáng môi trường thay đổi.
* **Trích xuất dữ liệu đa dạng:**
    * Xuất từng khung hình đã được vẽ bounding box (khung chữ nhật đỏ) và tọa độ tâm.
    * Vẽ và xuất bản đồ quỹ đạo chuyển động (Trajectory Map) của vật thể trên đồ thị 2D.
    * Tự động tổng hợp và render lại thành một video kết quả hoàn chỉnh bằng `moviepy`.

## 🛠️ Công nghệ & Thư viện sử dụng
* **Numpy & SciPy:** Xử lý ma trận ảnh và tính toán phép tương quan 2D.
* **Matplotlib:** Vẽ biểu đồ quỹ đạo và tạo giao diện chọn ROI.
* **Pillow (PIL):** Xử lý hình ảnh, vẽ khung bounding box và chèn text tọa độ.
* **MoviePy:** Đọc video gốc và render video đầu ra từ chuỗi ảnh.
