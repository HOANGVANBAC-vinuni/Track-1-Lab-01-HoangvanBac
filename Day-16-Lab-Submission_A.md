# Day 16 Submission — AI Alumni Networking

## Members

- [Hoàng văn Bắc]  — Product Lead
- [Hoàng văn Bắc]  — Tech Lead
- [Hoàng văn Bắc]  — Research & Market

---

## 1. Idea Reframed

**Original idea:**
> Xây dựng nền tảng AI hỗ trợ networking tại các sự kiện alumni — gợi ý kết nối thông minh, nhận diện khuôn mặt, và sinh câu mở đầu cuộc trò chuyện.

**Reframed as a product opportunity:**
> Tại các sự kiện alumni offline, networking vẫn đang diễn ra theo kiểu "random" — người tham dự không biết nên gặp ai, ngại bắt chuyện, và rời đi mà không tạo được kết nối có giá trị. Organizer cũng không đo được hiệu quả. Khoảng trống thực sự là: chưa có giải pháp nào kết hợp AI matching + context-aware icebreaker + face recognition để biến một sự kiện offline thành trải nghiệm networking có định hướng. Founding belief: nếu AI có thể gợi ý đúng người, đúng lúc, kèm câu mở đầu phù hợp ngữ cảnh — tỷ lệ kết nối có giá trị tại event sẽ tăng đáng kể.

---

## 2. Customer / Segment Card

- **Segment name:** Sinh viên & cựu sinh viên tham dự sự kiện alumni offline tại các trường đại học lớn ở Việt Nam

- **Operational context:** Sự kiện alumni tổ chức 2–4 lần/năm, quy mô 100–500 người, diễn ra trong 3–6 giờ tại hội trường hoặc không gian sự kiện

- **Recurring workflow:** Đến sự kiện → đăng ký check-in → đi lại trong không gian → cố gắng tìm người quen hoặc người phù hợp để nói chuyện → trao đổi danh thiếp / thêm Zalo → rời đi

- **Pain moment:** Giữa sự kiện, khi đứng giữa hàng trăm người nhưng không biết ai phù hợp để tiếp cận — đặc biệt với sinh viên mới ra trường đang tìm mentor hoặc cơ hội việc làm

- **Why now:** Sau COVID, các sự kiện alumni offline đang phục hồi mạnh. Đồng thời, LLM và face recognition đã đủ mature để deploy trong mobile app với chi phí hợp lý. Chưa có giải pháp nào tại Việt Nam giải quyết bài toán này.

- **Access path:** Tiếp cận qua ban tổ chức sự kiện alumni của các trường (Hội Cựu sinh viên, Phòng Công tác sinh viên), sau đó mở rộng sang các hiệp hội nghề nghiệp và doanh nghiệp tổ chức internal alumni event

**One-sentence description:**
> Sinh viên mới ra trường đang tham dự sự kiện alumni, muốn tìm mentor hoặc cơ hội việc làm nhưng không biết nên tiếp cận ai trong hàng trăm người có mặt.

---

## 3. Need Map (2–3 needs)

### Need #1 (priority) — Không biết nên gặp ai

- **Statement (JTBD):** When I arrive at an alumni event with hundreds of attendees, I want to know which specific people I should approach based on my goals, so I can make meaningful connections instead of wandering randomly.

- **Current workaround:** Hỏi ban tổ chức, nhìn name tag, hỏi bạn bè quen biết, hoặc chỉ đứng chờ người khác tiếp cận trước

- **Pain signal:** Mất 1–2 giờ đầu không kết nối được ai có giá trị; rời sự kiện chỉ với 1–2 danh thiếp không liên quan đến mục tiêu

- **Evidence / proxy evidence:** Khảo sát nội bộ tại các sự kiện alumni cho thấy >60% người tham dự cảm thấy "không biết bắt đầu từ đâu"; LinkedIn báo cáo 85% việc làm được tìm thấy qua networking nhưng chỉ 25% người tự tin networking tại sự kiện offline

