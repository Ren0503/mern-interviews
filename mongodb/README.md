# Câu hỏi phỏng vấn MongoDB

![](./assets/mongodb.jpg)

MongoDB là cơ sở dữ liệu hướng tài liệu vào năm 2007. Nó hoạt động dựa trên khái niệm collection và document. Một MongoDB Server có thể bao gồm nhiều cơ sở dữ liệu và hoạt động hiệu suất cao với bộ dự phòng và khả năng mở rộng dễ dàng. Collection trong MongoDB có thể xem là một nhóm document bới các trường khác khác nhau. Một document là một tập hợp key-value có lược đồ động, các trường chung có thể có kiểu dữ liệu khác nhau và các document trong cùng một collection không cần phải có cấu trúc giống nhau. Nếu bạn mới bắt đầu với MongoDB và đã làm việc với SQL trước đây, hãy xem bảng tương ứng của cả hai công nghệ như sau:

| RDBMS | MongoDB |
|-------|---------|
| Table | Collection |
| Row | Document |
| Column | Field |
| Table Join | Embedded documents |

## 1. Mongo Shell là gì?

Mongo shell là một JavaScript interface có thể dùng cho truy vấn và cập nhật dữ liệu. Nó cũng có thể dùng cho các thao tác của quản trị viên.

## 2. MongoDB lưu dữ liệu thế nào?

Là hướng tài liệu(document-based), MongoDB lưu trữ document dưới dạng BSON (Binary JavaScript Object Notation) là định dạng được mã hóa nhị phân của JSON.

## 3. MongoDB là loại cơ sở dữ liệu NoSQL nào?

Cơ sở dữ liệu document bao gồm các document như cặp key-value, cặp key-array và document lồng nhau.

## 4. Các tính năng quan trọng của MongoDB?

- Cơ sở dữ liệu có lược đồ động.
- Truy cập dữ liệu nhanh
- Tính năng như sharding, aggregation và replication giúp sử dụng dễ dàng.
- Đa nền tảng và hướng tài liệu.
- Tự động fall-over và độ khả dụng cao.

## 5. Mô hình dữ liệu trong MongoDB?

Trong MongoDB có hai cách để thực hiện liên kết các dữ liệu là:
- Sử dụng document con nằm trong một document khác (Embedded data model).
- Sử dụng tham chiếu từ document này sang document khác (Normalized data model).

## 6. MongoDB được gọi là schema-less có đúng không?

Khá phù hợp để nói MongoDB là lược đồ động vì nó dựa trên JSON có cấu trúc dữ liệu schema-free. Để tạo schema.

## 7. Namespace trong MongoDB?

Namespace là sự ghép nối của tên cơ sở dữ liệu và tên collection. Ví dụ - students.the subject, trong đố students là cơ sở dữ liệu và subject là collection.

## 8. Thưc hiện CRUD trong MongoDB như thế nào?

. C - Create - `db.collection.insert()`.

. R - Read - `db.collection.find()`.

. U - Update - `db.collection.update()`.

. D - Delete - `db.collection.remove()`.

## 9. Sự khác biệt giữa MySQL và MongoDB?

| MySQL | MonngoDB |
|-------|----------|
| Viết bằng C/C++ | Viết bằng C++ và JavaScript |
| Theo cấu trúc RDBMS | Cấu trúc hướng tài liệu |
| Cấu trúc dữ liệu được xác định chặt chẽ, lược đồ nghiêm ngặt và cần được xác định ngay từ đầu | Tạo lược đồ động và linh hoạt cho các dữ liệu phức tạp |
| Mở rộng theo chiều dọc | Mở rộng theo chiều ngang |
| Sử dụng SQL | Ngôn ngữ truy vấn phi cấu trúc |
| Sử dụng JOIN để liên kết dữ liệu từ nhiều bảng | Không hỗ trợ JOIN |
| Hiệu suất thấp với cơ sở dữ liệu lơn và dữ liệu phi cấu trúc | Xử lý hiệu quả dữ liệu phi cấu trúc với hiệu suất tốt |
| Không phù hợp với nền tảng đám mấy | Lựa chọn tốt cho các dịch vụ đám mây |

## 10. Ràng buộc trong MongoDB?

Bạn có thể thêm trình xác nhận dữ liệu hợp lệ cho MongoDB từ v3.2. Các chỉ mục cũng có thể tạo bằng cách:

```js
db.collection.createIndex({ "key" : 1 })
```

## 11. ObjectId là gì? Nó được cấu trúc như thế nào?

ObjectId là lớp khoá chính mặc định cho document trong MongoDB. Nó được tìm trong trường `_id` của document đã chèn. Đây là kiểu BSON 12 byte được tạo bằng thuật toán mặc định. Cấu trúc là:
- 4 byte đầu tiên biểu diễn số giây từ UNIX Epoch.
- 3 byte tiếp theo là id của máy.
- 2 byte kế tiếp là process id.
- Và 3 byte cuối cùng là một giá trị đếm ngẫu nhiên.

## 12. BSON là gì?

BSON , ᴠiết tắt của Binarу JSON, là một tuần tự được mã hóa nhị phân của các tài liệu giống như JSON.

## 13. Đánh chỉ mục trong MongoDB?

Sử dụng phương thức `ensureIndex()`:

```js
db.COLLECTION_NAME.ensureIndex()
```

## 14. Chỉ mục mặc định khi tạo collection là gì?

Chỉ mục mặc định được tạo cho collection mới là `_id`

## 15. Sharding là gì trong MongoDB?

MongoDB đáp ứng sự tăng trưởng dữ liệu bằng cách sử dụng Sharding, có nghĩa là sắp xếp các bản ghi dữ liệu trên nhiều máy khác nhau. Mỗi shard là một tập bản sao.