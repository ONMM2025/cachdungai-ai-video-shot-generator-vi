# Thiết kế shot video AI

Chuyển một cảnh thành prompt video rõ chủ thể, một hành động, camera, ánh sáng, chuyển động và giới hạn lỗi.

## Skill này giúp gì?

Skill chuyên thiết kế một shot có thể tạo được, thay vì biến một câu mô tả thành prompt dài không kiểm soát. Nó phân biệt ảnh đầu vào với chuyển động cần sinh, khóa chi tiết quan trọng, chỉ định camera và đưa ra cách sửa khi video bị sai hình, sai chuyển động hoặc không liên tục.

## Nội dung gói

- `SKILL.md`: quy trình chi tiết, đầu vào, đầu ra và tiêu chí tự kiểm tra.
- `README.md`: hướng dẫn cài và prompt bắt đầu.
- `LICENSE`: giấy phép MIT.

## Cách cài và dùng

1. Tải ZIP rồi giải nén; giữ nguyên thư mục có `SKILL.md`.
2. Mở phần Skills/Agent Skills của ứng dụng AI đang dùng và thêm thư mục hoặc tải gói theo hướng dẫn trong ứng dụng. Nếu ứng dụng chưa hỗ trợ nạp skill, dán nội dung `SKILL.md` vào chỉ dẫn của một cuộc trò chuyện/dự án và dùng prompt mẫu bên dưới.
3. Bắt đầu cuộc trò chuyện bằng mục tiêu, người xem, nền tảng, giới hạn và tệp tham chiếu bạn có quyền sử dụng. Không gửi mật khẩu, mã xác minh, token hoặc dữ liệu khách hàng không cần thiết.
4. Đọc phần **Giả định** và **Cần người dùng duyệt**. Kiểm tra kỹ quyền dùng tài nguyên, dữ liệu, giá và quy định hiện hành trước khi tạo tệp tốn phí hoặc đăng công khai.
5. Lặp lại bằng cách nêu một thay đổi cụ thể; yêu cầu Agent giữ nguyên những phần đã duyệt.

Cách nạp skill khác nhau giữa ứng dụng và tài khoản. Hãy làm theo giao diện hiện hành của ChatGPT, Claude hoặc Agent khác; đừng giả định một nút cài đặt giống nhau có ở mọi gói.

## Prompt bắt đầu

> Viết prompt image-to-video cho ảnh sản phẩm tôi gửi: camera tiến nhẹ trong 5 giây, ánh sáng cửa sổ, giữ nguyên hình dáng và nhãn, không thêm chữ; sản phẩm đứng yên trên bàn gỗ, chỉ có bóng lá chuyển động nhẹ ở hậu cảnh. Tách prompt chính, yếu tố cần khóa và 3 cách sửa nếu nhãn bị méo.

## Tác giả và watermark

Biên soạn: [cachdungai.blog](https://cachdungai.blog/)

Gói được phân phối miễn phí theo điều khoản trong `LICENSE`. Kết quả tạo media có thể cần công cụ, tài khoản hoặc chi phí riêng; hãy duyệt đầu ra trước khi dùng công khai.
