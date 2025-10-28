<!DOCTYPE html>
<html lang="zh-Hant">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>DM-豆漿三款-直式-印版</title>
  <style>
    html, body {
      margin: 0;
      padding: 0;
      height: 100%;
      width: 100%;
      background-color: #000;
      display: flex;
      justify-content: center;
      align-items: center;
      overflow: hidden;
      touch-action: manipulation; /* 讓點擊更順暢 */
    }
    img {
      max-width: 100%;
      max-height: 100%;
      object-fit: contain;
      display: block;
    }
    .hint {
      position: absolute;
      bottom: 20px;
      color: #fff;
      font-size: 1rem;
      text-align: center;
      opacity: 0.7;
      animation: blink 1.5s infinite;
    }
    @keyframes blink {
      0%, 50%, 100% { opacity: 0.7; }
      25%, 75% { opacity: 0.3; }
    }
  </style>
</head>
<body>
  <img src="DM-豆漿三款-直式-印版.jpg" alt="活動海報">
  <div class="hint">點一下畫面進入全螢幕</div>

  <script>
    function requestFullscreen() {
      const el = document.documentElement;
      if (el.requestFullscreen) el.requestFullscreen();
      else if (el.webkitRequestFullscreen) el.webkitRequestFullscreen();
      else if (el.mozRequestFullScreen) el.mozRequestFullScreen();
      else if (el.msRequestFullscreen) el.msRequestFullscreen();
    }

    // 使用者點擊畫面後觸發全螢幕
    document.body.addEventListener('click', () => {
      requestFullscreen();
      document.querySelector('.hint').style.display = 'none';
    });
  </script>
</body>
</html>
