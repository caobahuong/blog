# Rule: Viết bài blog chủ đề Kinh tế / Tài chính

Áp dụng cho mọi bài viết trong `./data` thuộc các tag: `Tài chính`, `Kinh tế học`, `Đầu tư` (hoặc tương đương).

Mục tiêu: trung hòa giữa **kiến thức/lý thuyết có sẵn** và **quan điểm cá nhân của người viết**, tránh hai thái cực — bài giáo khoa khô cứng không ai đọc, hoặc bài truyền cảm hứng một chiều thiếu căn cứ.

## 1. Độ dài

- Tổng: **1.600 – 2.400 từ** (tương ứng ~9–13 phút đọc, giá trị `readTime` khai báo khớp con số thực tế). Nếu case study có từ 3 trường hợp trở lên, được phép chạm trần 2.400 từ.
- Dưới 1.400 từ: thiếu chiều sâu, không đủ chỗ cho đủ 8 phần bên dưới.
- Trên 2.600 từ: cắt bớt, tách thành bài nhiều phần (series) thay vì nhồi vào một bài.

## 2. Cấu trúc bắt buộc (8 phần theo đúng thứ tự)

| # | Phần | Dung lượng | Yêu cầu |
|---|------|-----------|---------|
| 1 | Mở bài | 100–150 từ | Nêu nghịch lý/câu hỏi trung tâm bằng 1 quote hoặc số liệu thật. Không dùng câu cảm thán cường điệu. |
| 2 | Lý thuyết | 250–350 từ | Trình bày đúng lý thuyết gốc, gắn nhãn **"Theo lý thuyết gốc"**. Không chèn số liệu/ngưỡng tự đặt vào phần này. |
| 3 | Cơ chế | 200–300 từ | Giải thích **quá trình vận hành** của lý thuyết từng bước (vd. chuỗi phản ứng dây chuyền), không chỉ nêu khái niệm suông. Có thể dùng danh sách đánh số hoặc sơ đồ ASCII. |
| 4 | Tác hại | 150–250 từ | Hậu quả cụ thể nếu cơ chế ở phần 3 xảy ra trên thực tế — ai chịu ảnh hưởng, ở quy mô nào (hệ thống, doanh nghiệp, cá nhân). |
| 5 | Cách xử lý | 150–250 từ | Các công cụ/chính sách tổng quát thường dùng để phòng ngừa hoặc giảm thiểu tác hại — trình bày nguyên tắc chung, chưa đi vào case study cụ thể. |
| 6 | Case study | 350–600 từ | Bắt buộc có **ít nhất 1 ca thất bại và 1 ca thành công**, mỗi ca dùng heading `###` riêng. Trong mỗi ca, tách một heading con `####` tên **"Điểm bùng phát"** (hoặc tên tương đương gắn với lý thuyết, vd. "Khoảnh khắc Minsky") nêu rõ sự kiện/thời điểm cụ thể khi cơ chế ở phần 3 xảy ra trong thực tế — kể cả ở ca thành công, phải nêu rõ lý do vì sao điểm đó **không** xảy ra. Có nguồn cho số liệu/sự kiện. |
| 7 | Phản biện / Giới hạn | 150–250 từ | **Bắt buộc.** Nêu ít nhất 1 ý kiến trái chiều hoặc giới hạn đã biết của lý thuyết/case study. |
| 8 | Quan điểm cá nhân + Kết | 250–350 từ | Gắn nhãn rõ **"Quan điểm cá nhân"**. Đây là chỗ duy nhất được suy diễn, khuyến nghị, dùng văn phong truyền cảm hứng. Kết bằng 1 ý thực hành được, không lặp lại nguyên văn các phần trên. |

## 3. Quy tắc tách bạch Kiến thức vs Ý kiến

