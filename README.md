# SESSION 20 – BÀI TẬP TỔNG HỢP

## QUY TRÌNH GỠ LỖI THỰC TẾ CỦA DEVELOPER

# PHẦN 1 – GOOGLING ĐÚNG CÁCH

### 1. Vì sao câu hỏi văn nói tìm kiếm kém hiệu quả?

Câu hỏi `tại sao em cài node xong mà gõ npm nó không nhận vậy thầy ơi` sử dụng ngôn ngữ giao tiếp, quá dài và không có từ khóa kỹ thuật chính xác.

Google khó xác định lỗi cụ thể nên có thể trả về nhiều kết quả không liên quan.

Cần sử dụng thông báo lỗi nguyên văn và tên phần mềm để tìm kiếm chính xác hơn.

### 2. Bóc tách lỗi theo 3 thành phần

| Thành phần                  | Nội dung bóc tách                                                                             |
| --------------------------- | --------------------------------------------------------------------------------------------- |
| Tên phần mềm / Hệ điều hành | Node.js / Windows 11                                                                          |
| Mã lỗi nguyên văn           | `'npm' is not recognized as an internal or external command, operable program or batch file.` |
| Thao tác đang làm           | Gõ lệnh `npm -v` trong Terminal của VS Code để kiểm tra phiên bản npm.                        |

### 3. Ba câu truy vấn Google tối ưu

Câu 1 – Dùng `site:`

```
site:stackoverflow.com npm is not recognized Windows 11
```

Câu 2 – Dùng ngoặc kép `" "`

```
"npm is not recognized as an internal or external command"
```

Câu 3 – Dùng dấu `-`

```
npm is not recognized Windows 11 -windows-xp
```

# PHẦN 2 – THẨM ĐỊNH STACKOVERFLOW

### 1. So sánh câu trả lời A và B

| Tiêu chí                        | Câu trả lời A                            | Câu trả lời B                                      |
| ------------------------------- | ---------------------------------------- | -------------------------------------------------- |
| Vote & Tích xanh                | +186 vote, có tích xanh Accepted Answer. | +2 vote, không có tích xanh.                       |
| Thời gian đăng bài              | 2 năm trước, tương đối mới.              | 9 năm trước, khá cũ.                               |
| Tags khớp hệ điều hành/phần mềm | `node.js`, `windows`, `npm`, phù hợp.    | `node.js`, `windows-xp`, không phù hợp Windows 11. |

### 2. Lựa chọn câu trả lời

Em chọn Câu trả lời A vì có nhiều lượt bình chọn, được đánh dấu Accepted Answer và nội dung phù hợp với Node.js trên Windows.

Câu trả lời B là một cái bẫy nguy hiểm vì hướng dẫn cài lại driver mạng cho Windows XP không liên quan đến lỗi npm trên Windows 11. Nếu làm theo sẽ mất thời gian và có thể gây ra lỗi hệ thống khác.

### 3. Quy trình 30 giây đọc lướt StackOverflow

Thực hiện theo thứ tự:

1. Tags: Kiểm tra thẻ có đúng phần mềm và hệ điều hành không.
2. Vote: Xem số lượt bình chọn của câu trả lời.
3. Accepted Answer: Kiểm tra câu trả lời có tích xanh không.
4. Thời gian: Xem bài viết có quá cũ không.
5. Nội dung: Đọc nhanh giải pháp và kiểm tra xem có phù hợp với lỗi đang gặp không.

# PHẦN 3 – HỎI AI ĐÚNG CÁCH VÀ NHẬN DIỆN RỦI RO

### 1. Prompt hoàn chỉnh theo 3 thành phần

[Context – Ngữ cảnh]

Tôi là sinh viên đang học lập trình web trên laptop Windows 11. Tôi vừa cài đặt Node.js và sử dụng Terminal trong VS Code để kiểm tra phiên bản npm. Tôi đã thử thêm đường dẫn cài đặt Node.js vào biến môi trường PATH, sau đó đóng và mở lại Terminal mới nhưng lỗi vẫn xuất hiện.

[Raw Error – Lỗi nguyên văn]

```
'npm' is not recognized as an internal or external command, operable program or batch file.
```

[Instruction – Yêu cầu]

Hãy đóng vai một trợ giảng lập trình, giúp tôi:

