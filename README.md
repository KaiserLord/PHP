## Warm up(Tất cả nội dung mình viết ở đây đều được lấy ở trang <https://toidicode.com/> Bạn có thể học hỏi thêm trên đó nhé) 
- Để PHP có thể chạy được thì bắt buộc tên của files phải có phần mở rộng là .php 
- Tất cả các code PHP phải nằm trong Tag: `<?php ?>` hoặc `<?= ?>`
### 1. Comment trong PHP
- Ta dùng `//` cho comment 1 dòng
- Dùng cặp thẻ `/* noi dung */`
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
  - 
