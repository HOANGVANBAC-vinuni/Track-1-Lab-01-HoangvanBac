# Day 16 Submission — AI Alumni Networking

## Members

- [Hoàng văn Bắc]  — Product Lead
- [Hoàng văn Bắc]  — Tech Lead
- (auto-model-AI) — Research & Market

---

## 1. Idea Reframed

**Original idea:**
> Xây dựng nền tảng AI hỗ trợ networking tại các sự kiện alumni — gợi ý kết nối thông minh, nhận diện khuôn mặt, và sinh câu mở đầu cuộc trò chuyện.

**Reframed as a product opportunity:**
> Tại các sự kiện alumni offline, networking vẫn đang diễn ra theo kiểu "random" — người tham dự không biết nên gặp ai, ngại bắt chuyện, và rời đi mà không tạo được kết nối có giá trị. Organizer cũng không đo được hiệu quả. Khoảng trống thực sự là: chưa có giải pháp nào kết hợp AI matching + context-aware icebreaker để biến một sự kiện offline thành trải nghiệm networking có định hướng. Founding belief: nếu AI có thể gợi ý đúng người, đúng lúc, kèm câu mở đầu phù hợp ngữ cảnh — tỷ lệ kết nối có giá trị tại event sẽ tăng đáng kể. Face recognition là tính năng bổ sung sau khi core value đã được validate.

---

## 2. Customer / Segment Card

- **Segment name:** Sinh viên & cựu sinh viên (18–30 tuổi) tham dự sự kiện alumni offline tại các trường đại học lớn ở Việt Nam

- **Operational context:** Sự kiện alumni tổ chức 2–4 lần/năm, quy mô 100–500 người, diễn ra trong 3–6 giờ tại hội trường hoặc không gian sự kiện

- **Recurring workflow:** Đến sự kiện → đăng ký check-in → đi lại trong không gian → cố gắng tìm người quen hoặc người phù hợp để nói chuyện → trao đổi danh thiếp / thêm Zalo → rời đi

- **Pain moment:** Giữa sự kiện, khi đứng giữa hàng trăm người nhưng không biết ai phù hợp để tiếp cận — đặc biệt với sinh viên mới ra trường đang tìm mentor hoặc cơ hội việc làm

- **Why now:** Sau COVID, các sự kiện alumni offline đang phục hồi mạnh. LLM đã đủ mature để deploy AI matching và icebreaker trong mobile app với chi phí hợp lý. Chưa có giải pháp nào tại Việt Nam giải quyết bài toán này.

- **Access path:** Tiếp cận qua ban tổ chức sự kiện alumni của các trường (Hội Cựu sinh viên, Phòng Công tác sinh viên), sau đó mở rộng sang các hiệp hội nghề nghiệp và doanh nghiệp tổ chức internal alumni event

**One-sentence description:**
> Sinh viên mới ra trường đang tham dự sự kiện alumni, muốn tìm mentor hoặc cơ hội việc làm nhưng không biết nên tiếp cận ai trong hàng trăm người có mặt.

---

## 3. Need Map (2–3 needs)

### Need #1 (priority) — Không biết nên gặp ai

- **Statement (JTBD):** When I arrive at an alumni event with hundreds of attendees, I want to know which specific people I should approach based on my goals, so I can make meaningful connections instead of wandering randomly.

- **Current workaround:** Hỏi ban tổ chức, nhìn name tag, hỏi bạn bè quen biết, hoặc chỉ đứng chờ người khác tiếp cận trước

- **Pain signal:** Mất 1–2 giờ đầu không kết nối được ai có giá trị; rời sự kiện chỉ với 1–2 danh thiếp không liên quan đến mục tiêu

- **Evidence / proxy evidence (thực tế):**
  - Gen Z trung bình chỉ có **16 mối quan hệ nghề nghiệp mạnh**, so với 21 của Millennials và 40 của Gen X *(Freeman 2025 Gen Z Report / The Harris Poll — US data, dùng làm proxy cho xu hướng toàn cầu)*
  - **86% Gen Z** muốn công ty tăng chi tiêu cho live events để xây dựng kết nối; **89%** đồng ý rằng các mối quan hệ tạo ra tại in-person events là thiết yếu để xây dựng sự tự tin nghề nghiệp *(Freeman 2025 Gen Z Report / The Harris Poll, ~2,000 US professionals — proxy cho Gen Z VN cùng thế hệ digital native)*
  - **69% Gen Z** nói sự phát triển của công nghệ khiến họ cảm thấy ít kết nối và cô lập hơn với đồng nghiệp và ngành *(Freeman 2025 Gen Z Report / The Harris Poll)*
  - **Assumption cần validate:** Mức độ pain tại VN có thể khác US — sinh viên VN có văn hóa networking qua mối quan hệ gia đình/thầy cô nhiều hơn. Cần phỏng vấn 5–10 sinh viên VN để xác nhận.

