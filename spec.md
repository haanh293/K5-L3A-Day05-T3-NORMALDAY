# Bài nộp LAB5 — T3 Du lịch · Nhóm NORMALDAY

**Lớp:** L3A · **Bàn 6 / zone: 4 ** ____ · **Track:** T3 — Du lịch (Trợ lý đổi chuyến khi chuyến bay bị huỷ)

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
| Đặt chỗ của tôi (giống Traveloka) | Hành khách | Vừa nhận tin chuyến bị huỷ, nhắn hỏi | Đề xuất và giữ chỗ, hỏi lại, đổi vé, hay chuyển nhân viên | Khách tới nơi kịp, không mất vé hay tiền vì một thao tác không đảo được |

### 1.2. Ba việc tính năng này KHÔNG làm (và vì sao)
1. **Không tự động đổi tên hành khách hoặc tách mã đặt chỗ (Split PNR) để cho trẻ em (5 tuổi) bay một mình:**
   - *Vì sao:* Bộ 5 tool hiện có không hỗ trợ đổi tên hay tách PNR; mặt khác, việc tách trẻ nhỏ (`Nguyễn Gia Bình, 5 tuổi` trong đặt chỗ `TRV-7Q2K`) bay riêng là vi phạm quy định an toàn hàng không về trẻ em đi một mình (Unaccompanied Minor - UMNR), bắt buộc phải gọi `chuyen_nhan_vien`.
2. **Không xét duyệt hay cam kết bồi thường tiền mặt (ứng trước) khi chuyến bay bị huỷ:**
   - *Vì sao:* Theo dữ liệu chính sách hãng Bay Mẫu và mục "Sản phẩm thật hôm nay" (Vietnam Airlines), chuyến `BM 213` bị huỷ do thời tiết (bão - bất khả kháng) nên được miễn trừ trách nhiệm bồi thường tiền mặt; AI không có tool chi trả bồi thường và hứa sai sẽ gây khiếu nại pháp lý/mất niềm tin nghiêm trọng.
