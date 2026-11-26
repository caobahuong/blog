|=----------------------------------------------------------------------=|
|=    [Làm sao để tạo ra ứng dụng EASY (góc nhìn nhân viên EasyPos)]    =|
|=----------------------------------------------------------------------=|
|=                             [ huongcb ]                              =|
|=----------------------------------------------------------------------=|

--[ lời mở đầu ]
Một câu hỏi mà khiến mình đau đáu mấy hôm nay là: "làm sao để tạo ra một ứng
dụng đơn giản ?"
> Chữ "đơn giản" thật ra nó lại không "đơn giản".

Nhưng có lẽ điều may mắn của bản thân là được làm trong công ty với triết lý 
"Make It Simple" - đã giúp bản thân được tiếp xúc, nhìn nhận và phần nào có
suy nghĩ riêng về hai chữ giản "đơn giản".

Bài viết này sẽ đi vào chữ "Easy" trong EasyPos - phân tích cách hiểu của
bản thân, cách mà mình chia nhỏ sản phẩm với mỗi phần chính là một triết lý
khác nhau về sự "Easy".

--[ định nghĩa lại các khái niệm ]
Bản thân mình nghĩ: những định nghĩa dưới đây thực chất là nói ngắn gọn một
vài ý chính còn định nghĩa đúng nó phải đặt vào từng phần - từng thời điểm
của một sản phẩm.

+ "Đơn giản": nó không chỉ là ít nút hơn, ít thao tác hơn mà nó còn là suy
  nghĩ ít hơn, ...
+ "Tốc độ": nó không chỉ là ứng dụng nhanh, nó còn là tốc độ trong thao tác
  của người dùng, tốc độ phản ứng khi người dùng gặp tình huống (tốc độ não
  xữ lý)

--[ chia nhỏ EasyPos ]
Theo mình để một ứng dụng đơn giản - thứ đầu tiên mà nhà phát triển cần làm
là xác định được nhu cầu, hành vi khách hàng trong từng phần của một sản
phẩm.

Với EasyPos, khác với các chia domain trong công ty hiện tại để thực hiện
quản lý và coding - mình chia nó thành 3 phần:

----[ 3 phần của EasyPos ]
Trước khi đi vào chia, cần phải nói rằng EasyPos là phần mềm bán hàng tích 
hợp giải pháp hóa đơn. Mình nói ra đây để khẳng định một điều rằng thứ xoay 
quanh ứng dụng này là "bán hàng". 
Do vậy khi chia ta lấy "bán hàng" làm trung tâm - bao gồm:
+ Trước bán hàng
+ Bán hàng
+ Hậu bán hàng

Nhưng nếu nói tổng quan hơn chính là:
+ Thành phần xây dựng 
+ Thành phần thực thi
+ Thành phần hậu kiểm

> Việc đưa khái niệm về mặt tổng quan giúp mình mở rộng được sang hành vi
> chung của người dùng - thay vì gắn quá chặt với sản phẩm hay khung lý
> thuyết nhất định.

--[ thành phần xây dựng ]
Thành phần này bao gồm toàn bộ để có thể setup nên tư liệu sản xuất cho
thành phần thực thi sử dụng.
Trong EasyPos là: quản lý sản phẩm, quản lý khách hàng, quản lý ca, quản lý
voucher, ...
Đây là thành phần đầu tiên mà khách mới tiếp xúc đầu tiên, nó cũng là thành
phần nhiều luật nhất. Mỗi thao tác gắn với vô vàn luật lệ khác nhau. Một ví
dụ mà mình rất thích đưa ra là: "Đổi đơn vị tính bị cấm khi phát sinh giao
dịch" hay "Xóa sản phẩm bị cấm khi phát sinh giao dịch".

Do vậy mình gọi đây là:
> THÀNH PHẦN HÀNH VI QUYẾT ĐỊNH HÀNH VI

Đối với thành phần này: 
+ "đơn giản" ở đây nên là "đơn giản" trong các suy nghĩ.
+ "tốc độ" ở đây nên là "tốc độ" trong các suy nghĩ.

Tức là - phải đặt mục tiêu hành vi người dùng lên hàng đầu để xây dựng hành
vi của app. 
Khách muốn xóa sản phẩm đã bán -> nếu ứng dụng chặn phải làm sao ?
Tư duy: bản chất khách muốn xóa nghĩa là ẩn khỏi ứng dụng thì cứ cho họ ẩn
đi thôi nhưng có thể là chức năng ngừng kinh doanh thay vì xóa.

> Cố gắng khiến cho hành vi của người dùng phải đạt được mục đích

--[ thành phần thực thi ]
Thành phần này bao gồm toàn bộ để bán hàng chính phục vụ chính thứ cốt lõi
của ứng dụng và là nhu cầu chính của khách hàng.

Đối với mình gọi đây là:
> THÀNH PHẦN TỐC ĐỘ QUYẾT ĐỊNH HÀNH VI

Ngoài lề: theo mình thói quen chính không chỉ là tốc độ mà còn là sợi dây ràng buộc người dùng với ứng dụng. Do vậy ứng dụng càng giữ được thói quen trong thành phần thực thi thì tỷ lệ rời đi càng giảm.

Đối với thành phần này:
+ "đơn giản" ở đây là "đơn giản" trong thao tác người dùng 
   càng ít thao tác càng tốt.
+ "tốc độ" = "tốc độ ứng dụng" + "tốc độ dùng app của người dùng" (thói quen
  người dùng) 
   phản hồi càng nhanh càng tốt

Về cơ bản lúc bán hàng khách cũng đâu quan tâm tới phiếu kho, ...
Nên thành phần này:
> Cố gắng khiến cho tốc độ của người dùng phải nhanh nhất

Một cái thật sự cẩn thận ở đây, theo mình thành phần này nên là thành phần
ít thay đổi nhất, UI không nên thay đổi nhiều, danh sách sản phẩm hiện thị
nên cố định trong mọi thời điểm nếu cùng một yêu cầu. Vì sự thay đổi ảnh
hưởng tới thói quen người bán hàng tức là ảnh hưởng tới tốc độ của thành
phần.

--[ thành phần hậu kiểm ]
Thành phần này bao gồm toàn bộ để hậu kiểm sau khi thành phần thực thi hoàn
thành như: kiểm tra phiếu kho, hóa đơn, chứng từ, báo cáo.

Đối với mình gọi đây là:
> THÀNH PHẦN CHÍNH XÁC QUYẾT ĐỊNH HÀNH VI

Thành phần này không cần nhanh - thứ duy nhất nó cần là độ chính xác.

Đối với thành phần này:
+ "đơn giản" ở đây là trong cách người dùng đọc báo cáo, số liệu, bảng biểu
+ "tốc độ" ở đây là sự chính xác - nghĩa là người dùng không tốn thời gian
  sửa lại khi hậu kiểm.

--[ sau tất cả ]
Kết nối tất cả lại ta có một bức tranh toàn cảnh về định nghĩa của sự đơn
giản, tốc độ.
Chưa chắc đơn giản phải là dễ bấm - ít nút. Đơn giản có thể là đơn giản
trong việc người dùng sẽ được phép lười suy nghĩ.
Chưa chắc tốc độ là phải nhanh. Tốc độ có thể là việc tiết kiệm được thời
gian không cần chỉnh lại dữ liệu - hay tốc độ phản ứng khi gặp vấn đề cho
phép người dùng lười suy nghĩ.
