# Biến và Kiểu Dữ Liệu trong Python 

## 1. Biến
***Biến*** được dùng để lưu trữ dữ liệu trong chương trình.

Biến có thể chứa các kiểu dữ liệu khác nhau như số nguyên, số thực, chuỗi, danh sách, v.v.

### Các loại biến trong Python:

*- Biến số nguyên (int):* Lưu trữ các số nguyên.

*- Biến số thực (float):* Lưu trữ các số thập phân.

*- Biến chuỗi (str):* Lưu trữ các chuỗi ký tự.

*- Biến danh sách (list):* Lưu trữ một tập hợp các giá trị có thể thay đổi.

*- Biến tuple (tuple):* Lưu trữ một tập hợp các giá trị không thể thay đổi.

*- Biến boolean (bool):* Lưu trữ giá trị đúng (True) hoặc sai (False).

***Ví dụ:***
```
ten = "Nguyen Van A"  # Biến chuỗi
tuoi = 25              # Biến số nguyên
diem_trung_binh = 8.5  # Biến số thực
is_student = True      # Biến boolean
mon_hoc = ["Toan", "Ly", "Hoa"]  # Biến danh sách
thong_tin_sv = ("Nguyen Van A", 25, 8.5)  # Biến tuple
```

### Mutable và Immutable trong Python:

***- Biến mutable (có thể thay đổi):*** Danh sách (list), dictionary (dict), set

***- Biến immutable (không thể thay đổi):*** Số nguyên (int), số thực (float), chuỗi (str), tuple.

### Ép kiểu dữ liệu:
- Sử dụng hàm *int()*, *float()*, *str()* để chuyển đổi giữa các kiểu dữ liệu

***Ví dụ:***
```
    a = "10"
    b = int(a)  # Chuyển chuỗi sang số nguyên
    c = float(a)  # Chuyển chuỗi sang số thực
    d = str(b)  # Chuyển số nguyên sang chuỗi
```

### Type của biến:
- Sử dụng hàm *type()* để kiểm tra kiểu dữ liệu của một biến.

***Ví dụ:***
```
    x = 5
    print(type(x))  # Kết quả: <class 'int'>
    y = "Hello"
    print(type(y))  # Kết quả: <class 'str'>
```

### isInstance:
- Sử dụng hàm *isinstance()* để kiểm tra xem một biến có phải là một kiểu dữ liệu cụ thể hay không.

***Ví dụ:***
```
    z = [1, 2, 3]
    print(isinstance(z, list))  # Kết quả: True
    print(isinstance(z, dict))  # Kết quả: False
```

### id của biến:
- Sử dụng hàm *id()* để lấy địa chỉ bộ nhớ của một biến.

***Ví dụ:***
```
    a = 10
    print(id(a))  # Kết quả: Địa chỉ bộ nhớ của biến a
```

### List và Tuple:
- ***List*** là kiểu dữ liệu mutable, có thể thay đổi nội dung sau khi tạo.

***Ví dụ:***
```
    danh_sach = [1, 2, 3]
    danh_sach.append(4)  # Thêm phần tử vào danh sách
    print(danh_sach)  # Kết quả: [1, 2, 3, 4]
```

**Dùng List khi:**

+ Cần thay đổi, thêm, xóa phần tử trong tập hợp dữ liệu.

+ Cần sắp xếp hoặc lọc dữ liệu.

+ Cần lưu trữ dữ liệu có kích thước thay đổi.

**Phương thức của List:**
+ *append():* Thêm một phần tử vào cuối danh sách.    
```
*Ví dụ:* danh_sach.append(5)
```

+ *insert():* Chèn một phần tử vào vị trí chỉ định trong danh sách.   
```
*Ví dụ:* danh_sach.insert(1, 10) sẽ chèn số 10 vào vị trí index 1
```

+ *extend():* Mở rộng danh sách bằng cách thêm các phần tử từ một iterable khác.  
```
*Ví dụ:* danh_sach.extend([6, 7, 8])
```