- **Why underserved:** LinkedIn không tối ưu cho offline event realtime; Meetup không có matching thông minh; không có giải pháp nào kết hợp context sự kiện + profile matching + realtime suggestion

---

### Need #2 — Ngại bắt chuyện, không biết nói gì

- **Statement (JTBD):** When I want to approach someone I've been matched with at an event, I want a personalized conversation starter based on our shared context, so I can open the conversation naturally without feeling awkward.

- **Current workaround:** Tự nghĩ câu hỏi chung chung ("Bạn học ngành gì?"), nhờ người quen giới thiệu, hoặc không tiếp cận vì ngại

- **Pain signal:** Tỷ lệ "ghosting" cao — người được gợi ý nhưng không dám tiếp cận; stress xã hội đặc biệt với sinh viên mới ra trường

- **Evidence / proxy evidence (thực tế):**
  - Chỉ **42% Gen Z** cảm thấy tự tin khi small talk trong môi trường professional; chỉ **39%** thoải mái khi networking với người trong ngành *(Freeman 2025 Gen Z Report / The Harris Poll — US data, proxy cho xu hướng Gen Z toàn cầu)*
  - **1/3 young professionals (NowGen, 23–46 tuổi)** cho rằng các format networking hiện tại làm giảm giá trị hoặc tăng lo lắng — ngay cả khi đã đến event, người ta vẫn không biết cách bắt chuyện hiệu quả *(Freeman Trends Report, Jul 2025 — GlobeNewswire)*
  - **Assumption cần validate:** Tại VN, sinh viên thường ngại bắt chuyện với người lạ hơn do văn hóa thứ bậc (senpai/junior). Pain này có thể mạnh hơn US, nhưng cần phỏng vấn thực tế để xác nhận.

- **Why underserved:** Không có giải pháp nào sinh câu gợi ý dựa trên context cụ thể của sự kiện + profile của cả hai người

---

### Need #3 — Organizer không đo được hiệu quả networking

- **Statement (JTBD):** When I organize an alumni event, I want to measure how many meaningful connections were made, so I can improve future events and demonstrate ROI to stakeholders.

- **Current workaround:** Đếm số người tham dự, gửi survey sau sự kiện (tỷ lệ phản hồi thấp), hoặc không đo gì cả

- **Pain signal:** Không có dữ liệu để cải thiện event; khó thuyết phục ban lãnh đạo tăng ngân sách — dẫn đến ngân sách bị cắt hoặc event bị tổ chức thưa hơn

- **Evidence / proxy evidence (thực tế):**
  - **51% người tham dự** nói networking hiệu quả là lý do đủ để quay lại một event — nhưng **1/3 young professionals** cho rằng format networking hiện tại làm giảm giá trị hoặc tăng lo lắng *(Freeman Trends Report, Jul 2025)* → gap rõ ràng giữa kỳ vọng và thực tế, organizer cần công cụ để cải thiện
  - Global Event Management Software Market tăng từ **$9.2B (2025) → $32.94B (2035)** *(Spherical Insights, 2025)* — cho thấy organizer toàn cầu đang đầu tư mạnh vào công cụ đo lường và quản lý event
  - **Assumption cần validate:** Organizer alumni tại VN (thường là tình nguyện viên sinh viên, không phải event professional) có thực sự cần đo ROI không, hay đây là pain của corporate event organizer nhiều hơn? Cần phỏng vấn 3–5 ban tổ chức alumni tại VNU, HCMUT để xác nhận.

- **Why underserved:** Các giải pháp hiện tại chỉ đo attendance, không đo chất lượng networking; không có giải pháp nào tích hợp AI matching analytics cho alumni events tại Việt Nam

---

## 4. Strategy Statement

For **students and young alumni (18–30) attending offline alumni events at Vietnamese universities**

