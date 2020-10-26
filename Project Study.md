Phụ lục: Từ ngữ thường dùng trong tài liệu này:
---
- Sàn chính: sàn giao dịch gốc, nơi người dùng có thể giao dịch, đăng ký, nạp tiền, v/v.
- Hệ thống: trang web dành cho copy trading, là trang web mục tiêu của dự án.
- Người dùng: khách hàng của *sàn chính*, là người sử dụng *hệ thống* với mục đích trở thành follower hoặc leader.
- Nhà phát triển: người phát triển hệ thống.

---

**I. Chức năng đảm bảo**
===
Người dùng:
---
1. Đăng nhập
<!---
Một trong số các giải pháp sau:
     1. Sử dụng **API OAuth 2.0** do **sàn chính cung cấp** (khuyến khích nếu sàn **đã tích hợp sẵn OAuth**; nếu sàn **chưa tích hợp sẵn OAuth** thì không khuyến khích vì sẽ mất thời gian để phát triển và thử nghiệm).
     2. Sử dụng **email//số điện thoại** của người dùng trên *sàn chính* và **mã bí mật** *(secret code)* do *sàn chính* tạo ra, gửi cho *người dùng* và *hệ thống*.)
-->
     *Người dùng* có thể đăng nhập vào *hệ thống* thông qua thông tin của *sàn chính* mà **không cần sử dụng mật khẩu của người dùng tại *sàn chính***. 
     > Hiện *hệ thống* đang có 3 giải pháp có thể thực hiện chức năng này, thông tin về giải pháp sẽ được cung cấp với *sàn chính* sau khi *hệ thống* được chấp thuận.
2. Trở thành leader
<!---
     - *Người dùng* **cần** chọn tài khoản MT5 sẵn có.
--->
    *Người dùng* có thể chọn trở thành leader trong hệ thống. *Người dùng* **cần** cung cấp các thông tin cần thiết, các thông tin này được đề cập tại **mục II.2.ii**
3. Trở thành follower
<!---
     - *Người dùng* **phải** chọn tài khoản MT5 sẵn có.
--->
    *Người dùng* có thể chọn trở thành follower trong hệ thống. *Người dùng* **cần** cung cấp các thông tin cần thiết. Thông tin này được đề cập tại **mục II.2.i**.
4. Theo dõi tài khoản MT5.
     - *Người dùng* có thể theo dõi thông tin của (các) tài khoản MT5 của mình. Các thông tin này được đề cập tại **mục II.2.iiI**.
5. Thống kê lợi nhuận
     - *

Bảo mật:
---
- 

---

Dashboard
---

---

**II. Yêu cầu sàn chính cung cấp:**
===
1. Chức năng
     1. **API kiểm tra thông tin *người dùng*** để phục vụ cho chức năng đăng nhập tại **mục I.1**.
     > Thông tin của API sẽ được thống nhất với *sàn chính* sau khi *hệ thống* được chấp thuận.
     3. **API lấy thông tin tài khoản MT5** theo **mục II.4**.
2. Thông tin
     1. Những thông tin *người dùng* **cần** cung cấp khi chọn trở thành follower.
     2. Những thông tin *người dùng* **cần** cung cấp khi chọn trở thành leader.
     2. Những thông tin về tài khoản MT5 mà *người dùng* **được phép** theo dõi.
     3. Môi trường hoạt động *hệ thống*.
     > *Nhà phát triển* muốn phát triển *hệ thống* bằng ngôn ngữ **Python** *hoặc* **JavaScript**, hosting có sẵn của *sàn chính* **có thể** sẽ không thích hợp với các môi trường này.
     > *Sàn chính* có thể yêu cầu *nhà phát triển* sử dụng môi trường thuận tiện hơn cho *sàn chính* nhưng sẽ **tăng thời gian phát triển** của *hệ thống*
     <!--- Người dùng có thể vừa là leader vừa là follower trên cùng 1 tài khoản MT5? Trên nhiều tài khoản MT5?>
3. Tài nguyên
     1. **Tên miền** và **hosting** cho *hệ thống*. 

---

**III. Chức năng hệ thống không chịu trách nhiệm**
===
Hệ thống sẽ **không chịu trách nhiệm** hoặc **chưa chịu trách nhiệm** (*có thể hoàn thành vào các giai đoạn khác của dự án*) về những chức năng sau:

1. Chức năng **đăng ký** và **lấy lại** mật khẩu dành cho *người dùng*: *Người dùng* có thể dùng những chức năng này tại *sàn chính*.
2. Chức năng **tạo tài khoản MT5 mới** dành cho *người dùng*: *Người dùng* có thể dùng chức năng này tại *sàn chính*.
3. Chức năng **nạp tiền** và **gửi tiền** dưới bất kỳ hình thức nào dành cho *người dùng*: *Người dùng có thể dùng chức năng này tại sàn chính*.
3. *Nhà phát triển* không chịu trách nhiệm về **tên miền** và **hosting** cho hệ thống. Nếu *sàn chính*
4. *Hệ thống* không chịu trách nhiệm về *mã bí mật* của *người dùng*. *Sàn chính* và *người dùng* phải chịu trách nhiệm về *mã bí mật* của người dùng vì mọi chức năng của *hệ thống* chỉ có thể sử dụng khi có *mã bí mật* của *người dùng*.