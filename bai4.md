# BÀI 4: Phân tích & Lựa chọn (Liêm chính học thuật và Kiểm chứng đầu ra)

## Đáp án: Phương án B

## 1. Phân tích lý do lựa chọn phương án B

Phương án B là lựa chọn đúng đắn nhất vì thể hiện đầy đủ trách nhiệm học thuật của người học và vai trò "kiểm duyệt viên" (AI Verifier) thay vì chỉ là người sao chép kết quả do AI tạo ra.

Mặc dù đoạn mã nguồn do AI sinh ra có thể hoạt động đúng với một số trường hợp đơn giản, nhưng trong các bài toán tài chính, việc sử dụng kiểu dữ liệu `double` tiềm ẩn nguy cơ sai số làm tròn do cách biểu diễn số thực theo chuẩn nhị phân.

Ví dụ trong Java:

```java
System.out.println(0.1 + 0.2);
```

Kết quả:

```java
0.30000000000000004
```

Sai số này tuy nhỏ nhưng có thể tích lũy qua hàng trăm hoặc hàng nghìn lần tính lãi, dẫn đến kết quả không chính xác.

Phương án B thể hiện đúng tinh thần của Lesson 5 vì người học:

- Không tin tưởng tuyệt đối vào kết quả do AI sinh ra.
- Chủ động kiểm tra và đánh giá rủi ro kỹ thuật.
- Tra cứu tài liệu Java chính thức để tìm giải pháp phù hợp.
- Sử dụng lớp `BigDecimal`, vốn là giải pháp chuẩn cho các phép tính tài chính.
- Thiết kế lại prompt để AI tạo mã nguồn chính xác hơn.
- Tự viết các bộ kiểm thử với nhiều trường hợp biên nhằm xác minh kết quả.

Đây chính là quy trình làm việc chuyên nghiệp trong thực tế khi sử dụng AI hỗ trợ lập trình.

---

## 2. Liên hệ với tiêu chuẩn kỹ thuật thực tế

Trong các hệ thống:

- Ngân hàng
- Ví điện tử
- Thanh toán trực tuyến
- Kế toán
- Quản lý tài chính

Kiểu dữ liệu `BigDecimal` được sử dụng phổ biến vì:

- Độ chính xác cao.
- Không phát sinh sai số nhị phân như `double`.
- Hỗ trợ các chế độ làm tròn thông qua `RoundingMode`.
- Phù hợp với các yêu cầu nghiệp vụ liên quan đến tiền tệ.

Do đó, việc phát hiện hạn chế của `double` và thay thế bằng `BigDecimal` thể hiện năng lực kỹ thuật và ý thức trách nhiệm của người học.

---

## 3. Nhược điểm của phương án A

### Nội dung phương án A

Sao chép nguyên văn mã nguồn của AI vì hệ thống kiểm thử hiện tại vẫn cho kết quả đúng.

### Nhược điểm

1. Thiếu tinh thần kiểm chứng đầu ra của AI.
2. Tin tưởng tuyệt đối vào AI mà không đánh giá tính chính xác kỹ thuật.
3. Bỏ qua rủi ro sai số trong các bài toán tài chính.
4. Chỉ tập trung vượt qua bộ test thay vì đảm bảo chất lượng phần mềm.
5. Không phù hợp với nguyên tắc liêm chính học thuật được học trong Lesson 5.

Đây là hành vi sử dụng AI một cách thụ động và không có trách nhiệm.

---

## 4. Nhược điểm của phương án C

### Nội dung phương án C

Thay đổi từ `double` sang `float` để tiết kiệm bộ nhớ.

### Nhược điểm

1. `float` vẫn là kiểu số thực dấu phẩy động nên vẫn tồn tại lỗi làm tròn.
2. Độ chính xác của `float` còn thấp hơn `double`.
3. Không giải quyết được bản chất của bài toán tài chính.
4. Không thực hiện bất kỳ hoạt động kiểm chứng hoặc tra cứu tài liệu nào.
5. Đặt yếu tố tiết kiệm bộ nhớ lên trên độ chính xác dữ liệu tài chính.

Trong thực tế, việc dùng `float` cho tính toán tiền tệ là không phù hợp và có thể gây sai lệch kết quả nghiêm trọng.

---

## 5. Kết luận

Phương án **B** là đáp án đúng vì thể hiện đầy đủ trách nhiệm của người học khi sử dụng AI:

- Nhận diện hạn chế trong mã nguồn do AI sinh ra.
- Chủ động kiểm chứng bằng tài liệu chính thức.
- Áp dụng giải pháp chuẩn ngành là `BigDecimal`.
- Thiết kế lại prompt để cải thiện chất lượng đầu ra.
- Tự xây dựng các trường hợp kiểm thử để xác minh kết quả.

Điều này phù hợp với nguyên tắc liêm chính học thuật và vai trò "kiểm duyệt viên" mà người học cần có khi sử dụng AI trong học tập và phát triển phần mềm.
