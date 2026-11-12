# Bài nộp LAB5 — T3 Du lịch · Nhóm NORMALDAY

**Lớp:** L3A · **Bàn / zone:** ____ · **Track:** T3 — Du lịch (Trợ lý đổi chuyến khi chuyến bay bị huỷ)

| Họ và Tên | Mã Học Viên | Việc đã làm |
|---|---|---|
| Nguyễn Hà Anh | 2A202603605 | Phụ trách **§1 (Lát cắt & Phạm vi)** và **§4 (Mức tự chủ của 5 tool)** |
| Trần Xuân Trường | 2A202603617 | Phụ trách **§2 (9 Kịch bản rủi ro)** và **§3 (Thiết kế UX khi AI sai)** |
| Hoàng Đăng Kiên | 2A202603636 | Phụ trách **§5 (Xây dựng Prototype `index.html` & Chú thích ảnh)**, **§6 (3 tiêu chí nghiệm thu Pass/Fail)** và **§7 (Demo & Ca lạ)** |

---

## §1. Lát cắt & phạm vi *(Phụ trách: Nguyễn Hà Anh — 2A202603605)*

### 1.1. Lát cắt (chép nguyên văn từ Track T3)
<!-- Điền câu lát cắt và bảng tóm tắt lát cắt từ spec1.md -->

| Sản phẩm | Một người dùng | Một việc | Một quyết định của AI | Một kết quả |
|---|---|---|---|---|
|  |  |  |  |  |

### 1.2. Ba việc tính năng này KHÔNG làm (và vì sao)
1. **[Việc không làm 1]:**
   - *Vì sao:* ...
2. **[Việc không làm 2]:**
   - *Vì sao:* ...
3. **[Việc không làm 3]:**
   - *Vì sao:* ...

---

## §2. Kịch bản rủi ro (Chặng 2 — Mốc M1) *(Phụ trách: Trần Xuân Trường — 2A202603617)*

### 2.1. Bảng 9 kịch bản rủi ro (phủ đủ 4 lớp ①②③④)

> **Dữ liệu tham chiếu (`tra_cuu_dat_cho`):** Mã đặt chỗ `TRV-7Q2K` · Hành khách: `Nguyễn Minh An (34 tuổi)` & `Nguyễn Gia Bình (5 tuổi)` · Chuyến gốc: `BM 213 Hà Nội → TP.HCM, 12/11 19:00` (ĐÃ HUỶ do bão) · Chính sách Bay Mẫu: đổi miễn phí 1 lần trong 48h hoặc hoàn toàn bộ, không bồi thường tiền mặt do thời tiết, hoàn vé gửi rồi không rút lại được (tới 90 ngày) · Chuyến thay thế: `BM 217 (12/11 21:00 - còn 1 chỗ)`, `BM 201 (13/11 07:00 - còn 9 chỗ)`, `BM 205 (13/11 09:30 - còn 4 chỗ)`.

