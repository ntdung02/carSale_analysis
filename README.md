# Phân tích doanh số bán ô tô
Báo cáo này tập trung vào việc phân tích doanh số bán ô tô nhằm đánh giá hiệu suất của các nhà sản xuất, xác định xu hướng tiêu dùng về mẫu mã xe, và cung cấp những thông tin chi tiết về nhân khẩu học của khách hàng. Qua các chỉ số chính như doanh số bán hàng, thị phần của từng dòng xe và sự thay đổi trong nhu cầu, chúng ta sẽ có cái nhìn rõ nét hơn về sự phát triển của thị trường ô tô. Bên cạnh đó, các đặc điểm nhân khẩu học như giới tính và sở thích của khách hàng sẽ được phân tích để hỗ trợ các nhà sản xuất trong việc tối ưu hoá chiến lược sản phẩm và tiếp thị.

## Giới Thiệu Về Bộ Dữ Liệu
Tập dữ liệu có 23906 bản ghi và 9 cột. Ghi chép về thông tin giao dịch mua bán của một đại lý xe ô tô

Chi tiết từng cột

- Car_id: Mã định danh duy nhất cho mỗi xe 
- Date: Ngày bán
- Customer Name: Tên khách hàng mua
- Gender: Giới tính 
- Annual Income: Thu nhập hàng năm của khách hàng.
- Company: Thương hiệu của xe.
- Color: Màu sắc bên ngoài của xe
- Price ($): Giá bán niêm yết của xe
- Body Style: Kiểu dáng thân xe

## Xử lý và làm sạch dữ liệu
Dự án này chủ yếu tập trung vào việc đánh giá xu hướng mua xe và biến động trong doanh số bán ô tô để đánh giá hiệu suất của nhà sản xuất, sở thích về mẫu xe và thông tin chi tiết về nhân khẩu học. 

Bộ dữ liệu này không có các giá trị trùng lặp, chỉ có cột Date đang lỗi định dạng nền cần chuyển đổi kiểu về Date

