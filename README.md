# Reveal Deleted FB Messages

Reveal Deleted FB Messages là extension dành cho Chrome, giúp bạn lưu và xem lại những tin nhắn đã bị gỡ hoặc thu hồi trên Facebook Messenger.

> Repo này chỉ dùng để **hỗ trợ và nhận báo lỗi**. Mã nguồn của extension không được công khai.

## Tính năng

- Lưu lại tin nhắn văn bản trước khi người gửi thu hồi.
- Lưu và xem lại ảnh, video, âm thanh và file đính kèm đã bị gỡ.
- Hoạt động với cuộc trò chuyện cá nhân, nhóm và Messenger mã hóa đầu cuối.
- Tổng hợp các tin đã thu hồi trong popup để tìm kiếm và xem lại.
- Giao diện sáng và tối, tiếng Việt và tiếng Anh.
- Lưu dữ liệu ngay trên thiết bị của bạn, không gửi nội dung tin nhắn đến máy chủ bên ngoài.

## Cài đặt

Cài đặt từ Chrome Web Store. Liên kết sẽ được cập nhật tại đây khi extension được duyệt.

## Cách sử dụng

1. Mở Facebook hoặc Messenger và sử dụng các cuộc trò chuyện như bình thường.
2. Để extension có thể lưu tin, cuộc trò chuyện và tin nhắn cần được hiển thị trên màn hình trước khi bị thu hồi.
3. Khi một tin nhắn bị gỡ, nút hình con mắt sẽ xuất hiện cạnh thông báo thu hồi. Bấm vào nút này để xem lại nội dung đã lưu.
4. Bấm vào biểu tượng extension trên thanh công cụ Chrome để xem danh sách tất cả tin nhắn đã thu hồi.
5. Trong popup, bạn có thể tìm kiếm theo tên người gửi hoặc nội dung, chuyển giữa tin nhắn cá nhân và nhóm, mở lại nội dung hoặc xóa dữ liệu đã lưu.

Extension không thể khôi phục những tin đã bị gỡ trước khi được cài đặt hoặc trước khi nội dung đó xuất hiện trên màn hình. Với file và video dung lượng lớn, khả năng xem lại phụ thuộc vào việc dữ liệu đã được lưu thành công trước khi liên kết của Facebook hết hạn.

## Quyền riêng tư

Toàn bộ dữ liệu được lưu trên máy bạn. Xem chi tiết tại [Chính sách quyền riêng tư](PRIVACY.md).

## Báo lỗi

Nếu extension không lưu được tin, không hiện nút con mắt hoặc hoạt động sai, bạn có thể báo lỗi ở đây. Đã có sẵn biểu mẫu, bạn chỉ cần điền thông tin:

**[Báo lỗi trên GitHub](https://github.com/dohaidang/reveal-deleted-fb-messages-support/issues/new?template=bug_report.yml)**

Để mình sửa lỗi nhanh hơn, bạn hãy cho biết:

- Loại nội dung bị lỗi (văn bản, ảnh, video, âm thanh, file) và loại cuộc trò chuyện (cá nhân, nhóm, mã hóa đầu cuối).
- Các bước để tái hiện lỗi, ví dụ "người kia gửi ảnh rồi thu hồi, bấm nút con mắt thì báo không tìm thấy".
- Phiên bản extension (xem trong `chrome://extensions`) và phiên bản Chrome (xem trong `chrome://version`).

**Cách lấy file log (nhanh nhất):**

1. Ngay tại tab Facebook hoặc Messenger vừa bị lỗi, nhấn **`Alt` + `Shift` + `D`**.
2. Trình duyệt sẽ tải về một file có tên dạng `rvdfm-log-20261124-153000.log` và hiện thông báo ở cuối màn hình.
3. Kéo file đó vào biểu mẫu báo lỗi trên GitHub (ô "File log").

File log chỉ chứa thông tin kỹ thuật: phiên bản extension và Chrome, các cài đặt, số lượng tin đã lưu, số bong bóng và thông báo đang hiện trên màn hình, cùng các sự kiện và lỗi gần đây của extension. **Không có nội dung tin nhắn, tên người, ID hay đường dẫn.** File chỉ được lưu vào máy bạn, không tự gửi đi đâu. Bạn có thể mở bằng Notepad để kiểm tra trước khi đăng.

**Lưu ý riêng tư:** issue trên GitHub là công khai. Vui lòng không dán nội dung tin nhắn, tên hoặc ảnh của người khác. Hãy che hoặc thay bằng nội dung giả trước khi gửi. Nếu không muốn công khai, bạn có thể gửi email trực tiếp cho mình ở mục bên dưới.

## Hỗ trợ và liên hệ

Nếu bạn cần hỗ trợ hoặc có bất kỳ thắc mắc nào, hãy liên hệ với mình qua email [dangdohai.work@gmail.com](mailto:dangdohai.work@gmail.com).

Nếu thấy extension này hữu ích với bạn, hãy tặng mình một ⭐ trên GitHub. Và nếu có thể, bạn có thể mời mình một cốc cà phê bằng cách quét mã QR bên dưới. Cảm ơn bạn rất nhiều!

<p align="center">
  <img src="docs/donate-qr.png" alt="Mã QR TPBank - Do Hai Dang" width="260">
</p>

## Miễn trừ trách nhiệm

Extension này là sản phẩm độc lập, không liên kết, không được tài trợ hay xác nhận bởi Meta hoặc Facebook. Việc sử dụng cần tuân thủ điều khoản dịch vụ của Facebook. Bạn tự chịu trách nhiệm về cách sử dụng nội dung được khôi phục.