+ *remove():* Xóa một phần tử khỏi danh sách.     
```
*Ví dụ:* danh_sach.remove(2) sẽ xóa phần tử có giá trị 2.
```

+ *pop():* Xóa và trả về phần tử ở vị trí chỉ định (mặc định là cuối cùng).   
```
*Ví dụ:* danh_sach.pop() sẽ xóa và trả về phần tử cuối cùng.
```


- ***Tuple*** là kiểu dữ liệu immutable, không thể thay đổi nội dung sau khi tạo.

***Ví dụ:***
```
    bo_tu = (1, 2, 3)
    # bo_tu.append(4)  # Lỗi! Không thể thêm phần tử vào tuple
    print(bo_tu)  # Kết quả: (1, 2, 3)
```


**Dùng Tuple khi:**

+ Dữ liệu không cần thay đổi sau khi tạo.

+ Cần đảm bảo tính toàn vẹn của dữ liệu.

+ Cần sử dụng như khóa trong dictionary (vì khóa phải là immutable).

**Phương thức của Tuple:**

+ *count():* Đếm số lần xuất hiện của một phần tử trong tuple.    
```
Ví dụ: bo_tu.count(2) sẽ trả về 1.
```

+ *index():* Trả về chỉ số của phần tử đầu tiên có giá trị được chỉ định.     
```
Ví dụ: bo_tu.index(3) sẽ trả về 2.
```

### Ưu nhược điểm của List và Tuple:
- ***List:***
  + Ưu điểm: Có thể thay đổi nội dung, linh hoạt trong việc quản lý dữ liệu.
  + Nhược điểm: Tốn nhiều bộ nhớ hơn so với tuple.

- ***Tuple:***
  + Ưu điểm: Tốn ít bộ nhớ hơn, an toàn hơn vì không thể thay đổi nội dung.
  + Nhược điểm: Không thể thay đổi nội dung sau khi tạo.

### Chuyển đổi giữa List và Tuple:
- Sử dụng hàm list() để chuyển từ tuple sang list.
- Sử dụng hàm tuple() để chuyển từ list sang tuple.
***Ví dụ:***
```
    danh_sach = [1, 2, 3]
    bo_tu = tuple(danh_sach)  # Chuyển từ list sang tuple
    print(bo_tu)  # Kết quả: (1, 2, 3)
    bo_tu = (4, 5, 6)
    danh_sach = list(bo_tu)  # Chuyển từ tuple sang list
    print(danh_sach)  # Kết quả: [4, 5, 6]
```

### Set và Dictionary:
- ***Set*** là tập hợp các phần tử duy nhất, không có thứ tự.
Các phần tử trong set phải là kiểu dữ liệu không thể thay đổi (immutable).
- Ví dụ về các kiểu dữ liệu không thể thay đổi: số nguyên (int), số thực (float), chuỗi (string), tuple.
- Ví dụ về các kiểu dữ liệu có thể thay đổi: list, dictionary, set.

