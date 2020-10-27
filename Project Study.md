*Tài liệu này chỉ là tài liệu tóm tắt dùng để thể hiện nội dung sơ bộ của hệ thống, không phải là nội dung cuối cùng, có thể thêm, sửa hay xoá các yêu cầu vào thời gian sau này. Phương thức làm việc, cách triển khai hệ thống, cách thiết kế, cũng như các yêu cầu chi tiết đối với từng vấn đề giữa nhà phát triển và sàn sẽ được thoả thuận kỹ và có tài liệu chi tiết cung cấp cho sàn sau khi hệ thống được chấp thuận.*

---
Phụ lục: Từ ngữ thường dùng trong tài liệu này:
---
- *Quản trị viên*: là người có toàn quyền quản lý trang web quản lý copy-trading.
- *Hệ thống*: trang web quản lý copy trading, là trang web mục tiêu của dự án do *nhà phát triển* xây dựng.
- *Người dùng*: khách hàng của *sàn*, là người sử dụng *hệ thống* với mục đích quản lý tài khoản copy-trading của mình.
- *Nhà phát triển*: người viết tài liệu này và cũng là người phát triển *hệ thống*, chịu trách nhiệm với mọi vấn đề của *hệ thống*.
- API: Application Programming Interface, là phương thức kết nối, giao tiếp giữa trang web quản lý copy-trading và hệ thống có sẵn của sàn.
- *Tài liệu chi tiết*: là tài liệu được *nhà phát triển* cung cấp sau khi dự án được chấp thuận, có đầy đủ các phương thức làm việc, cách triển khai dự án, cách thiết kế, cũng như các yêu cầu chi tiết đối với từng vấn đề giữa hai bên sau khi thoả thuận với *sàn*.
---

**I. Chức năng đảm bảo**
===
Người dùng có thể:
---
1. Đăng nhập\
*Người dùng* có thể đăng nhập vào *hệ thống* thông qua thông tin của *người dùng* mà **không cần sử dụng mật khẩu của người dùng tại *sàn***.
     > Hiện *hệ thống* đang có 3 giải pháp có thể thực hiện chức năng này, thông tin về giải pháp sẽ được *nhà phát triển* thảo luận với *quản trị viên* và sẽ được trình bày đầy đủ trong *tài liệu chi tiết*.

2. Xem danh sách leader\
*Người dùng* có thể xem danh sách các leader đã được hệ thống xác thực, thể hiện các thông số của các leader đó (thông tin, lịch sử giao dịch, tổng lợi nhuận, v/v). Từ danh sách các leader, *người dùng* có thể chọn follow một (vài) leader trong danh sách đó.
3. Trở thành leader\
*Người dùng* có thể chọn trở thành leader trong hệ thống và vẫn giữ được các quyền của *người dùng*. *Người dùng* **cần** cung cấp các thông tin mà *quản trị viên* yêu cầu trước khi trở thành leader.
4. Trở thành follower\
    *Người dùng* sau khi follow một (vài) leader trong hệ thống sẽ trở thành follower và vẫn giữ nguyên các quyền của *người dùng*. *Người dùng* **cần** cung cấp các thông tin mà *quản trị viên* yêu cầu trước khi trở thành follower.
5. Theo dõi (các) tài khoản MT5 của mình.\
      *Người dùng*  có thể theo dõi thông tin (các) tài khoản MT5 của mình.
6. Thống kê lợi nhuận\
      *Người dùng* có thể xem thống kê lợi nhuận của mình theo nhiều phương thức như lợi nhuận ngày hay lợi nhuận ròng, v/v dưới dạng thống kê hay biểu đồ.
7. Nhận thông báo\
      *Người dùng* có thể xem thông báo do *quản trị viên* hoặc *hệ thống* gửi tới.
8. Liên hệ hỗ trợ\
      Nếu có vấn đề xảy ra trong quá trình sử dụng *hệ thống*, người dùng có thể liên hệ với *nhà phát triển* hoặc *quản trị viên*, tuỳ theo từng trường hợp vấn đề cụ thể.

