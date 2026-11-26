---
id: lam-sao-tao-ra-ung-dung-don-gian-goc-nhin-dev-easypos
title: Làm sao tạo ra ứng dụng đơn giản - góc nhìn của dev EasyPos
date: 2026-11-25
readTime: 6 phút đọc
tags: [Sản phẩm, Tư duy, EasyPos]
excerpt: Đơn giản không phải là ít nút. Bài viết chia EasyPos thành ba thành phần - xây dựng, thực thi, hậu kiểm - và cho thấy mỗi phần cần một kiểu "Easy" hoàn toàn khác nhau.
---

> **Ghi chú:** Bài viết được viết lại từ bài viết gốc: <a href="data/how_to_make_easy_app.md" download="easy_app.md">how_to_make_easy_app.md</a> (bấm để tải về). 
> Mình thích bản gốc hơn - nó mộc hơn nhưng có lẽ giọng văn mình hơi khó hiểu.

Hình dung một chủ cửa hàng muốn xóa một món không bán nữa. Họ bấm "Xóa", app báo: *"Sản phẩm đã phát sinh giao dịch, không thể xóa."* Họ không hiểu vì sao, bấm lại lần nữa, rồi gọi hỗ trợ.

Cả app không có gì phức tạp: một nút, một thông báo. Nhưng người dùng vẫn phải **suy nghĩ**, và vẫn không đạt được điều họ muốn.

Đó là lý do câu hỏi *"làm sao để tạo ra một ứng dụng đơn giản?"* khiến mình đau đáu mấy hôm nay. Chữ "đơn giản" thật ra không đơn giản.

Mình may mắn được làm trong công ty có triết lý "Make It Simple", nên có dịp nhìn kỹ hai chữ này. Bài viết là cách mình hiểu chữ "Easy" trong EasyPos, và cách mình chia sản phẩm thành ba phần, mỗi phần một kiểu "Easy" riêng.

> **Luận điểm của bài:** đơn giản không phải là ít nút hơn. Đơn giản là người dùng được phép **lười suy nghĩ**. Và "lười suy nghĩ" ở mỗi phần của sản phẩm lại có nghĩa khác nhau.

## Hai chữ cần định nghĩa lại

Trước khi đi tiếp, mình muốn tách hai khái niệm hay bị hiểu quá hẹp.

- **Đơn giản** không chỉ là ít nút, ít thao tác. Nó còn là **suy nghĩ ít hơn**.
- **Tốc độ** không chỉ là app chạy nhanh. Nó còn là tốc độ thao tác của người dùng, và tốc độ họ phản ứng được khi gặp tình huống (tốc độ xử lý của não).

Đây mới là định nghĩa ngắn gọn. Định nghĩa đầy đủ phải gắn với từng phần, từng thời điểm của sản phẩm, và đó là lý do mình chia nhỏ EasyPos.

## Chia EasyPos làm ba

Việc đầu tiên để làm ra một ứng dụng đơn giản là hiểu **nhu cầu và hành vi của khách trong từng phần sản phẩm**, không phải hiểu cả sản phẩm như một khối.

EasyPos là phần mềm bán hàng tích hợp giải pháp hóa đơn, nên mọi thứ xoay quanh "bán hàng". Mình không chia theo domain như cách công ty chia để quản lý và code, mà lấy bán hàng làm trung tâm:

- **Trước bán hàng** → *thành phần xây dựng*
- **Bán hàng** → *thành phần thực thi*
- **Sau bán hàng** → *thành phần hậu kiểm*

Mình cố ý dùng tên tổng quát ở vế sau, để nó mô tả hành vi chung của người dùng chứ không gắn chặt vào một sản phẩm hay một khung lý thuyết nhất định. Ba cái tên này dùng được cho nhiều loại ứng dụng khác ngoài POS.

## Thành phần xây dựng

> **HÀNH VI QUYẾT ĐỊNH HÀNH VI**

Đây là nơi setup "tư liệu sản xuất" cho phần thực thi: quản lý sản phẩm, khách hàng, ca, voucher, ... Khách mới gặp nó đầu tiên, và nó cũng là phần **nhiều luật nhất**. Mỗi thao tác kéo theo cả loạt ràng buộc:

- Đổi đơn vị tính bị cấm khi đã phát sinh giao dịch.
- Xóa sản phẩm bị cấm khi đã phát sinh giao dịch.

Mỗi luật đều có lý do chính đáng về dữ liệu. Nhưng người dùng không nhìn thấy lý do, họ chỉ thấy mình **bị chặn**.