**Các thao tác cơ bản với set:**
- **Tạo set:** sử dụng dấu ngoặc nhọn *{}* hoặc hàm *set()*.
***Ví dụ:***
```
    my_set = {1, 2, 3}
    another_set = set([4, 5, 6])
```
- **Thêm phần tử:** sử dụng phương thức *add()*.
***Ví dụ:***
```
    my_set.add(4)
```
- **Hợp nhất set:** sử dụng phương thức *update()* hoặc toán tử *|*.
***Ví dụ:***
```
    my_set.update(another_set) # my_set = { 1, 2, 3, 4, 5, 6 }
    my_set = my_set | another_set # my_set = { 1, 2, 3} | {4, 5, 6} = {1, 2, 3, 4, 5, 6}
```
- **Liên kết của hai set:** sử dụng phương thức *union()* hoặc toán tử *|*.
***Ví dụ:***
```
    union_set = my_set.union(another_set) # my_set = {1, 2, 3} union {4, 5, 6} = {1, 2, 3, 4, 5, 6}
    union_set = my_set | another_set # my_set = {1, 2, 3} | {4, 5, 6} = {1, 2, 3, 4, 5, 6}
```
- **Giao nhau của hai set:** sử dụng phương thức *intersection()* hoặc toán tử *&*.
***Ví dụ:***
```
    intersection_set = my_set.intersection(another_set) # my_set = {1, 2, 3} intersection {3, 4, 5} = {3}
    intersection_set = my_set & another_set # my_set = {1, 2, 3} & {3, 4, 5} = {3}
```
- **Hiệu của hai set:** sử dụng phương thức *difference()* hoặc toán tử *-*.
***Ví dụ:***
```
    difference_set = my_set.difference(another_set) # my_set = {1, 2, 3} difference {3, 4, 5} = {1, 2}
    difference_set = my_set - another_set # my_set = {1, 2, 3} - {3, 4, 5} = {1, 2}
```
- **Xóa phần tử:** sử dụng phương thức *remove()* hoặc *discard()*.
***Ví dụ:***
```
    my_set.remove(2)  # Nếu phần tử không tồn tại, sẽ
    my_set.discard(3)  # Nếu phần tử không tồn tại, không báo lỗi
```
- **Kiểm tra phần tử:** sử dụng toán tử *in*.
***Ví dụ:***
```
    if 1 in my_set:
        print("1 có trong set")
```
**Dùng Set khi nào?**
- Khi bạn cần lưu trữ các phần tử duy nhất, không trùng lặp.
***Ví dụ:***
```
    # Danh sách học sinh trong một lớp, các từ khóa trong một tài liệu.
    class_students = {"An", "Bình", "Chi", "An"}  # "An" chỉ xuất hiện một lần
```    
- Khi bạn cần thực hiện các phép toán tập hợp như hợp nhất, giao nhau, hiệu.
***Ví dụ:*** 
```
    # Tìm các phần tử chung giữa hai danh sách, tìm các phần tử khác nhau giữa hai tập hợp.
    list_a = {1, 2, 3, 4}
    list_b = {3, 4, 5, 6}
    common_elements = list_a & list_b  # Kết quả: {3, 4}
```
- Khi bạn cần kiểm tra sự tồn tại của một phần tử một cách nhanh chóng.
***Ví dụ:***
```
    # Kiểm tra xem một từ có trong từ điển hay không.
    my_set = {"apple", "banana", "cherry"}
    if "banana" in my_set:
        print("Từ 'banana' có trong từ điển")
```
- Khi bạn không quan tâm đến thứ tự của các phần tử.
***Ví dụ:*** 
```
    # Lưu trữ các thẻ (tags) cho một bài viết, nơi thứ tự không quan trọng.
    tags = {"python", "programming", "tutorial"}
    post_tags = tags  # Thứ tự không quan trọng
    print(post_tags)
```
- Khi bạn cần tối ưu hóa bộ nhớ cho các tập hợp lớn.
***Ví dụ:*** 
```
    # Lưu trữ các ID người dùng duy nhất trong một hệ thống lớn.
    list_user_ids = {1001, 1002, 1003, 1001, 1002}  # Chỉ lưu trữ các ID duy nhất
```
- Khi bạn cần loại bỏ các phần tử trùng lặp từ một danh sách.
***Ví dụ:*** 
```
    # Lọc các địa chỉ email trùng lặp từ một danh sách gửi thư.
    email_list = ["user1@gmail.com", "user2@gmai.com", "...."]
    unique_emails = set(email_list)  # Loại bỏ các email trùng lặp
```