who struggle with **not knowing which specific people to approach at a crowded event, leading to random and low-value networking**,

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
3. **Organizer lock-in** — khi organizer (đặc biệt corporate/professional association organizer) đã dùng dashboard analytics và thấy ROI, chi phí chuyển đổi sang giải pháp khác rất cao (data history, workflow quen thuộc). Với alumni event organizer là sinh viên tình nguyện, lock-in đến từ việc event đã có data lịch sử kết nối của trường.

**Why competitors cannot easily replicate this:**
> Để replicate cần đồng thời có: (1) dataset kết nối alumni Việt Nam đủ lớn để train matching model, (2) knowledge base từ hàng trăm event đã diễn ra, và (3) trust từ organizer đã dùng qua nhiều event. Một competitor mới không thể có cả ba thứ này cùng lúc — đây là flywheel cần thời gian để build.

---

## 6. Initial TAM / SAM / SOM View

> Lưu ý: Market sizing được thực hiện sau khi đã có customer, need, strategy rõ ràng. Tất cả con số đều tách biệt facts (có nguồn) và assumptions (team giả định). Platform free cho end-user, revenue từ advertising/sponsorship và freemium premium features.

*Inputs (facts có nguồn):*
- Việt Nam: **234 trường đại học** (174 công + 60 tư), **687,473 sinh viên** năm học 2023–24 *(British Council, dẫn MOET 2024)*
- **~615,000 sinh viên** tuyển sinh 2024 *(VnExpress, dẫn Bộ GD&ĐT 2024)*
- **86% Gen Z** muốn công ty tăng chi tiêu cho live events *(Freeman 2025 Gen Z Report / The Harris Poll)*
- **51% người tham dự** nói networking hiệu quả là lý do đủ để quay lại event *(Freeman Trends Report, Jul 2025)*

*Revenue model — Advertising/Sponsorship (doanh nghiệp tuyển dụng tiếp cận sinh viên):*
- Model phù hợp: **sponsored profile / job posting** (như LinkedIn Jobs) — doanh nghiệp trả để hiển thị cơ hội việc làm đến đúng profile sinh viên tại event
- Benchmark: LinkedIn Job Post VN ~$200–$500/post/30 ngày (assumption, chưa có data chính thức)
- 234 trường × 2 events/năm × avg 2–3 doanh nghiệp sponsor/event × $200/post = **TAM ~$190K–$280K/year** (VN only, assumption thận trọng — alumni event VN ít sponsor hơn corporate event)
- Nếu mở rộng toàn SEA (×10 thị trường): **TAM ~$1.9M–$2.8M/year**

*Revenue model — Freemium (premium features cho organizer/user):*
- Conversion rate freemium → paid thường 2–5%
- Pricing VN phù hợp: ~$2–$3/month (~50K–75K VND, phù hợp purchasing power sinh viên VN)
- 687,000 potential users × 3% × $2–$3/month × 12 = **TAM ~$500K–$750K/year** (nếu đạt full penetration VN)
- Realistic SAM năm 1–2: 5,000–10,000 active users × 3% × $2/month × 12 = **$3.6K–$7.2K/year**

| Layer | Estimate | Key assumptions | Confidence |
|---|---|---|---|
| TAM | $500K–$750K/year | Freemium VN full penetration, pricing $2–$3/month phù hợp purchasing power sinh viên | low |
| SAM | $3.6K–$7.2K/year | 5,000–10,000 active users năm 1–2, freemium conversion 3%, $2/month | low |
| SOM | $500–$2K/year (12–24 tháng) | 500–1,000 paying users giai đoạn validate, $2/month | low–med |

> **Ghi chú:** Advertising model ($190K–$280K/year VN) không được tính vào TAM vì assumption "2–3 doanh nghiệp sponsor/event" tại alumni event VN chưa được validate — alumni event thường do sinh viên tổ chức, ít có sponsor trả tiền. Nếu pivot sang corporate events, advertising sẽ trở thành revenue stream chính.

**Top 3 unknowns requiring further research:**
1. **Revenue model nào phù hợp nhất** — đây là unknown quan trọng nhất, cần quyết định trước khi sizing có ý nghĩa
2. Willingness to pay của sinh viên/organizer tại Việt Nam — purchasing power thấp, freemium khó convert
3. Tỷ lệ doanh nghiệp tuyển dụng sẵn sàng trả cho sponsored matching tại VN — chưa có data

**Judgment:**
- [ ] Worth pursuing now
- [x] Worth pursuing but not now — need thật và demand rõ ràng (Freeman data), nhưng SOM thực tế chỉ $500–$2K/year trong 12–24 tháng đầu — quá nhỏ để justify full product build. Cần validate freemium conversion rate và pricing phù hợp với sinh viên VN qua pilot 5–10 events trước khi commit build.
- [ ] Not worth pursuing as currently framed