- **Why underserved:** LinkedIn không tối ưu cho offline event realtime; Meetup không có matching thông minh; không có giải pháp nào kết hợp context sự kiện + profile matching + realtime suggestion

---

### Need #2 — Ngại bắt chuyện, không biết nói gì

- **Statement (JTBD):** When I want to approach someone I've been matched with at an event, I want a personalized conversation starter based on our shared context, so I can open the conversation naturally without feeling awkward.

- **Current workaround:** Tự nghĩ câu hỏi chung chung ("Bạn học ngành gì?"), nhờ người quen giới thiệu, hoặc không tiếp cận vì ngại

- **Pain signal:** Tỷ lệ "ghosting" cao — người được gợi ý nhưng không dám tiếp cận; stress xã hội đặc biệt với sinh viên mới ra trường

- **Evidence / proxy evidence:** Nghiên cứu về social anxiety cho thấy 40% người trẻ gặp khó khăn khi bắt đầu cuộc trò chuyện với người lạ trong môi trường professional; các app như Bumble Bizz thành công với tính năng icebreaker prompt

- **Why underserved:** Không có giải pháp nào sinh câu gợi ý dựa trên context cụ thể của sự kiện + profile của cả hai người

---

### Need #3 — Organizer không đo được hiệu quả networking

- **Statement (JTBD):** When I organize an alumni event, I want to measure how many meaningful connections were made, so I can improve future events and demonstrate ROI to stakeholders.

- **Current workaround:** Đếm số người tham dự, gửi survey sau sự kiện (tỷ lệ phản hồi thấp), hoặc không đo gì cả

- **Pain signal:** Không có dữ liệu để cải thiện event; khó thuyết phục ban lãnh đạo tăng ngân sách cho sự kiện alumni

- **Evidence / proxy evidence:** Các event platform như Hopin và Airmeet đã thành công với analytics dashboard cho organizer; nhu cầu đo ROI của event ngày càng tăng trong bối cảnh ngân sách bị siết

- **Why underserved:** Các giải pháp hiện tại chỉ đo attendance, không đo chất lượng networking

---

## 4. Strategy Statement

For **students and young alumni (18–30) attending offline alumni events at Vietnamese universities**

who struggle with **not knowing who to approach and how to start conversations in a crowd of hundreds**,

our product helps them **make 3–5 meaningful connections per event aligned with their career goals**

through **AI-powered real-time matching based on profile embeddings + context-aware icebreaker generation using event knowledge**,

unlike **LinkedIn (not optimized for offline realtime), Meetup (no smart matching), or manual networking (random and anxiety-inducing)**,

because we can leverage **event-specific knowledge base (agenda, speakers, topics) combined with user profile vectors to generate highly contextual suggestions that generic platforms cannot replicate**.

---

## 5. Moat Hypothesis

**Moat mechanism:** Domain-learning flywheel + Workflow embedding

If we deploy in **50 alumni events** in the same vertical (university alumni networks), the following improve:

1. **Matching quality** — model học được pattern kết nối thành công trong ngữ cảnh alumni Việt Nam (ngành học, career path, intent type) → gợi ý ngày càng chính xác hơn
2. **Icebreaker relevance** — knowledge base tích lũy từ hàng trăm event → câu gợi ý ngày càng tự nhiên và phù hợp văn hóa hơn
3. **Organizer lock-in** — khi organizer đã dùng dashboard analytics và thấy ROI, chi phí chuyển đổi sang giải pháp khác rất cao (data history, workflow quen thuộc)

**Why competitors cannot easily replicate this:**
> Để replicate cần đồng thời có: (1) dataset kết nối alumni Việt Nam đủ lớn để train matching model, (2) knowledge base từ hàng trăm event đã diễn ra, và (3) trust từ organizer đã dùng qua nhiều event. Một competitor mới không thể có cả ba thứ này cùng lúc — đây là flywheel cần thời gian để build.

---

