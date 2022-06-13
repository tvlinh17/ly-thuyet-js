# Lý thuyết JavaScript

## **Buổi 1**

### **Nhúng mã JavaScript vào trang web**

- External
- Internal
- Inline

### **Hàm cơ bản để tương tác (hiển thị dữ liệu) trên trình duyệt/console**

- `Alert()` để hiển thị 1 bảng cảnh báo với thông điệp là dòng text trong cặp dấu nhánh
- `Confirm()` để hiện thị chọn 1 bảng yes/no trên trình duyệt người dùng
- `Prompt()` để hiện thị 1 bảng input cho người dùng điền thông tin vào
- `Console.log()` để in 1 thông điệp ta tab console

### **Variables (Biến)**

- Biến khai báo với `let` không thể khai báo lại, tuy
  nhiên, giá trị của biến có thể thay đổi
- Biến khai báo với `const` (hằng số) không thể khai
  báo lại, và cũng không thể thay đổi giá trị

**Quy tắc đặt tên biến**

- Tên biến chỉ được chứa `ký tự`, `số` hoặc `ký tự đặc biệt $ và _`
- Tên biến `không được bắt đầu bằng một số`
- Tên biến `có phân biệt chữ hoa, chữ thường`
- Tên biến `không được trùng với từ khóa của JavaScript`

**Quy ước đặt tên biến**

- JavaScript sử dụng phong cách `camelCase` cho tên biến, hoặc hàm
- Với hằng số - `const` - sử dụng `UPPERCASE`

### **Kiểu dữ liệu trong JavaScript**

Kiểm tra kiểu dữ liệu của một biến/giá trị sử dụng typeof

typeof(1); //number

**Number**

- Infinity; Vô cực - chia cho 0
- -Infinity; Âm vô cực
- NaN; Not a Number - đại diện cho 1 phép tính sai

**String**

- `String` - bọc trong cặp dấu '' hoặc "" hoặc ``

  let name = "Linh";

**Boolean**

- `boolean` - logic - có 2 giá trị True or False

  let isHandSome = true;

  let isRich = false;

**Underfined**

- `underfined` - đại diện cho một biến chưa được gán giá trị

  let (x);

**Null**

- `Null` - đại diện cho những biến không tồn tại

**Object**

- `Object` - Tập hợp thông tin (giá trị) - mô tả 1 đối tượng trong thực tế

  let linh = {

  name: "Linh",

  age: 25,

  gender: "male",

  address: {

  no: "Số 38, ngõ 90/1",

  street: "Hoa Bằng",

  district: "Cầu Giấy",

  city: "Hà Nội"

  },

  phone: "0339378536",

  isInRelationship: true

};

console.log(linh);

Dot Notation - Object.property

console.log(linh.age);

**Function**

- `function`

  -Khai báo hàm

  let hello = function (name){

  };

  -Gọi hàm

  name();

## **Buổi 2**

### **Toán tử trong JavaScript được chia thành 5 loại:**

- Arithmetic
- Comparision
- Assignment
- Logical
- Bitwise

Quy tắc thực hiện biểu thức theo thứ tự từ trái qua phải, dựa theo độ ưu tiên toán tử. Các toán tử có độ
ưu tiên khác nhau, quyết định phép tính nào sẽ được thực hiện trước

JavaScript cũng tự động chuyển đổi các kiểu dữ liệu của các toán hạng về kiểu phù hợp khi thực hiện
các biểu thức tính toán hay so sánh

### **Type Conversions**

- **Chuyển đổi các kiểu về kiểu "string"**

  string(23); // "23"

  string(true); // "true"

- **Chuyển đổi các kiểu khác về kiểu `boolean`**

  boolean(12); // true

  - Một số giá trị đặc biệt

    "" , 0, Null, underfined, Nan // false

    Còn lại đều cho ra kết quả True

- **Chuyển đổi các kiểu khác về `number`**

  Number("12"); // 12

  Number(null); // 0

  Number(underfined); // Nan

  Number(true); // 1

  Number(false); // 0

  Number("12ab"); // NaN

  Number(""); // 0

### **Arithmetic Operators**

Đối với kiểu string phép + chuyển đổi kiểu của toán hạng về kiểu string và thực hiện nối chuỗi

Phép nối chuỗi chỉ hoạt động duy nhất với toán tử + , với những toán tử số học khác, mọi kiểu dữ liệu được chuyển về number

**Increment, Decrement (tự tăng/giảm)**

- `a++, a--` thực hiện phép toán trước rồi mới tăng/giảm `a`
- `++a, --a` tăng/giảm `a` trước rồi mới thực hiện phép toán

### **Toán tử so sánh == != > >= < <= === !==**

Kết quả của các phép so sánh luôn luôn là `một giá trị boolean`

**Khác nhau giữa** == != và === !==

- `== , !=` tự động chuyển đổi kiểu của 2 toán hạng về cùng một kiểu và thực hiện so sánh
- `=== , !==` so sánh cả kiểu giá trị của dữ liệu

**So sánh chuỗi**

JavaScript sử dụng bảng mã Unicode, khi so sánh 2 chuỗi, nó thực hiện so sánh từng ký tự dựa theo
thứ tự trong bảng mã (Unicode table)

**null, undefined, NaN**

null == 0; //false

null <= 0; // true

null == underfined //true

null === underfined //false

Mọi biểu thức so sánh với `NaN` đều cho kết quả `false`

### **Toán tử logic**

- `|| - or` tìm giá trị đúng đầu tiên trong biểu thức và trả về giá trị đó, nếu không có thì trả về giá trị cuối
  cùng trong biểu thức
- `&& - and` tìm giá trị sai đầu tiên trong biểu thức và trả về giá trị đó, nếu không có thì trả về giá trị cuối
  cùng trong biểu thức
- `! - not` chuyển giá trị về kiểu boolean và phủ định nó
