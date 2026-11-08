## Warm up(Tất cả nội dung mình viết ở đây đều được lấy ở trang [https://toidicode.com] Bạn có thể học hỏi thêm trên đó nhé) 
- Để PHP có thể chạy được thì bắt buộc tên của files phải có phần mở rộng là .php 
- Tất cả các code PHP phải nằm trong Tag: `<?php ?>` hoặc `<?= ?>`
### 1. Comment trong PHP
- Ta dùng `//` cho comment 1 dòng
- Dùng cặp thẻ `/* noi dung */`
- Dấu `.` trong PHP được dùng để nối các chuỗi lại với nhau
### 2. Hiển thị dữ liệu trong PHP
- Ta dùng `echo` để in ra dữ liệu ra màn hình
  ```
  echo "noidung";
  //hoặc
  echo ("noidung");
  //hoặc
  echo 'noi dung';
  ```
### 3. Chương trình Hello World
  ```
  <?= 'Hello world'; ?>
  
  <?php
      echo "hello world!";
  ?>
  // CẢ HAI CÁCH ĐỀU IN RA ĐƯỢC HELLO WORLD
  ```
### 4. Biến trong PHP
- Biến (variable) trong Lập trình có thể hiểu nôm na là các giá trị có thể thay đổi được
- Để khai báo biến trong PHP thì nó cũng có một số nguyên tắc sau:
  - Biến phải được bắt đầu bằng ký tự `$`.
  - Tên biến phải được bắt đầu bằng các chữ cái hoặc dấu `_` không được bắt đầu bằng số, và các ký tự khác ngoài _
- Ví dụ :
    ```
    <?php
    $php = 'hello';
    //đúng
    $_php = 'hello';
    //đúng
    $5php = 'hello';
    //sai vì bắt đầu bằng số;
    $-php = 'hello';
    //sai vì bắt đầu bằng -
    ?>
    ```
- Trong PHP, ta dùng dấu `=` để gán giá trị cho biến. Và bạn cũng có thể dùng `echo` để in ra giá trị của biến
  ```
  <?php

  $toidicode = 'website học lập trình online miễn phí';
  echo $toidicode;
  // out put: website học lập trình online miễn phí
  ?>
  ```
- Ngoài ra, biến cũng có thể thay đổi được
  ```
  <?php 
  $frist = 'hello';
  echo $frist;
  echo "<br/>";
  $frist = 'hello world!';
  echo $frist;
  ?>
  // output : hello<br/>hello world!
  ```
### 5. Hằng 
- Hằng bản chất là một loại biến nhưng không thể thay đổi giá trị được. Tuy rằng xét về bản chất là giống nhau nhưng cách khai báo thì hoàn toàn khác nhau.
- Cú pháp khai báo : `define('tenHang', 'giaTri');`
- Trong đó:
  - define: là cú pháp mặc định để tạo hàm trong PHP.
  - tenHang: là tên của hằng các bạn muốn đặt.
  - giaTri: là giá trị của hằng các bạn vừa đặt tên.
- Ta cũng có thể dùng `echo` để in ra giá trị của hằng
- Ví dụ:
  ```
  <?php

  define('NAME', 'Vu Thanh Tai');
  echo NAME;
  ?>
  ```
