# Photobooth Studio — Gian trưng bày 3D

Mô phỏng 3D gian photobooth **"Lưu Dấu Kỷ Niệm"** phục vụ triển lãm kỷ niệm
**20 năm thành lập Trường Đại học Kiến trúc Đà Nẵng (2006 – 2026)**.

Dự án mô phỏng toàn bộ gian hàng và diễn lại quy trình một lượt khách vào chụp ảnh:
từ lúc chạm màn hình kiosk, tạo dáng, đếm ngược, chụp, quét QR nhận ảnh,
cho tới khi máy in nhả tờ ảnh kỷ niệm.

Mục đích: **trình bày ý tưởng cho ban tổ chức duyệt** trước khi thi công thật.

---

## Xem thử

Mở trực tiếp trong trình duyệt, không cần cài đặt:

| Bản | File | Nội dung |
|---|---|---|
| **Chính** | [`gian-photobooth-20-nam-3d.html`](gian-photobooth-20-nam-3d.html) | Gian 3D đầy đủ: backdrop, tường trưng bày, máy in, hoạt cảnh 6 bước |
| Rút gọn | [`mo-phong-photobooth-3d.html`](mo-phong-photobooth-3d.html) | Chỉ cảnh chụp 3D, chưa có gian hàng |
| Sơ đồ | [`mo-phong-photobooth.html`](mo-phong-photobooth.html) | Bản vẽ 2D: mặt cắt ngang + mặt bằng bố trí |

> Cần kết nối mạng ở lần mở đầu để tải thư viện Three.js từ CDN.

Nếu bật **GitHub Pages** (Settings → Pages → Branch `main` / `root`),
trang sẽ chạy trực tiếp tại `https://niitbeo.github.io/photobooth-studio/`.

---

## Quy trình vận hành — 6 bước

Hoạt cảnh tự chạy lặp lại, mỗi vòng khoảng 22 giây.

| Bước | Diễn biến | Màn hình kiosk |
|---|---|---|
| 1 | Khách chạm màn hình để bắt đầu, chọn khung ảnh | `CHẠM ĐỂ BẮT ĐẦU ♡` |
| 2 | Cả nhóm lùi về vạch "Đứng tại đây", tạo dáng | Đếm ngược `3 · 2 · 1` |
| 3 | Đèn flash sáng, máy chụp, khách xem lại ảnh | Ảnh vừa chụp + `Đẹp quá ✓` |
| 4 | Khách quét mã QR để nhận ảnh về điện thoại | Mã QR |
| 5 | Máy in nhả tờ ảnh ra khay (~12 giây/tấm) | `ĐANG IN ẢNH` + thanh tiến trình |
| 6 | Khách cầm tờ ảnh kỷ niệm ra về | Quay lại màn hình chờ |

---

## Điều khiển

**Chuột**

- Kéo chuột — xoay quanh gian hàng
- Lăn chuột — phóng to / thu nhỏ
- Bấm ảnh mẫu góc trên phải — phóng to ảnh kiosk thật để đối chiếu

**Thanh dưới màn hình**

| Nút | Tác dụng |
|---|---|
| Góc 3/4 · Mặt trước kiosk · Từ camera kiosk · Mặt tiền gian · Tường hành trình · Từ trên xuống | Chuyển nhanh 6 góc nhìn dựng sẵn |
| Tạm dừng / Chạy tiếp | Dừng hoạt cảnh để xem kỹ |
| Chạy lại | Về bước 1 |
| Ẩn giao diện | Ẩn toàn bộ chữ và nút để chụp màn hình sạch (phím tắt `H`) |
| Ảnh mẫu | Bật / tắt khung ảnh kiosk thật |
| Vùng chụp | Hiện hình nón thể hiện khung hình camera bắt được |
| Kích thước | Hiện các đường kích thước gian hàng |

**Thanh 5 bước phía trên** — bấm vào bước nào để nhảy thẳng tới bước đó.

---

## Thông số gian hàng

