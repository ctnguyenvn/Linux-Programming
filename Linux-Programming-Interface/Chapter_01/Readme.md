### History and standards

#### 1. Lịch sử và các tiêu chuẩn 

Linux là một thành viên của hệ điều hành họ Linux, Trong thuật ngữ máy tính, UNIX có một lịch sử lâu dài. Phần đầu tiên của chương này cung cấp một phác thảo về lịch sử đó. Chúng ta bắt đầu với mô tả về nguồn gốc hệ thống UNIX và ngôn ngữ lập trình C, sau đó sẽ nêu hai chìa khóa dẫn đến sự tồn tại của hệ thống Linux ngày nay: Dự án GNU và sự phát triển Linux Kernel.

Một trong những tính năng đáng chú ý của hệ thống Linux là sự phát triển của nó không được kiểm soát với một nhà cung cấp hoặc một tổ chức duy nhất. Thay vào đó, nhiều tổ chức, cả thương mại và phi thương mại đều góp phần vào sự phát triển đó. Lịch sử này dẫn đến nhiều tính năng cải tiến được thêm vào UNIX, nhưng cũng có hệ quả tiêu cực là việc triển khai UNIX phân tán theo thời gian, vì vậy để viết các ứng dụng làm việc trên tất cả bản triển khai UNIX ngày càng trở nên khó
khăn hơn. Điều này dẫn đến cần một drive (ổ đĩa) cho việc chuẩn hóa các triển khai UNIX, chúng ta sẽ bàn luận trong phần hai của chương này. 
    Có hai định nghĩa về thuật ngữ UNIX được sử dụng phổ biến. Một trong số đó biểu thị các hệ điều hành đã vượt qua các kiểm tra tuân thủ chính thức cho đặc tả Single UNIX và do đó được chính thức cấp quyền mang nhãn hiệu UNIX của Open Group (các chủ sở hữu nhãn hiệu UNIX). Hai là biểu thị các hệ thống trông giống như các hệ thống UNIX cổ điển (ví dụ các phòng thí nghiệm Bell ban đầu là UNIX và sau đó có các triển khai là System V và BSD). Theo định nghĩa này, Linux thường
    được coi là một hệ thống UNIX.

#### 1.1 Tóm tắt lịch sử của UNIX và C

Bản UNIX đầu tiên được phát triển năm 1969 (cùng năm mà Linus Torvalds sinh ra)  bởi Ken Thompson tại Bell Laboratories, một bộ phận của tập toàn điện thoại, AT&T. Nó được viết bằng assembler cho máy tính kỹ thuật số mini PDP-7. Tên UNIX là một trò chơi chữ trên MULTICS (Multiplexed Information and Computing Service - Dịch vụ thông tin và tính toán ghép kênh), tên của một dự án hệ điều hành trước đó, trong đó AT&T hợp tác với Viện Công nghệ Massachusetts (Massachusetts Institute of Technology - MIT) và General Electric. Thompson đã rút ra một số ý tưởng cho hệ điều hành mới của mình từ MULTICS, bao gồm một hệ thống tập tin có cấu trúc cây, một chương trình riêng biệt để biên dịch các lệnh. (shell) và khái niệm về các file như là các luồng byte không có cấu trúc.

Năm 1970, UNIX được viết lại bằng ngôn ngữ assembly cho một máy tính mini Digital PDP-11 mới được mua lại, sau đó là một cỗ máy mới và mạnh mẽ. Các di tích của di sản PDP-11 này có thể được tìm thấy trong nhiều tên khác nhau vẫn được sử dụng trên hầu hết các phân phối UNIX, bao gồm cả Linux.

Một thời gian ngắn sau đó, Dennis Ritchie, một trong những đồng nghiệp của Thompson tại Bell Laboratories và là cộng tác viên đầu tiên với UNIX, đã thiết kế và triển khai ngôn ngữ lập trình C. Đây là một quá trình tiến hóa; C theo sau một ngôn ngữ diễn giải trước đó, B. B ban đầu được thực hiện bởi Thompson và đã vẽ nhiều ý tưởng của nó từ một ngôn ngữ lập trình vẫn còn trước đó có tên là BCPL. Đến năm 1973, C đã được phát triển, trưởng thành đến mức mà kernel UNIX có thể được viết lại gần như hoàn toàn bằng ngôn ngữ mới - C. Do đó, UNIX đã trở thành một trong những hệ điều hành sớm nhất được viết bằng một ngôn ngữ bậc cao, một thực tế đã làm cho việc chuyển đổi tiếp theo sang các kiến trúc phần cứng khác có thể.

