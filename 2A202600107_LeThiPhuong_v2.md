# Day 16 Submission v2

## 1. Idea reframed

Original idea:
> Học sinh Toán lớp 10 Việt Nam không thiếu tài liệu giải — họ thiếu lý do để tự giải. Sản phẩm dùng AI dẫn dắt từng bước thay vì đưa đáp án, kết hợp dashboard phân tích điểm nghẽn kiến thức cho giáo viên.

Reframed as a product opportunity:
> Chúng tôi quan sát thấy một "khoảng trống động lực": học sinh thường chọn copy đáp án từ ChatGPT/Loigiaihay vì việc tự giải quá "ma sát" và chậm chạp. Cơ hội nằm ở việc thiết kế một hệ thống nơi việc **tự giải thông qua các micro-steps (≤ 10s) trở nên nhanh hơn, dễ dàng hơn và có cảm giác tiến bộ rõ rệt hơn so với việc đi copy**. Chúng tôi tin rằng bằng cách tối ưu cho "tốc độ giải bài tiếp theo" (next-problem speed) thay vì chỉ bài hiện tại, chúng tôi sẽ thay đổi hoàn toàn hành vi học tập của học sinh.

---

## 2. Customer / Segment Card

- **Segment name:** Học sinh lớp 10 trường THPT tư thục/bán công tại các thành phố lớn (TP.HCM, Hà Nội).
- **Operational context:** Ngồi học một mình tại nhà sau 8h tối, điện thoại/tablet luôn mở sẵn nhiều tab giải bài (ChatGPT, Loigiaihay) để "cứu cánh" khi bế tắc.
- **Recurring workflow:** Nhận bài tập về nhà → thử làm → bế tắc sau 5 phút → mở tab khác copy đáp án → nộp bài cho xong nhưng không hiểu bản chất.
- **Pain moment:** Cảm giác "não trống rỗng" khi gặp bài khó lúc tối muộn, không có ai để hỏi ngay lập tức, dẫn đến việc chọn con đường ít nỗ lực nhất là sao chép.
- **Why now:** Áp lực đổi mới đánh giá năng lực của Bộ GD khiến các trường tư phải chứng minh "học thật - kết quả thật"; sự phổ biến của AI khiến việc gian lận trở nên quá dễ dàng, buộc phải có giải pháp đối trọng.
- **Access path:** Mô hình B2B2C — tiếp cận thông qua Ban giám hiệu và Tổ trưởng bộ môn Toán để tích hợp vào quy trình giao bài chính thức của trường.

One-sentence description:
> Những học sinh "muốn hiểu bài nhưng dễ bỏ cuộc", cần một người dẫn dắt để việc tự giải bài tập trở nên hấp dẫn và ít tốn sức hơn việc đi copy.

---

## 3. Need Map (2–3 needs)

### Need #1 (Ưu tiên)
- **Statement (JTBD):** Khi tôi bị bế tắc với một bài toán lúc tối muộn, tôi muốn có một cách để tiếp tục tiến về phía trước mà không cần phải rời khỏi ứng dụng, để tôi có thể hoàn thành bài tập về nhà nhanh hơn và cảm thấy tự tin hơn về sự tiến bộ của mình.
- **Current workaround:** Chuyển tab sang ChatGPT hoặc Loigiaihay để sao chép toàn bộ lời giải.
- **Pain signal:** Tỷ lệ thoát (bounce rate) cực cao khi học sinh gặp phải một bước giải "khó"; 80% bài tập nộp trong một lớp trông giống hệt nhau một cách đáng ngờ.
- **Evidence / proxy evidence:** Tỷ lệ tương tác cao của Khan Academy đối với các tính năng "Gợi ý" (Hint); sự thành công của Duolingo trong việc biến việc học thành một chuỗi các chiến thắng nhỏ, không tốn sức.
- **Why underserved:** Các công cụ hiện tại hoặc là đưa ra đáp án ngay lập tức (Loigiaihay) hoặc là hỗ trợ quá mức mà không theo dõi được mức độ hiểu bài của học sinh (ChatGPT).

### Need #2
- **Statement (JTBD):** Là giáo viên, tôi muốn biết chính xác cả lớp đang "hổng" kiến thức ở bước logic nào trước giờ lên lớp, để tôi có thể điều chỉnh giáo án tập trung vào đúng điểm yếu đó.
- **Current workaround:** Chấm tay bài tập về nhà (mất 2-3 tiếng) hoặc hỏi miệng đầu giờ (không chính xác).
- **Pain signal:** Giáo viên mất nhiều thời gian chấm bài nhưng học sinh vẫn sai cùng một lỗi trong bài kiểm tra định kỳ.
- **Evidence / proxy evidence:** Sự phổ biến của Google Classroom/Quizizz trong việc theo dõi tiến độ, nhưng các tool này thiếu chiều sâu về phân tích bước giải (reasoning steps).
- **Why underserved:** Chưa có công cụ nào cung cấp "Heatmap theo Concept" dựa trên dữ liệu thực tế từ quá trình giải bài từng bước của học sinh.