3. **Không xử lý đổi hành trình khác chặng (đổi sân bay đi/đến ngoài Hà Nội → TP.HCM), nâng hạng vé có thu chênh lệch, hoặc đặt dịch vụ phụ trợ (khách sạn, xe đưa đón):**
   - *Vì sao:* Lát cắt chỉ giải quyết việc đưa khách tới đích của chuyến bị huỷ bằng các chuyến thay thế miễn phí trong 48 giờ (`BM 217`, `BM 201`, `BM 205`); luồng Easy Reschedule thật trên Traveloka yêu cầu thanh toán chênh lệch riêng mà bộ tool hiện tại không có cổng thanh toán.

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
| `tra_cuu_dat_cho` | **Tự làm** | *Không cần duyệt.* | - **Sai ai chịu / Đảo được không:** Tool chỉ đọc (`Read-only`) dữ liệu đặt chỗ `TRV-7Q2K` và danh sách chuyến thay thế. Không làm thay đổi trạng thái vé hay tiền của khách (Cost-of-error = 0).<br>- **Chờ người thì mất gì:** Nếu bắt khách bấm cho phép mới tra cứu thì mất thêm 1 lượt chat vô nghĩa trong lúc khách đang hoảng loạn vì huỷ chuyến. | - *Đã cân nhắc:* Cần khách xác nhận mã đặt chỗ trước khi đọc.<br>- *Vì sao loại:* Khách đã mở chat ngay trong màn hình **Đặt chỗ của tôi (`TRV-7Q2K`)**, bắt xác nhận lại là thừa thãi. |
| `giu_cho_chuyen_moi` | **Tự làm** | *Không cần duyệt.* *(Trên màn hình có nút "Nhả chỗ / Đổi chuyến giữ" để khách chủ động huỷ nếu muốn).* | - **Sai ai chịu / Đảo được không:** Hoàn toàn **đảo lại được** — chỉ giữ ghế tạm trong 20 phút, chưa xuất vé, **không làm mất lần đổi miễn phí duy nhất** của khách. Hết 20 phút tự động nhả ghế.<br>- **Chờ người thì mất gì:** Khi 1 chuyến bay (`BM 213`) bị huỷ, hàng trăm hành khách cùng tranh nhau vài ghế trống trên các chuyến kế tiếp (`BM 205` chỉ còn 4 chỗ, `BM 201` còn 9 chỗ). Nếu chờ khách đọc tin và xác nhận mới giữ chỗ thì **chuyến tốt nhất đã hết sạch ghế** (Cost of waiting > Cost of error). | - *Đã cân nhắc:* Cần khách duyệt mới giữ chỗ.<br>- *Vì sao loại:* Chờ khách bấm duyệt mới giữ chỗ thì khách hay gặp tình trạng bấm vào đã báo "Hết chỗ", gây ức chế cực độ. |
| `doi_chuyen_bay` | **Cần người duyệt** *(kèm 10 phút Ân hạn Hoàn tác)* | - **Ai duyệt:** Chính hành khách bấm nút `Xác nhận đổi` trên Thẻ xác nhận UI.<br>- **Thấy gì trước khi bấm:** Thấy rõ Chuyến cũ (`BM 213`) → Chuyến mới (`BM 201 · 13/11 07:00`), Tên đủ **2 hành khách** (`Nguyễn Minh An` & `Nguyễn Gia Bình`), Phí `0đ`, và cảnh báo *"Dùng lần đổi miễn phí duy nhất trong 48h"*.<br>- **Quá hạn thì sao:** Nếu sau 20 phút giữ chỗ khách không bấm duyệt, ghế tạm tự nhả, vé giữ nguyên trạng thái cũ (còn nguyên quyền đổi trong 48h). | - **Sai ai chịu:** Nếu AI tự đổi nhầm chuyến (VD: đổi sang `07:00` khi khách cần `09:30`, hoặc đổi nhầm vào `BM 217` chỉ có 1 ghế), **hành khách chịu thiệt hại nặng**: mất quyền đổi miễn phí duy nhất, chuyến mình thực sự cần có thể hết chỗ.<br>- **Đảo lại được không:** **Rất khó** trên hệ thống hãng thật (phải qua nhân viên can thiệp ngoại lệ).<br>- **Chờ người thì mất gì:** Vì AI đã tự động gọi `giu_cho_chuyen_moi` (20 phút) trước đó, việc chờ khách đọc và bấm 1 nút xác nhận (mất 10–30 giây) **không làm khách mất ghế**. | - *Đã cân nhắc:* (1) **Tự làm** (đổi luôn khi khách nhắn); (2) **Cấm** (bắt nhân viên duyệt mọi ca đổi vé).<br>- *Vì sao loại:* Loại *Tự làm* vì ngôn ngữ tự nhiên rất hay mơ hồ (K2, K3), đổi sai là mất lượt đổi miễn phí. Loại *Cấm* vì 90% ca đổi đủ chỗ khách tự chốt được trong 10 giây, đẩy sang nhân viên sẽ làm nghẽn tổng đài ngày bão. |
| `gui_yeu_cau_hoan_ve` | **Cần người duyệt nghiêm ngặt (2 lớp)** *(Cấm AI tự gọi)* | - **Ai duyệt:** Hành khách phải (1) bấm mở hộp thoại Hoàn vé, (2) **tích chọn Checkbox cam kết** hiểu rõ rủi ro, rồi (3) bấm nút đỏ `Gửi yêu cầu hoàn vé`.<br>- **Thấy gì trước khi bấm:** Cảnh báo đỏ *"Gửi rồi KHÔNG huỷ lại được · Mất chỗ trên mọi chuyến thay thế · Tiền hoàn về thẻ gốc tới 90 ngày · Huỷ do bão không có bồi thường tiền mặt"*.<br>- **Quá hạn thì sao:** Khách đóng hộp thoại hoặc không bấm thì không có gì xảy ra, vé vẫn an toàn. | - **Sai ai chịu:** **Hành khách chịu mất trắng phương tiện di chuyển và bị giam vốn tới 90 ngày** (như ở K1).<br>- **Đảo lại được không:** **Tuyệt đối KHÔNG** (theo dữ liệu Track T3: *"Gửi rồi không huỷ được"*).<br>- **Chờ người thì mất gì:** Quyền hoàn vé có hiệu lực suốt 48 giờ+, việc bắt khách đọc kỹ và tích chọn thêm 15 giây **không gây mất mát gì**, nhưng cứu được 100% các ca khách nói "huỷ đi" lúc đang nóng giận. | - *Đã cân nhắc:* (1) **Tự làm** khi khách gõ chữ "hoàn tiền"; (2) **Cấm hoàn toàn trên AI** (bắt gặp nhân viên mới được hoàn).<br>- *Vì sao loại:* Loại *Tự làm* vì hậu quả không thể đảo ngược. Loại *Cấm hoàn toàn* vì trên Traveloka thật khách vẫn tự bấm hoàn vé được mà không cần nhân viên; chỉ cần thiết kế rào cản xác nhận (Friction Modal) là đủ. |
| `chuyen_nhan_vien` | **Tự làm** *(và luôn có nút cho khách tự bấm)* | *Không cần duyệt — AI tự chuyển ngay khi chạm ngưỡng an toàn, hoặc khách bấm nút "Gặp nhân viên" bất cứ lúc nào.* | - **Sai ai chịu / Đảo được không:** Hoàn toàn **đảo lại được**. Nếu AI chuyển thừa 1 ca sang nhân viên thì cái giá chỉ là vài phút làm việc của CSKH; nhưng nếu AI **không chuyển** ở các ca ngoài thẩm quyền (tách trẻ 5 tuổi bay lẻ ở K4, đổi tên ở K5, khách báo đã đổi nhầm mất lượt ở K7) thì khách mất chuyến bay hoặc vi phạm an toàn hàng không.<br>- **Chờ người thì mất gì:** Không mất gì vì trước khi chuyển, AI đã tự gọi `giu_cho_chuyen_moi` để giữ ghế 20 phút cho khách. | - *Đã cân nhắc:* Hỏi khách xác nhận rồi mới chuyển nhân viên ở mọi ca.<br>- *Vì sao loại:* Với các ca bị **Cấm về mặt nghiệp vụ** (như trẻ 5 tuổi bay một mình hoặc đã hết lượt đổi miễn phí), AI không có công cụ nào khác để giải quyết, nên tự động xếp hàng nhân viên ngay giúp tiết kiệm thời gian chờ cho khách. |

