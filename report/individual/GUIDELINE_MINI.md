# Mini guideline — bài làm cá nhân

> Điền nội dung này trước khi bắt đầu gán nhãn. Giữ lại các quyết định sau khi self-QC.

## Định nghĩa lớp

| Lớp | Định nghĩa của bạn | Ví dụ/điểm phân biệt |
| --- | --- | --- |
| `car` |Xe con chở người, thân liền, tối đa khoảng 7 chỗ |Sedan, hatchback, SUV, crossover, MPV nhỏ. Phân biệt: car có cửa sổ bên liên tục, không có thân hộp cao kiểu xe tải nhẹ |
| `truck` |Xe chuyên chở hàng, có cabin tách biệt với thùng hoặc khoang hàng |Xe tải thùng, xe ben, xe đầu kéo, xe bồn, pickup. Phân biệt: truck có cabin và thùng hàng tách rời rõ ràng |
| `bus` |Xe chở khách cỡ lớn, thân dài, nhiều hàng cửa sổ, thường trên 16 chỗ |Xe buýt thành phố, xe khách đường dài, xe đưa đón cỡ lớn. Phân biệt với: bus cao và dài hơn hẳn, có từ 2 cửa hành khách hoặc dài trên khoảng 7 m |
| `van` |Xe thân hộp liền khối, chở người hoặc hàng nhẹ, cabin và khoang sau liền nhau |Ford Transit, Hyundai Solati, xe van giao hàng, minibus 12–16 chỗ. Phân biệt với `car`: van cao hơn, thân hộp vuông. Phân biệt với `truck`: không có thùng tách rời |

## Quy tắc chung

- Box bám sát vật thể nghĩa là: hình chữ nhật nhỏ nhất bao trọn phần nhìn thấy của thân xe, tính cả bánh xe và gương chiếu hậu. Đồ gắn ngoài xe (hàng chất trên nóc, thang) chỉ tính nếu là phần cố định của xe.
- Vật thể bị che khuất: vẫn gán nhãn nếu còn thấy khoảng 30% diện tích trở lên hoặc còn nhận ra được lớp. Box chỉ bao phần nhìn thấy, không đoán phần bị che. Dưới ngưỡng này thì bỏ qua.
- Vật thể bị cắt bởi rìa ảnh: gán nhãn nếu còn nhận ra được lớp, box kéo sát đến mép ảnh, không vượt ra ngoài. Nếu chỉ còn một mảnh nhỏ (ví dụ chỉ thấy bánh xe hoặc một góc), bỏ qua.
- Vật thể rất nhỏ/mơ hồ: đặt ngưỡng tối thiểu khoảng 15×15 px. Nhỏ hơn hoặc không phân biệt được lớp thì không gán, không đoán. Xe nhỏ nhưng rõ lớp thì vẫn gán

## Ghi lại quyết định cho ít nhất ba ca mơ hồ

| Ảnh | Tình huống | Quyết định cuối | Lý do theo schema |
| --- | --- | --- | --- |
| `drive_002` |ảnh car nhỏ hơn 15x15 px |vẫn gán nhãn |ảnh tuy nhỏ nhưng vẫn nhìn rõ lớp |
| `drive_049` |ảnh vật thể car bị cắt bởi rìa ảnh |vẫn gán nhãn |vì vẫn còn nhận ra lớp, nhận ra được dó là car |
| `drive_050` |các vật thể car bị che khuất nhiều nhưng dùng mắt thường vẫn nhận ra |không gán nhãn |diện tích còn nhìn thầy dưới 30% |