1. Giải thích nguyên nhân lỗi bằng tiếng Việt đơn giản.
2. Đưa ra các bước kiểm tra và khắc phục trên Windows 11.
3. Hướng dẫn kiểm tra biến môi trường PATH và vị trí cài đặt npm.
4. Không đề xuất lệnh xóa dữ liệu hoặc thay đổi hệ thống nguy hiểm.
5. Giải thích rõ tác dụng của từng câu lệnh trước khi thực hiện.

### 2. Đánh giá câu trả lời AI ở mục 3e

Không an toàn – Tuyệt đối không thực hiện

Lệnh AI đề xuất:

```
del /f /s /q C:\Windows\System32\*
```

Đây là câu trả lời nguy hiểm vì:

- Nguyên tắc 1 – Không chạy lệnh mù quáng: Lệnh `del` có thể xóa hàng loạt tệp hệ thống Windows.
- Nguyên tắc 2 – Chống ảo giác AI: Lệnh xóa file trong System32 không giải quyết được lỗi biến môi trường PATH.
- Nguyên tắc 3 – Bảo vệ thông tin: Không cung cấp mật khẩu, API Key hoặc thông tin bí mật cho AI.

### 3. Cách phản hồi và hỏi lại AI

Em sẽ hỏi lại:

```
Lệnh bạn đề xuất có thể xóa các tệp quan trọng
trong thư mục C:\Windows\System32.

Hãy giải thích cụ thể tác dụng và rủi ro của lệnh này.
Tại sao lệnh xóa tệp hệ thống lại có thể sửa lỗi PATH?

Tôi không muốn thực hiện lệnh nguy hiểm.
Hãy đề xuất phương pháp kiểm tra PATH và npm
an toàn trên Windows 11, không làm mất dữ liệu.
```

Em sẽ không chạy lệnh cho đến khi xác minh được tính an toàn và sự cần thiết của nó.

# PHẦN 4 – VIẾT BUG REPORT CHUẨN ĐỂ NHỜ HỖ TRỢ

### 1. Tin nhắn kém

```
Thầy ơi máy em bị lỗi npm rồi,
em cài mãi không được, thầy giúp em với ạ!
```

### 2. Tin nhắn chuẩn theo Bug Reporting Framework 4 bước

| Mảnh ghép        | Nội dung trong tin nhắn                                                                                                                           |
| ---------------- | ------------------------------------------------------------------------------------------------------------------------------------------------- |
| Context          | Em đang sử dụng Windows 11, vừa cài Node.js và kiểm tra npm bằng Terminal trong VS Code.                                                          |
| Expected         | Mong muốn lệnh `npm -v` hiển thị phiên bản npm đã cài đặt.                                                                                        |
| Actual           | Terminal báo lỗi `'npm' is not recognized as an internal or external command, operable program or batch file.`                                    |
| Log & Screenshot | Em đã thử thêm đường dẫn cài đặt Node.js vào PATH và mở Terminal mới nhưng lỗi vẫn xuất hiện. Em gửi kèm ảnh chụp thông báo lỗi để thầy kiểm tra. |

Tin nhắn hoàn chỉnh gửi trợ giảng:

Em chào thầy ạ!

Em đang sử dụng Windows 11 và vừa cài đặt Node.js để học lập trình web. Khi mở Terminal trong VS Code và chạy lệnh `npm -v`, em gặp lỗi:

`'npm' is not recognized as an internal or external command, operable program or batch file.`

- **Expected:** Em mong muốn Terminal hiển thị phiên bản npm.
- **Actual:** Terminal báo lỗi không nhận diện được lệnh npm.
- **Đã thử:** Em đã thêm đường dẫn cài đặt Node.js vào biến môi trường PATH và mở lại Terminal mới nhưng vẫn không khắc phục được.

Em gửi kèm ảnh chụp thông báo lỗi. Mong thầy hướng dẫn em cách kiểm tra và khắc phục lỗi này ạ.

Em cảm ơn thầy!

### 3. Phím tắt chụp màn hình và lưu ý bảo mật

- Phím tắt: `Windows + Shift + S`.
- Dùng chuột chọn vùng màn hình chứa thông báo lỗi cần gửi.
- Lưu ý bảo mật: Kiểm tra và che các thông tin nhạy cảm như API Key, mật khẩu, token hoặc thông tin cá nhân trước khi gửi ảnh.