---

### 4.2. Phân tích Tool khó xếp nhất: `doi_chuyen_bay`

1. **Vì sao `doi_chuyen_bay` là tool khó xếp nhất (mỗi thành viên từng chọn gì & cái giá của mỗi phía):**
   - Trong 5 phút đầu khi 3 thành viên độc lập xếp mức tự chủ cho 5 tool, cả nhóm đồng thuận ngay ở 4 tool (`tra_cuu_dat_cho`, `giu_cho_chuyen_moi`, `gui_yeu_cau_hoan_ve`, `chuyen_nhan_vien`), nhưng lệch nhau hoàn toàn ở **`doi_chuyen_bay`**:
     - **Hoàng Đăng Kiên (`2A202603636`) — Ban đầu chọn `Tự làm`:** Lập luận rằng khách đang ở sân bay hoặc sắp tới giờ bay (`BM 213` bay 19:00 mà 15:00 mới báo huỷ), khách đi cùng con nhỏ 5 tuổi chỉ muốn nhắn 1 câu *"Đổi giúp mình sang chuyến tối nay / sáng mai"* là xong ngay, không muốn bấm nhiều bước. **Cái giá phải trả (trỏ về K2 & K3 ở §2):** Ở **K2**, khách nhắn *"Đổi gấp luôn chuyến BM 217 tối nay"*, nếu AI tự làm sẽ đâm đầu vào chuyến chỉ còn 1 chỗ (tách mẹ con hoặc lỗi mất lượt đổi); ở **K3**, khách nhắn *"Đổi sang sáng mai"*, AI tự chọn `07:00` trong khi khách cần `09:30` → mất oan lần đổi miễn phí duy nhất.
     - **Trần Xuân Trường (`2A202603617`) — Ban đầu chọn `Chỉ gợi ý / Chuyển nhân viên`:** Lập luận rằng vì chỉ có 1 lần đổi miễn phí duy nhất nên AI không được đụng vào, chỉ liệt kê giờ bay rồi bắt khách tự vào menu truyền thống hoặc chờ nhân viên đổi. **Cái giá phải trả:** Quay lại đúng nỗi đau của "Sản phẩm thật hôm nay" (*"Đừng bắt tôi bấm qua mười màn hình"*) và trong lúc chờ nhân viên thì 4 ghế cuối cùng của `BM 205` đã bị người khác đặt mất.
     - **Nguyễn Hà Anh (`2A202603605`) — Đề xuất phương án dung hoà:** Chỉ ra rằng tốc độ (nỗi lo của Kiên) có thể giải quyết bằng `giu_cho_chuyen_moi` (**Tự làm**), còn rủi ro mất lượt đổi (nỗi lo của Trường) có thể chặn bằng 1 bước bấm xác nhận của khách trên thẻ UI.