### Need #3 (optional)
- **Statement (JTBD):** Khi bắt đầu làm bài, tôi muốn thấy kết quả ngay lập tức, để tôi có thêm động lực để tiếp tục hoàn thành toàn bộ bài tập.
- **Current workaround:** Không có — học sinh thường chỉ thấy kết quả sau khi đã nộp bài và chờ giáo viên chấm.
- **Pain signal:** Tỷ lệ bỏ cuộc (drop-off) cực cao trong 2 phút đầu tiên nếu không thấy "lối thoát" cho bài toán.
- **Evidence / proxy evidence:** "First 60-second hook" trong game design; quy luật "Small Wins" trong tâm lý học hành vi.
- **Why underserved:** Các ứng dụng học tập hiện tại thường quá tập trung vào nội dung mà quên mất thiết kế trải nghiệm cảm xúc (cảm giác tiến bộ) cho người học.

---

## 4. Strategy Statement

For **học sinh lớp 10 trường THPT tư thục**
who struggle with **cảm giác bế tắc và thói quen copy đáp án khi làm bài về nhà**,
our product helps them **tự giải bài tập nhanh hơn và ít nỗ lực hơn việc đi copy**
through **cơ chế micro-steps (≤ 10s) dẫn dắt thông minh và hiển thị tiến độ tức thì (Progress Visibility)**,
unlike **Loigiaihay (cho đáp án ngay) hay ChatGPT (không có guardrail)**,
because we can leverage **sự tích hợp trực tiếp vào quy trình của nhà trường (B2B2C) để biến việc tự giải thành con đường duy nhất được ghi nhận điểm số**.

---

## 5. Moat Hypothesis

**Moat mechanism:** Khóa học liệu (Curriculum Lock-in) & Vòng lặp dữ liệu hành vi (Behavioral Data Flywheel).

Nếu chúng tôi triển khai **10** lần tại **các trường THPT tư thục tại TP.HCM**, các yếu tố sau sẽ được cải thiện:
1. **Curriculum lock-in:** Giáo viên đã upload và tinh chỉnh học liệu trên hệ thống sẽ có switching cost rất cao.
2. **Interaction Validation accuracy:** AI học được các mẫu hình bypass/gian lận đặc thù của học sinh Việt Nam để ngăn chặn hiệu quả hơn.
3. **Heatmap precision:** Dữ liệu về điểm nghẽn kiến thức theo từng khái niệm Toán 10 trở nên cực kỳ chính xác, tạo ra giá trị không thể thay thế cho giáo viên.

Why competitors cannot easily replicate this:
> Đối thủ quốc tế thiếu sự am hiểu về chương trình học và hành vi học tập đặc thù tại Việt Nam; đối thủ nội địa (sách giải) thiếu nền tảng công nghệ để xây dựng vòng lặp dữ liệu hành vi (behavioral data loop).

---

## 6. Initial TAM / SAM / SOM view

| Layer | Estimate | Key assumptions | Confidence |
|---|---|---|---|
| TAM | $600M–$900M | Thị trường EdTech K-12 Việt Nam và tiềm năng mở rộng ASEAN. | Low |
| SAM | $15M–$30M | 200,000 học sinh lớp 10 trường tư/quốc tế với ARPU $75–$150/năm. | Med |
| SOM | $300K–$700K | 15 trường pilot đầu tiên tại TP.HCM & Hà Nội trong 18 tháng. | High |

**Top 3 unknowns requiring further research:**
1. **Willingness-to-pay của BGH:** Liệu các trường có sẵn sàng trả phí SaaS thay vì bắt học sinh tự mua lẻ?
2. **Teacher activation:** Tỷ lệ giáo viên thực sự thay đổi giáo án dựa trên Heatmap dữ liệu là bao nhiêu?
3. **Bypass resistance:** Học sinh sẽ mất bao lâu để tìm ra cách "hack" hệ thống micro-steps mới?

**Judgment:**
- [x] Đáng để theo đuổi nhưng không phải ngay bây giờ (cần xác minh **Mức độ sẵn sàng chi trả của BGH** và **Tỷ lệ kích hoạt của giáo viên** trước)

---

## 7. Positioning Note (2 sentences)

**What we are:**
> Một hệ thống dẫn dắt tư duy Toán học bằng AI, biến việc tự giải bài tập thành một trải nghiệm "ít ma sát" và đầy cảm giác thành tựu cho học sinh.

**What we are not / not yet:**
> Chúng tôi không phải là một kho đáp án hay công cụ giải bài hộ, và hiện tại chỉ tập trung duy nhất vào môn Toán lớp 10 để đạt được PMF.
