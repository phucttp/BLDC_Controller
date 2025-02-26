# 📌 Mạch Điều Khiển Động Cơ Công Suất Cao sử dụng IR2136 & IRFZ44  

## 📖 Giới Thiệu  
Repository này chứa sơ đồ nguyên lý và thiết kế PCB cho mạch điều khiển động cơ ba pha, sử dụng **IC driver IR2136** và **MOSFET IRFZ44**. Mạch hỗ trợ bảo vệ lỗi, điều khiển bật/tắt và cảm biến dòng điện.  

## 🚀 Đặc Điểm Chính  
✔️ **Điều khiển động cơ ba pha** với IR2136  
✔️ **Sáu MOSFET IRFZ44** đảm bảo công suất cao  
✔️ **Bảo vệ quá dòng** bằng điện trở cảm biến **0.05 Ohm**  
✔️ **Ngõ ra FAULT & EN** giúp bảo vệ hệ thống  
✔️ **Bootstrap capacitor** hỗ trợ điều khiển MOSFET cao áp  
✔️ **Header giao tiếp** với vi điều khiển hoặc mạch ngoài  

## 🛠 Tổng Quan Sơ Đồ Nguyên Lý  
Mạch gồm các phần chính:  
- **IR2136 (U1)** – Điều khiển sáu MOSFET (Q1 - Q6)  
- **MOSFET IRFZ44** – Công suất cao, dòng tối đa **49A**, áp cấp tối đa **55V**  
- **Mạch bootstrap** – Tụ điện (`C1, C3, C4`) & diode (`D1, D2, D3`), hỗ trợ MOSFET cao áp  
- **Diode 1N4118** – Chống xung điện áp, bảo vệ linh kiện  
- **Điện trở & tụ điện** – Lọc nhiễu, ổn định mạch  
- **Ngõ vào điều khiển (HIN, LIN, FAULT, EN)** – Tương thích MCU, giao tiếp dễ dàng  
- **Nguồn cấp (VCC, VM, GND)** – Cấp nguồn cho hệ thống, đảm bảo hiệu suất
- 
## 🔌 Kết Nối  
| Chân | Chức năng |  
|------|----------|  
| **HIN1, HIN2, HIN3** | Điều khiển MOSFET high-side |  
| **LIN1, LIN2, LIN3** | Điều khiển MOSFET low-side |  
| **FAULT** | Ngõ cảnh báo lỗi |  
| **EN** | Bật/tắt hệ thống |  
| **VCC** | Nguồn cấp logic |  
| **VM** | Nguồn động cơ |  
| **VS1, VS2, VS3** | Điện áp pha động cơ |  
| **HO1, HO2, HO3** | Ngõ điều khiển MOSFET nhánh trên |  
| **LO1, LO2, LO3** | Ngõ điều khiển MOSFET nhánh dưới |  

## 🖥 Thiết Kế PCB  
📌 **Bố trí tối ưu** để đảm bảo hiệu suất:  
✅ **Dây đồng dày** đảm bảo dòng điện cao  
✅ **Khoảng cách hợp lý** tránh chạm mạch  
✅ **Bố trí linh kiện tối ưu** giúp tản nhiệt tốt  

## 🖼️ Hình Ảnh Thiết Kế
### 🔹 Ảnh 3D Mạch  
![3D PCB](3D.JPG)

### 🔹 Ảnh PCB  
![PCB Layout](bottom.JPG)

## 🎯 Hướng Dẫn Sử Dụng  
1️⃣ Cấp nguồn **VCC (logic)** & **VM (động cơ)**  
2️⃣ Kết nối **HIN, LIN, EN, FAULT** với vi điều khiển  
3️⃣ Nối động cơ vào **VS1, VS2, VS3**  
4️⃣ Kiểm tra nhiệt độ MOSFET, có thể cần **tản nhiệt**  
5️⃣ Lập trình MCU gửi **tín hiệu PWM** điều khiển tốc độ động cơ  

## 🔄 Cải Tiến Trong Tương Lai  
⚡ **Tích hợp cảm biến dòng điện** → Điều khiển vòng kín  
⚡ **Bảo vệ ngược cực nguồn** → Tránh hư hỏng linh kiện  
⚡ **Tối ưu PCB** → Giảm nhiễu và tăng độ bền  

## 📜 Giấy Phép  
🚀 **Dự án mã nguồn mở** – Sử dụng tự do cho học tập & thương mại 

---

🔥 Nếu bạn thấy hữu ích, đừng quên **⭐ Star** repo nhé!  
