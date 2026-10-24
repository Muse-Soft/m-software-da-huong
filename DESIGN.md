# DESIGN.md — Dạ Hương, nhà hương niche

> Tài liệu chỉ đạo nghệ thuật DUY NHẤT cho landing page Dạ Hương (repo `m-software-da-huong`).
> Dev, QA và mọi lần sửa sau đều đối chiếu theo tài liệu này. Mọi số liệu, giá,
> cảm nhận khách, địa chỉ, điện thoại trong trang đều là DỮ LIỆU MẪU, trừ khi ghi
> rõ là dữ liệu thật; địa chỉ/điện thoại thật để **[CẦN BỔ SUNG]**.

## 1. Bảng màu (mã hex + vai trò từng màu)

| Màu | Vai trò | Ghi chú dùng |
| --- | --- | --- |
| `#F4EFE8` — nền ngà | Nền chính toàn trang, nền các mục sáng | Nền mặc định; chữ trên nền này dùng `#1E1B16` |
| `#12100D` — nền tối | Nền hero, nền mục macro, nền footer | Nền tối chiếm tối thiểu 40% chiều cao trang; chữ trên nền này dùng `#F4EFE8` |
| `#1E1B16` — chữ | Chữ nội dung, tiêu đề trên nền sáng | Không dùng đen tuyệt đối `#000000` |
| `#A87E3F` — vàng đồng | Điểm nhấn duy nhất: hairline, số lớn, nhãn mục, nút chính, viền ảnh | Chỉ dùng cho nhấn; không dùng vàng chói, không dùng thêm màu nhấn thứ hai |
| `#F4EFE8` trên `#12100D` | Cặp nền–chữ ngược cho mục tối | Tỷ lệ tương phản tối thiểu 7:1 cho chữ lớn, 4.5:1 cho chữ nhỏ |

Quy tắc cứng: chỉ 4 màu trên + màu trắng ngà của nền. Không thêm màu pastel,
không thêm màu neon, không gradient nhiều màu. Hairline vàng đồng dày đúng 1px,
không dùng viền dày, không dùng bóng đổ màu.

## 2. Font chữ

- **Tiêu đề: Cormorant Garamond**, serif, weight 500 (tiêu đề lớn) và 600 (số lớn).
  Cỡ tiêu đề hero: 64–80px desktop, 40px mobile. Tiêu đề mục: 40–48px desktop.
- **Nội dung: Be Vietnam Pro**, weight 400 (nội dung) và 500 (nhãn, nút).
  Cỡ nội dung: 16–17px, line-height 1.7. Nút: 15px, chữ hoa, giãn cách chữ 0.12em.
- **Nhãn mục: Be Vietnam Pro 500, chữ hoa toàn bộ, giãn cách chữ (letter-spacing)
  0.28em**, cỡ 12px, màu `#A87E3F`, luôn đi kèm một hairline vàng đồng dài 48px
  phía trên nhãn.

Không dùng font hệ thống thay thế ngoài hai font trên; không dùng font trang trí
thứ ba. Tiêu đề tiếng Việt phải giữ dấu đầy đủ, không viết hoa toàn bộ tiêu đề
(trừ nhãn mục).

## 3. Phong cách tham chiếu (MỘT tên gọi rõ)

**Trang flagship của nhà hương xa xỉ quốc tế, phong cách editorial lệch lưới**
(kiểu tạp chí thời trang in: bố cục lệch lưới, ảnh lớn tràn biên, khoảng trắng
rộng làm nhịp, typography chồng lớp). Cụ thể: ảnh là nhân vật chính, chữ là
chú thích đắt giá — không phải lưới thẻ đều, không phải banner bán hàng.

## 4. Quy tắc hình ảnh

- **Tông ảnh bắt buộc:** nền tối, ánh sáng studio gắt tạo bóng đổ mềm, khói hương
  lảng bảng, macro đồng tông điện ảnh (ấm, trầm, ít bão hòa). Ảnh sáng phẳng kiểu
  bán hàng phổ thông (nền trắng sáng đều, không bóng) BỊ CẤM.
- **Tỉ lệ khung:**
  - Ảnh hero: 4:5 dọc, đặt lệch phải, tràn lên mép trên trang.
  - Ảnh bộ sưu tập: 3:4 dọc cho 2 mùi, 1:1 cho 1 mùi (lệch nhịp cố ý).
  - Ảnh macro toàn khổ: 16:9 ngang, tràn full chiều rộng.
  - Ảnh chân dung chế tác: 1:1 vuông.
- **Ảnh mẫu:** toàn bộ ảnh trong bản demo là ảnh mẫu chất lượng cao, đồng tông
  theo quy tắc trên, khai báo rõ là ảnh mẫu trong mã nguồn và trong comment kết quả.
- **Cấm:** icon stock, icon phẳng minh họa, ảnh template, ảnh có watermark,
  ảnh lệch tông (sáng/chói/lạnh) so với tông tối–ấm đã định.

## 5. Bố cục — 7 mục, thứ tự cố định

### Mục 1 — Hero lệch phải, typography chồng lớp (nền tối `#12100D`)
- Ảnh chai hương 4:5 đặt lệch phải, chiếm 55% chiều rộng, tràn mép trên.
- Tiêu đề "Dạ Hương" (Cormorant Garamond 72px, `#F4EFE8`) chồng LÊN ảnh, lệch
  sang trái 8% chiều rộng ảnh, tạo lớp chữ–ảnh chồng nhau.