2. **Cách chốt của nhóm & Luật bổ sung / Tách bước Tool:**
   - **Chốt mức:** Cả nhóm thống nhất xếp `doi_chuyen_bay` ở mức **Cần người duyệt (Khách bấm xác nhận trên thẻ UI)**, kết hợp chặt với `giu_cho_chuyen_moi` (**Tự làm**) và thêm **2 luật thiết kế (Guardrails)**:
     1. **Luật kiểm tra điều kiện cứng trước khi mở nút duyệt (Pre-condition Rule):** Chỉ cho phép kích hoạt nút duyệt `doi_chuyen_bay` khi `so_cho_trong_chuyen_moi >= so_hanh_khach_trong_dat_cho` (với `TRV-7Q2K` là `>= 2`). Nếu `< 2` (như `BM 217` còn 1 chỗ ở K2), hệ thống khoá nút đổi trên UI và chuyển sang hướng giữ chỗ chuyến kế tiếp (`BM 201`) hoặc gặp nhân viên tách PNR.
     2. **Tách `doi_chuyen_bay` thành 2 pha (Soft-Commit & Hard-Commit với 10 phút Hoàn tác):** Khi khách bấm `Xác nhận đổi`, hệ thống ghi nhận ở trạng thái **Chờ xuất vé (10 phút ân hạn)** kèm nút **Hoàn tác (Undo)** ngay trên màn hình chat. Nếu trong 10 phút khách phát hiện con bấm nhầm hoặc muốn đổi giờ khác (như **K7**), khách bấm `Hoàn tác` là lấy lại được ngay quyền đổi miễn phí mà không cần chờ nhân viên.

---

### 4.3. Thử nghiệm mức tự chủ đã đặt trên 3 kịch bản (2 đắt nhất + 1 bình thường)