- ***Dictionary*** là tập hợp các cặp khóa-giá trị, cho phép truy cập nhanh theo khóa.
- Mỗi khóa trong dictionary phải là duy nhất và không thể thay đổi (immutable), 
trong khi giá trị có thể là bất kỳ kiểu dữ liệu nào và có thể thay đổi (mutable).
- ***Ví dụ*** về các kiểu dữ liệu không thể thay đổi: số nguyên (int), số thực (float), chuỗi (string), tuple.
- ***Ví dụ*** về các kiểu dữ liệu có thể thay đổi: list, dictionary, set.
### Các thao tác cơ bản với dictionary:
- **Tạo dictionary:** sử dụng dấu ngoặc nhọn *{}* hoặc hàm *dict()*.
***Ví dụ:***
```
    my_dict = {'a': 1, 'b': 2, 'c': 3}
    another_dict = dict(d=4, e=5, f=6)
```
- **Thêm hoặc cập nhật phần tử:** sử dụng cú pháp *my_dict[key] = value*.
***Ví dụ:***
```
    my_dict['d'] = 4  # Thêm phần tử mới
    my_dict['a'] = 10 # Cập nhật giá trị của khóa 'a'
```
- **Xóa phần tử:** sử dụng phương thức *del()* hoặc *pop()*.
***Ví dụ:***
```
    del my_dict['b']        # Xóa phần tử với khóa 'b'
    value = my_dict.pop('c') # Xóa và trả về giá trị của khóa 'c'
```
- **Truy cập phần tử:** sử dụng cú pháp *my_dict[key]* hoặc phương thức *get()*.
***Ví dụ:***
```
    value = my_dict['a']        # Truy cập giá trị của khóa 'a'
    value = my_dict.get('b', 0) # Truy cập giá trị của khóa 'b', trả về 0 nếu không tồn tại
```
- **Lặp qua dictionary:** sử dụng vòng lặp *for* để lặp qua các khóa, giá trị hoặc cặp khóa-giá trị.
***Ví dụ:***
```
    for key in my_dict:
        print(key, my_dict[key])

    for key, value in my_dict.items():
        print(key, value)
```
- **Kiểm tra khóa:** sử dụng toán tử *in*.
***Ví dụ:***
```
    if 'a' in my_dict:
        print("Khóa 'a' tồn tại trong dictionary")
```
- **Lấy tất cả các khóa hoặc giá trị:** sử dụng phương thức *keys()* hoặc *values()*.
***Ví dụ:***
```
    keys = my_dict.keys()     # Lấy tất cả các khóa
    values = my_dict.values() # Lấy tất cả các giá trị
```
- **Lấy tất cả các cặp khóa-giá trị:** sử dụng phương thức *items()*.
***Ví dụ:***
```
    items = my_dict.items()   # Lấy tất cả các cặp khóa-giá trị
```
- **Xóa tất cả các phần tử:** sử dụng phương thức *clear()*.
***Ví dụ:***
```
    my_dict.clear()           # Xóa tất cả các phần tử trong dictionary
```
- **Sao chép dictionary:** sử dụng phương thức *copy()*.
***Ví dụ:***
```
    new_dict = my_dict.copy() # Tạo bản sao của dictionary
```
- **Kích thước của dictionary:** sử dụng hàm *len()*.
***Ví dụ:***
```
    size = len(my_dict)       # Lấy số lượng phần tử trong dictionary
```
- **Hàm tích hợp:** *len()*, *id()*
***Ví dụ:***
```
    length = len("Hello")     # Kích thước của chuỗi "Hello"
    address = id(my_dict)     # Địa chỉ bộ nhớ của dictionary
```
**Dùng dictionary khi nào?**
- Khi bạn cần lưu trữ dữ liệu theo cặp khóa-giá trị để truy cập nhanh.
***Ví dụ:*** lưu trữ thông tin sinh viên với mã số sinh viên làm khóa và tên
sinh viên làm giá trị.
```
    student_info = {
        "SV001": "An",
        "SV002": "Bình",
        "SV003": "Chi"
    }
```
- Khi bạn cần ánh xạ (mapping) giữa các giá trị.
***Ví dụ:*** ánh xạ mã sản phẩm với tên sản phẩm trong một cửa hàng.
```
    product_catalog = {
        "P001": "Laptop",
        "P002": "Smartphone",
        "P003": "Tablet"
    }
```
- Khi bạn cần đếm tần suất xuất hiện của các phần tử.
***Ví dụ:*** đếm số lần xuất hiện của các từ trong một đoạn văn bản.
```
    text = "python is great and python is easy"
    word_count = {}
    for word in text.split():
        if word in word_count:
            word_count[word] += 1
        else:
            word_count[word] = 1
    # Kết quả: {'python': 2, 'is': 2, 'great': 1, 'and': 1, 'easy': 1}
```
- Khi bạn cần lưu trữ cấu hình hoặc thiết lập cho một ứng dụng.
***Ví dụ:*** lưu trữ các thiết lập người dùng trong một ứng dụng.
```
    user_settings = {
        "theme": "dark",
        "notifications": True,
        "language": "en"
    }
    # Truy cập thiết lập
    theme = user_settings["theme"]
    # Cập nhật thiết lập
    user_settings["language"] = "vi"
    # Thêm thiết lập mới
    user_settings["font_size"] = 14
```
- Khi bạn cần nhóm dữ liệu liên quan với nhau.
***Ví dụ:*** lưu trữ thông tin về một cuốn sách với các thuộc tính như tiêu đề,
tác giả và năm xuất bản.
```
    book_info = {
        "title": "Learn Python",
        "author": "John Doe",
        "year": 2021
    }
    # Truy cập thông tin sách
    title = book_info["title"]
    author = book_info["author"]
    year = book_info["year"]
```
- Khi bạn cần thực hiện các phép toán trên các cặp khóa-giá trị.
***Ví dụ:*** hợp nhất hai dictionary, tìm các khóa chung hoặc khác nhau giữa hai dictionary.
```
    dict_a = {"a": 1, "b": 2, "c": 3}
    dict_b = {"b": 3, "c": 4, "d": 5}
    # Hợp nhất hai dictionary
    merged_dict = {**dict_a, **dict_b} # Kết quả: {'a': 1, 'b': 3, 'c': 4, 'd': 5}
    # Tìm các khóa chung
    common_keys = dict_a.keys() & dict_b.keys() # Kết quả: {'b', 'c'}
    # Tìm các khóa khác nhau
    different_keys = dict_a.keys() ^ dict_b.keys() # Kết quả: {'a', 'd'}
```
- Khi bạn cần tối ưu hóa bộ nhớ cho các tập hợp lớn.
***Ví dụ:*** lưu trữ các cấu hình hệ thống hoặc dữ liệu tạm thời trong một ứng dụng lớn.
```
    system_config = {
        "max_users": 1000,
        "timeout": 300,
        "enable_logging": True
    }
    # Truy cập cấu hình hệ thống
    max_users = system_config["max_users"]
    timeout = system_config["timeout"]
    enable_logging = system_config["enable_logging"]
```
- Khi bạn cần loại bỏ các phần tử trùng lặp từ một danh sách dựa trên một thuộc tính cụ thể.
***Ví dụ:*** lọc các sản phẩm trùng lặp dựa trên mã sản phẩm từ
```
    product_list = [
        {"code": "P001", "name": "Laptop"},
        {"code": "P002", "name": "Smartphone"},
        {"code": "P001", "name": "Laptop Pro"},
    ]

    unique_products = {}

    for product in product_list:
        unique_products[product["code"]] = product
    # Kết quả: {
    #   'P001': {'code': 'P001', 'name': 'Laptop Pro'},
    #   'P002': {'code': 'P002', 'name': 'Smartphone'}
    # }
```
- Khi bạn cần lưu trữ dữ liệu có cấu trúc phức tạp.
***Ví dụ:*** lưu trữ thông tin về một người dùng với các thuộc tính như tên,
địa chỉ và số điện thoại.
```
    user_profile = {
        "name": "An",
        "address": {
            "street": "123 Đường A",
            "city": "Hà Nội",
            "zip": "100000"
        },
        "phone_numbers": ["0123456789", "0987654321"]
    }
    # Truy cập thông tin người dùng
    name = user_profile["name"]
    street = user_profile["address"]["street"]
    phone_numbers = user_profile["phone_numbers"]
```
- Khi bạn cần lưu trữ dữ liệu tạm thời trong quá trình xử lý.
***Ví dụ:*** lưu trữ kết quả trung gian trong một thuật toán phức tạp.
```
    temp_results = {}
    for i in range(10):
        temp_results[i] = i * i
    # Kết quả: {0: 0, 1: 1, 2: 4, 3: 9, 4: 16, 5: 25, 6: 36, 7: 49, 8: 64, 9: 81}
```
- Khi bạn cần lưu trữ dữ liệu cấu hình cho các mô-đun hoặc thư viện.
***Ví dụ:*** lưu trữ các thiết lập cấu hình cho một thư viện xử lý ảnh.
```    
    image_processing_config = {
        "resize": (800, 600),
        "format": "JPEG",
        "quality": 85
    }
    # Truy cập cấu hình xử lý ảnh
    resize = image_processing_config["resize"]
    format = image_processing_config["format"]
    quality = image_processing_config["quality"]
```
- Khi bạn cần lưu trữ dữ liệu đa ngôn ngữ cho một ứng dụng.
***Ví dụ:*** lưu trữ các chuỗi dịch cho nhiều ngôn ngữ trong một ứng dụng.
```
    translations = {
        "en": {
            "greeting": "Hello",
            "farewell": "Goodbye"
        },
        "vi": {
            "greeting": "Xin chào",
            "farewell": "Tạm biệt"
        }
    }
    # Truy cập chuỗi dịch
    greeting_en = translations["en"]["greeting"]
    farewell_vi = translations["vi"]["farewell"]
```
- Khi bạn cần lưu trữ dữ liệu cấu hình cho các dịch vụ web.
***Ví dụ:*** lưu trữ các thiết lập cấu hình cho một dịch vụ API.
```
    api_config = {
        "base_url": "https://api.example.com",
        "timeout": 30,
        "headers": {
            "Authorization": "Bearer your_token_here",
            "Content-Type": "application/json"
        }
    }
    # Truy cập cấu hình API
    base_url = api_config["base_url"]
    timeout = api_config["timeout"]
    headers = api_config["headers"]
```
- Khi bạn cần lưu trữ dữ liệu cấu hình cho các ứng dụng web.
***Ví dụ:*** lưu trữ các thiết lập cấu hình cho một ứng dụng web Django.
```
    web_app_config = {
        "DEBUG": True,
        "ALLOWED_HOSTS": ["localhost", ""]
    }
    # Truy cập cấu hình ứng dụng web    
    debug_mode = web_app_config["DEBUG"]
    allowed_hosts = web_app_config["ALLOWED_HOSTS"]
```
**Ưu và nhược điểm của Set và Dictionary:**
- **Ưu điểm:**
    + **Truy cập nhanh:** Cả set và dictionary đều cung cấp thời gian truy cập trung bình O(1) cho các thao tác như thêm, xóa và kiểm tra sự tồn tại của phần tử.
    + **Loại bỏ trùng lặp:** Set tự động loại bỏ các phần tử trùng lặp, giúp duy trì tính duy nhất của dữ liệu.
    + **Linh hoạt:** Dictionary cho phép lưu trữ dữ liệu theo cặp khóa+giá trị, giúp tổ chức dữ liệu một cách hiệu quả.
    + **Hỗ trợ các phép toán tập hợp:** Set hỗ trợ các phép toán như hợp nhất, giao nhau và hiệu, giúp thực hiện các thao tác tập hợp một cách dễ dàng.
    + **Tiết kiệm thời gian:** Sử dụng set và dictionary có thể giúp giảm thời gian phát triển và tối ưu hóa hiệu suất của ứng dụng.
    + **Dễ sử dụng:** Cả set và dictionary đều có cú pháp đơn giản và dễ hiểu, giúp người dùng nhanh chóng làm quen và sử dụng chúng trong mã nguồn.
    + **Tính mở rộng:** Cả set và dictionary có thể mở rộng để lưu trữ một lượng lớn dữ liệu mà không ảnh hưởng đáng kể đến hiệu suất.
    + **Hỗ trợ nhiều kiểu dữ liệu:** Cả set và dictionary có thể lưu trữ các kiểu dữ liệu khác nhau, bao gồm số nguyên, chuỗi, tuple và các đối tượng phức tạp hơn.
    + **Tính năng động:** Cả set và dictionary có thể thay đổi kích thước động, cho phép thêm hoặc xóa phần tử một cách linh hoạt trong quá trình thực thi chương trình.
    + **Hỗ trợ lặp:** Cả set và dictionary hỗ trợ lặp qua các phần tử, giúp dễ dàng xử lý và thao tác với dữ liệu.
    + **Tích hợp tốt với các thư viện Python:** Nhiều thư viện Python phổ biến sử dụng set và dictionary làm cấu trúc dữ liệu chính, giúp tích hợp và sử dụng chúng dễ dàng trong các dự án.