- Dòng phụ 1 câu, Be Vietnam Pro 17px, `#F4EFE8` mờ 85%: "Hương niche, chế tác
  thủ công, số lượng giới hạn." (nội dung mẫu).
- Nút chính duy nhất: viền vàng đồng 1px, chữ hoa giãn cách, nền trong suốt,
  chữ `#A87E3F`; hover: nền `#A87E3F`, chữ `#12100D`.
- Cuộn xuống: chỉ báo cuộn là một hairline dọc vàng đồng dài 64px, không dùng
  mũi tên icon.

### Mục 2 — Tuyên ngôn, khoảng trắng rộng (nền ngà `#F4EFE8`)
- Khoảng trắng trên–dưới mỗi bên tối thiểu 120px desktop.
- Một đoạn tuyên ngôn duy nhất, Cormorant Garamond 32px, căn giữa, tối đa
  2 dòng, nội dung mẫu: "Mùi hương không ồn ào. Nó ở lại sau khi người ta đã đi."
- Không ảnh, không nút, không trang trí thêm — khoảng trắng chính là thiết kế.

### Mục 3 — Bộ sưu tập 3 mùi, editorial lệch lưới (nền ngà)
- 3 mùi, mỗi mùi một tông màu riêng (ghi rõ là tên mẫu):
  1. **Dạ Trầm** — tông trầm gỗ, ảnh 3:4, đặt lệch trái, tiêu đề Cormorant 36px.
  2. **Dạ Hoa** — tông hoa trắng–vàng nhạt, ảnh 1:1, đặt lệch phải và thụt xuống
     80px so với mùi 1 (lệch nhịp).
  3. **Dạ Khói** — tông khói tối, ảnh 3:4, đặt lệch trái và thụt xuống 40px.
- Mỗi mùi: tên, 1 câu mô tả (tối đa 20 chữ), giá mẫu (ví dụ 1.850.000đ — ghi rõ
  là giá mẫu), nút "Xem mùi" viền hairline vàng đồng.
- Cấm xếp 3 mùi thành lưới 3 cột đều nhau.

### Mục 4 — Macro toàn khổ + marquee (nền tối `#12100D`)
- Ảnh macro khói hương 16:9 tràn full chiều rộng, không bo góc.
- Marquee chạy ngang phía dưới ảnh: dòng chữ hoa giãn cách rộng, Cormorant
  Garamond 28px, `#A87E3F`, nội dung lặp: "CHẾ TÁC THỦ CÔNG — SỐ LƯỢNG GIỚI HẠN — "
  (chạy chậm, 30 giây một vòng, dừng khi người dùng bật giảm chuyển động).

### Mục 5 — Số lớn chế tác (nền ngà)
- 3 con số lớn, Cormorant Garamond 600, cỡ 72px, màu `#A87E3F`, xếp hàng ngang
  với hairline vàng đồng ngăn cách (không dùng card, không dùng icon):
  - **21** — ngày ủ hương (số liệu mẫu).
  - **3** — số mùi trong bộ sưu tập đầu tiên (số liệu mẫu).
  - **100** — số chai mỗi mẻ, đánh số tay (số liệu mẫu).
- Dưới mỗi số: nhãn 1 dòng, Be Vietnam Pro 13px chữ hoa giãn cách.

### Mục 6 — Trích dẫn tối giản (nền ngà)
- Một trích dẫn khách duy nhất, căn giữa, Cormorant Garamond italic 28px,
  tối đa 2 dòng, kèm tên người nói + ghi rõ "(cảm nhận mẫu)".
- Không slider, không nhiều trích dẫn xếp chồng, không dấu ngoặc kép trang trí lớn.

### Mục 7 — Form đặt mua, chỉ giao diện (nền tối `#12100D`)
- Tiêu đề "Đặt mua" + nhãn mục vàng đồng theo quy tắc mục 2.
- Form 4 trường: họ tên, số điện thoại, mùi muốn đặt, số lượng.
- Form CHỈ chạy phía giao diện, không gửi dữ liệu thật; ngay dưới nút gửi ghi rõ
  dòng: "Bản demo — form chưa gửi dữ liệu thật."
- Dưới form: địa chỉ và điện thoại để **[CẦN BỔ SUNG]** (không bịa số thật).

## 6. Nhịp, khoảng trắng, responsive

- Khoảng cách giữa các mục: tối thiểu 96px desktop, 56px mobile.
- Chiều rộng nội dung tối đa 1200px, căn giữa; ảnh tràn biên được phép vượt
  khung này ở mục 1 và mục 4.
- Mobile (dưới 768px): hero chuyển thành ảnh trên–chữ dưới, tiêu đề 40px;
  bộ sưu tập xếp dọc, giữ nguyên lệch thụt (40px thay vì 80px); marquee giữ nguyên.
- Không dùng hiệu ứng chuyển động mạnh; chuyển động duy nhất là marquee mục 4
  và hover nút (đổi màu, 200ms).

## 7. Danh sách cấm (QA đối chiếu trực tiếp)

1. Không mô tả chung chung "đẹp, hiện đại" — mọi quyết định phải có thông số.
2. Không template, không icon stock, không lưới thẻ đều.
3. Không ảnh sáng phẳng kiểu bán hàng phổ thông.
4. Không thêm màu ngoài 4 màu mục 1.
5. Không font thứ ba.
6. Không bịa địa chỉ, điện thoại, giá thật — chỗ nào chưa có dữ liệu thật phải
   là **[CẦN BỔ SUNG]** hoặc ghi rõ là mẫu.
7. Không form gửi dữ liệu thật — form chỉ giao diện, có dòng ghi rõ bản demo.
