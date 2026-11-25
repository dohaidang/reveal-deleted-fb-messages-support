# Chính sách quyền riêng tư — Reveal Deleted FB Messages

**Cập nhật lần cuối:** 24/11/2026

## Tóm tắt

Tiện ích này lưu một bản chụp nội dung tin nhắn Facebook Messenger **trên
chính trình duyệt của bạn** để có thể hiển thị lại khi tin nhắn bị gỡ hoặc
thu hồi. Dữ liệu **không rời khỏi thiết bị của bạn**: không có máy chủ, không
tài khoản, không phân tích, không quảng cáo, không bên thứ ba.

## Dữ liệu tiện ích xử lý

Khi bạn mở một cuộc trò chuyện trên `facebook.com` hoặc `messenger.com`, tiện
ích đọc nội dung các bong bóng tin nhắn đang hiển thị trên màn hình và lưu lại:

- Nội dung văn bản của tin nhắn
- Ảnh trong tin nhắn (có thể tắt trong phần Cài đặt)
- Video, âm thanh và file đính kèm (txt, doc, docx, xls, xlsx, pdf, ...)
  khi dung lượng nằm trong giới hạn bên dưới
- Tên người gửi, mốc thời gian hiển thị và loại cuộc trò chuyện (cá nhân hoặc
  nhóm)
- Mã định danh nội bộ của tin nhắn và của cuộc trò chuyện
  (`data-message-id`)

Ngoài ra, để hiển thị tài khoản đang dùng trong cửa sổ pop-up, tiện ích đọc
**tên, UID và ảnh đại diện** của tài khoản Facebook bạn đang đăng nhập. UID
được lấy từ cookie `c_user` của trang, chỉ để nhận diện tài khoản và không
được gửi đi đâu.

Tiện ích **không** đọc mật khẩu, danh bạ, cuộc gọi hay nội dung bài viết, và
không xử lý các trang web khác ngoài `facebook.com` và `messenger.com`.

## Nơi lưu trữ

- **Tin nhắn và tệp đính kèm:** lưu trong **IndexedDB của trình duyệt**, cục
  bộ trên máy bạn.
- **Cài đặt và thông tin tài khoản (tên, UID, ảnh đại diện):** lưu trong
  `chrome.storage.local`, cũng cục bộ.

Tiện ích không gửi dữ liệu tới máy chủ của nhà phát triển hay bất kỳ bên thứ
ba nào. Với ảnh, video và file có địa chỉ tạm thời của Facebook, tiện ích tải
lại chính nội dung đó từ CDN của Facebook (`fbcdn.net`, `fbsbx.com`) để lưu
thành bản sao cục bộ trước khi địa chỉ tạm hết hạn. Việc tải này gửi trực
tiếp từ trình duyệt của bạn tới Facebook, không qua trung gian và không kèm
cookie.

## Bạn kiểm soát dữ liệu

Trong phần Cài đặt của tiện ích (biểu tượng bánh răng trong cửa sổ pop-up):

- **Tạm dừng ghi** bất cứ lúc nào: tiện ích sẽ không lưu thêm gì.
- **Tắt lưu ảnh**: chỉ lưu văn bản.
- **Tự xoá sau** 7 / 30 / 90 ngày, hoặc không bao giờ.
- **Xóa tất cả**: xoá sạch toàn bộ dữ liệu đã lưu ngay lập tức.

Tiện ích tự giới hạn dung lượng: tối đa 1.000 tin hoặc 50 MB, mỗi ảnh khoảng
5 MB và mỗi video hoặc file khoảng 18 MB. Khi vượt quá, các bản ghi cũ nhất
được xoá trước.

Gỡ tiện ích khỏi Chrome sẽ xoá toàn bộ dữ liệu nó đã lưu.

## File log chẩn đoán

Khi bạn nhấn **Alt + Shift + D** trên Facebook hoặc Messenger, tiện ích tạo một
file log (`rvdfm-log-....log`) và lưu vào thư mục Tải xuống của bạn để bạn đính
kèm khi báo lỗi. File chỉ chứa thông tin kỹ thuật: phiên bản tiện ích và trình
duyệt, các cài đặt, số lượng tin đã lưu, số bong bóng và thông báo đang hiện
trên màn hình, cùng các sự kiện và lỗi gần đây của tiện ích. File **không chứa**
nội dung tin nhắn, tên người, mã định danh hay đường dẫn. File chỉ được tạo khi
bạn chủ động nhấn phím tắt, và **không bao giờ được tự động gửi đi**. Bạn tự
quyết định có đính kèm nó vào báo lỗi công khai hay không.

## Chia sẻ dữ liệu

Không. Dữ liệu không được bán, không được chia sẻ, không được truyền tới bất
kỳ đâu.

## Quyền hạn tiện ích yêu cầu

| Quyền | Lý do |
|---|---|
| `storage` | Lưu cài đặt và thông tin tài khoản đang dùng |
| Truy cập `facebook.com`, `messenger.com` | Đọc nội dung tin nhắn trên trang để chụp lại, và hiện nút xem lại tin đã gỡ |
| Truy cập `fbcdn.net`, `fbsbx.com` | Tải ảnh, video, file Messenger về IndexedDB cục bộ trước khi địa chỉ tạm hết hạn |

Tiện ích cũng chạy một đoạn mã nhỏ trong chính trang Facebook để chụp ảnh và
video dạng `blob:` (thường gặp ở Messenger mã hóa đầu cuối) trước khi
chúng bị Facebook thu hồi. Đoạn mã này chỉ chuyển dữ liệu trong cùng thẻ
trình duyệt, không gửi ra ngoài.

## Giới hạn

Tiện ích chỉ khôi phục được nội dung mà nó **đã nhìn thấy** trên màn hình
trước khi bị gỡ. Nó không giải mã, không phá mã hóa của Facebook, và không
thể lấy lại tin nhắn chưa từng xuất hiện trên màn hình của bạn.

## Liên hệ

Mọi thắc mắc: dangdohai.work@gmail.com

## Miễn trừ trách nhiệm

Tiện ích này không liên kết với Meta / Facebook. Việc sử dụng cần tuân thủ
điều khoản dịch vụ của Facebook. Bạn tự chịu trách nhiệm về cách sử dụng nội
dung được khôi phục.
