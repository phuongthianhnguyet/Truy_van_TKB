## Phương Thị Ánh Nguyệt-K225480106098
Bài tập 4: (sql server)
Yêu cầu bài toán:
 - Tạo csdl cho hệ thống TKB (đã nghe giảng, đã xem cách làm)
 - Nguồn dữ liệu: TMS.tnut.edu.vn
 - Tạo các bảng tuỳ ý (3nf)
 - Tạo được query truy vấn ra thông tin gồm 4 cột: họ tên gv, môn dạy, giờ vào lớp, giờ ra.
   Trả lời câu hỏi: trong khoảng thời gian từ datetime1 tới datetime2 thì có những gv nào đang bận giảng dạy.

Các bước thực hiện:
1. Tạo github repo mới: đặt tên tuỳ ý (có liên quan đến bài tập này)
2. tạo file readme.md, edit online nó:
   paste những ảnh chụp màn hình
   gõ text mô tả cho ảnh đó

Gợi ý:
  Sử dung tms => dữ liệu thô => tiền xử lý => dữ liệu như ý (3NF)
  Tạo các bảng với struct phù hợp
  Insert nhiều rows từ excel vào cửa sổ edit dữ liệu 1 table (quan sát thì sẽ làm đc)
 deadline: 15/4/2025

## BÀI LÀM.

Thiết kế CSDL cho hệ thống TKB
Cấu trúc chuẩn theo dạng chuẩn 3NF.
Ta có các bảng sau:
- giaovien(#magiaovien, hoten).
- lophp(#malophp, tenlop).
- monhoc(#mamonhoc, tenmonhoc).
- phong(#maphong, tenphong).
- TKB(#id_TKB, @magiaovien, @mamonhoc, @maphong, @malophp, giobatdau, gioketthuc).

1. Bảng giaoVien(#magiaovien, hoten).

![image](https://github.com/user-attachments/assets/861542f1-783f-435d-b059-abd9fddcf410)

2. Bảng lophp(#malophp, tenlop).

![image](https://github.com/user-attachments/assets/251e23c7-0f25-4ea2-98c8-53c47cd8b57c)

3. Bảng monhoc(#mamonhoc, tenmonhoc).

![image](https://github.com/user-attachments/assets/752e851a-0527-4a3f-8d91-ffc8ed79f376)

4. Bảng phong(#maphong, tenphong).

![image](https://github.com/user-attachments/assets/e9afa2b7-4055-4a14-b24c-3cef1db1068c)

5. Bảng TKB(#id_TKB, @magiaovien, @mamonhoc, @maphong, @malophp, giobatdau, gioketthuc).

![image](https://github.com/user-attachments/assets/a472791f-6625-470c-ac8f-5547d502cae3)


- giobatdau:

![image](https://github.com/user-attachments/assets/4158a6a2-be63-4e44-b16d-0482c46b984b)

-gioketthuc:

![image](https://github.com/user-attachments/assets/1d42deec-47d8-4bc7-baf8-418dd94e3678)

- ngay:
  
![image](https://github.com/user-attachments/assets/dd340bea-a633-446c-ac35-9c082bc2a9c8)

- thu:

![image](https://github.com/user-attachments/assets/d1b1ad8f-19a0-42a4-9a07-de563dc8f74b)

- sotiet:

![image](https://github.com/user-attachments/assets/eb4100ab-a7fa-420a-af1c-48229c62971c)


# Diagram.

![image](https://github.com/user-attachments/assets/a2b3be39-3b55-48a7-90b3-8becec1d0e7d)


# Thêm thông tin cho các bảng từ EXCEL.

Nguồn dữ liệu: TMS.tnut.edu.vn

![image](https://github.com/user-attachments/assets/a2a0496e-81a7-4ae2-9d1b-0b2395a7fb13)

Đưa dữ liệu từ TMS.tnut.edu.vn sang EXCEL.

![image](https://github.com/user-attachments/assets/f45dd0e1-9a96-431d-9f9c-99d20dfc0c1d)

1. Điền dữ liệu cho bảng giáo viên.

Copy cột B sang cột Q.

![image](https://github.com/user-attachments/assets/5b8ea29f-0952-40f4-83fc-364db18505fc)

Tiếp tục chọn cột Q và chọn DATA --> Remove Duplicates --> Ok.
Kết quả sẽ cho đưa ra họ tên của các thầy cô mà không bị trùng lặp lại.

![image](https://github.com/user-attachments/assets/5f9888ab-c78e-4b98-88a7-56de85e92fca)

Copy các dữ liệu cần đưa vào bảng là hoàn tất.

![image](https://github.com/user-attachments/assets/4ebba67c-0564-457c-99cd-3167bc6bdab2)



Tương tự ta sẽ thực hiện với các bảng tiếp theo.
2. Điền dữ liệu cho bảng lớp học phần.

![image](https://github.com/user-attachments/assets/7cf6d998-3d04-4900-8c5b-29b678feed5e)

![image](https://github.com/user-attachments/assets/18758e55-1524-42cf-9b0b-9a80aa5d93d1)

3. Điền dữ liệu cho bảng môn học.

![image](https://github.com/user-attachments/assets/d2ae16d4-3daa-45cb-b2bb-3d0845cf1c4b)

![image](https://github.com/user-attachments/assets/6776e6d6-603f-4f97-927b-71d6755e7d50)

4. Điền dữ liệu cho bảng phòng.


![image](https://github.com/user-attachments/assets/1d24074c-3552-4430-ad69-61f5e44695d6)

![image](https://github.com/user-attachments/assets/efbe63df-342d-454f-bb78-950d1b70cb03)


5. Điền dữ liệu cho bảng TKB.

![image](https://github.com/user-attachments/assets/cc92b854-0059-41de-8f6f-3de7a8746b32)

![image](https://github.com/user-attachments/assets/8731fdea-8cb4-4ff0-a9cf-b7012cef2ad2)


# Tạo được query truy vấn ra thông tin gồm 4 cột: họ tên gv, môn dạy, giờ vào lớp, giờ ra.

Trả lời câu hỏi: trong khoảng thời gian từ datetime1 tới datetime2 thì có những gv nào đang bận giảng dạy.
