Ở phần này, cả "đơn giản" lẫn "tốc độ" đều nằm trong **suy nghĩ**: khách phải nghĩ ít nhất có thể để đạt được mục đích.

Quay lại ví dụ đầu bài. Khi khách bấm "Xóa", họ không thật sự muốn dữ liệu biến mất. Họ muốn món đó **không hiện ra nữa**. Hiểu được mục đích đó, lời giải không còn là "giải thích vì sao không xóa được" mà là cho họ đúng thứ họ cần: **ngừng kinh doanh**. Món ẩn khỏi app, lịch sử giao dịch vẫn nguyên vẹn, và khách không phải học thêm luật nào.

Luật vẫn còn đó. Khác ở chỗ người dùng không phải đụng vào nó.

> Cố gắng để hành vi của người dùng luôn đạt được mục đích.

## Thành phần thực thi

> **TỐC ĐỘ QUYẾT ĐỊNH HÀNH VI**

Đây là nơi bán hàng, thứ cốt lõi của ứng dụng và cũng là nhu cầu chính của khách. Giữa giờ cao điểm, thu ngân không quan tâm phiếu kho hay luật gì cả. Họ chỉ cần bán xong đơn tiếp theo.

Ở phần này:

- **Đơn giản** là đơn giản trong thao tác: càng ít thao tác càng tốt.
- **Tốc độ** gồm hai vế cộng lại: tốc độ của ứng dụng và tốc độ dùng app của người dùng, tức thói quen. Phản hồi càng nhanh càng tốt.

Vế thứ hai hay bị quên. Một thu ngân dùng quen một màn hình sẽ bấm bằng **trí nhớ cơ bắp**, không cần nhìn. Nếu hôm nay mình dời một nút hay đổi thứ tự danh sách sản phẩm, app có thể đẹp hơn, nhưng họ phải nhìn lại, tức là **chậm hơn**.

Vì vậy theo mình, đây nên là thành phần **ít thay đổi nhất**. UI hạn chế đổi, danh sách sản phẩm hiển thị cố định ở mọi thời điểm nếu cùng một yêu cầu. Mọi cải tiến ở phần này đều phải trả giá bằng thói quen của người dùng.
Ngoài lề một chút - theo mình thói quen chính không chỉ là tốc độ mà còn là sợi dây ràng buộc người dùng với ứng dụng. Do vậy ứng dụng càng giữ được thói quen trong thành phần thực thi thì tỷ lệ rời đi càng giảm.

> Cố gắng để tốc độ của người dùng là nhanh nhất.

## Thành phần hậu kiểm

> **CHÍNH XÁC QUYẾT ĐỊNH HÀNH VI**

Sau khi bán xong là lúc kiểm tra: phiếu kho, hóa đơn, chứng từ, báo cáo. Phần này **không cần nhanh**. Thứ duy nhất nó cần là **chính xác**.

Hình dung cuối ngày chủ cửa hàng đối chiếu doanh thu mà số trong báo cáo lệch với số trong tay. Dù báo cáo load trong một giây, họ vẫn mất cả buổi tối để lần ra chỗ sai. Đó mới là chậm.

Ở phần này:

- **Đơn giản** là đọc được báo cáo, số liệu, bảng biểu mà không phải diễn giải.
- **Tốc độ** chính là chính xác: dữ liệu đúng ngay từ đầu thì người dùng không tốn thời gian sửa lại.

> Một con số đúng quan trọng hơn một báo cáo nhanh.

## Một chữ Easy, ba nghĩa

Đặt ba phần cạnh nhau:

- **Xây dựng:** đơn giản là *không phải nghĩ về luật*, tốc độ là *nghĩ ít*.
- **Thực thi:** đơn giản là *ít thao tác*, tốc độ là *thói quen + phản hồi nhanh*.
- **Hậu kiểm:** đơn giản là *đọc là hiểu*, tốc độ là *không phải sửa lại*.

Ba phần này có cùng đích đến, là để người dùng được **lười suy nghĩ**, nhưng đi bằng ba con đường khác nhau. Một ứng dụng áp một tư duy chung cho cả ba sẽ hỏng ở đâu đó: bắt người bán hàng học cách làm mới giữa giờ cao điểm, hoặc hy sinh độ chính xác của báo cáo để cho nhanh.

Vì vậy thay vì tìm một tư duy chung để xử lý ứng dụng, ta nên **tách nhỏ ra, mỗi phần một tư duy độc lập**.