### 6. Các kiểu dữ liệu trong PHP
  - 6.1 INT(SỐ NGUYÊN)
    - Để khai báo biến dưới dạng INT thì giá trị của biến không được chứa dấu `'` hoặc `"`
    - Kiểu INT có kích thước 32bit (khi vượt quá thì nó sẽ tự động chuyển sang kiểu khác).
    - Các kiểu INT qua dạng số mà PHP hỗ trợ
      ```
      <?php
      $a = 1234; // hệ số thập phân
      $a = -123; // số âm
      $a = 0123; // Bát phân
      $a = 0x1A; // Hệ thập lục
      $a = 0b11111111; // Hệ nhị phân
      ?>
      ```
  - 6.2 Kiểu số thực
    - Kiểu số thực các bạn có thể hiểu nôm na là số có phần dư,.. như: 5.5 hoặc 8.9.
    - Trong PHP kiểu số thực tồn tại ở 2 dạng là float và double. Cách khai báo cũng tương tự như kiểu INT.
  - 6.3 Kiểu Boolean
    - Là một kiểu dữ liệu mà giá trị của nó chỉ tồn tại 2 giá trị TRUE,FALSE (có thể viết hoa, thường cũng được).
  - 6.4 Kiểu chuỗi
    - Kiểu chuỗi trong PHP tồn tại ở hai dạng là String và Char. Để khai báo chuỗi thì giá trị của chuỗi phải được đặt trong cặp dấu ngoặc `'` hoặc `"`.
      ```
      <?php
      $string = 'toidicode.com';
      //đúng
      $string = "toidicode.com";
      // đúng
      $string = toidicode.com;
      // sai
      ?>
      ```
    - Riêng đối với chuỗi, trong PHP có cung cấp cho chúng ta hàm `is_string()` kiểm tra xem phần tử có phải chuỗi hay không. Hàm này kết quả sẽ trả về TRUE nếu đúng và FALSE nếu sai.
      ```
      <?php
      $a = 'toidicode.com';
      //khai bao bien a
      $b = 95;
      //khai bao bien b
      is_string($a); // true
      is_string($b); // false
      ?>
  - 6.5 Kiểu mảng
      - Kiểu mảng hay còn gọi là array trong PHP là một danh sách các phần tử có cùng, hoặc không cùng kiểu dữ liệu. Nó gồm có 2 loại mảng là **mảng một chiều** và **mảng đa chiều** và trong mỗi loại mảng đó nó lại phân ra thành **mảng tuần tự** và **mảng bất tuần tự**. Và để truy xuất phần tử trong mảng thì chúng ta cần phải dự vào vị trí của nó.
      - Khai báo mảng
        - Để khai báo mảng trong PHP chúng ta có 2 cách khởi tạo:
          ```
          // CÁCH 1
          <?php
          $array = array();
          ?>

          // CÁCH 2 (Đối với PHP>=5.4)
          <?php
          $array = [];
          ?>
          ```
        - Bên cạnh đó các bạn cũng có thể khai báo kèm thêm với giá trị của mảng tương ứng với 2 cách trên.
          ```
          <?php
          $array = array('giá trị 1', 'giá trị 2');
          ?>

          <?php
          $array = ['giá trị 1', 'giá trị 2'];
          ?>
          ```
      - Hiển thị mảng
          - Trong PHP có cung cấp cho chúng ta hàm print_r() để in ra tất cả các phần tử và vị trí của nó trong mảng.
          - VD: Mình sẽ khởi tạo một mảng $ten gồm 4 giá trị là Nguyễn, Phạm, Minh, Chiến và đồng thời cho in ra giá trị của các mảng luôn.
          ```
          <?php
          $ten= array('Nguyễn','Phạm','Minh','Chiến');
          print_r($ten);
          ?>
          ```
          - Và đây là kết quả sau khi chạy đoạn code này
          ```
          Array
          (
              [0] => Nguyễn
              [1] => Phạm
              [2] => Minh
              [3] => Chiến
          )
          ```
          - Nhìn vào kết quả trên các bạn cũng đã thấy được vị trí của mảng sẽ bắt đầu từ 0 cho đến n (chú ý: chỉ áp dụng với mảng tuần tự).
          - Giờ nếu muốn in ra một phần tử thì các bạn sẽ phải dựa vào vị trí của phần tử đó.
          ```
          <?php
          $ten = array('Nguyễn', 'Phạm', 'Minh', 'Chiến');
          // khởi tạo mảng
          echo $ten[0]; //Nguyến
          echo $ten[1]; //Phạm
          echo $ten[2]; // Minh
          echo $ten[3]; // Chiến
          ?>
          ```
      - Thêm phần tử vào mảng
        - Để thêm phần tử vào mảng, ta làm theo cú pháp sau:
          ```
          $TenMang['key'] = 'value';
          ```
        - Trong đó:
          - Tenmang: Là tên của mảng.
          - Key: là key của mảng, nếu không điền thì php sẽ tự thêm vào cuối mảng.
          - Value: là giá trị phần tử. 
      - Sửa phần tử trong mảng
        - Cú pháp:
          ```
          <?php
          $mang['index'] = 'giá trị mới';
          ?>
          ```
        - Trong đó:
          - mang: Là tên của mảng.
          - index: là key của mảng, nếu không điền thì php sẽ tự thêm vào cuối mảng.
          - giá trị mới: là giá trị phần tử.
  - 6.6 Kiểu Null
    - Đây là một kiểu dữ liệu rỗng. Khi khai báo biến kiểu này bộ nhớ sẽ tiếp nhận tên biến mà không tốn thêm bất kỳ một ô nhớ nào.
    - Cú pháp:
      ```
      <?php
      $a = null;
      ?>
      ```
  - 6.7 Ép kiểu
    - Cú pháp:
      ```
      <?php
      $bienMoi = (kieudulieu) $bien;
      ?>
      ```
    - Trong đó :
      - $bienMoi: là biến mới chứa dữ liệu sau khi đã ép.
      - $kieudulieu: là một trong các kiểu dữ liệu mình nêu ở trên.
      - $bien: là biến mà bạn muốn ép kiểu (có thể là dữ liệu sẵn).
    - Ví dụ:
    ```
      <?php
      $a = 9; //khai báo biến a kiểu int
      $b = (string) $a; // ép kiểu sang string
      ?>
    ```
    - Để kiểm tra xem dữ liệu đang ở kiểu nào các bạn có thể dùng hàm `var_dump()`;
### 7. Câu lệnh điều kiện if else trong PHP
  - 7.1 Câu lệnh if
    - Câu lệnh if chứa thông tin điều kiện đúng thì thực hiện nội dung bên trong theo cú pháp:
    ```
    <?php
    if (true) {
        // code
    }
    ?>
    ```
    - Trong đó: True là các toán tử,biểu thức logic,quan hệ hoặc là các giá trị kiểu boolean.
    - Ví dụ : Kiểm tra biến $a nếu lớn hơn 4 thì hiển thị nội dung thông báo.
    ```
    <?php
    $a = 5;
    if ($a > 4) {
        echo $a . 'lớn hơn 4';
    }
    ?>
    ```
  - 7.2 Câu lệnh if-else
    - Phần trên chúng ta mới chỉ dùng lệnh if để kiểm tra nếu đúng thì sao còn chưa bắt được sự kiện nếu sai thì làm gì. Do đó trong PHP hay bất kỳ ngôn ngữ lập trình nào đó đều cung cấp cho chúng ta câu lệnh else để xử lý điều kiện sai, theo cú pháp:
    ```
    <?php
    if (true) {
        //code
    } else {
        //code
    }
    ?>
    ```
    - Ví dụ:
    ```
    <?php
    $tuoi = 19;
    if ($tuoi < 18) {
        echo "bạn chưa đủ 18 tuổi";
    } else {
        echo "bạn đã đủ 18 tuổi rồi";
    }
    // kết quả : bạn đã đủ 18 tuổi rồi
    ?>
    ```
- 7.3 Câu lệnh elseif
    - Đây là câu lệnh kết hợp với if để tạo ra nhiều nhánh có điều kiện xác định khác nhau.
    - Có thể dùng `elseif` hoặc `else if`
    - Cú pháp
    ```
    <?php
    if (true) {
        // code
    } elseif (true) {
        //code
    }
    ?>
    ```
    - Trong đó nếu điều kiện elseif đúng thì chương trình mới chạy phần code bên trong elseif.
- 7.4 Câu lệnh if-else lồng
  - Ví dụ:
  ```
  <?php
  $diem = 5;
  if ($diem <= 10) {
      if ($diem < 4) {
          echo "Học Lại";
      } else if ($diem >= 4 && $diem < 5.5) {
          echo "Loại D";
      } else if ($diem >= 5.5 && $diem < 7) {
          echo "Loại C";
      } else if ($diem >= 7 && $diem < 8.5) {
          echo "Loại B";
      } else if ($diem >= 8.5 && $diem <= 10) {
          echo "Loại A";
      }
  } else {
      echo "Điểm không hợp lệ";
  }
  ?>
  ```
### 8. Vòng lặp for và foreach
  - 8.1 Vòng lặp for
    - Cú pháp:
      ```
      for (bienkhoitao; dieukienthucthi; buocnhay) { 
      // code...
      } 
      ```
    - Trong đó:
      - bienkhoitao: là giá trị khởi tạo ban đầu của vòng lặp.
      - dieukienthucthi: là điều kiện mà vòng lặp được phép chạy (chú ý: Nếu bạn muốn lặp vô tận thì có thể bỏ trống).
      - buocnhay: là khoảng đệm nhảy của mỗi vòng lặp.
    - Xét ví dụ sau:
      ```
      <?php
      for ($i = 0; $i <= 10; $i++) {
          echo 'Tôi đang chạy đến số ' . $i . '<br/>';
      }
      ?>
      ```
    - Ở bài toán trên ta đã cho khởi tạo vòng lặp chạy từ 1 cho đến 10: và cứ mỗi một lần lặp thì in ra dòng chữ : 'tôi đang chạy đến số' + số mà vòng lặp chạy tới.
      ```
      //Output
      Tôi đang chạy đến số 0
      Tôi đang chạy đến số 1
      Tôi đang chạy đến số 2
      Tôi đang chạy đến số 3
      Tôi đang chạy đến số 4
      Tôi đang chạy đến số 5
      Tôi đang chạy đến số 6
      Tôi đang chạy đến số 7
      Tôi đang chạy đến số 8
      Tôi đang chạy đến số 9
      Tôi đang chạy đến số 10
      ```
- 8.2 Vòng lặp foreach
  - Cú pháp
    ```
    <?php
    foreach ($variable as $key => $value) {
        // code...
    }
    ?>
    ```
  - hoặc nếu không muốn lặp key của mảng, object.
    ```
    <?php 
    foreach ($variable as $value) {
        // code...
    }   
    ?>
    ```
  - Trong đó:
    - `$variable`: Là biến mà các bạn muốn lặp (có thể là array, object).
    - `$key`: Là các key của mảng hoặc properties của object. Tức là vị trí của phần tử đó trong arry hoặc object bắt đầu bằng số 0
    - `$value`: Là giá trị của mảng,object. 
- 8.3 For và Foreach lồng
  - Cũng giống như trong câu lệnh rẽ nhánh, vòng lặp cũng hoàn toàn có thể lồng nhau được.
### 9. Vòng lặp While và do While
  - 9.1 Vòng lặp While
    - Vòng lặp while cũng dùng để lặp dữ liệu như các vòng lặp khác nhưng ưu điểm của nó là có thể giải quyết những bài toán không biết chính xác số vòng lặp (for cũng có thể làm đc) và cách sử dụng nó cũng rất đơn giản.
    - Cú pháp :
    ```
    <?php 
    while ($dieukien) {
        // code...
    }
    ?>
    ```
    - Trong đó: `$dieukien` là điều kiện của vòng lặp. Nếu điều kiện trả về true thì vòng lặp sẽ chạy và ngược lại false thì sẽ dừng.
    - Xét ví dụ sau:
    ```
    <?php
    $i = 0; // khởi tạo biến
    while ($i <= 10 /* điều kiện dừng*/) {
        echo $i . "<br>"; // in ra số
        $i++; //sau mỗi lần lặp biến $i tăng thêm 1 đơn vị
    }
    ?>
    ```
    - Output của ví dụ này là:
    ```
    0
    1
    2
    3
    4
    5
    6
    7
    8
    9
    10
    ```
- 9.2 Vòng lặp do-while
  - Đây là một vòng lặp ngược lại với các vòng lặp từ trước đến giờ, các vòng lặp khác kiểm tra điều kiện trước rồi với thực thi câu lệnh, còn vòng lặp do-while thực thi câu lệnh trước rồi mới kiểm tra điều kiện.
  - Cú pháp :
    ```
    <?php
    do {
         // code....
    } while ($dieukien);
    ?>
    ```
  - Trong đó: `$dieukien` là điều kiện của vòng lặp. Nếu điều kiện trả về true thì vòng lặp sẽ chạy và ngược lại false thì sẽ dừng.
  - **Chú ý**: Phải có dấu ; ở phía sau while không chương trình sẽ báo lỗi.
  - VD: in ra các số từ 0 đến 10 bằng vòng lặp do while.
    ```
    <?php
    $i = 0; //khởi tạo biến $i bằng 0
    do {
        echo "$i <br>"; // thực hiện in ra $i hiện tại
        $i++; // cộng thêm 1 đơn vị sau mỗi lần lặp
    } while ($i <= 10/* nếu $i mà lớn hơn 10 dừng vòng lặp*/);
    ?>
    ```
- 9.3 While, do-while lồng nhau.
  - Cũng giống như vòng lặp for và foreach trong while,do-while cũng có thể lồng nhau được.
### 10. Hàm
- 10.1 Cấu trúc của hàm
  - Cú pháp
    ```
    function tenHam($param)
    {
        // code 
    } 
    ```
  - Trong đó:
      - function: là từ khóa bắt buộc để khai báo hàm trong PHP.
      - tenHam: là tên của Hàm các bạn muốn đặt nó cũng bao gồm các ràng buộc như đặt tên biến.
      - $param: là các tham số mà các bạn muốn truyền vào trong hàm(không giới hạn số lượng tham số truyền vào).
  - **Chú ý**: Trong PHP không ràng buộc hàm có giá trị trả về với không có giá trị trả về nên có thể chứa return hoặc không.
  - 10.2 Gọi hàm
    - Cú pháp
      ```
      tenHam();
      //hoặc
      tenHam($param); 
      ```
    - Trong đó:
      - tenHam: là tên của hàm các bạn muốn gọi.
      - $param: là tham số các bạn muốn truyền vào hàm (nếu lúc khai báo hàm có yêu cầu truyền tham số).
  - 10.3 Kiểm tra hàm đã tồn tại
    - Cú pháp
    ```
    function_exists('functionName');
    ```
    - Trong đó: functionName là tên của hàm các bạn kiểm tra và hàm này sẽ trả về giá trị TRUE nếu hàm đã tồn tại và  ngược lại FALSE nếu chưa tồn tại.