---

## 7. Positioning Note (2 sentences)

**What we are:**
> AI networking assistant cho sự kiện alumni offline — giúp người tham dự biết nên gặp ai và nói gì, ngay tại thời điểm sự kiện diễn ra.

**What we are not / not yet:**
> Chúng tôi không phải LinkedIn hay event management platform — chúng tôi là layer AI chạy bên trên sự kiện offline, và hiện tại chỉ tập trung vào alumni events tại Việt Nam trước khi mở rộng sang các loại event khác.

---

## 8. Self-assessment before Day 17

**Trong 6 mắt xích (Idea → Customer → Need → Strategy → Moat → Market Size), mắt xích yếu nhất:**
> Market Size — SOM thực tế chỉ $500–$2K/year trong 12–24 tháng đầu, quá nhỏ để justify full product build. TAM freemium VN đạt $500K–$750K/year nhưng chỉ khi đạt full penetration — đây là assumption rất lớn. Cần validate freemium conversion rate và pricing phù hợp với sinh viên VN qua pilot trước khi tự tin với con số này.

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
| Lack of evidence | Có — Need #3 thiếu evidence | Accept — thêm evidence từ Freeman Trends Report (51% attendees, 1/3 young professionals) và G2/Spherical Insights market data | Không bịa số |
| Strategy too generic | Có — strategy statement ban đầu không nêu rõ distinct approach | Accept — thêm "event-specific knowledge base + profile vectors" | Tạo sự khác biệt rõ hơn |
| Moat too weak | Có — ban đầu chỉ nói "AI matching tốt hơn" | Accept — reframe thành flywheel cụ thể với 3 cơ chế | Có logic compound rõ ràng |

---

## Sources — Research & Market (verified, April 2025)

> Chỉ giữ lại sources có primary research rõ ràng. Đã loại bỏ: blog tổng hợp không có primary source, vendor blogs, editorial estimates.

| # | Claim | Primary Source | URL |
|---|---|---|---|
| 1 | Gen Z avg 16 strong relationships vs 21 (Millennials) vs 40 (Gen X); 86% muốn tăng chi tiêu live events; 89% relationships tại events thiết yếu cho career confidence; 69% cảm thấy ít kết nối hơn do công nghệ | **Freeman 2025 Gen Z Report** — conducted with The Harris Poll, ~2,000 US professionals (Jan 2025) | https://www.globenewswire.com/news-release/2025/01/28/3016515/0/en/New-Research-Reveals-Gen-Z-Digital-Natives-Crave-In-Person-Events-for-Building-Connections-and-Advancing-Their-Careers.html |
| 2 | 91% Gen Z: technology made them feel less connected; 86% in-person events key to career development; 84% best setting for strong business relationships; 42% confident small talk; 39% comfortable networking in industry | **Freeman 2025 Gen Z Report** / The Harris Poll — via MCEC (Apr 2025) | https://www.mcec.com.au/stories-and-ideas/what-do-gen-z-want-from-their-events |
| 3 | 51% attendees: effective networking = reason to return; 1/3 young professionals: current networking formats detract value or increase anxiety | **Freeman Trends Report** (Jul 2025) — GlobeNewswire | https://www.globenewswire.com/news-release/2025/07/23/3120447/0/en/New-Freeman-Trends-Report-Reveals-Meaningful-Networking-is-Key-to-Event-Growth.html |
| 4 | Vietnam: 174 public + 60 private = 234 universities; 687,473 students (2023–24); ~615,000 tuyển sinh 2024 | **British Council** dẫn số liệu **MOET** (Bộ GD&ĐT) 2024 | https://opportunities-insight.britishcouncil.org/short-articles/news/viet-nams-emphasis-education-quality-and-partnerships |
| 5 | EventMobi pricing ~$3,000/event; Whova G2 score 4.8/5 | **G2** — platform review độc lập (2025) | https://learn.g2.com/best-mobile-event-apps |
| 6 | Global Event Management Software Market $9.2B (2025) → $32.94B (2035), CAGR 13.72% | Spherical Insights (2025) — dùng làm proxy trend, không phải Gartner/IDC | https://www.sphericalinsights.com/blogs/top-30-companies-in-global-event-management-software-market-2026-2035-expert-view-by-spherical-insights |
