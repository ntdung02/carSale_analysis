# Đánh giá Xu hướng và Biến động trong Doanh số Bán Ô Tô
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

##  Đánh giá xu hướng và biến động trong Doanh số bán ô tô

- Doanh số bán xe theo từng ngày theo số liệu trong năm 2022 - 2023





