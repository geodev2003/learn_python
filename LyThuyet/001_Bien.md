# Biến và Kiểu Dữ Liệu trong Python 

## 1. Biến
***Biến*** được dùng để lưu trữ dữ liệu trong chương trình.
Biến có thể chứa các kiểu dữ liệu khác nhau như số nguyên, số thực, chuỗi, danh sách, v.v.

**Các loại biến trong Python:**
*- Biến số nguyên (int):* Lưu trữ các số nguyên.
*- Biến số thực (float):* Lưu trữ các số thập phân.
*- Biến chuỗi (str):* Lưu trữ các chuỗi ký tự.
*- Biến danh sách (list):* Lưu trữ một tập hợp các giá trị có thể thay đổi.
*- Biến tuple (tuple):* Lưu trữ một tập hợp các giá trị không thể thay đổi.
*- Biến boolean (bool):* Lưu trữ giá trị đúng (True) hoặc sai (False).

***Ví dụ:***
```ten = "Nguyen Van A"  # Biến chuỗi
tuoi = 25              # Biến số nguyên
diem_trung_binh = 8.5  # Biến số thực
is_student = True      # Biến boolean
mon_hoc = ["Toan", "Ly", "Hoa"]  # Biến danh sách
thong_tin_sv = ("Nguyen Van A", 25, 8.5)  # Biến tuple```

Mutable và Immutable trong Python:
- Biến mutable (có thể thay đổi): Danh sách (list), dictionary (dict), set.
- Biến immutable (không thể thay đổi): Số nguyên (int), số thực (float), chuỗi (str), tuple.

Ép kiểu dữ liệu:
- Sử dụng hàm int(), float(), str() để chuyển đổi giữa các kiểu dữ liệu.
- Ví dụ:
    a = "10"
    b = int(a)  # Chuyển chuỗi sang số nguyên
    c = float(a)  # Chuyển chuỗi sang số thực
    d = str(b)  # Chuyển số nguyên sang chuỗi

Type của biến:
- Sử dụng hàm type() để kiểm tra kiểu dữ liệu của một biến.
- Ví dụ:
    x = 5
    print(type(x))  # Kết quả: <class 'int'>
    y = "Hello"
    print(type(y))  # Kết quả: <class 'str'>

isInstance:
- Sử dụng hàm isinstance() để kiểm tra xem một biến có phải là một kiểu dữ liệu cụ thể hay không.
- Ví dụ: 
    z = [1, 2, 3]
    print(isinstance(z, list))  # Kết quả: True
    print(isinstance(z, dict))  # Kết quả: False

id của biến:
- Sử dụng hàm id() để lấy địa chỉ bộ nhớ của một biến.
- Ví dụ:
    a = 10
    print(id(a))  # Kết quả: Địa chỉ bộ nhớ của biến a

# List và Tuple:
- List là kiểu dữ liệu mutable, có thể thay đổi nội dung sau khi tạo.
Ví dụ:
    danh_sach = [1, 2, 3]
    danh_sach.append(4)  # Thêm phần tử vào danh sách
    print(danh_sach)  # Kết quả: [1, 2, 3, 4]

Dùng List khi:
- Cần thay đổi, thêm, xóa phần tử trong tập hợp dữ liệu.
- Cần sắp xếp hoặc lọc dữ liệu.
- Cần lưu trữ dữ liệu có kích thước thay đổi.

Phương thức của List:
- append(): Thêm một phần tử vào cuối danh sách.    Ví dụ: danh_sach.append(5)
- insert(): Chèn một phần tử vào vị trí chỉ định trong danh sách.   Ví dụ: danh_sach.insert(1, 10) sẽ chèn số 10 vào vị trí index 1.
- extend(): Mở rộng danh sách bằng cách thêm các phần tử từ một iterable khác.  Ví dụ: danh_sach.extend([6, 7, 8])
- remove(): Xóa một phần tử khỏi danh sách.     Ví dụ: danh_sach.remove(2) sẽ xóa phần tử có giá trị 2.
- pop(): Xóa và trả về phần tử ở vị trí chỉ định (mặc định là cuối cùng).   Ví dụ: danh_sach.pop() sẽ xóa và trả về phần tử cuối cùng.


- Tuple là kiểu dữ liệu immutable, không thể thay đổi nội dung sau khi tạo.
Ví dụ:
    bo_tu = (1, 2, 3)
    # bo_tu.append(4)  # Lỗi! Không thể thêm phần tử vào tuple
    print(bo_tu)  # Kết quả: (1, 2, 3)

Dùng Tuple khi:
- Dữ liệu không cần thay đổi sau khi tạo.
- Cần đảm bảo tính toàn vẹn của dữ liệu.
- Cần sử dụng như khóa trong dictionary (vì khóa phải là immutable).

Phương thức của Tuple:
- count(): Đếm số lần xuất hiện của một phần tử trong tuple.    Ví dụ: bo_tu.count(2) sẽ trả về 1.
- index(): Trả về chỉ số của phần tử đầu tiên có giá trị được chỉ định.     Ví dụ: bo_tu.index(3) sẽ trả về 2.

Ưu nhược điểm của List và Tuple:
- List:
  + Ưu điểm: Có thể thay đổi nội dung, linh hoạt trong việc quản lý dữ liệu.
  + Nhược điểm: Tốn nhiều bộ nhớ hơn so với tuple.

- Tuple:
  + Ưu điểm: Tốn ít bộ nhớ hơn, an toàn hơn vì không thể thay đổi nội dung.
  + Nhược điểm: Không thể thay đổi nội dung sau khi tạo.

Chuyển dổi giữa List và Tuple:
- Sử dụng hàm list() để chuyển từ tuple sang list.
- Sử dụng hàm tuple() để chuyển từ list sang tuple.
Ví dụ:
    danh_sach = [1, 2, 3]
    bo_tu = tuple(danh_sach)  # Chuyển từ list sang tuple
    print(bo_tu)  # Kết quả: (1, 2, 3)
    bo_tu = (4, 5, 6)
    danh_sach = list(bo_tu)  # Chuyển từ tuple sang list
    print(danh_sach)  # Kết quả: [4, 5, 6]


Set và Dictionary:
- Set là tập hợp các phần tử duy nhất, không có thứ tự.
- Dictionary là tập hợp các cặp khóa-giá trị, cho phép truy cập nhanh theo khóa.

Độ phạm vi của biến:
- Biến toàn cục (global): Có thể được truy cập từ bất kỳ đâu trong chương trình.
- Biến cục bộ (local): Chỉ có thể được truy cập trong phạm vi của hàm hoặc khối mã nơi nó được định nghĩa.

Độ dài của kiểu dữ liệu:
- Sử dụng hàm len() để xác định độ dài của chuỗi, danh sách, tuple hoặc dictionary.
- Ví dụ:
  chuoi = "Hello"
  print(len(chuoi))  # Kết quả: 5
    danh_sach = [1, 2, 3, 4, 5]
    print(len(danh_sach))  # Kết quả: 5

Địa chỉ bộ nhớ:
- Mỗi biến trong Python đều có một địa chỉ bộ nhớ riêng biệt.
- Sử dụng hàm id() để lấy địa chỉ bộ nhớ của một biến.
- Ví dụ:
  a = 10
  print(id(a))  # Kết quả: Địa chỉ bộ nhớ của biến a
