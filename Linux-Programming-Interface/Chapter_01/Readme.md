### History and standards

Linux là một thành viên của hệ điều hành họ Linux, Trong thuật ngữ máy tính, UNIX có một lịch sử lâu dài. Phần đầu tiên của chương này cung cấp một phác thảo về lịch sử đó. Chúng ta bắt đầu với mô tả về nguồn gốc hệ thống UNIX và ngôn ngữ lập trình C, sau đó sẽ nêu hai chìa khóa dẫn đến sự tồn tại của hệ thống Linux ngày nay: Dự án GNU và sự phát triển Linux Kernel.

Một trong những tính năng đáng chú ý của hệ thống Linux là sự phát triển của nó không được kiểm soát với một nhà cung cấp hoặc một tổ chức duy nhất. Thay vào đó, nhiều tổ chức, cả thương mại và phi thương mại đều góp phần vào sự phát triển đó. Lịch sử này dẫn đến nhiều tính năng cải tiến được thêm vào UNIX, nhưng cũng có hệ quả tiêu cực là việc triển khai UNIX phân tán theo thời gian, vì vậy để viết các ứng dụng làm việc trên tất cả bản triển khai UNIX ngày càng trở nên khó
khăn hơn. Điều này dẫn đến cần một drive (ổ đĩa) cho việc chuẩn hóa các triển khai UNIX, chúng ta sẽ bàn luận trong phần hai của chương này. 
    Có hai định nghĩa về thuật ngữ UNIX được sử dụng phổ biến. Một trong số đó biểu thị các hệ điều hành đã vượt qua các kiểm tra tuân thủ chính thức cho đặc tả Single UNIX và do đó được chính thức cấp quyền mang nhãn hiệu UNIX của Open Group (các chủ sở hữu nhãn hiệu UNIX). Hai là biểu thị các hệ thống trông giống như các hệ thống UNIX cổ điển (ví dụ các phòng thí nghiệm Bell ban đầu là UNIX và sau đó có các triển khai là System V và BSD). Theo định nghĩa này, Linux thường
    được coi là một hệ thống UNIX.

#### Tóm tắt lịch sử của UNIX và C

Bản UNIX đầu tiên được phát triển năm 1969 (cùng năm mà Linus Torvalds sinh ra)  bởi Ken Thompson tại Bell Laboratories, một bộ phận của tập toàn điện thoại, AT&T. Nó được viết bằng assembler cho máy tính kỹ thuật số mini PDP-7. Tên UNIX là một trò chơi chữ trên MULTICS (Multiplexed Information and Computing Service - Dịch vụ thông tin và tính toán ghép kênh), tên của một dự án hệ điều hành trước đó, trong đó AT&T hợp tác với Viện Công nghệ Massachusetts (Massachusetts Institute of Technology - MIT) và General Electric. Thompson đã rút ra một số ý tưởng cho hệ điều hành mới của mình từ MULTICS, bao gồm một hệ thống tập tin có cấu trúc cây, một chương trình riêng biệt để biên dịch các lệnh. (shell) và khái niệm về các file như là các luồng byte không có cấu trúc.

Năm 1970, UNIX được viết lại bằng ngôn ngữ assembly cho một máy tính mini Digital PDP-11 mới được mua lại, sau đó là một cỗ máy mới và mạnh mẽ. Các di tích của di sản PDP-11 này có thể được tìm thấy trong nhiều tên khác nhau vẫn được sử dụng trên hầu hết các phân phối UNIX, bao gồm cả Linux.

Một thời gian ngắn sau đó, Dennis Ritchie, một trong những đồng nghiệp của Thompson tại Bell Laboratories và là cộng tác viên đầu tiên với UNIX, đã thiết kế và triển khai ngôn ngữ lập trình C. Đây là một quá trình tiến hóa; C theo sau một ngôn ngữ diễn giải trước đó, B. B ban đầu được thực hiện bởi Thompson và đã vẽ nhiều ý tưởng của nó từ một ngôn ngữ lập trình vẫn còn trước đó có tên là BCPL. Đến năm 1973, C đã được phát triển, trưởng thành đến mức mà kernel UNIX có thể được viết lại gần như hoàn toàn bằng ngôn ngữ mới - C. Do đó, UNIX đã trở thành một trong những hệ điều hành sớm nhất được viết bằng một ngôn ngữ bậc cao, một thực tế đã làm cho việc chuyển đổi tiếp theo sang các kiến trúc phần cứng khác có thể.

Nguồn gốc của C giải thích tại sao nó, và hậu duệ của nó C++, đã được sử dụng rộng rãi như các ngôn ngữ lập trình hệ thống ngày nay. Thiết kế của C phát sinh từ những ý tưởng và nhu cầu của một vài cá nhân làm việc hướng tới một mục tiêu duy nhất: phát triển một ngôn ngữ bậc cao để thực hiện kernel UNIX và các phần mềm liên quan. Cũng giống như hệ điều hành UNIX, C được thiết kế bởi các lập trình viên chuyên nghiệp để sử dụng riêng cho họ. Kết quả chúng ta được ngôn ngữ nhỏ, hiệu quả, mạnh mẽ, ngắn gọn, mô-đun, thực dụng và mạch lạc trong thiết kế.





































