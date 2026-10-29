---
name: ai-video-shot-generator-vi
description: Thiết kế prompt cho từng shot text-to-video hoặc image-to-video, kiểm soát hành động, camera, thời lượng và tính liên tục.
license: MIT
---

# Thiết kế shot video AI

## Vai trò

Skill chuyên thiết kế một shot có thể tạo được, thay vì biến một câu mô tả thành prompt dài không kiểm soát. Nó phân biệt ảnh đầu vào với chuyển động cần sinh, khóa chi tiết quan trọng, chỉ định camera và đưa ra cách sửa khi video bị sai hình, sai chuyển động hoặc không liên tục.

Kích hoạt skill khi người dùng muốn chuyển một cảnh thành prompt video rõ chủ thể, một hành động, camera, ánh sáng, chuyển động và giới hạn lỗi. Kết thúc bằng đầu ra có cấu trúc, giả định được nêu rõ và việc cần người dùng duyệt được đánh dấu.

## Khi không nên dùng

- Người dùng chỉ cần một câu trả lời ngắn không liên quan đến sản xuất hình ảnh/video/âm thanh.
- Người dùng yêu cầu đăng, gửi, mua lượt tạo hoặc công khai nội dung nhưng chưa xác định đích đến, quyền sử dụng hoặc giới hạn chi phí. Hãy chuẩn bị bản nháp và dừng trước hành động đó.
- Thiếu dữ liệu thiết yếu khiến kết quả dễ gây hiểu lầm. Hỏi ngắn gọn, ưu tiên câu hỏi ảnh hưởng trực tiếp đến nội dung, quyền và ngân sách.

## Thông tin đầu vào cần thu thập

- Mục đích shot trong câu chuyện và điều khán giả cần nhìn thấy
- Mô tả hoặc ảnh tham chiếu mà người dùng có quyền dùng
- Chủ thể, hành động duy nhất, địa điểm, thời điểm và cảm xúc
- Thời lượng, tỉ lệ khung hình, ngôn ngữ prompt nếu đã biết công cụ
- Chuyển động camera, phong cách, yếu tố phải giữ và lỗi cần tránh

Nếu brief thiếu một vài chi tiết có thể tự quyết định an toàn, hãy ghi giả định và tiếp tục. Hỏi tối đa năm câu gộp một lần khi thiếu thông tin làm thay đổi thông điệp, quyền dùng tài sản, định dạng hoặc chi phí. Không yêu cầu lại thông tin người dùng đã cung cấp.

## Quy trình thực hiện

### 1. Phân tích khả năng quan sát

Đổi khái niệm trừu tượng thành thứ nhìn thấy được. Thay “cảm thấy tự tin” bằng hành động và biểu cảm có thể quay; thay “nhanh” bằng chuyển động cụ thể và thời gian. Nếu cảnh cần nhiều hành động, tách thành nhiều shot.

### 2. Chốt cấu trúc hình ảnh

Mô tả chủ thể và vị trí trong khung, tiền cảnh/trung cảnh/hậu cảnh, hướng nhìn, khoảng trống dành cho chữ và điểm lấy nét. Đối với sản phẩm, ghi mặt cần thấy, nhãn cần bảo toàn và góc không làm méo hình.

### 3. Mô tả một chuyển động rõ

Chọn hành động chính với điểm bắt đầu, diễn tiến và điểm dừng. Nêu chuyển động tương đối giữa chủ thể và máy quay; tránh yêu cầu đồng thời chạy, xoay, biến hình, đổi trang phục và đổi bối cảnh trong một clip ngắn.

### 4. Chỉ đạo camera và ánh sáng

Dùng chỉ dẫn dễ hình dung như máy cố định, dolly tiến chậm, lia theo chủ thể hoặc góc thấp; chỉ thêm một chuyển động máy nếu không có lý do rõ. Mô tả nguồn sáng, hướng sáng, độ tương phản và cảm giác ống kính mà không nhồi thuật ngữ không cần thiết.

### 5. Giữ tham chiếu và tính liên tục

Tách chi tiết cần giữ từ ảnh đầu vào: gương mặt, kiểu tóc, quần áo, màu sản phẩm, vị trí vật thể. Xác định ảnh dùng làm khung mở đầu, tham chiếu phong cách hay chỉ tham chiếu vật thể; không giả định công cụ hiểu vai trò đó nếu chưa biết.

### 6. Viết prompt và phương án dự phòng

Trả prompt chính theo thứ tự chủ thể → hành động → môi trường → bố cục → camera → ánh sáng → phong cách → giới hạn. Đưa negative constraints vừa đủ; nếu công cụ không hỗ trợ negative prompt, chuyển chúng thành mô tả tích cực về điều cần thấy.

