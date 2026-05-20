## 2. Firmware:

1. Setpoint của nhiệt độ sẽ thay đổi theo thời gian cho đến khi đạt đến giá trị mong muốn chứ không phải là đặt setpoint là target?

- Vì khi chênh lêchj nhiệt độ giữa target và PV quá lớn sẽ PID sẽ output 100%, integral cộng mạnh, dễ vượt lố nhiệt độ( do nhiệt độ thay đổi chậm và có quán tính lớn và phản hồi sựu thay đổi chậm, khi bớm nhiệt qua lớn thì khi đo được nhiệt độ đang gần bằng  targetheater trước đó đã bơm rất nhiều nhiệt, khối nhiệt vẫn còn tích năng lượng nên nhiệt vẫn tiếp tục tăng). Còn setpoint tăng dần giúp làm nhiệt độ bám từ từ, mướt hơn nhiều.

- Nếu chỉ tool thông số PID thì thường giảm Kp(để giảm phản ứng theo sai số hiện tại), giảm Ki(giảm tích lũy lỗi theo thời gian), tăng Kd(tằng phản ứng khi gặp thay đỏi sai số) thì hệ sẽ chậm hơn, lên xuống nhiệt chậm hơn, phản ứng kém hơn.



1. Tại sao phải cần board MPU làm trung gian? Còn phải xử lí camera, muốn MPU làm CAN Bus--hỏi kỉ  hơn là node chính hay node trong heej thoongs lowns
2. Tại sao bootloader không tự động nhảy sau 1 khoảng thời gian sau khi check header?
3. Tại sao lại phải dung PRAM và không đưa thẳng qua MPU?
4. ECC cuar protocol là gì? Giải thích được ý nghĩ và công dung của từng cái?
5. Vung RAM trống cho đầu APP để làm gì? (shared data)
6. Treen MCU UART nào là MCU <--> MPU, UART debug lênh help xem cmd?
7. ECC là gì? Nếu kĩ thì đưa rõ hơn hơn vào báo cáo giải thích frame.
8. Status của BLD là làm gì, nhận gì về vậy? Thử go lệnh bping, bverify từ terminal debug EXP thử được không? Xem thử tại sao chờ timeout nó không tự nhảy đến application?
9. bsp_photo_start_sampling() nó gọi TC0_CH1 đếm timer trong bao lâu thì mới gọi spi đầu tiên ra?
10. Nhiệt độ hiển thị ra là gì, 
11. Tại sao phải có 8 profile, và phải đi config cho từng profile, gây khó khan cho người dung mà không set nhiệt độ chung và cả 8 cái tự động điều chỉnh, hay là hiển thi nhiệt độ 8 NTC nhỉ ( hay chỉ log nhiệt độ 8 NTC khi chạy thôi)
12. Tại sao lại cần board IF?
13. Tại sao phải lại dung double queue của  PRAM?

