TODO:

# SO SÁNH SỰ KHÁC NHAU GIỮA `var, let, const`

# giống nhau: cả 3 từ khóa đều được sử dụng để khai báo biến trong JS

# Khác nhau:

1. var

- scope (phạm vi) : `function-level-scope` (phạm vi hàm): điều này có nghĩa là
  biến được khai báo trong một hàm chỉ có thể truy cập bên trong hàm đó, nếu biến được khai báo ngoài hàm thì nó sẽ có phạm ` toàn cục (global scope)`
  --> điều này dẫn đến vấn đề trùng lặp tên biến và khó kiểm soát

2. let

- scope : `block-level-scope`: điều này có nghĩa là biến chỉ có thể truy cập được trong phạm vi khối mã mà nó được khai báo
- chẳng hạn như một ngoặc nhọn `{}` hoặc một vòng lặp `for`
- không thể khai báo lại trong một phạm vi, trong một phạm vi nó chỉ có thể cập nhật lại giá trị cho biến

3. const

- tương tự như `let`, `const` cũng có phạm vi là `block-level-scoped`
- Tuy nhiên, khác với "let", biến được khai báo bằng "const" là hằng số và không thể thay đổi giá trị sau khi được gán. Việc sử dụng "const" giúp đảm bảo tính nguyên vẹn của dữ liệu.

# hoisting

- Hoisting là một tính năng trong JavaScript cho phép các khai báo biến và hàm được di chuyển lên đầu phạm vi của nó trước khi mã được thực thi. Tức là, bất kỳ khai báo biến hoặc hàm nào trong phạm vi sẽ được xử lý trước khi trình thông dịch thực hiện bất kỳ câu lệnh nào trong phạm vi đó.

Từ khóa "var", "let" và "const" là các từ khóa để khai báo biến trong JavaScript. Tuy nhiên, chúng có những điểm khác nhau quan trọng:

"var": Đây là cách khai báo biến trong JavaScript trước khi "let" và "const" xuất hiện. Tính năng hoisting đã được áp dụng cho từ khóa này. Biến được khai báo bằng "var" sẽ được tự động gán giá trị "undefined" nếu không có giá trị được chỉ định.

"let": Đây là từ khóa để khai báo biến với phạm vi (scope) chỉ nằm trong block code nơi nó được khai báo. Khác với "var", biến được khai báo bằng "let" sẽ không được tự động gán giá trị "undefined".

"const": Tương tự như "let", "const" cũng được sử dụng để khai báo biến với phạm vi chỉ nằm trong block code. Tuy nhiên, biến được khai báo bằng "const" không thể thay đổi giá trị sau khi đã gán, nó có tính chất không thay đổi (immutable).

#

<script>
    console.log(a);
    var a;
    a = 10;
    console.log(a);
<script>
--> ở trong ví dụ này, `var a` sẽ được đưa lên đầu và set bằng undefined
- console.log(a) sẽ được thực hiện, in ra undefined 
- gán lại bằng 10
- console.log(a) ra 10

<script>
    console.log(a);
    let a;
    a = 10;
    console.log(a);
<script>
- thử lại đối với let thì lỗi, lý do nó được đưa lên nhưng không được gán giá trị 
undefined, và nó báo không thể sử dụng biến trước khi bai báo
 ReferenceError: Cannot access 'a' before initialization
 at main.js:1:13
