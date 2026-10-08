# Bài 5: Quy trình đưa yêu cầu mới vào Sprint – RikkeiGo

**Người thực hiện:** Lan (Scrum Master)  
**Người xem xét:** Đức (Product Owner)

**Phạm vi:** Quy trình áp dụng cho mọi story mới do Marketing, Chăm sóc khách hàng (CSKH) và Vận hành đề xuất, từ lúc được đề xuất đến lúc vào Sprint Backlog. Ba công cụ phối hợp trên một đường đi:

- **AC (Acceptance Criteria):** định nghĩa *story này đúng khi nào*, viết riêng cho từng story, 3–7 AC dạng Given – When – Then.
- **DoD (Definition of Done):** định nghĩa *việc này xong khi nào*, dùng chung một bộ cho mọi story, chỉ nâng dần theo năng lực đội.
- **MoSCoW:** định nghĩa *story này quan trọng đến đâu*, gắn với **một lần phát hành** cụ thể, Must ≈ 60% năng lực.

---

## Phần 1 – Thiết kế quy trình (5 bước)

```
[1 Tiếp nhận] → [2 Làm rõ & viết AC] → [3 Xếp MoSCoW] → [4 Kiểm tra Ready + DoD] → [5 Chọn vào Sprint]
```

| Bước | Việc cần làm | Người chịu trách nhiệm | Điều kiện sang bước sau |
|---|---|---|---|
| **1. Tiếp nhận** | Bộ phận đề xuất gửi story theo mẫu: *Là [vai trò], tôi muốn [việc], để [giá trị]*, kèm người đề xuất và lý do. Story vào Product Backlog ở trạng thái "Mới", **chưa gán MoSCoW**. | Người đề xuất (gửi); **PO** (ghi nhận, sở hữu Backlog) | Story đủ 3 phần vai trò – việc – giá trị và có người đề xuất. |
| **2. Làm rõ & viết AC** | Buổi refinement 3 bên: người đề xuất + PO + Developers. Viết 3–7 AC dạng Given – When – Then; ước lượng sơ bộ; nếu story quá lớn thì tách. SM điều phối và kiểm tra định dạng AC. | **PO** (chịu trách nhiệm nội dung AC); **Developers** (xác nhận hiểu và kiểm thử được); **SM** (điều phối) | Có 3–7 AC kiểm thử được; Developers xác nhận hiểu và đã ước lượng sơ bộ. |
| **3. Xếp MoSCoW** | Gắn nhãn Must / Should / Could / Won't **cho một bản phát hành cụ thể**, dựa trên giá trị, rủi ro, hạn chót. Các bộ phận trình bày lý do, không tự gán nhãn. Cộng tổng Must và đối chiếu với năng lực. | **PO** quyết định; Developers cung cấp ước lượng và năng lực; SM giữ cho cuộc thảo luận dựa trên tiêu chí | Mỗi story có đúng một nhãn kèm lý do; tổng Must ≤ ~60% năng lực của bản phát hành. |
| **4. Kiểm tra Ready + DoD** | Đối chiếu checklist Ready: AC đạt, ước lượng xong, vừa trong một Sprint, phụ thuộc đã rõ, **DoD chung áp dụng nguyên vẹn** (không có DoD riêng cho từng story). | **Developers** (xác nhận Ready); **PO** (xác nhận AC); **SM** (kiểm tra checklist) | Mọi mục checklist đạt → trạng thái "Ready". Chưa đạt thì quay lại bước 2. |
| **5. Chọn vào Sprint** | Tại Sprint Planning, PO đặt Sprint Goal; Developers chọn story Ready từ trên xuống theo năng lực. Story mới phát sinh **giữa Sprint** không đi tắt vào đây mà quay về bước 1 và chờ Planning kế tiếp. | **Developers** (chọn khối lượng); **PO** (Sprint Goal, thứ tự); **SM** (bảo vệ Sprint) | Story nằm trong Sprint Backlog, tổng khối lượng không vượt năng lực, phục vụ Sprint Goal. |

**Nguyên tắc xuyên suốt**

