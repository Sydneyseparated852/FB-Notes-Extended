# FB Notes Extended

[English Version](./README.en.md)

Tiện ích Chrome cho phép viết ghi chú Facebook dài, cắt nhạc, nghe thử và tuỳ chỉnh thời hạn hiển thị.

## Có gì mới ở bản 1.1.0

- **Cắt nhạc & nghe thử:** Chọn đoạn 30 giây bất kỳ của bài hát để đính kèm vào ghi chú, kéo thả trực quan dạng sóng âm thanh, nghe thử ngay trong popup.
- **Phát nhạc trực tiếp:** Có thể phát/preview nhạc ngay từ kết quả tìm kiếm.
- **Giao diện mới:** Thêm nút phát/tạm dừng/lưu, thanh cuộn đẹp hơn, chọn nhạc dễ hơn.
- **Giới hạn nội dung:** Nội dung ghi chú tối đa 600 ký tự (tương thích tốt hơn với Facebook).
- **Sửa lỗi & mượt hơn:** Trải nghiệm chọn nhạc, bạn bè, xử lý lỗi tốt hơn.

## Tính năng

- **Vượt giới hạn 60 ký tự:** Viết ghi chú dài tới 600 ký tự (giới hạn API Facebook cho note có nhạc)
- **Thời hạn tuỳ chỉnh:** Chọn thời gian hiển thị từ 1 giờ đến 8 ngày, hoặc nhập số phút tuỳ ý
- **Chọn đối tượng:** Công khai, bạn bè, danh bạ, hoặc tuỳ chỉnh danh sách bạn bè
- **Đính kèm & cắt nhạc:** Thêm bài hát, chọn đoạn 30s, nghe thử trước khi chia sẻ
- **Giao diện tối:** Thiết kế tối giản, dễ nhìn
- **Đa ngôn ngữ:** Hỗ trợ Tiếng Việt và English

<img src="screenshots/image.png" width="300" alt="screenshot"/>

## Cài đặt

### Cách 1: Tải extension đã build sẵn (Khuyên dùng)

1. Tải file `FB-Notes-Extended.zip` từ [Releases](https://github.com/DuckCIT/FB-Notes-Extended/releases)
2. Giải nén file zip vào một thư mục bất kỳ
3. Mở Chrome, truy cập `chrome://extensions/`
4. Bật **Chế độ dành cho nhà phát triển** (Developer mode) ở góc trên bên phải
5. Nhấn **Tải tiện ích đã giải nén** (Load unpacked)
6. Chọn thư mục vừa giải nén
7. Extension đã sẵn sàng sử dụng!

### Cách 2: Build từ source

Yêu cầu: Node.js 18+

1. Clone repository về máy
2. Mở terminal tại thư mục project
3. Chạy `npm install` để cài đặt dependencies
4. Chạy `npm run build` để build extension
5. Load thư mục `dist` như extension unpacked trong Chrome

## Hướng dẫn sử dụng

### Tạo ghi chú mới

1. Mở [Facebook](https://facebook.com) và đăng nhập
2. Nhấn vào icon extension trên thanh công cụ Chrome
3. Viết nội dung ghi chú (tối đa 600 ký tự)
4. Chọn các tuỳ chọn:
   - **Đối tượng:** Công khai, Bạn bè, Danh bạ, hoặc Tuỳ chỉnh
   - **Thời hạn:** 1h, 6h, 24h, 3d, hoặc nhập số phút tuỳ ý (tối đa 8 ngày)
   - **Nhạc:** Tìm kiếm, nghe thử, cắt đoạn và chọn bài hát để đính kèm
5. Nhấn **Chia sẻ**

### Xoá ghi chú hiện tại

Khi đã có ghi chú đang hiển thị, nút xoá (biểu tượng thùng rác) sẽ xuất hiện ở góc trên bên phải của popup. Nhấn vào để xoá ghi chú hiện tại.

## Lưu ý

- Extension chỉ hoạt động khi bạn đang ở trang facebook.com
- Giới hạn ký tự thực tế là 600 (do giới hạn API Facebook cho note có nhạc)
- Thời hạn tối đa có thể vượt quá 3 ngày nếu nhập số phút tùy ý

## Cấu trúc project

```
├── dist/                  # Extension đã build (load folder này vào Chrome)
├── public/
│   ├── icons/            # Icons của extension
│   └── manifest.json     # Chrome extension manifest
├── src/
│   ├── background/       # Service worker xử lý API calls
│   ├── content/          # Content script
│   ├── lib/              # Utilities
│   └── popup/            # Popup UI (React)
├── popup.html
├── package.json
├── tsconfig.json
└── vite.config.ts
```

## Development

- `npm install` - Cài đặt dependencies
- `npm run dev` - Development mode với hot reload
- `npm run build` - Production build

## Đóng góp

Mọi đóng góp đều được chào đón! Vui lòng tạo Pull Request hoặc Issue trên GitHub.

## Giấy phép

MIT License

---

**English Version**: [README.en.md](./README.en.md)
