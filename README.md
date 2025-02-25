Mạch Điều Khiển Động Cơ Công Suất Cao sử dụng IR2136 và IRFZ44
Giới Thiệu
Repository này chứa sơ đồ nguyên lý và thiết kế PCB cho mạch điều khiển động cơ công suất cao, sử dụng IC driver IR2136 và MOSFET IRFZ44. Mạch được thiết kế để điều khiển động cơ ba pha, có tích hợp chức năng bảo vệ lỗi, điều khiển bật/tắt, và cảm biến dòng điện.

Đặc Điểm Chính
Điều khiển động cơ ba pha sử dụng IR2136.
Sáu MOSFET IRFZ44 để chuyển mạch công suất cao.
Bảo vệ quá dòng bằng điện trở cảm biến 0.05 Ohm.
Phát hiện lỗi (FAULT) và ngõ vào điều khiển (EN) đảm bảo an toàn.
Tụ bootstrap hỗ trợ điều khiển MOSFET phía cao áp.
Header giao tiếp với vi điều khiển hoặc mạch logic bên ngoài.
Tổng Quan Sơ Đồ Nguyên Lý
Mạch bao gồm các thành phần chính sau:

IC IR2136 (U1): Điều khiển sáu MOSFET (Q1 - Q6).
MOSFET IRFZ44: Đóng cắt dòng điện cho động cơ ba pha.
Diode 1N4118: Bảo vệ chống xung điện áp.
Điện trở & tụ điện: Lọc nhiễu và ổn định mạch.
Ngõ vào điều khiển (HIN, LIN, FAULT, EN): Kết nối với vi điều khiển.
Nguồn cấp (VCC, VM, GND): Cấp nguồn cho mạch.
Kết Nối
Chân	Mô tả
HIN1, HIN2, HIN3	Ngõ vào điều khiển MOSFET phía cao áp
LIN1, LIN2, LIN3	Ngõ vào điều khiển MOSFET phía thấp áp
FAULT	Cảnh báo lỗi
EN	Ngõ vào bật/tắt mạch
VCC	Nguồn logic
VM	Nguồn động cơ
VS1, VS2, VS3	Cảm biến điện áp pha
HO1, HO2, HO3	Điều khiển MOSFET phía cao áp
LO1, LO2, LO3	Điều khiển MOSFET phía thấp áp
Thiết Kế Mạch In (PCB)
PCB được tối ưu để đảm bảo dòng điện cao và tản nhiệt tốt:

Dây đồng dày cho đường dòng lớn.
Khoảng cách hợp lý để tránh đoản mạch.
Bố trí linh kiện tối ưu giúp tản nhiệt hiệu quả.
Hướng Dẫn Sử Dụng
Kết nối nguồn VCC (nguồn logic) và VM (nguồn động cơ).
Giao tiếp HIN, LIN, EN, FAULT với vi điều khiển.
Kết nối ba pha động cơ vào VS1, VS2, VS3.
Kiểm tra MOSFET có cần gắn tản nhiệt hay không.
Lập trình vi điều khiển để gửi tín hiệu PWM điều khiển tốc độ và hướng quay của động cơ.
