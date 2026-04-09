# Individual reflection — Nguyễn Tiến Dũng (2A202600219)

## 1. Role
Frontend UI/UX Developer & Route Architect.

Role chính: Thiết kế giao diện (Mockup) và xây dựng hệ thống điều hướng (Routing).

## 2. Đóng góp cụ thể
- UI/UX Design: Thiết kế mockup cho các màn hình Login/Signup và giao diện chính dựa trên ngôn ngữ thiết kế của VinFast app (modern, tối giản, chuyên nghiệp).

- Frontend Architecture: Tạo các components dùng chung và thiết lập hệ thống Routes cho phép tương tác mượt mà giữa các trang (Home ↔ Chat Advisor ↔ Calculator ↔ Lead Form).

- Prompt Engineering Support: Phối hợp cùng nhóm viết và hiệu chỉnh System Prompt để đảm bảo phản hồi của AI đồng bộ với giao diện mockup (ví dụ: định dạng text để hiển thị đẹp trên mobile web).

## 3. SPEC mạnh/yếu
- Mạnh nhất (Phần 2 - Technical Implementation): Hệ thống Routing và Components được xây dựng với tư duy dự phòng. Tôi đã chuẩn bị sẵn cấu trúc để xử lý các trường hợp mở rộng như so sánh xe hoặc lưu lịch sử chat mà không cần thay đổi cấu trúc cốt lõi.
- Yếu nhất (Phần 5 - Evaluation Metrics): Vì đây là giai đoạn Prototype, việc thu thập dữ liệu thực tế để đánh giá các chỉ số như Precision hay Lead Conversion Rate chưa được chuẩn bị kỹ lưỡng. Hệ thống hiện tại mới chỉ tập trung vào việc chạy đúng luồng (Happy Path) hơn là đo lường hiệu quả định lượng.

## 4. Đóng góp khác
- Hỗ trợ tinh chỉnh System Prompt cho AI Advisor.
- Xử lý lỗi hiển thị và lỗi điều hướng khi người dùng chuyển đổi giữa free-chat và flow câu hỏi cố định.

## 5. Điều học được
Trước hackathon, tôi nghĩ UI/UX chỉ đơn thuần là thẩm mỹ. Qua dự án AI Advisor này, tôi nhận ra UI là "điểm chạm" của sự tin tưởng (Trust). Đối với sản phẩm giá trị cao như xe điện, giao diện phải cực kỳ chỉn chu (dựa theo VinFast standard) thì người dùng mới dám tin vào những con số chi phí hay gợi ý mà AI đưa ra. Nếu UI sơ sài, dù AI thông minh đến đâu khách hàng cũng sẽ nghi ngờ kết quả.

## 6. Nếu làm lại
Tôi sẽ triển khai Global State Management (như Context API hoặc Redux) sớm hơn. Trong quá trình làm, việc truyền dữ liệu người dùng (Intake data) từ trang Chat sang trang Calculator bằng props gặp nhiều khó khăn. Nếu có Global State, việc quản lý "Context" của người dùng xuyên suốt các trang sẽ sạch sẽ và chuyên nghiệp hơn rất nhiều.

## 7. AI giúp gì / AI sai gì
- **Giúp:** Sử dụng AI để nhanh chóng chuyển đổi các hình ảnh tham chiếu từ app VinFast thành mã CSS/Tailwind cụ thể, giúp tăng tốc độ hoàn thiện mockup giao diện mobile web.
- **Sai/mislead:** Khi yêu cầu AI hỗ trợ viết Route phức tạp (Nested Routes), AI đôi khi gợi ý các đoạn code cũ (React Router v5) hoặc gây lỗi vòng lặp chuyển hướng (infinite redirect) khi kết hợp với logic Login.
  Bài học: AI hỗ trợ rất tốt phần "vỏ" (UI/CSS), nhưng với phần "lõi" logic (Routing/State), cần phải kiểm soát chặt chẽ và không được copy-paste mù quáng mà thiếu sự hiểu biết về phiên bản thư viện đang dùng.