| # | Tin người dùng nhắn (giống người thật) | Lớp rủi ro | AI có thể sai thế nào (trỏ vào tool / dòng dữ liệu cụ thể) | Một sản phẩm tốt nên làm gì | Nhãn mức hại |
|---|---|---|---|---|---|
| **K1** *(Đắt nhất #1)* |  |  |  |  |  |
| **K2** *(Đắt nhất #2)* |  |  |  |  |  |
| **K3** *(Suýt chọn)* |  |  |  |  |  |
| **K4** |  |  |  |  |  |
| **K5** |  |  |  |  |  |
| **K6** |  |  |  |  |  |
| **K7** |  |  |  |  |  |
| **K8** |  |  |  |  |  |
| **K9** |  |  |  |  |  |

---

### 2.2. Quyết định chọn 2 kịch bản đắt nhất (Lập luận 4 ý)

- **Các phương án đã cân nhắc:** ...
- **Quyết định chọn:** ...
- **Vì sao chọn K1 và K2 (đắt hơn các kịch bản còn lại ở điểm nào):**
  1. ...
  2. ...
- **Kịch bản nào suýt được chọn và vì sao loại:**
  - ...

---

## §3. Khi AI sai (Chặng 3 — 25 điểm) *(Phụ trách: Trần Xuân Trường — 2A202603617)*

### 3.1. Thiết kế chi tiết cho Kịch bản đắt nhất #1 (K2 — Đổi gấp sang chuyến `BM 217 21:00` chỉ còn 1 chỗ cho 2 mẹ con)

> **Tin nhắn của khách:** *"..."*

1. **AI nói gì (nguyên văn) · Người dùng thấy gì · Làm gì tiếp · Ai được báo:**
   - **Câu AI nói nguyên văn:**
     > *"..."*
   - **Người dùng thấy gì ngoài câu chữ (trên UI):**
     - ...
   - **Bước người dùng làm tiếp & Nếu không làm gì thì sao:**
     - ...
   - **Ai được báo, sau bao lâu:**
     - ...

2. **Quyết định xử lý (Lập luận 4 ý):**
   - **Các phương án đã cân nhắc:** ...
   - **Chọn phương án nào:** ...
   - **Vì sao chọn:** ...
   - **Vì sao loại các phương án kia:** ...

3. **Phân loại lỗi & Cách nói, cách sửa theo loại lỗi:**
   - **Loại lỗi:** ...
   - **Cách nói & cách sửa đi theo loại lỗi:** ...

---

### 3.2. Thiết kế chi tiết cho Kịch bản đắt nhất #2 (K1 — Khách giận đòi hoàn tiền ngay để mua vé mới tối nay + đòi bồi thường)

> **Tin nhắn của khách:** *"..."*

1. **AI nói gì (nguyên văn) · Người dùng thấy gì · Làm gì tiếp · Ai được báo:**
   - **Câu AI nói nguyên văn:**
     > *"..."*
   - **Người dùng thấy gì ngoài câu chữ (trên UI):**
     - ...
   - **Bước người dùng làm tiếp & Nếu không làm gì:**
     - ...
   - **Ai được báo, sau bao lâu:**
     - ...

2. **Quyết định xử lý (Lập luận 4 ý):**
   - **Các phương án đã cân nhắc:** ...
   - **Chọn phương án nào:** ...
   - **Vì sao chọn:** ...
   - **Vì sao loại các phương án kia:** ...

3. **Phân loại lỗi & Cách nói, cách sửa theo loại lỗi:**
   - **Loại lỗi:** ...
   - **Cách nói & cách sửa:** ...

---

### 3.3. Ánh xạ 3 nguyên tắc HAX / PAIR vào chỗ cụ thể

1. **HAX G2 & HAX G10:**
   - *Trỏ vào chỗ cụ thể:* ...
2. **HAX G11 & PAIR Explainability + Trust:**
   - *Trỏ vào chỗ cụ thể:* ...
3. **HAX G8/G9 & PAIR Errors + Graceful Failure:**
   - *Trỏ vào chỗ cụ thể:* ...

---

### 3.4. Lỗi nào "sửa câu chữ (prompt) không cứu được", chỉ thiết kế hệ thống/UI mới cứu được?

- **Lỗi không thể cứu bằng câu chữ:** ...
- **Thiết kế cứu lỗi này thế nào (Architectural Guardrail & UI Gate):**
  1. ...
  2. ...
  3. ...

---

## §4. Mức tự chủ (Chặng 4 — Mốc M2 — 25 điểm) *(Phụ trách: Nguyễn Hà Anh — 2A202603605)*

### 4.1. Bảng phân quyền mức tự chủ cho 5 Tool (theo Cost-of-Error)

| Tên Tool | Mức tự chủ của nhóm | Nếu cần duyệt: Ai duyệt · Thấy gì · Quá hạn thì sao | Lý do theo Cost-of-Error (Sai ai chịu · Đảo được không · Chờ người mất gì) | Phương án đã cân nhắc & Vì sao loại |
|---|---|---|---|---|
| `tra_cuu_dat_cho` |  |  |  |  |
| `giu_cho_chuyen_moi` |  |  |  |  |
| `doi_chuyen_bay` |  |  |  |  |
| `gui_yeu_cau_hoan_ve` |  |  |  |  |
| `chuyen_nhan_vien` |  |  |  |  |

---

### 4.2. Phân tích Tool khó xếp nhất: `doi_chuyen_bay`

1. **Vì sao `doi_chuyen_bay` là tool khó xếp nhất (mỗi thành viên từng chọn gì & cái giá của mỗi phía):**
   - **Hoàng Đăng Kiên (`2A202603636`):** ...
   - **Trần Xuân Trường (`2A202603617`):** ...
   - **Nguyễn Hà Anh (`2A202603605`):** ...
2. **Cách chốt của nhóm & Luật bổ sung / Tách bước Tool:**
   - **Chốt mức:** ...
     1. ...
     2. ...

---

### 4.3. Thử nghiệm mức tự chủ đã đặt trên 3 kịch bản (2 đắt nhất + 1 bình thường)

| Kịch bản thử nghiệm | Luồng chạy của AI với mức tự chủ đã đặt | ① Cái sai ở §2 có bị chặn không? | ② Có việc nào AI vẫn làm khi lẽ ra phải hỏi không? | ③ Người dùng bình thường có phải chờ vô ích không? |
|---|---|---|---|---|
| **K2 (Đắt nhất #1)** |  |  |  |  |
| **K1 (Đắt nhất #2)** |  |  |  |  |
| **K9 (Bình thường)** |  |  |  |  |

---

### 4.4. Một mức tự chủ đã thay đổi "Lời hứa với người dùng" như thế nào?

- **Lời hứa cũ (nếu AI Tự làm):** ...
- **Lời hứa mới của nhóm NORMALDAY:** ...

---

## §5. Prototype (Chặng 5 — Mốc M3 — 25 điểm) *(Phụ trách: Hoàng Đăng Kiên — 2A202603636)*

### 5.1. Thông tin kỹ thuật của Prototype
- **File chạy trực tiếp:** [`prototype/index.html`](prototype/index.html)
- **Ảnh chụp màn hình có đánh số `[1]`–`[6]`:**
  - Ảnh 1: [`prototype/screen1-k2-autonomy.png`](prototype/screen1-k2-autonomy.png)
  - Ảnh 2: [`prototype/screen2-k1-refund-modal.png`](prototype/screen2-k1-refund-modal.png)
- **Công cụ xây dựng:** ...
- **Phần nào Mock & Phần nào chạy thật:** ...

---

### 5.2. Bảng giải thích các vị trí đánh số `[1]` – `[6]` trên Prototype

![Màn hình 1: Xử lý Ca khó K2 và Ma trận mức tự chủ](prototype/screen1-k2-autonomy.png)

![Màn hình 2: Xử lý Ca khó K1 và Friction Modal xác nhận hoàn vé 2 lớp](prototype/screen2-k1-refund-modal.png)

| Số trên ảnh | Vị trí trên màn hình Prototype | Thể hiện điều gì | Nguyên tắc HAX / PAIR tương ứng | Mức tự chủ thể hiện |
|---|---|---|---|---|
| **`[1]`** |  |  |  |  |
| **`[2]`** |  |  |  |  |
| **`[3]`** |  |  |  |  |
| **`[4]`** |  |  |  |  |
| **`[5]`** |  |  |  |  |
| **`[6]`** |  |  |  |  |

---

### 5.3. Quyết định thiết kế giao diện (Lập luận 4 ý)

1. **Cách hiển thị Độ chắc chắn / Bằng chứng (Confidence & Explainability):**
   - **Đã cân nhắc các phương án nào:** ...
   - **Vì sao chọn & loại các phương án kia:** ...
2. **Cách thiết kế Điều khiển mức tự chủ (Autonomy Controls):**
   - **Đã cân nhắc các phương án nào:** ...
   - **Vì sao chọn & loại các phương án kia:** ...

---

## §6. Tốt là gì (Chặng 6 — 5 điểm) *(Phụ trách: Hoàng Đăng Kiên — 2A202603636)*

### 6.1. Ba tiêu chí nghiệm thu Pass / Fail (Ai chấm cũng ra cùng một kết quả)

1. **Tiêu chí 1:**
   - **Đạt (PASS) khi:** ...
   - **Không đạt (FAIL) khi:** ...
2. **Tiêu chí 2:**
   - **Đạt (PASS) khi:** ...
   - **Không đạt (FAIL) khi:** ...
3. **Tiêu chí 3:**
   - **Đạt (PASS) khi:** ...
   - **Không đạt (FAIL) khi:** ...

---

### 6.2. Chấm thử thiết kế của nhóm trên 2 kịch bản đắt nhất & Lỗi còn lại

| Kịch bản đắt nhất | Tiêu chí 1 (Chặn thao tác không đảo được) | Tiêu chí 2 (Trung thực dữ liệu & chính sách) | Tiêu chí 3 (Giữ chỗ & Đường lui) | Kết quả chung |
|---|---|---|---|---|
| **K2 (Đổi gấp sang `BM 217 21:00` chỉ còn 1 chỗ cho 2 mẹ con)** |  |  |  |  |
| **K1 (Khách giận đòi hoàn tiền ngay mua vé tối nay + đòi bồi thường 400k)** |  |  |  |  |

- **Lỗi / Giới hạn còn lại chưa giải quyết triệt để trong thiết kế hiện tại:**
  1. ...
  2. ...

---

## §7. Demo & Kịch bản phản ứng với Ca lạ (Chặng 7 — 5 điểm + Bonus) *(Phụ trách: Hoàng Đăng Kiên — 2A202603636)*

### 7.1. Kịch bản trình bày Demo 4 phút (Phân công 3 thành viên)
1. **Phần 1 — Nguyễn Hà Anh (`2A202603605`) · Phút 0:00 – 1:15 (Lát cắt, Phạm vi & Ma trận Mức tự chủ §1 + §4):**
   - ...
2. **Phần 2 — Trần Xuân Trường (`2A202603617`) · Phút 1:15 – 2:30 (2 Kịch bản đắt nhất & Nguyên tắc HAX/PAIR §2 + §3):**
   - ...
3. **Phần 3 — Hoàng Đăng Kiên (`2A202603636`) · Phút 2:30 – 4:00 (Tương tác Prototype, Hoàn tác & Xử lý "Ca lạ" §5 + §6 + §7):**
   - ...

---

### 7.2. Ghi nhận Ca lạ tại buổi Demo & Đánh giá sau thử nghiệm
- **Cách Prototype xử lý mọi Ca lạ (Unseen Cases):**
  - ...
- **Bài học & Điều chỉnh sau khi thử các Ca lạ:**
  - ...