- **Nhược điểm:**
    + **Không có thứ tự:** Set không duy trì thứ tự của các phần tử, điều này có thể gây khó khăn khi thứ tự quan trọng.
    + **Sử dụng bộ nhớ:** Cả set và dictionary có thể sử dụng nhiều bộ nhớ hơn so với các cấu trúc dữ liệu khác như list hoặc tuple do cách chúng lưu trữ dữ liệu.
    + **Khóa không thể thay đổi:** Trong dictionary, các khóa phải là kiểu dữ liệu không thể thay đổi (immutable), điều này giới hạn loại dữ liệu có thể sử dụng làm khóa.
    + **Hiệu suất giảm khi có nhiều va chạm:** Khi nhiều phần tử được ánh xạ đến cùng một vị trí trong bộ nhớ (va chạm), hiệu suất của set và dictionary có thể giảm do cần phải xử lý va chạm.
    + **Không hỗ trợ các phép toán thứ tự:** Cả set và dictionary không hỗ trợ các phép toán dựa trên thứ tự như sắp xếp hoặc truy cập theo chỉ số, điều này có thể hạn chế trong một số trường hợp sử dụng.
    + **Khó khăn trong việc gỡ lỗi:** Do tính chất không có thứ tự và cách lưu trữ dữ liệu, việc gỡ lỗi các vấn đề liên quan đến set và dictionary có thể khó khăn hơn so với các cấu trúc dữ liệu khác.
    + **Không thể sử dụng các kiểu dữ liệu có thể thay đổi làm khóa:** Trong dictionary, chỉ các kiểu dữ liệu không thể thay đổi (immutable) mới có thể được sử dụng làm khóa, điều này giới hạn sự linh hoạt trong việc chọn loại dữ liệu cho khóa.


### Độ phạm vi của biến:
- ***Biến toàn cục (global):*** Có thể được truy cập từ bất kỳ đâu trong chương trình.
- ***Biến cục bộ (local):*** Chỉ có thể được truy cập trong phạm vi của hàm hoặc khối mã nơi nó được định nghĩa.

### Độ dài của kiểu dữ liệu:
- Sử dụng hàm *len()* để xác định độ dài của chuỗi, danh sách, tuple hoặc dictionary.
***Ví dụ:***
```
  chuoi = "Hello"
  print(len(chuoi))  # Kết quả: 5
    danh_sach = [1, 2, 3, 4, 5]
    print(len(danh_sach))  # Kết quả: 5
```

### Địa chỉ bộ nhớ:
- Mỗi biến trong Python đều có một địa chỉ bộ nhớ riêng biệt.
- Sử dụng hàm id() để lấy địa chỉ bộ nhớ của một biến.
***Ví dụ:***
```
  a = 10
  print(id(a))  # Kết quả: Địa chỉ bộ nhớ của biến a
```