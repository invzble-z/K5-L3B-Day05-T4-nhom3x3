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

*Đường correction: người mua cho rằng shop sai, nhưng bằng chứng lại khớp với mô tả.*

**Tin người mua:** "Áo ghi L mà mặc như M, shop lừa đảo, hoàn tiền cho mình" (kèm ảnh tem áo ghi **L**). Đơn DH-4502, mô tả lúc đặt (05/11): "Size L · vòng ngực 100 cm", mô tả chưa từng bị sửa (§0).

**AI nói (nguyên văn):**
> Mình đã xem ảnh bạn gửi: tem áo ghi **L**, và **mô tả lúc bạn đặt (05/11)** ghi "Size L · vòng ngực 100 cm". Size trên tem khớp với mô tả, nên hiện mình **chưa thấy căn cứ** là hàng không đúng mô tả.
> Áo mặc chật thì rất bực, mình hiểu. Có một cách kiểm: bạn trải phẳng áo, đo từ nách bên này sang nách bên kia rồi nhân 2, chụp ảnh có thước. Nếu kết quả nhỏ hơn 100 cm rõ rệt, đó là căn cứ để xét lại.
> Mình **không đóng** khiếu nại của bạn. Bạn còn **4 ngày (đến 23:59 17/11)** và có thể nhờ nhân viên xem lại bất cứ lúc nào.

Câu này **không hứa** hoàn tiền và **không kết luận** shop đúng, chỉ nói "chưa thấy căn cứ". Khung chat luôn ghi người mua đang trò chuyện với **trợ lý AI**, và quyết định cuối do shop hoặc nhân viên sàn đưa ra.

**Người dùng thấy** (ca B trên prototype, Màn 1):
- Nhãn ① **"Tem khớp mô tả lúc đặt · chưa thấy căn cứ"**, màu xám chứ không đỏ, để không mang nghĩa phán xử.
- ② Bằng chứng đặt cạnh nhau: ảnh tem L và dòng mô tả lúc đặt, có nhãn "mô tả chưa từng bị sửa".
- Ô nhập số đo vòng ngực.
- ③ Dòng "Khiếu nại **vẫn mở** · còn 4 ngày (đến 23:59 17/11). Mình không đóng khiếu nại, và shop chưa bị báo gì."

**Làm gì tiếp:**
- **Gửi số đo:**
  - Dưới 98 cm: AI nói đã đủ căn cứ và hiện nút **"Mở yêu cầu trả hàng (giữ hạn)"**. **Người mua tự bấm**, giống ca A, vì không tool nào trong 7 tool cho AI mở yêu cầu. Sau khi người mua mở, AI mới tự gửi `yeu_cau_bang_chung` cho shop (đúng luật ở §4). Hoàn tiền vẫn **cần shop hoặc nhân viên duyệt**.
  - Từ 98 cm trở lên: AI nói số đo khớp và giữ nguyên khiếu nại (không đóng).
- **④ "Gặp nhân viên ngay"** (`chuyen_truong_nhom`).
- **④ "AI hiểu sai? Sửa lại"**: người mua chọn AI sai ở điểm nào.
- **Nếu không làm gì:** khiếu nại vẫn mở tới hết hạn 23:59 17/11. AI không tự đóng.

**Ai được báo, sau bao lâu:**
- **Chưa báo ai ngay.** Shop không nhận tin chỉ vì người mua bực. Shop chỉ được báo **sau khi người mua tự mở yêu cầu** (thường là sau khi số đo cho thấy lệch); lúc đó AI gửi `yeu_cau_bang_chung` và shop có 48 giờ để phản hồi.
- Nếu người mua bấm gặp nhân viên, trưởng nhóm nhận hồ sơ và trả lời trong 24 giờ.

**Quyết định (1 quyết định = 4 ý):**
- **Đã cân nhắc:** (a) hỏi lại / đòi thêm bằng chứng · (b) trả lời kèm giới hạn · (c) dừng và chuyển người ngay · (d) từ chối khiếu nại · (e) hoàn tiền cho xong.
- **Chọn:** (b) trả lời kèm giới hạn ("chưa thấy căn cứ"), kết hợp (a) **hỏi đúng một bằng chứng** là số đo vòng ngực.
- **Vì sao:**
  - Bằng chứng hiện có (tem L khớp "Size L") nghiêng về phía shop, nhưng chưa đủ để kết luận. Size có thể đúng mà kích thước vẫn sai.
  - Một số đo duy nhất phân định được, vì mô tả lúc đặt có con số cụ thể (100 cm).
  - Người mua tự làm được ngay, không phải chờ ai.
