<!DOCTYPE html>
<html lang="zh-Hant">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>鮮到味</title>

<style>
body {
  margin: 0;
  font-family: Arial, sans-serif;
}

/* 三頁滑動 */
.container {
  display: flex;
  width: 300vw;
  transition: 0.5s;
}

.page {
  width: 100vw;
  height: 100vh;
  flex-shrink: 0;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

/* 背景 */
.page1 { background: #f6c90e; }
.page2 { background: #6fcf97; }
.page3 { background: #56ccf2; }

/* 按鈕 */
.btn {
  margin-top: 20px;
  padding: 10px 20px;
  background: #333;
  color: #fff;
  text-decoration: none;
  border-radius: 8px;
}

/* 第三頁按鈕 */
.btn-group {
  margin-top: 20px;
}

.order-btn {
  display: block;
  margin: 10px auto;
  padding: 15px;
  width: 200px;
  border-radius: 10px;
  text-decoration: none;
  color: #fff;
  font-size: 18px;
  background: #ff7a00;
}

.store {
  background: #009944;
}

/* 左右切換 */
.nav {
  position: fixed;
  top: 50%;
  transform: translateY(-50%);
  font-size: 30px;
  cursor: pointer;
}

.left { left: 10px; }
.right { right: 10px; }
</style>
</head>

<body>

<div class="nav left" onclick="move(-1)">‹</div>
<div class="nav right" onclick="move(1)">›</div>

<div class="container" id="slider">

  <!-- 第一頁 -->
  <div class="page page1">
    <div>
      <h1>非基改豆漿</h1>
      <p>高纖低糖・健康安心</p>
      <a href="#" onclick="move(1)" class="btn">下一頁</a>
    </div>
  </div>

  <!-- 第二頁 -->
  <div class="page page2">
    <div>
      <h1>早餐 / 早午晚餐</h1>
      <p>蛋餅｜鐵板麵｜雞腿排</p>
      <a href="#" onclick="move(1)" class="btn">去下單</a>
    </div>
  </div>

  <!-- 第三頁（重點） -->
  <div class="page page3">
    <div>
      <h1>立即下單</h1>

      <div class="btn-group">
        
        <!-- 立即網購 -->
        <a href="https://freshbreakfast.github.io/order-group/" target="_blank" class="order-btn">
          🛒 立即網購
        </a>

        <!-- 門市取貨 -->
        <a href="https://famistore.famiport.com.tw/users/2903801" target="_blank" class="order-btn store">
          🏪 門市取貨
        </a>

      </div>

      <p>全家配送｜門市取貨｜現金付款</p>
    </div>
  </div>

</div>

<script>
let current = 0;

function move(step) {
  current += step;
  if (current < 0) current = 0;
  if (current > 2) current = 2;

  document.getElementById("slider").style.transform =
    "translateX(-" + (current * 100) + "vw)";
}
</script>

</body>
</html>