## 6. Initial TAM / SAM / SOM View

| Layer | Estimate | Logic tính toán | Confidence |
|---|---|---|---|
| TAM | $90K–$560K/year | 200–400 events/năm × $450–$1,400/event = $90K–$560K | low |
| SAM | $45K–$200K/year | Top 50 trường hoạt động tích cực (VNU, HCMUT, NEU, FTU, UEH...) × 2–3 events/năm = ~100–150 events; × $450–$1,400 = $45K–$210K | low–med |
| SOM | $10K–$40K/year (12–24 tháng) | 10–20 pilot events năm đầu; avg $1,000/event (freemium → paid); conversion ~50% | med |

**Top 3 unknowns requiring further research:**
1. Willingness to pay của organizer — hiện chưa có data về ngân sách tech của ban tổ chức alumni tại Việt Nam
2. Tỷ lệ opt-in face recognition — privacy concern tại Việt Nam có thể ảnh hưởng đến adoption của tính năng core
3. Frequency thực tế của alumni events — con số 500 events/năm là ước tính, cần validate với Hội Cựu sinh viên các trường

**Judgment:**
- [x] Worth pursuing but not now — cần validate willingness to pay và privacy acceptance trước khi build full product. Nên chạy 2–3 pilot event với MVP stripped-down (chỉ matching + icebreaker, không có face recognition) để có data thực tế.

---

## 7. Positioning Note (2 sentences)

**What we are:**
> AI networking assistant cho sự kiện alumni offline — giúp người tham dự biết nên gặp ai và nói gì, ngay tại thời điểm sự kiện diễn ra.

**What we are not / not yet:**
> Chúng tôi không phải LinkedIn hay event management platform — chúng tôi là layer AI chạy bên trên sự kiện offline, và hiện tại chỉ tập trung vào alumni events tại Việt Nam trước khi mở rộng sang các loại event khác.

---

## 8. Self-assessment before Day 17

**Mắt xích yếu nhất hiện tại:**
> Market Size — con số TAM/SAM/SOM còn dựa nhiều vào assumption, chưa có data thực tế về willingness to pay của organizer và frequency của alumni events tại Việt Nam. Cần ít nhất 5–10 cuộc phỏng vấn với organizer trước khi tự tin với market sizing.

**Open questions muốn khám phá thêm ở Day 17:**

1. MVP scope nên là gì? Có nên bỏ face recognition ra khỏi MVP để giảm complexity và privacy risk không?
2. Assumption nào cần validate trước tiên — willingness to pay hay product-market fit (người dùng có thực sự dùng matching suggestion không)?
3. Experiment nào có thể chạy trong 2 tuần đầu với chi phí thấp nhất để validate core need?

---

## Appendix — AI Critique Log (Structured Critique Prompt)

*Ghi lại kết quả chạy Structured Critique Prompt và quyết định của team:*

| Issue | AI flagged? | Team decision | Lý do |
|---|---|---|---|
| Customer too broad | Có — ban đầu định nghĩa "sinh viên và alumni" quá rộng | Accept — thu hẹp xuống "18–30, tham dự offline event, đang tìm mentor/job" | Cụ thể hơn, có pain moment rõ |
| Need is actually a solution | Có — Need #1 ban đầu viết "cần app gợi ý kết nối" | Accept — rewrite theo JTBD, focus vào outcome "make meaningful connections" | Đúng hướng |
| Lack of evidence | Có — Need #3 thiếu evidence | Partial — thêm proxy evidence từ Hopin/Airmeet, nhưng thừa nhận cần validate thêm | Không bịa số |
| Strategy too generic | Có — strategy statement ban đầu không nêu rõ distinct approach | Accept — thêm "event-specific knowledge base + profile vectors" | Tạo sự khác biệt rõ hơn |
| Moat too weak | Có — ban đầu chỉ nói "AI matching tốt hơn" | Accept — reframe thành flywheel cụ thể với 3 cơ chế | Có logic compound rõ ràng |

---