- **Loại các cách kia vì sao:**
  - *Chuyển người ngay (c):* người mua phải chờ tới 24 giờ, nhân viên nhận một hồ sơ chưa có thông tin gì mới, trong khi chỉ cần một số đo.
  - *Từ chối (d):* đóng khiếu nại thì người mua mất quyền, nếu áo thật sự nhỏ hơn mô tả thì không còn đường sửa. "Từ chối cho chắc" cũng là một kiểu sai. AI cũng không có quyền làm việc này (`tu_choi_khieu_nai` cấm với AI, §4).
  - *Hoàn cho xong (e):* người bán đúng mà vẫn mất tiền và hàng, đúng điều lát cắt muốn tránh. Đây cũng là đường dễ bị lời doạ ("shop lừa đảo") kéo theo.
  - *Chỉ hỏi lại, không nói gì về tem (a đơn thuần):* người mua lại thấy "cứ bị hỏi lại mà không ai nói còn thiếu gì". Phải nói rõ AI đã thấy gì trước, rồi mới hỏi.

**Loại lỗi:**
- Đây là **lỗi người dùng / kỳ vọng**: người mua mong áo rộng hơn, chứ shop không sai mô tả.
- **Cách nói:** không quy lỗi (không nói "bạn chọn sai size"), ghi nhận cảm xúc, đưa căn cứ để người mua tự kiểm.
- **Cách sửa:** giữ đường lui (khiếu nại vẫn mở, có nút gặp nhân viên). Nếu số đo cho thấy shop sai thì AI **đổi hướng ngay**. Lỗi người dùng không sửa bằng xin lỗi, mà bằng cách cho người dùng một cách tự kiểm.

### Nguyên tắc HAX/PAIR (trỏ vào chỗ cụ thể — xem ảnh đánh số ở §5)

- **G1 — Làm rõ AI làm được gì** *(kèm Luật AI 134/2025 Điều 11.1)* → dòng cố định ở đầu khung chat Màn 1, ngay trên ①: "Bạn đang trò chuyện với **trợ lý AI** của Sàn Mẫu. Quyết định hoàn tiền hay từ chối do shop hoặc nhân viên sàn đưa ra." Người mua biết mình đang nói với AI, và biết AI không phải người quyết.
- **G2 — Làm rõ AI làm tốt đến đâu** → nhãn độ chắc ở đầu mỗi câu trả lời: "Chưa đủ căn cứ · cần người xét" (A) và "Tem khớp mô tả · chưa thấy căn cứ" (B). Ảnh ①. Ở Màn 2, dòng "AI không đề xuất ai đúng ở ca này". Ảnh ⑥.
- **G11 — Giải thích vì sao** → thẻ so sánh "Mô tả lúc đặt vs hiện tại" có ngày sửa (A), và ảnh tem cạnh dòng mô tả (B). Ảnh ②. Ở Màn 2, phải tick "Tôi đã đối chiếu mô tả lúc đặt" thì mới mở được nút quyết định. Ảnh ⑤.
- **G9 — Sửa dễ dàng / G8 — Gạt bỏ dễ dàng / G15 — Mời feedback chi tiết** → nút "AI hiểu sai? Sửa lại" (người mua chọn sai ở điểm nào, AI hỏi lại) và "Gặp nhân viên ngay" luôn hiện dưới câu trả lời. Ảnh ④.
- **PAIR · Errors + Graceful Failure** → khi chưa đủ căn cứ, AI giữ hạn trả hàng và chỉ bước tiếp theo, không bỏ người mua lại. Thanh trạng thái 3 bước và chip "còn 2 ngày, đã giữ". Ảnh ③.

**Soát câu AI nói (TV3 kiểm câu của ca A, ca B và prototype):**
- *Không hứa liều:* AI chỉ nói "đã chuyển", "đã gửi" khi tool đã trả về thành công, có nhãn "AI đã tự chuyển / AI đã tự gửi" đi kèm. Câu "Bạn sẽ được hoàn 1.290.000đ" chỉ xuất hiện **sau khi** nhân viên bấm duyệt ở Màn 2, không bao giờ do AI tự nói trước.
- *Minh bạch AI:* mọi tin của trợ lý có nhãn "Trợ lý AI · Sàn Mẫu", và dòng G1 luôn ở đầu khung chat.

### Lỗi mà sửa câu chữ không cứu được

**"So với mô tả hiện tại"** (kịch bản A). Nếu tool đọc đơn chỉ trả về mô tả hiện tại thì prompt "hãy so với mô tả lúc đặt" cũng vô ích: AI **không có** dữ liệu lúc đặt, nên sẽ hoặc bịa, hoặc dùng bản đã sửa mà không biết là đã sửa. Câu chữ chỉ đổi được cách AI *nói*, không đổi được thứ AI *nhìn thấy*.

**Thiết kế cứu:** nhóm thêm tool `xem_don_hang` (§4). Tool này trả **snapshot lúc đặt** cùng **lịch sử sửa có ngày giờ**, và luật xét chỉ được dùng snapshot. Trên màn hình, bản sửa hiện có gạch chân đỏ kèm dòng "không dùng để xét" (ảnh ②), để cả người mua lẫn trưởng nhóm thấy AI xét theo bản nào.

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

