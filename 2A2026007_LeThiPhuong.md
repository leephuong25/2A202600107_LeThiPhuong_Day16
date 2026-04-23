# Day 16 Submission v1



---

## 1. Idea Reframed

**Original idea:**
> Một hệ thống bài tập thông minh tập trung vào Toán lớp 10, đóng vai trò như một gia sư Socratic đưa ra các gợi ý từng bước (hint-based) nhưng tuyệt đối không cung cấp đáp án cuối cùng, nhằm dạy học sinh cách tư duy.

**Reframed as a product opportunity:**

> **Khoảng trống quan sát được:**  
> Học sinh Việt Nam đang bị mắc kẹt trong vòng lặp "bế tắc → tra giải → chép → nộp bài → không hiểu". Vòng lặp này không phải do lười biếng — mà do *không có công cụ nào dạy tư duy từng bước trong lúc làm bài một mình lúc tối muộn*.
>
> **Tại sao giải pháp hiện tại thất bại:**  
> — Sách giải (Loigiaihay, VietJack): Đưa đáp án ngay, không scaffold, không hỏi "em hiểu chưa?"  
> — Gia sư: Có khả năng dẫn dắt nhưng không available 24/7, chi phí 200.000–500.000 VNĐ/buổi  
> — ChatGPT / Gemini: Giải hộ hoàn toàn nếu hỏi đúng cách — không có cơ chế kiểm soát nào  
> — Google Classroom / LMS trường: Chỉ là nơi giao bài, không có logic hỗ trợ tư duy
>
> **Founding belief (non-obvious insight):**  
> Học sinh không cần AI thông minh hơn — họ cần AI *biết im lặng đúng lúc*. Giá trị cốt lõi không nằm ở chất lượng giải toán, mà nằm ở **cơ chế kiểm soát luồng gợi ý theo tiến trình tư duy thực sự của học sinh**. Đây là thứ không app nào ở Việt Nam đang làm.

---

## 2. Customer / Segment Card

### Segment A — Học sinh THPT Lớp 10 (Primary User)

| Trường | Nội dung |
|---|---|
| **Segment name** | Học sinh lớp 10 trường THPT tư thục / bán công tại TP.HCM và Hà Nội |
| **Operational context** | Một mình tại nhà sau 8 giờ tối, dùng điện thoại Android hoặc tablet, internet ổn định |
| **Recurring workflow** | Nhận bài tập từ giáo viên → thử làm → bế tắc sau 5–10 phút → tra Google/sách giải → chép → nộp → lặp lại hôm sau |
| **Pain moment** | Gặp bài chưa biết bắt đầu từ đâu — não trống, tự ti, chọn con đường kháng cự nhất: copy giải sẵn |
| **Why now** | Sau COVID, thói quen dùng điện thoại học đã bình thường hóa. Phụ huynh ngày càng lo ngại tình trạng học vẹt. Bộ GD đang push đổi mới đánh giá năng lực — tạo áp lực cho giáo viên phải chứng minh học sinh *hiểu thật* |
| **Access path** | **B2B2C** — tiếp cận học sinh qua giáo viên giao bài, không phải B2C tự mua app |

**One-sentence description:**
> Học sinh lớp 10 bị bế tắc khi làm bài Toán một mình vào buổi tối, chưa có công cụ nào giúp họ *tư duy từng bước có giám sát* mà không lộ đáp án.

---

### Segment B — Giáo viên Toán THPT (Decision Maker & Activator)

| Trường | Nội dung |
|---|---|
| **Segment name** | Giáo viên Toán lớp 10, trường THPT tư thục / bán công, 5–15 năm kinh nghiệm |
| **Operational context** | Dạy 2–4 lớp/ngày, giao bài tập về nhà định kỳ, không có cơ chế xem học sinh làm bài như thế nào |
| **Recurring workflow** | Soạn bài → dạy → giao bài về nhà → thu bài → chấm tay → không biết ai hiểu thật ai chép |
| **Pain moment** | Phát hiện học sinh hổng kiến thức chỉ khi chấm kiểm tra — quá muộn để sửa trước kỳ thi |
| **Access path** | Qua tổ trưởng bộ môn hoặc BGH trường tư — cần demo + chứng minh ROI rõ ràng |


---

## 3. Need Map

### Need #1 — Học sinh cần người dẫn dắt tư duy từng bước lúc làm bài một mình (Ưu tiên cao nhất)