- Không story nào vào Sprint nếu thiếu AC hoặc chưa Ready.
- Chỉ PO quyết định thứ tự ưu tiên; chỉ Developers quyết định khối lượng nhận vào Sprint.
- DoD chỉ thay đổi ở buổi Retrospective, khi năng lực đội tăng, không thay đổi theo từng story hay từng bộ phận.

---

## Phần 2 – Xử lý tình huống

### Tình huống 1: Giữa Sprint, Marketing đòi đưa ngay story "Tặng mã giới thiệu bạn bè" (chưa có AC) vào Sprint đang chạy

**Cách xử lý:** Story chưa có AC nên không đạt điều kiện Ready, không thể vào Sprint. Lan (SM) bảo vệ Sprint Goal: story được ghi vào Product Backlog (bước 1), viết AC trong buổi refinement (bước 2), xếp MoSCoW (bước 3), rồi được xét ở Sprint Planning kế tiếp. Nếu Marketing cho rằng việc này khẩn cấp, Đức (PO) là người quyết định; nếu đưa vào thì phải có AC đầy đủ trước và Developers đồng ý đổi lấy một story khác có khối lượng tương đương mà không làm hỏng Sprint Goal.

**AC mẫu cho story "Tặng mã giới thiệu bạn bè":**

> **AC1 – Tặng thưởng khi bạn bè hoàn tất chuyến đầu**
> **Given** người dùng A có mã giới thiệu của mình và người dùng B là tài khoản mới chưa từng đặt chuyến,
> **When** B đăng ký bằng mã của A và hoàn tất chuyến đi đầu tiên,
> **Then** cả A và B nhận mã giảm giá trong ví trong vòng 5 phút và nhận được thông báo trong ứng dụng.

(Các AC còn lại của story cần phủ: mã không hợp lệ/hết hạn, tự dùng mã của mình, một tài khoản chỉ nhận thưởng một lần, giới hạn số lượt giới thiệu mỗi người.)

### Tình huống 2: Cả 3 bộ phận đều cho rằng yêu cầu của mình là Must

**Cách xử lý:** Nhãn MoSCoW không do bộ phận tự gán mà do PO gán theo tiêu chí chung cho một bản phát hành cụ thể: nếu thiếu thì bản phát hành có dùng được không, có rủi ro vận hành/pháp lý/doanh thu không. Tổng Must phải nằm trong ~60% năng lực; phần vượt quá được hạ xuống Should hoặc Could và đưa vào bản phát hành sau. Lan chỉ điều phối buổi thảo luận để mọi bên trình bày bằng tiêu chí, không bằng độ lớn tiếng nói.

**Cách gán nhãn mẫu – Bản phát hành 1.2 (năng lực 40 SP, ngưỡng Must ≤ 24 SP):**

| Story | Bộ phận | Ước lượng | Nhãn | Lý do |
|---|---|---|---|---|
| Hoàn tiền tự động khi chuyến bị lỗi | CSKH | 8 SP | **Must** | Thiếu thì khiếu nại tồn đọng, ảnh hưởng uy tín và quy định thanh toán. |
| Cảnh báo khi tài xế liên tục hủy cuốc | Vận hành | 13 SP | **Must** | Thiếu thì vận hành không kiểm soát được chất lượng dịch vụ. |
| Tặng mã giới thiệu bạn bè | Marketing | 13 SP | **Should** | Tăng trưởng quan trọng nhưng ứng dụng vẫn phát hành được nếu thiếu. |

Tổng Must = 21 SP (~53% năng lực, trong ngưỡng 60%). Marketing không bị bỏ rơi: story của họ ở nhãn Should, được làm nếu còn năng lực, và PO giải thích lý do bằng tiêu chí đã thống nhất.

---

## Kết luận

Quy trình 5 bước giúp mọi story đi qua cùng một đường: **có AC trước, có nhãn MoSCoW theo tiêu chí, đạt DoD chung, rồi mới vào Sprint**. Cả hai tình huống đều được xử lý đúng nguyên tắc Scrum: Sprint Goal được bảo vệ, PO quyết định ưu tiên, Developers quyết định khối lượng.