- **File:** [`prototype/index.html`](prototype/index.html), một file HTML, mở bằng trình duyệt. Mở `index.html#console` để vào thẳng Màn 2. Hướng dẫn bấm: [`prototype/README.md`](prototype/README.md).
- **Công cụ:** HTML/JS viết tay với sự hỗ trợ của coding agent.
- **Phần mock:** toàn bộ dữ liệu (§0) và câu trả lời của AI đều viết sẵn theo §3. Không backend, **không có lời gọi AI thật**, không gửi dữ liệu đi đâu.
- **Màn 1 · Chat người mua:** chọn ca A (nồi chiên, mô tả bị sửa) hoặc ca B (áo tem L, người bán đúng).
- **Màn 2 · Console trưởng nhóm:** "ai quyết" ở ca A, nơi duy nhất có nút hoàn tiền / từ chối.
- **Ô "ca lạ":** người xem gõ tin tự do. Prototype nhận các loại: lời doạ bóc phốt, xin số điện thoại, nghi hàng giả, tự xưng nhân viên, đòi hoàn ngay, hỏi hạn. Không khớp loại nào thì AI rơi về đường an toàn: hỏi lại một câu (đơn nào, sai ở điểm nào), kèm nút gặp nhân viên.

**Ảnh đánh số:**

| Màn 1 · Chat người mua (ca A) | Màn 2 · Console trưởng nhóm |
|---|---|
| ![Màn 1](prototype/screen-1-chat.png) | ![Màn 2](prototype/screen-2-console.png) |

| Số | Thể hiện gì | HAX/PAIR | Mức tự chủ |
|---|---|---|---|
| ① | Nhãn độ chắc ở đầu câu trả lời ("Chưa đủ căn cứ · cần người xét" ở ca A / "Tem khớp mô tả lúc đặt · chưa thấy căn cứ" ở ca B) | G2 | — |
| ② | Bằng chứng đặt cạnh nhau: mô tả lúc đặt (dùng để xét) vs mô tả hiện tại (sửa 10/11, không dùng) / ảnh tem vs mô tả lúc đặt | G11 · PAIR Explainability + Trust | `xem_don_hang`: tự làm |
| ③ | Thanh trạng thái 3 bước + chip "Hạn trả hàng còn 2 ngày · đến 23:59 15/11". Dòng "Hoàn tiền: cần shop hoặc nhân viên duyệt · AI không có nút hoàn" | PAIR Errors + Graceful Failure | `yeu_cau_bang_chung`: tự làm (nhãn "AI đã tự gửi") · `thuc_hien_hoan_tien`: cần duyệt, **không có nút cho AI** |
| ④ | Nút "AI hiểu sai? Sửa lại" (chọn sai ở điểm nào) và "Gặp nhân viên ngay" | G9 · G8 · G15 | `chuyen_truong_nhom`: tự làm |
| ⑤ | Console: nút Duyệt hoàn / Từ chối chỉ có ở đây, chỉ mở khoá sau khi tick "Tôi đã đối chiếu mô tả lúc đặt" | G11 | `thuc_hien_hoan_tien`: cần duyệt · `tu_choi_khieu_nai`: chỉ người làm |
| ⑥ | Tóm tắt trung lập: "AI không đề xuất ai đúng ở ca này" | G2 · chống anchoring | luật ở §4 |

**Quyết định — cách hiện độ chắc / bằng chứng (4 ý):**
- **Đã cân nhắc:** (a) phần trăm độ tin cậy ("72%") · (b) nhãn bằng chữ + bằng chứng đặt cạnh nhau · (c) chỉ hiện kết luận, ẩn bản mô tả đã sửa.
- **Chọn:** (b).
- **Vì sao:** nhãn chữ nói luôn bước tiếp theo ("cần người xét", "chưa thấy căn cứ"). Bằng chứng đặt cạnh nhau cho người mua tự kiểm, đúng tinh thần PAIR "tin đúng mức, không tin tối đa".
- **Loại (a):** con số không giúp người mua biết phải làm gì, và tạo cảm giác AI đang phán xử ai đúng.
- **Loại (c):** người mua sẽ không hiểu vì sao shop nói "đã ghi rõ 5L". Hiện bản sửa và gạch chân thì cả hai bên thấy AI xét theo bản nào.

**Quyết định — điều khiển mức tự chủ trên màn hình (4 ý):**
- **Đã cân nhắc:**
  - (a) Một nút "Hoàn tiền" cho người mua bấm xác nhận.
  - (b) Việc cần duyệt hiện thành **trạng thái** ("chờ shop / chờ nhân viên"), nút quyết định chỉ có trên console.
  - (c) Không hiện gì về hoàn tiền trong chat.
- **Chọn:** (b), thêm nhãn "AI đã tự gửi / đã tự chuyển" cho việc AI tự làm. Việc cấm thì không có nút nào trong chat.
- **Vì sao:** người duyệt hoàn tiền phải là bên chịu mất (shop) hoặc trưởng nhóm (§4), không phải người mua.
- **Loại (a):** người mua là bên được lợi, nên bước xác nhận của họ không chặn được kịch bản #4 và #5.
- **Loại (c):** người mua không biết hồ sơ đang ở bước nào, trái với lời hứa ở §4.

---

## §6. Tốt là gì

---

## §7. Demo
