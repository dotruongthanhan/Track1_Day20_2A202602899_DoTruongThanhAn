# SteelLearn — AI SOP Tutor Agent
### Bản Thiết Kế Chiến Lược Sản Phẩm, Hệ Thống Chỉ Số (Metric System) & Kế Hoạch Đo Lường

**Mã học viên:** 2A202602899  
**Họ và tên:** Đỗ Trương Thành An   

---

## 📌 Giới thiệu dự án

**SteelLearn** là nền tảng trợ lý AI gia sư hướng dẫn quy trình thao tác chuẩn (**SOP — Standard Operating Procedure**) và luyện tập kiểm tra an toàn theo ngữ cảnh dành cho công nhân nhà máy thép (đặc biệt là công nhân mới onboarding tại các phân xưởng Cán thép & Luyện thép).

Hệ thống kết hợp:
- **Video mô phỏng thao tác thực địa:** Giúp công nhân tiếp thu trực quan các bước vận hành máy móc nặng.
- **Tài liệu SOP Markdown chuẩn hóa:** Cung cấp thông số kỹ thuật, ngưỡng áp suất, nhiệt độ và các quy chuẩn dừng khẩn cấp (E-STOP).
- **AI SOP Tutor Agent:** Gia sư AI tương tác giải đáp thắc mắc có đối chiếu trích dẫn điều mục an toàn trực tiếp từ CSDL tài liệu.
- **In-Context Safety Quiz:** Bộ câu hỏi trắc nghiệm tình huống an toàn giúp xác nhận năng lực độc lập đứng máy trước khi vào ca thực tế.

---

## 🎨 Bảng màu thiết kế (Color Palette)

Giao diện HTML được thiết kế theo đúng bảng màu quy định:
- **Màu chủ đạo (Primary Accent):** `#c15f3c` (Màu gạch nung / oxit sắt / thép tôi nhiệt)
- **Màu nền chính (Background):** `#ffffff` (Nền thẻ nội dung, sạch sẽ, chuẩn công nghiệp)
- **Màu nền phụ (Subtle Surface):** `#f4f3ee` (Màu ngà ấm nhẹ / bề mặt phụ tạo phân cấp thị giác)
- **Màu viền & phân cách (Borders & Dividers):** `#b1ada1` (Màu xám ấm đá vôi luyện kim)
- **Màu chữ (Typography):** `#000000` (Độ tương phản cao, tối ưu khả năng đọc)

---

## 📂 Cấu trúc tài liệu HTML (`index.html`)

Tài liệu được đóng gói toàn vẹn trong file [`index.html`](index.html), bao gồm đầy đủ 5 Phase chiến lược:

1. **Phase 0 — Chốt phạm vi (Scope Definition):**
   - Dự án SteelLearn & Bối cảnh nhà máy thép
   - Target Persona: Trần Văn Bình (23 tuổi, công nhân mới ca 1, Xưởng Cán / Luyện thép)
   - Core Job: *"Tôi muốn nắm chắc và làm đúng các bước vận hành máy móc an toàn để tự tin vào ca làm việc độc lập mà không phạm lỗi kỹ thuật nguy hiểm."*

2. **Phase 1 — Core Action (Hành vi cốt lõi):**
   - Phân biệt 4 khái niệm cốt lõi: Core Job, Core Action, Core Value, Core Value Event
   - Thẻ Core Action Card chi tiết (9 trường dữ liệu)
   - Tự kiểm 5 tiêu chí Core Action (Đạt 5/5 tiêu chí)

3. **Phase 2 — Nature & Cadence (Bản chất & Nhịp hành vi):**
   - Thẻ Action Nature Card (Actor, Intent, Trigger, Effort, Value Timing, State, Dependency, Repeat Condition)
   - Kết luận Cadence: Nhịp **Weekly** tương thích ca kíp onboarding (3 – 5 SOP/tuần/công nhân)
   - Rationale: Lý do không dùng Daily và không tối đa hóa số lần chat AI

4. **Phase 3 — Metric System + Retention (Hệ thống Chỉ số & Giữ chân):**
   - Activation Metric: `worker_first_login` &rarr; `first_sop_quiz_passed` (&ge; 80%) trong 48h
   - Engagement Metric: Frequency (`Weekly Passed SOPs per Active Worker`) & Depth (`First-Attempt Pass Rate`)
   - Retention Definition 6 thành phần (Unit, Cohort Entry, Return Event, Window, Threshold, Segment)
   - North Star Metric (NSM): **Số lượng quy trình SOP được công nhân kiểm tra đạt chuẩn hàng tuần**
   - Leading Indicators (3 chỉ số) & Counter-metrics (AI Hallucination & Post-Onboarding Safety Incidents)

5. **Phase 4 — Product Loop & Event Tracking (Vòng lặp & Đo lường):**
   - Progress Loop 2 chu kỳ liên tiếp (Chu kỳ 1: SOP đầu tiên &rarr; Chu kỳ 2: SOP tiếp theo)
   - Metric Hypothesis chuẩn & Reason to Return
   - Bảng Tracking Plan chi tiết 7 Core Events chuẩn hóa (`object_action`)
   - Tiêu chí nghiệm thu (AC1 & AC2)

6. **Phase 5 — Tự soi lỗi & Rationale tinh chỉnh:**
   - Bảng đối chiếu tự kiểm tra (7 tiêu chí)
   - Rationale: Giải trình chuyển đổi Core Action từ *"Hỏi đáp AI"* sang *"Hoàn thành kiểm tra hiểu biết SOP"*

7. **Bonus — Live Interactive Demo Simulator:**
   - Trải nghiệm mô phỏng màn hình học SOP của công nhân (xem video mock, đọc Markdown trích dẫn, làm quiz an toàn 2 câu, chấm điểm tức thì và bắn sự kiện `sop_mastery_achieved`).

---

## 🚀 Hướng dẫn mở và xem tài liệu

Bạn có thể mở trực tiếp file `index.html` bằng bất kỳ trình duyệt web hiện đại nào (Chrome, Safari, Edge, Firefox):

```bash
# Cách 1: Mở trực tiếp trên macOS
open index.html

# Cách 2: Chạy web server cục bộ
python3 -m http.server 8000
# Sau đó truy cập: http://localhost:8000
```