| Kịch bản thử nghiệm | Luồng chạy của AI với mức tự chủ đã đặt | ① Cái sai ở §2 có bị chặn không? | ② Có việc nào AI vẫn làm khi lẽ ra phải hỏi không? | ③ Người dùng bình thường có phải chờ vô ích không? |
|---|---|---|---|---|
| **K2 (Đắt nhất #1):** *"Tối nay 9h có chuyến BM 217 đúng không? Đổi gấp luôn chuyến đó cho mình nhé!"* | 1. AI tự chạy `tra_cuu_dat_cho` → thấy `BM 217` còn 1 chỗ < 2 khách.<br>2. Luật cứng chặn `doi_chuyen_bay(BM 217)`.<br>3. AI tự chạy `giu_cho_chuyen_moi(BM 201 - 07:00)` (giữ 2 chỗ trong 20 phút).<br>4. Hiển thị thẻ xác nhận `BM 201` (cần khách bấm duyệt) hoặc nút `Gặp nhân viên` nếu muốn tách vé đi lẻ. | **Bị chặn 100%.** Không xảy ra việc đổi nhầm làm tách mẹ con 5 tuổi hay mất lượt đổi miễn phí. | **Không.** Việc duy nhất AI tự làm là `giu_cho_chuyen_moi(BM 201)` — việc này miễn phí và tự nhả sau 20 phút nên không xâm phạm quyền tự quyết của khách. | **Không phải chờ.** Khách biết ngay lập tức `BM 217` chỉ còn 1 ghế và đã có sẵn 2 ghế `BM 201` được giữ an toàn, chỉ cần 1 cú chạm để chốt. |
| **K1 (Đắt nhất #2):** *"Thôi hoàn tiền ngay cho tôi tự mua vé khác bay tối nay, cộng thêm bồi thường 400k!"* | 1. AI tự chạy `tra_cuu_dat_cho` → thấy lý do huỷ là `Thời tiết (bão)`.<br>2. AI bị **Cấm** tự gọi `gui_yeu_cau_hoan_ve`.<br>3. AI giải thích rõ hoàn vé mất 90 ngày & bão không có bồi thường tiền mặt; tự chạy `giu_cho_chuyen_moi(BM 201)` làm đường lui.<br>4. Nếu khách vẫn muốn hoàn, phải bấm mở Modal và tích checkbox mới gọi được `gui_yeu_cau_hoan_ve`. | **Bị chặn 100%.** Khách không bị mất vé oan vì một câu nói lúc nóng giận, và AI không hứa bừa tiền bồi thường. | **Không.** Mọi quyết định huỷ/hoàn hoặc đổi vé đều nằm dưới ngón tay xác nhận của khách. | **Không.** Khách muốn đổi vé thì bấm ngay trên thẻ; khách thực sự muốn hoàn vé thì chỉ tốn 5 giây tích chọn checkbox trong Modal mà không phải xếp hàng chờ nhân viên. |
| **K9 (Bình thường):** *"Cho mình xem các chuyến còn trống ngày mai nhé, mình chưa chốt đổi đâu, hỏi gia đình đã."* | 1. AI tự chạy `tra_cuu_dat_cho`.<br>2. Hiển thị rõ `BM 201 (07:00 - còn 9 chỗ)` và `BM 205 (09:30 - còn 4 chỗ)`.<br>3. Tự chạy `giu_cho_chuyen_moi(BM 201)` giữ 2 chỗ tạm 20 phút giúp khách yên tâm bàn với gia đình, kèm nút chọn đổi khi đã sẵn sàng. | **Bị chặn 100%.** Không tự ý khoá/đổi vé khi khách đang hỏi thông tin. | **Không.** Giữ chỗ tạm 20 phút đúng tâm lý hỗ trợ khách trong lúc hỏi ý kiến người nhà. | **Không.** Phản hồi tức thì trong 1 giây, đầy đủ số chỗ trống chính xác từ dữ liệu. |

---

### 4.4. Một mức tự chủ đã thay đổi "Lời hứa với người dùng" như thế nào?

- Khi chuyển `doi_chuyen_bay` từ mức **Tự làm** sang mức **Cần khách duyệt (kèm AI tự động giữ chỗ 20 phút & hoàn tác 10 phút)**, lời hứa giá trị (Value Proposition) của sản phẩm đối với hành khách thay đổi căn bản:
  - **Lời hứa cũ (nếu AI Tự làm):** *"Bạn chỉ cần nhắn tin, AI sẽ đổi vé xong xuôi thay bạn"* — Lời hứa này nghe hấp dẫn lúc quảng cáo nhưng thực chất là **lời hứa nguy hiểm**, biến trợ lý thành người quyết định thay số phận chuyến đi của khách khi thông tin còn mơ hồ hoặc thiếu chỗ.
  - **Lời hứa mới của nhóm NORMALDAY:** *"AI giữ ngay ghế trống cho mẹ con bạn trong tích tắc để không ai giành mất, nhưng **quyền bấm chốt lượt đổi miễn phí duy nhất luôn nằm trong tay bạn** — và nếu lỡ bấm nhầm, bạn vẫn có 10 phút để hoàn tác."*

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
