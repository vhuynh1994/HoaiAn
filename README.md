# 💌 Gửi Hoài An

Một trang web tỏ tình nhỏ, gồm 5 màn:

1. **Phong thư** có dấu sáp hình trái tim. Chạm vào để mở.
2. **Lá thư** tự viết ra từng chữ như đang viết tay. Chạm vào thư để hiện hết ngay.
3. **Những điều thích ở người ấy**, mỗi lần bấm hiện thêm một điều.
4. **Câu hỏi**: *"Hoài An ơi, làm người yêu tớ nhé?"*. Nút **Không** sẽ chạy trốn, nút **Đồng ý** thì to dần 😝
5. **Pháo hoa trái tim** khi đồng ý, kèm *ngày đầu tiên của chúng mình*.

Trang chỉ có một file `index.html`: không cần cài gì, không cần build, xem tốt trên cả điện thoại lẫn máy tính.

## Xem thử

Mở file `index.html` bằng trình duyệt (bấm đúp vào file là được).

## Sửa nội dung

Toàn bộ chữ trên trang nằm trong khối `CONFIG` ở **đầu file `index.html`**:

| Mục | Ý nghĩa |
| --- | --- |
| `name` | Tên người nhận (mặc định `Hoài An`) |
| `me` / `you` | Cách xưng hô, mặc định `tớ` / `cậu`. Muốn xưng anh – em thì đổi thành `anh` / `em` |
| `signature` | Tên người gửi để ký cuối thư. Để trống sẽ ký *"Người luôn nghĩ về cậu"* |
| `letter` | Nội dung lá thư (xuống dòng bằng Enter) |
| `reasons` | Danh sách những điều bạn thích ở người ấy. Để `[]` nếu muốn bỏ qua màn này |
| `noTexts` | Các câu nút "Không" lần lượt đổi sang mỗi lần chạy trốn |
| `replyLink` | Link Messenger/Zalo để người ấy nhắn lại ngay, vd `https://m.me/ten-cua-ban` hoặc `https://zalo.me/09xxxxxxxx`. Để trống sẽ ẩn nút |
| `music` | Nhạc nền (xem bên dưới) |

Trong các đoạn chữ có thể dùng `{name}`, `{me}`, `{you}`. Viết hoa chữ đầu (`{Me}`, `{You}`) khi đứng đầu câu.

### Thêm nhạc nền

1. Bỏ một file nhạc, ví dụ `music.mp3`, vào cùng thư mục với `index.html`.
2. Sửa `music: "music.mp3"` trong `CONFIG`.

Nhạc bắt đầu phát khi người ấy chạm mở phong thư. Góc phải dưới sẽ có nút ♪ để bật/tắt.

## Đăng lên mạng bằng GitHub Pages (miễn phí)

1. Vào repo trên GitHub → **Settings** → **Pages**.
2. Ở mục **Build and deployment**, chọn **Source: Deploy from a branch**.
3. Chọn nhánh chứa code (ví dụ `main` hoặc `claude/epic-thompson-volgy0`), thư mục **`/ (root)`**, rồi bấm **Save**.
4. Đợi 1–2 phút, trang sẽ có ở: **https://vhuynh1994.github.io/HoaiAn/**

> ⚠️ Với tài khoản GitHub miễn phí, GitHub Pages chỉ chạy khi repo để **Public**. Như vậy ai biết repo cũng đọc được nội dung thư.

### Ảnh xem trước khi gửi link

Khi dán link vào Messenger/Zalo sẽ hiện ảnh `preview.png` và tiêu đề *"Gửi Hoài An 💌"*. Nếu đổi tên người nhận hoặc dùng tên miền khác, nhớ sửa các thẻ `<title>` và `og:*` ở đầu `index.html`, rồi chụp lại `preview.png` (kích thước 1200×630).

## Chi tiết nhỏ

- Ngày bấm **Đồng ý** lần đầu được lưu trong trình duyệt của người ấy. Những lần mở lại sau trên cùng máy, trang sẽ hiện *"Đã bên nhau N ngày 💗"*.
- Ở màn cuối, chạm vào bất kỳ chỗ nào trên màn hình sẽ bắn thêm trái tim.
- Máy đang bật chế độ *giảm chuyển động* (reduce motion) thì hiệu ứng sẽ được giảm bớt.

Chúc bạn thành công! 💖
