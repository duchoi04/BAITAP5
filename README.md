baitap5: HOÀNG ĐỨC HỘI - K225480106085 - HQTCSDL

BÀI TẬP VỀ NHÀ 05, Môn Hệ quản trị csdl.

CHỦ ĐỀ: Trigger trên mssql

A. Trình bày lại bài đầu tiên của đồ án PT&TKHT:

1. Mô tả bài toán của đồ án PT&TKHT Tiệm bán xe máy , yêu cầu của bài toán đó

2. Cơ sở dữ liệu của Đồ án PT&TKHT Tiệm bán xe máy : Có cơ sở dữ liệu với các bảng dữ liệu cần thiết (3nf), Các bảng này cần có PK, FK, CK

B. Nội dung Bài tập 05:

1. Cơ sở dữ liệu là csdl của Project

2. Tìm cách bổ sung xung thêm 1 (hoặc một số) trường phi chuẩn (là trường tính toán, nhưng bổ sung vào thì ok hơn, ok hơn theo 1 logic nào đó, vd ok hơn về tốc độ) => rõ rõ điều này!

3. Viết trigger cho 1 bảng nào đó, mà có thể sử dụng trường phi tiêu chuẩn này, nhằm đạt được 1 vài mục tiêu nào đó. => chỉ định các mục tiêu

4. Nhập dữ liệu có kiểm soát, nhằm để kiểm tra hiệu quả của việc tự động kích hoạt công việc.

5. Kết luận về Trigger đã giúp ích gì cho sơ đồ của em.



A. Trình bày lại bài đầu tiên của đồ án PT&TKHT:

Yêu cầu sơ đồ: Hệ thống thiết kế phân vùng mà bạn có thể chơi

Bạn có thể thao tác theo yêu cầu của hệ thống, em có các dữ liệu bảng cần thiết (3NF) như sau:

- Bảng chi tiết hóa đơn:


![Screenshot 2025-04-26 182638](https://github.com/user-attachments/assets/11e2a19e-4e69-42e2-8b11-1f32dc7a36ee)


- Bảng hóa đơn:
  
![Screenshot 2025-04-26 182631](https://github.com/user-attachments/assets/1ac95307-ba44-406a-8337-3be12f9f76c6)


- Bảng khách hàng:


![Screenshot 2025-04-26 182626](https://github.com/user-attachments/assets/2b25ee94-4199-4cd1-a820-1e2717ab0ee4)


- Bảng nhân viên:
  

![Screenshot 2025-04-26 182621](https://github.com/user-attachments/assets/28018768-6e84-44f8-aacc-f91944f0cf72)


- Bảng xe máy:
  

![Screenshot 2025-04-26 182614](https://github.com/user-attachments/assets/9706167d-6498-4abc-b98c-1800ebaa5994)


- Với các liên kết ngoại khóa cho các bảng:
  

![Screenshot 2025-04-26 233739](https://github.com/user-attachments/assets/822fb151-c5f1-4893-8a1c-ce88ec6d9aa7)



![Screenshot 2025-04-26 233753](https://github.com/user-attachments/assets/936a43f5-bfac-45ee-b340-7661a1554fac)



- Sau khi đặt các khóa chính và các liên kết khóa ngoại trừ ta được liên kết sơ đồ sau (cơ sở dữ liệu sơ đồ):


![Screenshot 2025-04-26 151019](https://github.com/user-attachments/assets/30180dce-00af-44b4-9ccc-2270a3303f61)

B. Nội dung Bài tập 05:

1. Tạo csdl cho hệ thống bạn tìm kiếm:

- Nhấn dấu "+" vào bảng và chuột phải vào Triggers ---> new trigger:


![Screenshot 2025-04-26 234300](https://github.com/user-attachments/assets/fc87aec5-11e3-46a1-ba80-709373a48628)



2. Bổ sung xung thêm 1 trường phi chuẩn: Thêm cột ThanhTien vào bảng CHITIETHD, bổ sung ThanhTien để tối ưu tốc độ truy vấn báo cáo.

:

![Screenshot 2025-04-27 001749](https://github.com/user-attachments/assets/a1a04ffd-6580-40bc-b77a-14fa773421eb)


3. Viết Trigger cho bảng CHITIETHD:

![Screenshot 2025-04-26 234511](https://github.com/user-attachments/assets/e7d6caa4-b59a-4e61-9631-f5c48ca3791e)

4. Nhập dữ liệu có kiểm soát, nhắm để kiểm tra hiệu quả của việc tự động kích hoạt công việc:


![Screenshot 2025-04-27 003525](https://github.com/user-attachments/assets/d5062fc0-73bd-4fea-8364-3fc2caa22c57)

5. Kết luận về Trigger
   
  Trigger đã giúp:

- Tự động hóa công việc tính toán ThanhTien, không cần lập trình viên hay người dùng tự nhập.

- Đảm bảo toàn vẹn dữ liệu: Không xảy ra sai sót trong tính toán thủ công.

- Tối ưu quy trình nhập liệu: Giảm số trường cần nhập.

- Tăng hiệu suất truy vấn báo cáo, vì đã có sẵn ThanhTien, không cần tính lại.