---
Follower có thể:
---
1. Xem danh sách leader đã follow\
      *Người dùng* có thể xem danh sách các leader đã follow, từ đó có thể thực hiện các tác vụ khác.

2. Ngừng follow leader\
      *Người dùng* có quyền huỷ follow (một hay nhiều) các leader trong danh sách leader đã follow.
3. Chỉnh sửa thông tin copy-trading\
      *Người dùng* có thể chỉnh sửa thông tin (tỷ lệ chia lợi nhuận, tỷ lệ lot, v/v) của gói copy-trading của (một hay nhiều) leader.

---
Leader có thể:
---
1. Xem danh sách các follower\
      Leader có thể xem danh sách các *người dùng* follow mình.
2. Xem thống kê \
      Leader có thể xem thống kê (tổng lợi nhuận, tỷ lệ lợi nhuận đã được chia, v/v) theo dạng thông số hoặc biểu đồ.
3. Chỉnh sửa thông tin\
      Leader có thể chỉnh sửa các thông gói copy-trading của mình như tỷ lệ chia lợi nhuận, tài khoản tối thiểu, v/v.

---
*Quản trị viên* có thể:
---
1. Xem thông tin *người dùng*\
      *Quản trị viên* có thể xem thông tin (một hay nhiều) *người dùng* bất kỳ trong *hệ thống*.

2. Duyệt leader\
      *Người dùng* sau khi đăng ký làm leader sẽ được đưa vào hàng chờ, *hệ thống* có thể xem thông tin *người dùng*, sau đó có thể phê duyệt để (một hay nhiều) *người dùng* đó trở thành leader hoặc từ chối.
      > Hoặc *hệ thống* có thể tự động hoá quá trình này.
3. Thêm leader\
      *Quản trị viên* có thể thêm (một hay nhiều) leader trực tiếp vào *hệ thống* mà không cần phải chờ leader đăng ký.
4. Huỷ tư cách leader\
      *Quản trị viên* có thể huỷ tư cách (một hay nhiều) leader của bất kỳ leader nào. Có thể thông báo hoặc không thông báo cho leader đó.
5. Gửi thông báo\
      *Hệ thống* cho phép *quản trị viên* gửi (một hay nhiều) thông báo cho tất cả *người dùng* copy-trading hoặc một *người dùng* cụ thể. Có thể cài đặt trước thông báo và gửi thông báo lặp lại (sau một khoảng thời gian).
6. Xem thống kê *hệ thống*\
      *Quản trị viên* có thể xem thống kê về mọi thông số (số người dùng, tổng thu, lợi nhuận, v/v) của *hệ thống*.
      > Thông tin của các thông số mà *quản trị viên* muốn theo dõi sẽ được thoả thuận đầy đủ tại *tài liệu chi tiết*.
7. Xuất thông tin\
      *Quản trị viên* có thể xuất các thông tin khác nhau (doanh số, người dùng, lợi nhuận, v/v).

---
**II. Ước lượng thời gian thực hiện**
===


1. Người dùng:

- Đăng nhập: 6h
- Xem danh sách leader: 12h
- Trở thành leader: 2h
- Trở thành follower: 2h
- Theo dõi (các) tài khoản MT5: 6h
- Thống kê lợi nhuận: 12h
- Nhận thông báo: 2h
- Liên hệ hỗ trợ: 1h
Tổng cộng: 43h


2. Follower:

- Xem danh sách leader đã follow: 4h
- Ngừng follow leader: 2h
- Chỉnh sửa thông tin copy-trading: 2h
Tổng cộng: 8h
3. Leader:

- Xem danh sách các follower: 4h
- Xem thống kê: 16h
- Chỉnh sửa thông tin: 2h
Tổng cộng: 22h
4. Quản trị viên:

- Xem thông tin người dùng: 1h
- Duyệt leader: 1h
- Thêm leader: 1h
- Huỷ tư cách leader: 1h
- Gửi thông báo: 8h
- Xem thống kê hệ thống: 16h
- Xuất thông tin: 6h
Tổng cộng: 34h
5. Giao diện:

