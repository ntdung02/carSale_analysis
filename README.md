# Phân tích doanh số bán ô tô
Báo cáo này tập trung vào việc phân tích doanh số bán ô tô nhằm đánh giá hiệu suất của các nhà sản xuất, xác định xu hướng tiêu dùng về mẫu mã xe, và cung cấp những thông tin chi tiết về nhân khẩu học của khách hàng. Qua các chỉ số chính như doanh số bán hàng, thị phần của từng dòng xe và sự thay đổi trong nhu cầu, chúng ta sẽ có cái nhìn rõ nét hơn về sự phát triển của thị trường ô tô. Bên cạnh đó, các đặc điểm nhân khẩu học như giới tính và sở thích của khách hàng sẽ được phân tích để hỗ trợ các nhà sản xuất trong việc tối ưu hoá chiến lược sản phẩm và tiếp thị.

Nguồn dữ liệu: https://www.kaggle.com/datasets/missionjee/car-sales-report/data 

## Giới Thiệu Về Bộ Dữ Liệu
Tập dữ liệu có 23906 bản ghi và 16 cột.

Chi tiết từng cột

- Car_id: Mã định danh duy nhất cho mỗi xe 
- Date: Ngày bán
- Customer Name: Tên khách hàng mua
- Gender: Giới tính 
- Annual Income: Thu nhập hàng năm của khách hàng.
- Dealer_Name:  Tên của đại lý liên quan đến giao dịch bán xe.
- Company: Thương hiệu của xe.
- Model: Tên mẫu xe
- Engine: Thông số kỹ thuật của động cơ
- Transmission: Loại truyền động của xe
- Color: Màu sắc bên ngoài của xe
- Price ($): Giá bán niêm yết của xe
- Dealer_No: Mã số đại lý liên quan đến giao dịch bán xe
- Body Style: Kiểu dáng thân xe 
- Phone: Số điện thoại liên hệ liên quan đến giao dịch bán xe
- Dealer_Region:  Khu vực của đại lý bán xe.

## Xử lý và làm sạch dữ liệu
Dự án này chủ yếu tập trung vào việc đánh giá xu hướng chung và biến động trong doanh số bán ô tô để đánh giá hiệu suất của nhà sản xuất, sở thích về mẫu xe và thông tin chi tiết về nhân khẩu học cho nên sẽ xoá một số cột thông tin không cần thiết như Engine, Transmission, Dealer_No, Phone.

Bộ dữ liệu này không có các giá trị trùng lặp, chỉ có cột Date đang lỗi định dạng nền cần chuyển đổi kiểu về Date

![image](https://github.com/user-attachments/assets/7a0c403b-f124-4d3b-a76f-a1cba4aa3be0)

Tại cột Model có một số dòng chứa giá trị kiểu Date, vì vậy cần xoá các dòng đó đi thay vì đổi kiểu định dạng

![image](https://github.com/user-attachments/assets/20c8df2f-c259-4eef-9ebd-652bb9499533)

##  Đánh giá biến động trong Doanh số và xu hướng mua xe

- Doanh số bán xe theo từng tháng (theo số liệu từ năm 2022 - 2023)

![image](https://github.com/user-attachments/assets/487936ca-080f-4c62-ac0d-286ca4c38f2e)

Nhìn vào doanh số bán được trong 2 năm ta nhận thấy doanh số có xu hướng tăng cao vào cuối năm, có thể do các dịp mua sắm lớn, chương trình khuyến mãi cuối năm hoặc do lương thưởng cuối năm đổ về nên nhu cầu mua xe tăng cao.
Đầu năm thường là thời điểm doanh số bán hàng thấp, có thể do nhu cầu mua sắm giảm sau dịp lễ hoặc ảnh hưởng từ tình hình kinh tế.

- Phân phối giá xe theo số lượng

![image](https://github.com/user-attachments/assets/6f9cd718-ea37-492a-94c6-0aeca5e61bd3)

Nhu cầu thị trường tập trung chủ yếu vào các xe có giá tầm trung, đặc biệt là từ 10,000$ - 30,000$. Điều này cho thấy phân khúc xe trong khoảng giá trung bình thấp là phổ biến nhất, có thể do khả năng chi trả và nhu cầu cao ở mức giá này.

Sau khoảng 30,000$, số lượng xe bán ra giảm đáng kể, đặc biệt từ 50,000$ trở lên. Điều này cho thấy các dòng xe cao cấp hơn có nhu cầu thấp hơn, có thể do giá cao vượt khả năng chi trả của phần lớn khách hàng

- Doanh Số Theo Body Style và Gender

![image](https://github.com/user-attachments/assets/c7d8b08a-0c38-45fd-a91c-554bbbfa7d84)

Xu hướng mua xe ở nam giới và nữ giới lênh lệch nhau rất lớn, phần lớn là nam giới chiếm số lượng nhiều hơn. Nhìn chung cả nam và nữ đều ưa chuộng kiểu xe SUV và Hatchback, đây là 2 kiểu xe có lượt mua cao nhất.

- Tốc độ tăng trưởng doanh số bán xe theo Body Style qua các năm (2022 - 2023)

![image](https://github.com/user-attachments/assets/3a8dcacd-9b23-4959-84ab-38146791a1b1)

SUV và Hatchback vẫn là 2 kiểu xe có doanh số bán cao nhất, vượt xa Hardtop, Passenger, Sedan. SUV có tốc độ tăng trưởng mạnh nhất, từ 2646 xe (năm 2022) lên 3728 xe (năm 2023), cho thấy nhu cầu ngày càng cao và xu hướng ưa chuộng loại xe này.

Hatchback tuy có doanh số cao nhưng tốc độ tăng trưởng chậm nhất, chỉ từ 3013 xe lên 3076 xe, điều này phản ánh rằng dòng xe này đang bão hòa và không còn thu hút nhiều khách hàng mới. Trong khi các dòng xe còn lại như Hardtop, Passenger, Sedan có tốc độ tăng cao hơn, trong tương lai có thể vượt qua Hatchback.