- Mọi số liệu/ngưỡng định lượng cụ thể (vd. `ICR > 3.0`, `trần đòn bẩy 20:1`) **phải có nguồn** (tên tổ chức, năm, hoặc link) hoặc được gắn nhãn rõ là ước tính/tham khảo của người viết — không trình bày lẫn vào văn bản như thể là định nghĩa gốc của lý thuyết.
- Không viết một câu vừa chứa sự thật đã kiểm chứng vừa chứa suy diễn cá nhân mà không có từ tín hiệu phân tách: *"theo tôi"*, *"có thể hiểu là"*, *"nhiều nhà kinh tế cho rằng"*, *"cá nhân tôi nghiêng về..."*.
- Phần 2 (lý thuyết gốc) và phần 8 (quan điểm cá nhân) không được dùng chung giọng văn — phần 2 trung tính, phần 8 được phép chủ quan.

## 4. Nguồn tham khảo

- Nếu bài có trích số liệu, định nghĩa, hoặc case study từ nguồn ngoài → bắt buộc có mục **"Nguồn tham khảo"** ở cuối bài (danh sách gạch đầu dòng, tên nguồn + năm, không cần link nếu không có).
- Không bịa số liệu cụ thể (phần trăm, tỷ lệ, mốc thời gian) nếu không chắc chắn về nguồn — thà viết định tính còn hơn đưa số sai.

## 5. Chuẩn heading (phục vụ mục lục tự động)

Trang blog tự sinh mục lục từ các heading `##` (H2) khi bài có từ 2 heading trở lên — không đụng tới `###`/`####`. Vì vậy:

- Chỉ 8 heading cấp `##` tương ứng 8 phần ở mục 2 (Mở bài có thể không cần heading riêng). Không chẻ thêm `##` ngoài 8 phần này.
- Tên heading `##` ngắn gọn (dưới ~6 từ), không lặp lại nguyên văn tên lý thuyết — vì sẽ hiển thị nguyên trong mục lục.
- Heading từng case study trong phần 6 dùng `###`; heading "Điểm bùng phát" trong mỗi case dùng `####` — cả hai cấp này **không** xuất hiện trong mục lục, chỉ có tác dụng điều hướng trong mắt đọc.

## 6. Văn phong

- Tối đa **1–2 ẩn dụ văn học/hình ảnh** mỗi bài (vd. "vũ điệu trên miệng núi lửa"). Dùng nhiều hơn làm loãng tính nghiêm túc.
- Tránh các cụm mang tính PR/motivational quá đà ở phần 1–4 (giữ cho phần 5 và phần kết).
- Khung/sơ đồ minh họa (nếu có) đặt trong code block, dùng ký tự ASCII thuần (`+ - | v ->`), tránh ký tự Unicode vẽ khung (┌─┐│└┘▼) vì có thể gây lệch font khi hiển thị.

## 7. Checklist trước khi publish

- [ ] Đủ 8 phần theo đúng thứ tự: Mở bài → Lý thuyết → Cơ chế → Tác hại → Cách xử lý → Case study → Phản biện → Quan điểm cá nhân/Kết.
- [ ] Phần lý thuyết gốc không lẫn số liệu tự chế.
- [ ] Phần cơ chế trình bày theo bước (không chỉ nêu khái niệm suông).
- [ ] Case study có ít nhất 1 ca thất bại và 1 ca thành công, mỗi ca dùng heading `###` riêng.
- [ ] Mỗi ca có heading con `####` "Điểm bùng phát" (hoặc tên tương đương) chỉ rõ sự kiện/thời điểm cụ thể, kể cả khi ca thành công không có điểm bùng phát nào.
- [ ] Chỉ có đúng 8 heading `##`, đặt tên ngắn gọn — vì sẽ hiển thị nguyên trong mục lục tự động của trang.
- [ ] Phần phản biện/giới hạn tồn tại và không rỗng tuếch.
- [ ] Phần quan điểm cá nhân được gắn nhãn rõ ràng.
- [ ] Mọi số liệu định lượng có nguồn hoặc nhãn ước tính.
- [ ] Có mục "Nguồn tham khảo" nếu bài trích dẫn số liệu ngoài.
- [ ] Tổng độ dài nằm trong khoảng 1.600–2.400 từ.