- Tạo giao diện cho toàn trang web: 36h
- Đảm bảo trang web hoạt động trên nhiều loại thiết bị: 24h\
Tổng cộng: 60h


Thời gian ước tính cho toàn hệ thống: 167h.
Mức chi phí cho hệ thống được nhắc tới tại **mục III.6**.
---

---
**II. Trách nhiệm của *nhà phát triển***
===
*Nhà phát triển* đảm bảo:

- theo dõi bảo trì hệ thống liên tục một tháng đầu tiên sau khi hệ thống hoàn thành (*hệ thống* vốn được thiết kế để không cần phải bảo trì thường xuyên).
- sửa lỗi (nếu có) liên quan đến chức năng mà *nhà hệ thống* chịu trách nhiệm.
- ưu tiên hợp tác với *sàn* nếu có nhu cầu thêm chức năng hoặc bàn giao *hệ thống* tới nhà phát triển khác của *sàn*.
- bảo mật thông tin của *người dùng* và *quản trị viên*.
- *hệ thống* hoạt động thông suốt, nhanh chóng với thời gian chết ngắn hoặc không có.
- *hệ thống* ổn định, có thể phục hồi nhanh nếu xảy ra sự cố.
- mọi hoạt động được tạo ra bởi *người dùng* hoặc *quản trị viên* đều được thực hiện chính xác với thời gian chờ thấp.

**III. Trách nhiệm của *sàn***
===
Để đẩy nhanh quá trình phát triển *hệ thống*, *sàn* nên có trách nhiệm cung cấp:

1. **API kiểm tra thông tin *người dùng*** để phục vụ cho chức năng đăng nhập tại **mục I.1**.
2. **API lấy thông tin tài khoản MT5** để phục vụ cho chức năng theo dõi tài khoản MT5 tại **mục I.4** và chức năng thống kê lợi nhuận tại **mục I.5**.
     >Thông tin về giải pháp API sẽ được đề cập đầy đủ tại *tài liệu chi tiết*.


3. **Tên miền** cho *hệ thống*.
4. **Hosting** cho *hệ thống*.
     > *Nhà phát triển* đã có giải pháp giành cho tên miền và hosting của *hệ thống*, sẽ được đề cập đầy đủ tại *tài liệu chi tiết*.
5. (tuỳ ý) **Hệ thống lưu trữ** sử dụng cho việc back-up *hệ thống*.
6. Mức chi trả 1500$ cho việc hoàn thành *hệ thống*. Sau thời gian 1 tháng như *nhà phát triển* đảm bảo, nếu *sàn* vẫn muốn *nhà phát triển* bảo trì trang web hoặc thêm/ chỉnh sửa chức năng, *sàn* phải chịu trách nhiệm thêm về phần chi phí này với mức 10$/h.

---
**IV. Lý do nên chọn *hệ thống* này:**
===
- *Hệ thống* không cần sử dụng database, từ đó tiết kiệm chi phí cho *Quản trị viên* và tiết kiệm thời gian phát triển *hệ thống*.
- *Hệ thống* sử dụng thông tin trực tiếp từ hệ thống có sẵn của sàn mà vẫn đảm bảo bảo mật thông tin cho *người dùng*. *Người dùng* có thể dễ dàng sử dụng *hệ thống* và *Quản trị viên* có thể dễ dàng quản lý *người dùng* cũng như *hệ thống*.
- *Hệ thống* hoạt động trên môi trường web, có thể truy cập, hiển thị và hoạt động được bằng phần lớn các thiết bị có kết nối Internet cơ bản.
- *Nhà phát triển* sẽ có *tài liệu chi tiết* chứa đầy đủ thông tin của *hệ thống*, thuận lợi cho việc nâng cấp và bảo trì *hệ thống* sau này.
- *Sàn* sẽ có quyền theo dõi tất cả quá trình phát triển của *hệ thống*.