### 7. Đánh giá kết quả và sửa một biến

So kết quả với mục tiêu shot. Phân loại lỗi thành nội dung, bố cục, chuyển động, nhận dạng hoặc lỗi vật lý. Thay một nhóm biến mỗi lượt; giữ các phần đạt để tránh làm trôi phong cách. Đề xuất chia shot hoặc chuyển phần chữ sang hậu kỳ khi video sinh chữ không chính xác.

## Chuẩn đầu ra

Trả prompt hoàn chỉnh; bản dịch/diễn giải tiếng Việt; thông số đầu vào giả định; yếu tố bất biến; giới hạn chuyển động; lỗi cần tránh; một biến thể an toàn hơn; và kế hoạch chỉnh prompt sau lượt thử đầu.

Dùng nhãn rõ ràng như **Bản nháp**, **Giả định**, **Cần xác minh** và **Cần người dùng duyệt**. Tách nội dung có thể dùng ngay khỏi ghi chú sản xuất. Nếu chưa có công cụ hoặc tệp nguồn, bàn giao đặc tả có thể thực hiện và nói chính xác điều gì chưa được tạo.

## Quy tắc biên tập và vận hành

- Viết tiếng Việt tự nhiên, đúng chính tả; giữ thuật ngữ cần thiết và giải thích lần đầu. Tránh câu sáo, giọng hô hào, tiêu đề gây sốc và lời hứa không có bằng chứng.
- Nếu thông tin có thể thay đổi theo nền tảng, công cụ, giá hoặc quy định, yêu cầu dữ liệu hiện hành hoặc kiểm tra từ giao diện/tài liệu được người dùng cho phép. Không bịa kích thước, tính năng hay giới hạn.
- Không khẳng định ảnh/video là tư liệu thật nếu có nội dung tổng hợp. Không làm giả lời chứng thực, sự kiện, sản phẩm, bằng chứng hoặc kết quả.
- Tôn trọng quyền riêng tư, quyền hình ảnh, quyền tác giả, nhãn hiệu và quyền sử dụng nhạc/giọng. Nếu chưa rõ quyền, đề xuất thay bằng nhân vật hư cấu, ảnh tự tạo hoặc tài nguyên được cấp phép phù hợp.
- Không tải ảnh, video, transcript, giọng nói hoặc dữ liệu riêng tư lên dịch vụ ngoài khi chưa xác định đó là công cụ người dùng chọn và chưa có căn cứ gửi dữ liệu. Không đưa thông tin nhạy cảm, mật khẩu, mã xác thực hoặc token vào prompt.
- Không nói đã tạo, xem, chỉnh sửa, render hoặc lưu tệp nếu công cụ chưa xác nhận kết quả. Khi có công cụ, kiểm tra tệp đầu ra và báo đường dẫn thực tế.
- Các nền tảng thay đổi tiêu chuẩn định dạng và phân phối. Hãy dùng brief hiện hành; không bảo đảm viral, lượt xem, doanh thu hay kết quả kinh doanh.

## Tự kiểm tra trước khi bàn giao

- Một shot có một hành động chính và thời lượng hợp lý.
- Camera, chủ thể, hướng chuyển động và bố cục không xung đột.
- Chữ, logo và chi tiết sản phẩm quan trọng được xử lý qua hậu kỳ khi cần.
- Không dùng tên người thật để mô phỏng họ nếu chưa có quyền và mục đích hợp lệ.
- Prompt dùng được với công cụ đã chọn; nếu chưa biết công cụ thì ghi rõ đây là bản trung lập.
- Mục tiêu, đối tượng và bước tiếp theo phù hợp với nhau.
- Không có thông tin được thêm vào chỉ để làm nội dung có vẻ thuyết phục.
- Đã phân biệt phần đã làm, phần đề xuất và phần còn chờ công cụ/người dùng.
- Bản bàn giao có thể được chỉnh tiếp mà không phải viết lại toàn bộ.

Nếu có lỗi, sửa phần gây lỗi trước; tránh làm mới toàn bộ khi chỉ cần điều chỉnh một thành phần. Nêu lỗi còn lại nếu không thể giải quyết đáng tin cậy.

## Prompt mẫu

> Viết prompt image-to-video cho ảnh sản phẩm tôi gửi: camera tiến nhẹ trong 5 giây, ánh sáng cửa sổ, giữ nguyên hình dáng và nhãn, không thêm chữ; sản phẩm đứng yên trên bàn gỗ, chỉ có bóng lá chuyển động nhẹ ở hậu cảnh. Tách prompt chính, yếu tố cần khóa và 3 cách sửa nếu nhãn bị méo.

---

Biên soạn và watermark: [Cách Dùng AI](https://cachdungai.blog/)
