# Bài nộp LAB5 — T4 Thương mại điện tử · Nhóm nhom3x3

**Lớp:** L3B · **Bàn / zone:** ____ · **Track:** T4 Thương mại điện tử

| Họ và Tên | Mã Học Viên | Việc đã làm |
|---|---|---|
| Lê Phạm Thành Đạt | 2A202604027 | **Kịch bản & ca A:** §1 lát cắt và phạm vi · §2 kịch bản rủi ro, lý do chọn 2 kịch bản đắt nhất · §3 kịch bản A (nồi chiên): câu AI nói, quyết định 4 ý, loại lỗi · §6 tiêu chí Pass/Fail · chuẩn bị ca lạ. Demo: mở đầu 30 giây (lát cắt và vì sao #3, #4 đắt nhất) |
| Trần Đức Duy | 2A202604071 | **Ca B & prototype:** §3 kịch bản B (áo tem L): câu AI nói, quyết định 4 ý, loại lỗi · §5 prototype · `prototype/` (HTML, ảnh đánh số, README). Demo: bấm ca A và ca B trên Màn 1, chỉ các số ①–④ |
| Nguyễn Khắc Bào | 2A202604072 | **Nguyên tắc, mức tự chủ & nộp bài:** tạo repo · §0 dữ liệu dựng · §3 nguyên tắc HAX/PAIR, lỗi mà sửa câu chữ không cứu được, soát "không hứa liều, minh bạch AI" · §4 mức tự chủ (thêm `xem_don_hang`, tách `soan_hoan_tien`) · §7 demo · nộp link. Demo: Màn 2 console, bảng mức tự chủ, trả lời ca lạ theo mức đã đặt |
| *Cả nhóm* | | Mỗi người tự xếp mức cho 7 tool trước rồi so và chốt (ghi ở §4, "Tool khó xếp nhất") · cùng đọc soát toàn bộ spec |

> Dữ liệu trong bài là **dựng**: đơn hàng, shop, chính sách thời hạn đều do nhóm tự sinh. Khoá học và nhóm không liên kết với Shopee.

---

## §0. Dữ liệu dựng nhóm dùng (tự sinh, vì track T4 không cấp fixture)

Bây giờ: **13/11/2026 15:00**.

**Chính sách dựng của "Sàn Mẫu"** (khác chính sách thật của Shopee):
- Người mua mở yêu cầu trả hàng trong **7 ngày kể từ ngày nhận**. Đã mở yêu cầu thì hạn được giữ, kể cả khi đang chờ xét.
- Người bán có **48 giờ** để phản hồi một yêu cầu. Quá hạn không phản hồi thì hồ sơ lên trưởng nhóm.
- Trưởng nhóm trả lời trong **24 giờ** kể từ khi nhận hồ sơ.
- Hệ thống lưu **bản chụp mô tả lúc đặt hàng** (snapshot) và lịch sử sửa mô tả.

| | Đơn A · DH-4417 | Đơn B · DH-4502 |
|---|---|---|
| Sản phẩm | Nồi chiên không dầu KitchenMau | Áo thun nam basic |
| Shop | Gia Dụng Mẫu | Thời Trang Mẫu |
| Giá | 1.290.000đ | 189.000đ |
| Đặt / nhận | đặt 03/11 · nhận 08/11 | đặt 05/11 · nhận 10/11 |
| Hạn trả hàng | **15/11 23:59** (còn 2 ngày) | **17/11 23:59** (còn 4 ngày) |
| Mô tả **lúc đặt** (snapshot) | "Dung tích: 6 lít" | "Size L · vòng ngực 100 cm" |
| Mô tả **hiện tại** | "Dung tích tổng 6L · lòng nồi 5L" — **sửa 10/11**, sau khi người mua đặt | không đổi |
| Bằng chứng người mua | chưa có | ảnh tem áo ghi **L** |

---

## §1. Lát cắt & phạm vi

---

## §2. Kịch bản rủi ro

---

## §3. Khi AI sai

### Kịch bản A — #3 Nồi chiên "6 lít", mô tả đã bị sửa

### Kịch bản B — #4 Áo tem L, người bán đúng

### Nguyên tắc HAX/PAIR

### Lỗi mà sửa câu chữ không cứu được

---

## §4. Mức tự chủ

**Nhóm thêm hoặc tách tool (và vì sao):**
- **Thêm `xem_don_hang`** (chỉ đọc): trả về đơn, ngày nhận, hạn trả, **snapshot mô tả lúc đặt và lịch sử sửa**. Track không có tool đọc đơn, nhưng không có nó thì AI không so được với mô tả (xem §3). Tool **không trả về** số điện thoại hay địa chỉ của bên kia, nên kịch bản #7 bị chặn từ gốc dữ liệu chứ không chỉ bằng câu chữ.
- **Tách `soan_hoan_tien` thành hai:**
  - **`soan_de_xuat_hoan`**: AI soạn hồ sơ (lý do, bằng chứng, hạn). Không động tới tiền.
  - **`thuc_hien_hoan_tien`**: chuyển tiền thật.
  - Lý do tách: tool gốc tên là "soạn" nhưng thực tế hoàn luôn. Khi tách ra, kịch bản #1, #4, #5 bị chặn ở bước thực hiện mà AI vẫn làm được phần việc nhanh.

| Tool | Mức | Ai duyệt / thấy gì / quá hạn | Lý do theo cost-of-error | Phương án đã loại |
|---|---|---|---|---|
| `xem_don_hang` *(thêm)* | **tự làm** | — | Chỉ đọc, sai thì không ai mất gì. Bắt hỏi người mới được đọc thì mọi ca đều chậm vô ích | — |
| `yeu_cau_bang_chung` | **tự làm** + luật | — | Sai thì cùng lắm một bên nhận một tin xin bằng chứng thừa và tốn vài phút; không mất tiền. Chờ người duyệt thì 48 giờ của shop bắt đầu muộn, người mua chờ lâu hơn. **Luật:** dùng mẫu cố định không buộc tội; chỉ gửi shop **sau khi** người mua chọn đúng đơn và mở yêu cầu (chặn #2 gửi nhầm shop) | *Cần duyệt:* loại vì đây là việc rẻ và cần nhanh nhất |
| `chuyen_truong_nhom` | **tự làm** | Trưởng nhóm trả lời trong 24 giờ | Chuyển thừa thì tốn thời gian nhân viên. Chuyển thiếu đắt hơn nhiều (ca mơ hồ bị AI tự xử). **Luật:** AI chỉ nói "đã chuyển" khi tool trả về thành công, và nói rõ giờ dự kiến | *Cần duyệt:* vô lý, vì người duyệt chính là người nhận |
| `soan_de_xuat_hoan` *(tách)* | **tự làm** | — | Chỉ là bản nháp, chưa ai mất tiền. Sai thì người duyệt sửa | — |
| `thuc_hien_hoan_tien` *(tách)* | **cần người duyệt** | **Shop** bấm "Đồng ý hoàn" trong app (bên chịu mất đã đồng ý), **hoặc trưởng nhóm** duyệt. Người duyệt thấy: khiếu nại, snapshot và diff, bằng chứng hai bên. **Quá hạn:** shop không phản hồi sau 48 giờ thì hồ sơ lên trưởng nhóm; **không bao giờ tự hoàn vì hết giờ** | Sai thì shop mất tiền và hàng, khó đòi lại (#4, #5). Một bước xác nhận của đúng người chặn được. Chờ duyệt thì người mua chờ tối đa khoảng 72 giờ (48 giờ shop + 24 giờ trưởng nhóm), nhưng hạn của họ được giữ nên không mất quyền | *Tự làm khi người mua có ảnh:* loại vì có ảnh không có nghĩa là có căn cứ (#4 có ảnh tem L) |
| `tu_choi_khieu_nai` | **cấm với AI** | Chỉ trưởng nhóm dùng, trên console của họ. Người mua tự rút khiếu nại bằng nút của mình | Sai thì người mua mất tiền và giữ món hàng sai (#3 nếu AI so mô tả hiện tại). "Từ chối cho chắc" là kiểu lười dễ xảy ra nhất. Trong chat, AI chỉ nghe một phía (người mua), nên không đủ để đóng | xem "tool khó xếp nhất" bên dưới |
| `phat_shop` | **cấm** | Chuyển bộ phận chuyên trách qua `chuyen_truong_nhom` (nhãn "nghi hàng giả") | Ảnh hưởng cả shop, khó đảo, và không thuộc luồng khiếu nại một đơn. Một bước xác nhận trong chat không đủ, vì cần điều tra nhiều đơn | *Cần duyệt:* loại vì người duyệt trong luồng khiếu nại không có đủ thông tin để phạt |

**Vì sao `thuc_hien_hoan_tien` chỉ cần duyệt mà `tu_choi_khieu_nai` lại cấm?** Cả hai đều khó đảo, nhưng khác nhau ở **ai đã được nghe** lúc quyết. Hoàn tiền có người duyệt là chính bên chịu mất (shop bấm đồng ý) hoặc trưởng nhóm đã thấy bằng chứng hai bên, nên một bước xác nhận là đủ chặn. Từ chối thì bên chịu mất là người mua, mà người mua chính là người đang chat với AI và đang đòi hoàn: không có "bên chịu mất đồng ý" nào để làm bước xác nhận. Nếu cho AI đề xuất từ chối, trưởng nhóm dễ bấm theo (xem dưới), nên nhóm cắt hẳn quyền này khỏi AI.

### Tool khó xếp nhất: `tu_choi_khieu_nai`

Ba thành viên xếp lệch nhau:
- **Lê Phạm Thành Đạt chọn tự làm khi người mua không gửi bằng chứng sau 72 giờ.** Cái giá nếu không làm: ở #4 shop đúng mà tiền bị treo, hồ sơ dồn cho nhân viên.
- **Trần Đức Duy chọn cần người duyệt (AI đề xuất từ chối, trưởng nhóm bấm).** Cái giá: trưởng nhóm dễ bấm theo đề xuất của AI (anchoring). Ở #3, nếu AI đề xuất từ chối vì đọc mô tả hiện tại, nhân viên có thể duyệt luôn.
- **Nguyễn Khắc Bào chọn cấm với AI.** Cái giá: #4 xử lâu hơn, shop chờ tiền thêm khoảng 24 giờ.

**Nhóm chốt: cấm với AI**, kèm hai luật:
1. Người mua không bổ sung bằng chứng sau 72 giờ thì AI nhắc một lần, rồi chuyển hồ sơ cho trưởng nhóm. Không tự đóng.
2. Trong hồ sơ gửi trưởng nhóm, AI chỉ viết **tóm tắt trung lập** (hai bên nói gì, khớp hay không khớp với snapshot), **không** viết "đề xuất: từ chối".

Lý do: cái giá phía chọn "cấm" (shop chờ thêm khoảng 24 giờ, tiền không mất) **rẻ hơn** cái giá phía chọn "tự làm" (người mua mất 1,29 triệu ở #3, không đảo được).

### Thử mức đã đặt trên 3 kịch bản

| | #3 Nồi chiên (đắt) | #4 Áo tem L (đắt) | #1 Áo nhận nhầm size, shop nhận lỗi (bình thường) |
|---|---|---|---|
| Với mức này, AI làm gì | `xem_don_hang` thấy snapshot "6 lít" và bản sửa 10/11 → `yeu_cau_bang_chung` gửi shop sau khi người mua mở yêu cầu → `chuyen_truong_nhom` khi đủ bằng chứng | `xem_don_hang` → thấy tem khớp → hỏi số đo. Không gọi tool nào động tới tiền | `xem_don_hang` → hướng dẫn mở yêu cầu → `yeu_cau_bang_chung` → shop bấm "Đồng ý hoàn" → `thuc_hien_hoan_tien` |
| Cái sai ở §2 có bị chặn không | **Có.** AI không có `tu_choi`, chỉ đọc snapshot | **Có.** `thuc_hien_hoan_tien` cần shop hoặc trưởng nhóm | **Có.** AI không tin câu "shop nhận rồi"; shop tự xác nhận trong app |
| Còn việc nào AI làm khi lẽ ra phải hỏi | `yeu_cau_bang_chung` tự gửi, nhưng chỉ sau khi người mua đã chọn đơn và mở yêu cầu, nên chấp nhận được | Không | Không |
| Người dùng bình thường có phải chờ vô ích không | Có chờ, nhưng **không vô ích**: ca này thật sự cần người quyết | Không. Một số đo là đủ, không xếp hàng chờ nhân viên | Chờ shop bấm (vài giờ). Đó là bước bắt buộc, vì shop là bên mất tiền. **Không** phải chờ trưởng nhóm |

### Một mức tự chủ đã đổi lời hứa với người dùng

Khi tách `soan_hoan_tien` thành "soạn" (tự làm) và "thực hiện" (cần duyệt), lời hứa đổi từ **"Trợ lý hoàn tiền cho bạn"** thành **"Trợ lý chuẩn bị hồ sơ và giữ hạn cho bạn. Shop hoặc nhân viên sàn sẽ duyệt hoàn, và bạn luôn biết hồ sơ đang ở bước nào, hạn tới bao giờ."** Vì vậy prototype có thanh trạng thái 3 bước (③) thay cho nút "Hoàn ngay", và dòng đầu khung chat ghi rõ "Quyết định hoàn tiền hay từ chối do shop hoặc nhân viên sàn đưa ra".

---

## §5. Prototype

---

## §6. Tốt là gì

---

## §7. Demo
