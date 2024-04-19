STM32 giao tiếp 1 nút nhấn, một LED và giao tiếp máy tính qua UART

Nếu nút nhấn được nhấn, thì LED được đảo trạng thái. (nếu led đang tắt, nhấn nút làm led sáng và ngược lại). Khi nhả nút LED giữ nguyên trạng thái

UART gửi các command sau:

ON\CR\LF làm LED sáng

OFF\CR\LF làm LED tắt

TOGGLE\CR\LF làm LED đảo trạng thái

Sử dụng 1 task LED điều khiển LED, 1 task SW giao tiếp nút nhấn, 1 task UART giao tiếp UART. Có thể sử dụng ngắt UART để truyền dữ liệu cho task UART.

3 task thông tin với nhau qua queue