![image](https://github.com/user-attachments/assets/7a0c403b-f124-4d3b-a76f-a1cba4aa3be0)

##  Đánh giá biến động trong Doanh số bán hàng và xu hướng mua xe

- Doanh số bán xe theo từng tháng (theo số liệu từ năm 2022 - 2023)

![image](https://github.com/user-attachments/assets/bff0ac90-58c8-427e-a8f5-8873b0129950)

Nhìn vào doanh số bán được trong 2 năm ta nhận thấy doanh số có xu hướng tăng cao vào cuối năm, có thể do các dịp mua sắm lớn, chương trình khuyến mãi cuối năm hoặc do lương thưởng cuối năm đổ về nên nhu cầu mua xe tăng cao.
Đầu năm thường là thời điểm doanh số bán hàng thấp, có thể do nhu cầu mua sắm giảm sau dịp lễ hoặc ảnh hưởng từ tình hình kinh tế.

- Sự phân phối giữa Thu nhập hàng năm của người mua xe và giá cả xe hơi mà họ mua

![image](https://github.com/user-attachments/assets/345afd38-0202-458f-b301-7009c692b8f6)

Phần lớn khách hàng có thu nhập hàng năm dưới $400,000 và mua xe có giá từ $10,000 đến $50,000. Điều này cho thấy rằng các xe trong tầm giá này rất phổ biến đối với những người có thu nhập trung bình đến thấp.

Có những khách hàng có thu nhập trên $2,000,000 nhưng vẫn mua xe ở mức giá trung bình, từ $20,000 đến $50,000. Điều này có thể phản ánh những ưu tiên cá nhân khác của khách hàng giàu có, chẳng hạn như chi tiêu thận trọng hoặc đầu tư vào các tài sản khác thay vì xe cộ.

Đối với các xe có giá từ $60,000 trở lên là những dòng xe cao cấp và số lượng khách hàng mua giảm đáng kể. Nhóm này có xu hướng bao gồm các khách hàng có thu nhập cao hơn, nhưng vẫn chỉ chiếm một tỷ lệ nhỏ trong tổng số khách hàng.

Ở mức giá từ $70,000 trở lên, số lượng khách hàng giảm mạnh, điều này cho thấy thị trường cho các dòng xe cao cấp này khá hạn chế, chỉ phù hợp với một nhóm nhỏ khách hàng có thu nhập rất cao.

Cụ thể hơn chúng ta có thể xem xét biểu đồ Phân phối số lượng xe đã bán theo mức giá

![image](https://github.com/user-attachments/assets/20229c2a-4c30-46e0-8709-f75ab933b125)

 Số liệu cho thấy khoảng giá từ 10001-20001 có số lượng xe bán nhiều nhất với 8,075 chiếc, tiếp theo là khoảng giá 20002-30002 với 7,733 chiếc. Càng lên các mức giá cao hơn, số lượng xe bán ra càng giảm dần, thể hiện qua các khoảng giá từ 30003 trở lên chỉ dao động từ vài trăm đến khoảng 2,000 xe. Điều này cho thấy thị trường xe tập trung chủ yếu vào phân khúc bình dân và trung cấp có thể do khả năng chi trả hoặc nhu cầu cao ở mức giá này, trong khi các dòng xe cao cấp có giá trên 50005 có doanh số thấp hơn nhiều, chỉ đạt vài trăm chiếc mỗi phân khúc. Đáng chú ý là phân khúc xe giá rẻ dưới 10000 cũng không phải là lựa chọn phổ biến với chỉ 413 xe được bán ra, có thể do những hạn chế về chất lượng và tính năng. Qua đó có thể thấy người tiêu dùng có xu hướng ưa chuộng các dòng xe ở mức giá vừa phải, đảm bảo cân bằng giữa chi phí và chất lượng sản phẩm.

-  Doanh số bán theo các hãng sản xuất xe

![image](https://github.com/user-attachments/assets/ec5deb18-c568-4eac-bef1-23e506678a48)

Trong năm 2022, ba thương hiệu xe hơi có doanh số bán đứng đầu là Chevrolet, Dodge, Ford và có sự cạnh tranh khá sát nhau, trong đó Chevrolet nhỉnh hơn một chút. Tuy nhiên, đến năm 2023, Chevrolet đã tạo ra khoảng cách rõ rệt  với mức tăng trưởng đáng kể so với hai thương hiệu còn lại, cho thấy khách hàng ngày càng ưa chuộng loại xe này

- Doanh số bán theo Body Style qua từng năm 

![image](https://github.com/user-attachments/assets/d476e5c0-587b-4152-bb48-9c6f038dd3e4)

Số liệu cho thấy SUV và xe Hatchback là hai phân khúc dẫn đầu về doanh số trong suốt giai đoạn này. SUV có xu hướng tăng mạnh từ Quý 2/2023 và đạt đỉnh vào Quý 3/2023 với khoảng 1,300 xe vượt mặt Hatchback đang dẫn đầu trước đó, trong khi Hatchback duy trì ở mức ổn định và đạt đỉnh vào Quý 4/2022 với khoảng 1,100 xe.

Xe Sedan và Passenger có đường biểu diễn khá tương đồng, dao động ở mức trung bình với xu hướng tăng nhẹ qua các quý. Đáng chú ý là xe Hardtop có doanh số thấp nhất trong hầu hết các quý, tuy nhiên lại có sự tăng trưởng đột biến vào Quý 4/2023, tăng từ khoảng 200 lên gần 800 xe. 

Nhìn chung, thị trường có sự sụt giảm đồng loạt vào Quý 1/2023 ở tất cả các phân khúc, sau đó phục hồi và tăng trưởng trở lại trong các quý tiếp theo, có lẽ do sự tác động của nhu cầu mua sắm qua các dịp lễ tết trong năm.

- Doanh Số Theo Color và Gender

![image](https://github.com/user-attachments/assets/4edebb85-c06f-4ca5-ba0a-8768427aad2f)

Xu hướng mua xe ở nam giới và nữ giới lênh lệch nhau rất lớn, phần lớn là nam giới chiếm số lượng nhiều hơn với tổng số lượng xe nam giới mua vào khoảng 18,634 chiếc so với khoảng 5,062 chiếc của nữ giới. 

Về sở thích màu sắc, cả nam và nữ đều có xu hướng ưa chuộng màu trắng ngà (Pale White) nhất, thể hiện qua phần màu xám nhạt chiếm tỷ trọng lớn nhất trong cả hai cột. Tiếp theo là màu đen (Black) và cuối cùng là màu đỏ (Red) chiếm tỷ lệ ít nhất trong cả hai nhóm giới tính. Điều này cho thấy bất kể là nam hay nữ, màu trắng ngà vẫn là lựa chọn phổ biến và an toàn nhất khi mua xe.

- Bảng điều khiển

![image](https://github.com/user-attachments/assets/b84184cb-7fe7-4733-8bb4-16456ad21950)












