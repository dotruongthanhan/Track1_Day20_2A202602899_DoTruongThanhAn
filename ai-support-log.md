# AI Support Log — SteelLearn

### AI đã giúp tôi ở đâu?

- **Brainstorm ứng viên Core Action & bộ câu hỏi phản biện:** Gợi ý danh sách các hành vi khả dĩ (`xem video mô phỏng`, `hỏi đáp AI Tutor`, `làm quiz xác nhận an toàn`) và cung cấp các câu hỏi phản biện giúp tôi tự tranh luận, bóc tách giữa thao tác giao diện bề nổi với hành vi chạm tới giá trị cốt lõi.
- **Gợi ý tên event dạng `object_action` & khung Acceptance Criteria mẫu:** Đề xuất quy ước đặt tên 7 sự kiện đo lường theo chuẩn (`sop_workspace_viewed`, `tutor_inquiry_responded`, `sop_quiz_evaluated`, `sop_mastery_achieved`,...) và cấu trúc mẫu cho 2 tiêu chí nghiệm thu AC1 (nghiệm thu event giá trị) và AC2 (idempotency, chống bắn trùng lặp).
- **Đóng vai "khách hàng khó tính":** Giả lập góc nhìn của Quản đốc phân xưởng luyện/cán thép khắt khe về an toàn lao động để thử thách lại tính thực tế của Core Job và tính khả thi trong ca kíp sản xuất.

---

### AI sai, hời hợt hoặc đề xuất metric sai nature ở đâu?

- **Đề xuất metric sai bản chất dạng "vanity chat":** Do thiên kiến chatbot, AI ban đầu đề xuất chọn Core Action là *"Hỏi đáp với AI Tutor"* và tối đa hóa *"Số lượt chat / độ dài hội thoại"*. Trong nhà máy thép, công nhân cần nắm quy trình chuẩn nhanh nhất; chat càng nhiều chứng tỏ tài liệu khó hiểu hoặc AI trả lời lan man, đi ngược lại hiệu quả vận hành an toàn.
- **Áp đặt nhịp đo Daily của app tiêu dùng:** AI gợi ý theo dõi DAU và gửi push notification hàng ngày. Điều này sai lệch hoàn toàn với bối cảnh công nhân đi làm theo ca kíp (3 ca 4 kíp, có ngày nghỉ luân phiên hoặc ngày đứng máy thực địa), dễ tạo ra tín hiệu rời bỏ giả (false churn).
- **Bịa số liệu benchmark EdTech không có nguồn:** AI đưa ra các con số benchmark retention 60–70% theo kiểu ứng dụng học trực tuyến B2C đại trà, không phản ánh đúng chương trình đào tạo hội nhập nội bộ mang tính bắt buộc và gắn liền với giấy phép vận hành máy móc.

---

### Tôi đã tự sửa hoặc quyết định lại điều gì?

- **Tự chọn Core Action & Core Value Event:** Dứt khoát loại bỏ hành vi chat, chốt Core Action là *"Làm và nộp bài kiểm tra xác nhận hiểu biết quy trình SOP"* với Core Value Event là `sop_mastery_achieved` (điểm $\ge 80\%$, có trích dẫn điều mục an toàn kỹ thuật như áp suất 4.5–6.0 bar, E-STOP). Chuyển việc hỏi đáp AI thành một Leading Indicator hỗ trợ.
- **Tự quyết định Cadence và động lực giữ chân thực tế:** Chốt nhịp đo lường là **Weekly** (3–5 SOP/tuần/công nhân) tương thích với 4 tuần onboarding; xác định động lực quay lại (Reason to return) đến từ trách nhiệm an toàn sinh mạng và điều kiện bắt buộc để hoàn thành Ma trận Kỹ năng (Skill Matrix) trước khi được giao ca độc lập (không dựa vào notification).
- **Tự viết Metric Hypothesis & hệ thống Counter-metrics an toàn:** Tự xây dựng giả thuyết tăng trưởng một câu (tăng W2 Retention từ 45% lên 70% trong 30 ngày) và gắn chặt hai chỉ số đối trọng sống còn của nhà máy thép (`AI Hallucination & Citation Failure < 2%` và `Post-Onboarding Safety Incident Rate giảm $\ge 50%$`).

