TODO: CÁC CÁCH ĐỂ THÊM JS VÀO TRONG MỘT TRANG WEB

# 1: Inline Script

- tức là viết JS ngay bên trong thuộc tính của một tag html

 <!DOCTYPE html>
<html>
  <head>
    <title>30DaysOfScript:Inline Script</title>
  </head>
  <body>
    <button onclick="alert('Welcome to 30DaysOfJavaScript!')">Click Me</button>
  </body>
</html>

# 2: Internal Script

- tức là mã JS sẽ được viết ở bên trong tag `head` hoặc `body` của mã HTML thông qua tag <script>
  <!DOCTYPE html>
  <html>
    <head>
      <title>30DaysOfScript:Internal Script</title>
      <script>
        console.log('Welcome to 30DaysOfJavaScript')
      </script>
    </head>
    <body></body>
  </html>

# 3: External Script

- tức là mã JS sẽ được viết ở một file riêng biệt và được nhúng vào thông qua tag <script> để sử dụng
- có thể sử dụng <script> ở trong tag `head` hoặc `body`

ví dụ như:

<!DOCTYPE html>
<html>
  <head>
    <title>30DaysOfScript:Internal Script</title>
    <script>
      console.log('Welcome to 30DaysOfJavaScript')
    </script>
  </head>
  <body></body>
</html>

hoặc

 <!DOCTYPE html>
<html>
  <head>
    <title>30DaysOfJavaScript:External script</title>
  </head>
  <body>
    //it could be in the header or in the body // Here is the recommended place
    to put the external script
    <script src="introduction.js"></script>
  </body>
</html>

# 4:Multiple External Scripts

- chúng ta có thể nhúng nhiều file JS thông qua tag <script>

<!DOCTYPE html>
<html>
  <head>
    <title>Multiple External Scripts</title>
  </head>
  <body>
    <script src="./helloworld.js"></script>
    <script src="./introduction.js"></script>
  </body>
</html>

FIXME: LƯU Ý RẰNG, FILE main luôn luôn phải được đặt sau các file khác