- **Statement (JTBD):**  
  *Khi tôi bế tắc với bài Toán lúc tối muộn, tôi muốn được gợi ý từng bước nhỏ — không giải hộ — để tôi tự hiểu và không cảm thấy bị phán xét khi sai.*

- **Current workaround:**  
  Tra Loigiaihay / VietJack → chép đáp án. Hỏi bạn qua Zalo. Gõ vào ChatGPT "giải giúp em". Bỏ qua bài đó.

- **Pain signal:**  
  — Loigiaihay đạt ~20–30 triệu pageviews/tháng (Similarweb proxy) — phần lớn là học sinh tra giải sẵn  
  — Giáo viên phản ánh bài nộp của cả lớp giống nhau đến mức đáng ngờ  
  — Tỷ lệ học sinh Việt Nam đạt điểm cao nhưng không giải được bài biến thể là vấn đề được báo cáo trong đề thi THPT quốc gia nhiều năm

- **Evidence / proxy evidence:**  
  *(Proxy — chưa có user research thực tế từ team)*  
  Khan Academy báo cáo engagement cao nhất ở tính năng "Hint" step-by-step — chứng minh học sinh muốn được dẫn dắt, không chỉ muốn đáp án, *nếu được thiết kế đúng*.

- **Why underserved:**  
  Các giải pháp hiện tại không có cơ chế kiểm soát: Loigiaihay/VietJack cho đáp án ngay; ChatGPT giải hộ nếu prompt đúng; YouTube không tương tác với bài cụ thể của học sinh; gia sư thì đắt và không available 24/7.


---

### Need #2 — Giáo viên cần biết học sinh hổng chỗ nào *trước* tiết học ngày hôm sau

- **Statement (JTBD):**  
  *Là giáo viên, tôi muốn biết cả lớp đang mắc kẹt ở khái niệm nào — tối hôm trước, không phải sau khi chấm bài kiểm tra — để tôi điều chỉnh giáo án kịp thời.*

- **Current workaround:**  
  Chấm tay sau khi thu bài (mất 1–3 tiếng). Hỏi miệng đầu giờ (không representative). Quan sát cảm tính. Chờ kết quả kiểm tra 15 phút (quá trễ).

- **Pain signal:**  
  — Nhiều giáo viên THPT tư thục đang bị BGH yêu cầu báo cáo learning outcome định kỳ — tạo nhu cầu có data  
  — Xu hướng trường tư chuyển sang "học bằng chứng" (evidence-based teaching) ngày càng rõ  
  *(Inferred — cần xác nhận bằng interview giáo viên thật)*

- **Evidence / proxy evidence:**  
  Google Classroom, Kahoot, Quizizz đều có tính năng analytics cho giáo viên và được dùng rộng rãi ở trường tư — chứng minh nhu cầu có data về học sinh là thật. Vấn đề: các tool này không có Heatmap theo khái niệm Toán cụ thể.

- **Why underserved:**  
  Không có công cụ Việt Nam nào cung cấp real-time mistake heatmap theo từng khái niệm Toán 10. Các LMS hiện tại chỉ tracking nộp bài / điểm tổng — không phân tích được "hổng ở bước nào trong bài toán".


---

### Need #3 — Học sinh cần môi trường tâm lý an toàn để dám thử và sai

- **Statement (JTBD):**  
  *Là học sinh hay lo lắng bị chê điểm kém hoặc bị bạn bè đánh giá, tôi muốn được sửa sai trong không gian riêng tư — không bị ghi điểm, không bị phán xét — để tôi dám thử dù chưa chắc đúng.*

- **Current workaround:**  
  Không làm bài, hoặc chép bạn để tránh nộp bài sai. Không giơ tay hỏi trên lớp.

- **Why underserved:**  
  Không có app học Toán Việt Nam nào thiết kế psychological safety và persona cảm xúc làm core experience — toàn bộ thị trường đang tập trung vào nội dung, không phải trải nghiệm cảm xúc.

---

## 4. Strategy Statement

> Dành cho **học sinh THPT lớp 10 tại trường tư thục Việt Nam** đang bế tắc khi tự học Toán về nhà,  
> sản phẩm giúp họ **tự tìm ra lời giải qua gợi ý thích ứng từng bước — không bị lộ đáp án**  
> thông qua **cơ chế Anti-answer kết hợp Effort Tracking, scaffold động, và môi trường tâm lý không phán xét**,  
> khác với Loigiaihay / VietJack (đưa đáp án ngay) và ChatGPT (giải hộ nếu biết cách hỏi),  
> vì chúng tôi tích hợp trực tiếp vào quy trình giao bài của giáo viên — **tạo switching cost hai chiều**: học sinh không thể bypass, giáo viên có data thật để dạy.