| Hạng mục | Kích thước đề xuất |
|---|---|
| Kích thước gian | 6,0 m × 5,0 m, cao 3,0 m |
| Backdrop chụp ảnh | 3,6 m × 2,7 m, viền LED |
| Kiosk → vạch đứng chụp | ≈ 2,0 m (2–4 người); 2,5–3,0 m cho nhóm 5–6 người |
| Người → backdrop | ≈ 0,7 – 1,1 m (tránh đổ bóng lên backdrop) |
| Camera trên đầu mascot | cao ≈ 1,9 m, chúc xuống 3–5° |
| Màn hình cảm ứng | tâm màn hình cao ≈ 1,3 m |
| Ánh sáng | 2 đèn LED đứng hai bên kiosk + đèn rọi trên xà |
| Máy in ảnh | Bục cao 0,85 m đặt bên trái kiosk, khổ ảnh 10 × 15 cm |
| Lối vào | Bên phải, cọc dây chắn cho hàng chờ |

---

## Bố trí trong gian

```
                    ┌──────────── TƯỜNG SAU (lam đỏ) ────────────┐
   Tường trái       │        ┌──────────────────────┐            │   Tường phải
  HÀNH TRÌNH        │  🎈    │  BACKDROP 3,6 × 2,7  │    🎈      │  ĐỒ ÁN SINH VIÊN
    20 NĂM          │        └──────────────────────┘            │   + bục mô hình
 2006→2026          │             👤 👤 👤  ← vạch đứng          │
                    │                                            │
                    │   🖨 máy in      🤖 KIOSK      💡          │
                    │                                            │
   số "20" 3D       └──── BẢNG HIỆU MẶT TIỀN ─────  🚧 hàng chờ ─┘
```

---

## Cấu trúc thư mục

```
photobooth-studio/
├── index.html                      # Chuyển hướng sang bản chính
├── gian-photobooth-20-nam-3d.html  # BẢN CHÍNH — gian 3D đầy đủ
├── mo-phong-photobooth-3d.html     # Bản 3D rút gọn, chỉ cảnh chụp
├── mo-phong-photobooth.html        # Bản 2D: mặt cắt + mặt bằng
├── assets/
│   └── kiosk-goc.png               # Ảnh thiết kế kiosk gốc (đã duyệt)
└── README.md
```

Mỗi file HTML là **một file độc lập**: toàn bộ mô hình 3D, hình ảnh và hoạt cảnh
đều nằm trong file. Gửi file cho ai họ mở cũng chạy được, không cần kèm thư mục.

---

## Công nghệ

- [Three.js](https://threejs.org/) r128 (tải từ CDN jsDelivr) — dựng và đổ bóng cảnh 3D
- `OrbitControls` — xoay / zoom bằng chuột
- Toàn bộ vật thể dựng bằng hình khối cơ bản, không dùng file model ngoài
- Chữ trên backdrop, bảng hiệu, màn hình kiosk, tờ ảnh in đều vẽ bằng
  HTML Canvas rồi đắp lên vật thể, nên **sửa nội dung chỉ cần sửa code, không cần phần mềm đồ hoạ**

---

## Chạy tại máy

Mở thẳng file `.html` bằng trình duyệt là đủ. Nếu muốn chạy qua máy chủ cục bộ:

```bash
python -m http.server 8765
```

Rồi mở `http://localhost:8765/`.

---

## Cần xác nhận trước khi thi công

Các thông tin dưới đây là **ước lượng**, cần đối chiếu thực tế:

- **Năm thành lập 2006** — cần xác nhận lại với nhà trường
- **Kích thước gian 6 × 5 m** — cần đo theo mặt bằng thật của khu triển lãm
- **Khoảng cách kiosk → người 2,0 m** — phụ thuộc tiêu cự ống kính máy ảnh sẽ dùng
- **Thời gian in 12 giây/tấm** — theo máy in nhiệt phổ thông, cần kiểm tra theo máy thực tế
- **Ảnh tư liệu trên tường hành trình** — hiện là ô trống, chờ ảnh thật từ nhà trường

---

## Ghi chú

Mô hình 3D trong dự án dựng bằng khối hình đơn giản, dùng để **duyệt bố cục,
kích thước và màu sắc**. Đây không phải bản render thật để in ấn.
Muốn có phối cảnh chân thực, chụp màn hình góc ưng ý (bấm *Ẩn giao diện* trước khi chụp)
rồi đưa vào công cụ tạo ảnh AI cùng ảnh kiosk gốc trong `assets/`.

---

*Thiết kế cho Trường Đại học Kiến trúc Đà Nẵng — Kiến tạo không gian · Kiến tạo tương lai*