Nguồn gốc của C giải thích tại sao nó, và hậu duệ của nó C++, đã được sử dụng rộng rãi như các ngôn ngữ lập trình hệ thống ngày nay. Thiết kế của C phát sinh từ những ý tưởng và nhu cầu của một vài cá nhân làm việc hướng tới một mục tiêu duy nhất: phát triển một ngôn ngữ bậc cao để thực hiện kernel UNIX và các phần mềm liên quan. Cũng giống như hệ điều hành UNIX, C được thiết kế bởi các lập trình viên chuyên nghiệp để sử dụng riêng cho họ. Kết quả chúng ta được ngôn ngữ nhỏ, hiệu quả, mạnh mẽ, ngắn gọn, mô-đun, thực dụng và mạch lạc trong thiết kế.

##### UNIX phiên bản từ một đến sáu

Giữa năm 1969 và 1979, UNIX đã trải qua một số phiên bản, được gọi là edittions. Về cơ bản, các bản phát hành này là snapshots của phiên bản phát triển đang phát triển tại AT & T.

- Phiên bản đầu tiên (11-1971): Thời gian này UNIX đang chạy trên PDP-11 với compiler FORTRAN và nhiều chương trình được sử dụng đến nay bao gồm ar, cat, chmod, chown, cp, dc, ed, find, ln, ls, mail, mkdir, mv, rm, sh, và who.

- Phiên bản thứ hai (06-1972): UNIX được cài đặt trên 10 máy trong AT&T.

- Phiên bản thứ ba (02-1973): Phiên bản bao gồm C compiler và lần đầu tiên sử dụng pipe.

- Phiên bản thứ tư (11-1973): đây là phiên bản đầu tiên gần như hoàn toàn được viết bằng C.

- Phiên bản thứ năm (06-1974): Lúc này UNIX đã được cài đặt trên hơn 50 hệ thống.

- Phiên bản thứ sáu (05-1975): Đây là phiên bản đầu tiên được sử dụng rộng rãi ngoài AT&T.

Trong giai đoạn này, việc sử dụng và danh tiếng của UNIX bắt đầu được lan truyền, đầu tiên ở AT&T và sau đó vượt ra ngoài. Một đóng góp quan trọng cho sự lan truyền rộng rãi là việc xuất bản một bài báo về UNIX trên tạp chí ACM.

Lúc này, AT&T được chính phủ phê chuẩn sự độc quyền trên hệ thống telephone của US. Các điều khoản thỏa thuận của AT & T với chính phủ Hoa Kỳ đã ngăn không cho họ bán phần mềm, điều đó có nghĩa là nó không thể bán UNIX như một sản phẩm thương mại. Thay vào đó, bắt đầu vào năm 1974 với phiên bản thứ 5, và đặc biệt là với phiên bản thứ 6, AT & T được cấp phép để UNIX sử dụng trong các trường đại học với một khoản phí trên danh nghĩa. Các bản phân phối của trường đại học bao gồm tài liệu và mã nguồn kernel (khoảng 10.000 dòng tại thời điểm đó).

Việc AT&T phát hành UNIX vào các trường đại học đã góp phần rất lớn vào sự phổ biến và sử dụng hệ điều hành này, và vào năm 1977, UNIX đã chạy ở khoảng 500 nơi, bao gồm 125 trường đại học ở Hoa Kỳ và một số quốc gia khác. UNIX cung cấp cho các trường đại học một hệ điều hành đa người dùng tương tác, rẻ nhưng mạnh mẽ, vào thời điểm các hệ điều hành thương mại rất tốn kém. Nó cũng cho các khoa khoa học máy tính của trường đại học mã nguồn của một hệ điều hành thực sự mà họ có thể sửa đổi và cung cấp cho sinh viên của họ để học hỏi và thử nghiệm. Một số sinh viên, được trang bị kiến thức UNIX, đã trở thành những người truyền bá UNIX. Những người khác tiếp tục phát triển hoặc tham gia vô số các công ty khởi nghiệp bán các máy trạm dễ dàng chuyển đổi sang chạy các hệ thống UNIX.