---

## 5. Moat Hypothesis

**Moat mechanism:**  
*Behavioral data flywheel kết hợp institutional lock-in* — càng nhiều học sinh dùng, Effort Validation Engine càng chính xác hơn; giáo viên đã upload curriculum thì switching cost cao; trường đã mua thì khó đổi vendor giữa năm học.

**Nếu triển khai ở quy mô, những điều sau sẽ cải thiện:**

1. **Độ chính xác Effort Validation Engine** — phân biệt genuine vs fake effort tinh vi hơn khi có thêm mẫu hành vi học sinh Việt làm Toán (pattern bypass địa phương rất khác với dataset quốc tế)
2. **Chất lượng Heatmap giáo viên** — pattern lỗi theo từng chương, từng khái niệm được làm giàu liên tục; trở thành benchmark ngành sau 2–3 năm
3. **Curriculum lock-in** — giáo viên đã upload và calibrate Grounding Knowledge cho tool → switching cost cao → retention tự nhiên mà không cần gimmick

**Tại sao đối thủ khó copy:**
> Không phải vì thuật toán khó — mà vì **dataset hành vi học sinh Việt Nam làm Toán theo từng khái niệm** là thứ không thể mua hay transfer. Ai có data này trước, người đó định nghĩa được benchmark "nỗ lực thật sự" và "điểm nghẽn kiến thức" cho thị trường Việt. Thêm vào đó, mỗi trường đã onboard là một moat nhỏ — thoát ra nghĩa là giáo viên phải upload lại toàn bộ curriculum từ đầu.


---

## 6. Initial TAM / SAM / SOM View

| Layer | Estimate | Key Assumptions | Confidence |
|---|---|---|---|
| **TAM** | ~$600M–$900M | Thị trường EdTech K-12 Việt Nam (học thêm + tool học) × dài hạn mở rộng sang môn khác và ASEAN | Low |
| **SAM** | ~$15–$30M/năm | ~1 triệu học sinh lớp 10 VN × 20% trường tư/bán công có khả năng trả × ARPU $75–150/học sinh/năm (school subscription) | Low–Med |
| **SOM (Year 1–2)** | ~$300K–$700K | 10–15 trường pilot tại TP.HCM + Hà Nội × 200–500 học sinh/trường × $50–80/học sinh/năm | Med |


**Top 3 unknowns cần nghiên cứu trước khi build:**

1. **Willingness-to-pay của BGH trường tư:** Họ có sẵn sàng trả ~50.000–100.000 VNĐ/học sinh/năm cho tool học Toán không? Hay họ kỳ vọng miễn phí như Google Classroom?
2. **Activation rate của giáo viên:** Bao nhiêu % giáo viên sau khi được training sẽ thực sự upload curriculum và enforce học sinh dùng trong quy trình giao bài — sau tháng đầu hứng khởi?
3. **Hiệu quả đo được:** Sau 1 học kỳ, học sinh dùng app có cải thiện điểm Toán và tỷ lệ giải bài biến thể không? Đây là KPI duy nhất giúp justify giá, renew hợp đồng, và mở rộng.

**Judgment:**
- [x] **Worth pursuing — với điều kiện validate 3 unknowns trên trước khi build full-stack**  
  Nếu Unknown #1 và #2 cho kết quả tích cực → green light build MVP. Nếu không → pivot model trước khi đốt engineering resource.


---

## 7. Positioning Note

**Chúng tôi là:**
> Hệ thống học Toán có AI đóng vai người dẫn dắt tư duy — không phải người giải bài — tích hợp vào quy trình giao bài của giáo viên để học sinh tự tìm ra lời giải và giáo viên có dữ liệu thật về điểm nghẽn kiến thức của cả lớp.

**Chúng tôi không phải / chưa phải:**
> — Không phải app giải toán (đối lập trực tiếp với Loigiaihay, PhotoMath, Mathway)  
> — Không phải LMS tổng quát (không cạnh tranh với Google Classroom, VietSchool, MISA)  
> — Không phải AI gia sư all-in-one (không thay thế con người — bổ trợ giáo viên)  
> — Chưa phải đa môn — **Toán 10 là beachhead duy nhất**, không mở rộng trước khi có product-market fit rõ ràng


---




