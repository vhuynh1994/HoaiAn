# 💌 Gửi Hoài An

Một trang web tỏ tình nhỏ, gồm 5 màn:

1. **Phong thư** có dấu sáp hình trái tim. Chạm vào để mở.
2. **Lá thư** tự viết ra từng chữ như đang viết tay. Chạm vào thư để hiện hết ngay.
3. **Những điều thích ở người ấy**, mỗi lần bấm hiện thêm một điều.
4. **Câu hỏi**: *"Hoài An ơi, làm người yêu anh nhé?"*. Nút **Không** sẽ chạy trốn, nút **Đồng ý** thì to dần 😝
5. **Pháo hoa trái tim** khi đồng ý, kèm *ngày đầu tiên của chúng mình* và nút **nhắn Zalo** cho anh.

Nhạc nền piano + hộp nhạc bắt đầu nhẹ nhàng ngay khi mở phong thư.

Trang chỉ có một file `index.html`: không cần cài gì, không cần build, xem tốt trên cả điện thoại lẫn máy tính.

## Xem thử

Mở file `index.html` bằng trình duyệt (bấm đúp vào file là được).

## Sửa nội dung

Toàn bộ chữ trên trang nằm trong khối `CONFIG` ở **đầu file `index.html`**:

| Mục | Ý nghĩa |
| --- | --- |
| `name` | Tên người nhận (mặc định `Hoài An`) |
| `me` / `you` | Cách xưng hô, đang để `anh` / `em` (có thể đổi thành `tớ` / `cậu`…) |
| `signature` | Tên người gửi để ký cuối thư. Để trống sẽ ký *"Người luôn nghĩ về em"* |
| `letter` | Nội dung lá thư (xuống dòng bằng Enter) |
| `reasons` | Danh sách những điều bạn thích ở người ấy. Để `[]` nếu muốn bỏ qua màn này |
| `noTexts` | Các câu nút "Không" lần lượt đổi sang mỗi lần chạy trốn |
| `replyLink` | Link để người ấy nhắn lại ngay, đang để Zalo `https://zalo.me/0339655414`. Để trống `""` sẽ ẩn nút |
| `music` | File nhạc nền, đang để `music.mp3`. Để trống `""` sẽ tắt nhạc |

Trong các đoạn chữ có thể dùng `{name}`, `{me}`, `{you}`. Viết hoa chữ đầu (`{Me}`, `{You}`) khi đứng đầu câu.

### Nhạc nền

`music.mp3` là một bản nhạc không lời **sáng tác riêng cho trang này** (piano và hộp nhạc, giọng Đô trưởng, khoảng 1 phút 40 giây, tự lặp lại). Vì là bản gốc nên không vướng bản quyền, đăng công khai thoải mái.

Nhạc bắt đầu khi người ấy chạm mở phong thư, âm lượng tăng dần trong 3 giây. Góc phải dưới có nút ♪ để bật/tắt.

Muốn dùng bài hát khác thì chép file mp3 của bạn đè lên `music.mp3` (hoặc đặt tên khác rồi sửa `music` trong `CONFIG`). Lưu ý: bài hát có bản quyền mà đăng công khai thì có thể bị GitHub gỡ.

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