##### Sự ra đời của BSD và System V

Tháng 1 năm 1979 chứng kiến việc phát hành phiên bản UNIX thứ 7, cải thiện độ tin cậy của hệ thống và cung cấp một hệ thống tập tin nâng cao. Phiên bản này cũng chứa một số công cụ mới, bao gồm awk, make, sed, tar, uucp, shell Bourne và trình biên dịch FORTRAN 77. Bản phát hành của Seventh Edition này cũng rất quan trọng bởi vì, từ thời điểm này, UNIX phân tách thành hai biến thể quan trọng: BSD và System V

[Lược bỏ]

#### 1.2. Lịch sử của Linux.

Thuật ngữ Linux thường được sử dụng để chỉ toàn bộ hệ điều hành giống UNIX mà Linux kernel một phần trong đó. Tuy nhiên, đây có lẽ là một sự nhầm lẫn, vì nhiều thành phần chính trong một bản phân phối Linux thương mại điển hình thực sự bắt nguồn từ một dự án mà trước khi Linux bắt đầu vài năm.

#### 1.2.1 Dự án GNU.

Năm 1984, Richard Stallman, một lập trình viên tài năng làm việc tại MIT, đã bắt tay vào việc tạo ra một bản UNIX "free". Mong muốn của Stallman là về khía cạnh đạo đức, và [free](http://www.gnu.org/philosophy/free-sw.html) được định nghĩa theo nghĩa hợp pháp, chứ không phải là ý nghĩa tài chính. Tuy nhiên, sự tự do pháp lý mà Stallman mô tả mang theo nó là hệ quả ngầm định rằng phần mềm như hệ điều hành sẽ có sẵn mà không có chi phí hoặc rất thấp.

Stallman đã chiến đấu chống lại các hạn chế pháp lý được đặt trên các hệ điều hành độc quyền bởi các nhà cung cấp máy tính. Những hạn chế này có nghĩa là người mua phần mềm máy tính nói chung không thể nhìn thấy mã nguồn của phần mềm họ đang mua và họ chắc chắn không thể sao chép, thay đổi hoặc phân phối lại phần mềm đó. Ông chỉ ra rằng một khuôn khổ như vậy khuyến khích các lập trình viên cạnh tranh với nhau và tích trữ công việc của họ, thay vì hợp tác và chia sẻ nó.

Đáp lại, Stallman bắt đầu dự án GNU (một từ viết tắt được định nghĩa cho “GNU’s not UNIX”) để phát triển toàn bộ hệ thống giống UNIX, tự do, bao gồm kernel và tất cả các gói phần mềm liên quan, và khuyến khích người khác tham gia. Năm 1985, Stallman thành lập Quỹ Phần mềm Tự do (FSF), một tổ chức phi lợi nhuận để hỗ trợ dự án GNU cũng như phát triển phần mềm tự do nói chung.

> Khi dự án GNU được bắt đầu, BSD không free theo nghĩa của Stallman. Việc sử dụng BSD vẫn yêu cầu giấy phép từ AT&T và người dùng không thể tự do sửa đổi và phân phối lại mã nguồn AT&T mà đã hình thành một phần của BSD.

Một trong những kết quả quan trọng của dự án GNU là sự phát triển của Giấy phép Công cộng GNU (GPL), hiện thân pháp lý của khái niệm về phần mềm tự do của Stallman. Phần lớn phần mềm trong bản phân phối Linux, bao gồm kernel, được cấp phép theo GPL hoặc một trong một số giấy phép tương tự. Phần mềm được cấp phép theo GPL phải được cung cấp ở dạng mã nguồn và phải được phân phối lại tự do theo các điều khoản của GPL. Các sửa đổi đối với phần mềm được cấp phép GPL được cho phép tự do, nhưng bất kỳ sự phân phối phần mềm được sửa đổi nào cũng phải tuân theo các điều khoản của GPL. Nếu phần mềm sửa đổi được phân phối dưới dạng thực thi, tác giả cũng phải cho phép bất kỳ người dùng nào cũng có thể lấy mã nguồn được sửa đổi mà không cần chi phí phân phối. Phiên bản đầu tiên của GPL được phát hành vào năm 1989. Phiên bản hiện tại của giấy phép là GPL-3, được phát hành năm 2007. Version 2 của giấy phép, được phát hành vào năm 1991, vẫn được sử dụng rộng rãi và là giấy phép được sử dụng cho kernel Linux.

Dự án GNU ban đầu không tạo ra một kernel UNIX, nhưng đã tạo ra một loạt các chương trình khác. Vì các chương trình này được thiết kế để chạy trên một hệ điều hành giống UNIX, chúng có thể được sử dụng trên các triển khai UNIX hiện có và trong một số trường hợp, thậm chí được chuyển đến các hệ điều hành khác. Trong số các chương trình nổi tiếng hơn do dự án GNU tạo ra là trình soạn thảo văn bản Emacs, GCC (ban đầu là trình biên dịch GNU C, nhưng bây giờ được đổi tên thành bộ sưu tập trình biên dịch GNU, bao gồm các trình biên dịch cho C, C ++ và các ngôn ngữ khác), bash shell, và glibc (thư viện GNU C).

Vào đầu những năm 1990, dự án GNU đã tạo ra một hệ thống gần như hoàn chỉnh, ngoại trừ một thành phần quan trọng: kernel UNIX hoạt động. Dự án GNU đã bắt đầu làm việc trên một thiết kế kernel đầy tham vọng, được gọi là GNU/HURD, dựa trên Mach microkernel. Tuy nhiên, HURD đã không được phát hành. (Tại thời điểm viết bài, công việc tiếp tục trên HURD, hiện chỉ chạy trên kiến ​​trúc x86-32.)

Mọi thứ đã được thiết lập. Tất cả những thứ được yêu cầu là kernel làm việc để kết hợp với hệ thống UNIX đã sẵn sàng trong dự án GNU.

#### 1.2.2 The Linux Kernel

Năm 1991, Linus Torvalds, một sinh viên Phần Lan tại Đại học Helsinki, đã được truyền cảm hứng để viết một hệ điều hành cho máy tính Intel 80386 của mình. Trong quá trình nghiên cứu của mình, Torvalds đã tiếp xúc với Minix, một kernel hệ điều hành giống UNIX nhỏ được phát triển vào giữa những năm 1980 bởi Andrew Tanenbaum, một giáo sư đại học ở Hà Lan. Tanenbaum tạo Minix, hoàn chỉnh với mã nguồn, có sẵn như một công cụ để dạy thiết kế hệ điều hành trong các khóa học đại học. kernel Minix có thể được xây dựng và chạy trên hệ thống 386. Tuy nhiên, vì mục đích chính của nó là một công cụ giảng dạy, nó được thiết kế phần lớn độc lập với kiến trúc phần cứng, và nó không tận dụng được tối đa khả năng của bộ vi xử lý 386.

Do đó, Torvalds bắt đầu một dự án để tạo ra một nhân UNIX hiệu quả, đầy đủ tính năng để chạy trên 386. Trong một vài tháng, Torvalds đã phát triển một hạt nhân cơ bản cho phép anh ta biên dịch và chạy các chương trình GNU khác nhau. Sau đó, vào ngày 5 tháng 10 năm 1991, Torvalds đã yêu cầu sự giúp đỡ của các lập trình viên khác, làm cho thông báo sau đây được công bố nhiều về phiên bản 0.02 của hạt nhân của anh ta trong nhóm tin Usenet comp.os.minix:

> Do you pine for the nice days of Minix-1.1, when men were men and wrote their own device drivers? Are you without a nice project and just dying to cut your teeth on a OS you can try to modify for your needs? Are you finding it frustrating when everything works on Minix? No more all-nighters to get a nifty program working? Then this post might be just for you. As Imentioned a month ago, I’m working on a free version of a Minix-look-alike for AT-386 computers. It has finally reached the stage where it’s even usable (though may not be depending on what you want), and I am willing to put out the sources for wider distribution. It is just version 0.02 . . . but I’ve successfully run bash, gcc, gnu-make, gnu-sed, compress, etc. under it. Following a time-honored tradition of giving UNIX clones names ending with the letter X, the kernel was (eventually) baptized Linux. Initially, Linux was placed under a more restrictive license, but Torvalds soon made it available under the GNU GPL.

Sự kêu gọi đã hiệu quả. Các lập trình viên khác đã tham gia cùng Torvalds trong sự phát triển của Linux, thêm nhiều tính năng khác nhau, chẳng hạn như hệ thống tệp được cải thiện, hỗ trợ mạng, trình điều khiển thiết bị và hỗ trợ đa bộ xử lý. Vào tháng 3 năm 1994, các nhà phát triển đã có thể phát hành phiên bản 1.0. Linux 1.2 xuất hiện vào tháng 3 năm 1995, Linux 2.0 vào tháng 6 năm 1996, Linux 2.2 vào tháng 1 năm 1999 và Linux 2.4 vào tháng 1 năm 2001. Làm việc trên hạt nhân 2.5 phát triển bắt đầu vào tháng 11 năm 2001 và dẫn đến việc phát hành Linux 2.6 vào tháng 12 năm 2003.

[lược bỏ]

##### Linux distributions

Nói một cách chính xác, thuật ngữ Linux chỉ đề cập đến hạt nhân được phát triển bởi Linus Torvalds và những người khác. Tuy nhiên, thuật ngữ Linux thường được sử dụng với nghĩa là hạt nhân, cộng với một loạt các phần mềm khác (công cụ và thư viện) mà cùng nhau tạo ra một hệ điều hành hoàn chỉnh. Trong những ngày đầu của Linux, người dùng được yêu cầu kết hợp tất cả phần mềm này, tạo ra một hệ thống tập tin, đặt chính xác và cấu hình tất cả các phần mềm trên hệ thống tập tin đó. Điều này đòi hỏi thời gian và chuyên môn đáng kể. Kết quả là, một thị trường mở cho các nhà phân phối Linux, người tạo ra các gói (bản phân phối) để tự động hóa hầu hết quá trình cài đặt, tạo ra một hệ thống tệp, cài đặt hạt nhân và phần mềm cần thiết khác.

Các bản phân phối sớm nhất xuất hiện vào năm 1992, và bao gồm MCC Interim Linux (Trung tâm Máy tính Manchester, Vương quốc Anh), TAMU (Đại học Texas A&M) và SLS (SoftLanding Linux System). Bản phân phối thương mại còn tồn tại lâu đời nhất, Slackware, xuất hiện vào năm 1993. Bản phân phối Debian phi thương mại xuất hiện cùng lúc, và SUSE và Red Hat đã sớm theo sau. Bản phân phối Ubuntu rất phổ biến đầu tiên xuất hiện vào năm 2004. Ngày nay, nhiều công ty phân phối cũng sử dụng các lập trình viên tích cực đóng góp cho các dự án phần mềm miễn phí hiện có hoặc khởi tạo các dự án mới

### 1.3 Standardization

[Lược bỏ]

#### 1.3.6 UNIX Standards Timeline

![hình 1-1](https://github.com/ctnguyenvn/Linux-Programming/blob/master/Linux-Programming-Interface/Chapter_01/img/1.png)

> Hình 1-1 tóm tắt các mối quan hệ giữa các tiêu chuẩn khác nhau được, và đặt các chuẩn theo thứ tự thời gian. Trong sơ đồ này, các đường liền mạch chỉ ra gốc trực tiếp giữa các chuẩn và mũi tên đứt quãng cho biết các trường hợp tiêu chuẩn ảnh hưởng đến một chuẩn khác, được kết hợp như một phần của tiêu chuẩn khác, hoặc đơn giản là trì hoãn một chuẩn khác.

[Lược bỏ]

### 1.4 Summary

Hệ thống UNIX lần đầu tiên được triển khai vào năm 1969 trên máy tính mini PDP-7 của Ken Thompson tại Phòng thí nghiệm Bell (một phần của AT&T). Hệ điều hành đã thu hút nhiều ý tưởng. Vào năm 1973, UNIX đã được chuyển sang máy tính mini PDP-11 và viết lại bằng C, một ngôn ngữ lập trình được thiết kế và triển khai tại Phòng thí nghiệm Bell bởi Dennis Ritchie. Bị ngăn cản một cách hợp pháp khi bán UNIX, AT&T thay vì phân phối hệ thống hoàn chỉnh cho các trường đại học với một khoản phí không đáng kể. Bản phân phối này bao gồm mã nguồn và trở nên rất phổ biến trong các trường đại học, vì nó cung cấp một hệ điều hành giá rẻ có mã được nghiên cứu và sửa đổi bởi các học giả và sinh viên khoa học máy tính.

Đại học California tại Berkeley đóng một vai trò quan trọng trong sự phát triển của hệ thống UNIX. Ở đó, Ken Thompson và một số sinh viên tốt nghiệp đã mở rộng hệ điều hành. Đến năm 1979, trường đại học đã sản xuất phân phối UNIX của riêng mình, BSD. Sự phân bố này trở nên phổ biến trong các học viện và hình thành cơ sở cho một số triển khai thương mại.

Trong khi đó, sự phân chia độc quyền AT&T cho phép công ty bán hệ thống UNIX. Điều này dẫn đến một biến thể quan trọng khác của UNIX, System V, cũng đã hình thành cơ sở cho một số triển khai thương mại.

Hai dòng khác nhau dẫn đến sự phát triển của GNU/Linux. Một trong số đó là dự án GNU, được sáng lập bởi Richard Stallman. Vào cuối những năm 1980, dự án GNU đã tạo ra một triển khai UNIX hoàn toàn phân tán và tự do. Một phần còn thiếu là một hạt nhân hoạt động. Năm 1991, lấy cảm hứng từ hạt nhân Minix được viết bởi Andrew Tanenbaum, Linus Torvalds đã tạo ra một hạt nhân UNIX làm việc cho kiến ​​trúc Intel x86-32. Torvalds mời các lập trình viên khác tham gia cùng anh ta trong việc cải thiện hạt nhân. Nhiều lập trình viên đã làm như vậy, và, theo thời gian, Linux đã được mở rộng và chuyển sang một loạt các kiến ​​trúc phần cứng.

Các vấn đề về tính di động phát sinh từ các biến thể trong việc triển khai UNIX và C đã tồn tại vào cuối những năm 1980 đã tạo ra một áp lực mạnh mẽ cho tiêu chuẩn. Ngôn ngữ C được tiêu chuẩn hóa vào năm 1989 (C89), và một tiêu chuẩn sửa đổi được sản xuất vào năm 1999 (C99). Nỗ lực đầu tiên để chuẩn hóa giao diện hệ điều hành mang lại POSIX.1, được phê chuẩn như một tiêu chuẩn IEEE vào năm 1988 và là tiêu chuẩn ISO vào năm 1990. Trong thập niên 1990, các tiêu chuẩn khác đã được soạn thảo, bao gồm các phiên bản khác nhau của Đặc tả UNIX đơn. Năm 2001, tiêu chuẩn kết hợp POSIX 1003.1-2001 và SUSv3 đã được phê chuẩn. Tiêu chuẩn này củng cố và mở rộng các tiêu chuẩn POSIX trước đó và các phiên bản trước của Đặc tả UNIX Đơn. Trong năm 2008, bản sửa đổi tiêu chuẩn đã được hoàn thành ít hơn, tạo ra tiêu chuẩn kết hợp POSIX 1003.1-2008 và SUSv4.

Không giống như hầu hết các triển khai UNIX thương mại, Linux phân tách việc triển khai thực hiện từ các phân phối. Do đó, không có bản phân phối Linux “chính thức” duy nhất. Mỗi bản phân phối của nhà phân phối Linux bao gồm snapshot hạt nhân ổn định hiện tại, với nhiều bản vá được áp dụng. LSB phát triển và thúc đẩy một bộ tiêu chuẩn cho các hệ thống Linux với mục đích đảm bảo khả năng tương thích ứng dụng nhị phân trên các bản phân phối Linux, do đó các ứng dụng đã biên dịch có thể chạy trên bất kỳ hệ thống tuân thủ LSB nào chạy trên cùng phần cứng.