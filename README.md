# bandoquyhoachhanoidemo
## Đã sửa lỗi

- Thêm Tailwind CSS v4 vào `src/index.css`; trước đó project có plugin Tailwind nhưng CSS không import Tailwind nên phần lớn class giao diện không được sinh ra.
- Sửa CSS mặc định của Vite (`display:flex`, `place-items:center`, dark color scheme) gây sai kích thước/căn giữa toàn trang bản đồ.
- Sửa đường dẫn các file GeoJSON trong `public/` để hoạt động đúng khi deploy với Vite `base` khác `/`.
- Sửa race condition khi đổi lớp bản đồ trước khi MapLibre hoàn tất tải style; trạng thái lớp và opacity sẽ được áp dụng lại sau `load`.
- Bổ sung xử lý lỗi MapLibre và dọn `mapRef` khi component unmount.
- Loại `node_modules` khỏi source bàn giao; cài dependency mới bằng `npm install` thay vì dùng thư mục `node_modules` lỗi/không đầy đủ trong file nén ban đầu.

## Chạy project

```bash
npm install
npm run dev
```

Build production:

```bash
npm run build
```
