<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <title>Solar System</title>
  <style>
    body {
      margin: 0;
      background: radial-gradient(#000, #111);
      overflow: hidden;
      height: 100vh;
    }
    .sun {
      position: absolute;
      top: 50%;
      left: 50%;
      width: 80px;
      height: 80px;
      margin: -40px 0 0 -40px;
      background: radial-gradient(circle, #ffcc00, #ff9900);
      border-radius: 50%;
      box-shadow: 0 0 30px #ff9900;
    }
    .orbit {
      position: absolute;
      top: 50%;
      left: 50%;
      border: 1px dashed rgba(255,255,255,0.1);
      border-radius: 50%;
      transform: translate(-50%, -50%);
    }
    .planet {
      position: absolute;
      top: 50%;
      left: 50%;
      border-radius: 50%;
      transform: translate(-50%, -50%);
    }
    .mercury {
      width: 10px;
      height: 10px;
      background: gray;
      animation: orbit 4s linear infinite;
    }
    .venus {
      width: 14px;
      height: 14px;
      background: #c2b280;
      animation: orbit 7s linear infinite;
    }
    .earth {
      width: 16px;
      height: 16px;
      background: #2e8b57;
      animation: orbit 10s linear infinite;
    }
    .mars {
      width: 12px;
      height: 12px;
      background: #b22222;
      animation: orbit 15s linear infinite;
    }
    @keyframes orbit {
      from { transform: rotate(0deg) translateX(var(--distance)) rotate(0deg); }
      to { transform: rotate(360deg) translateX(var(--distance)) rotate(-360deg); }
    }
  </style>
</head>
<body>
  <div class="sun"></div>
  <div class="orbit" style="width: 100px; height: 100px;">
    <div class="planet mercury" style="--distance: 50px;"></div>
  </div>
  <div class="orbit" style="width: 140px; height: 140px;">
    <div class="planet venus" style="--distance: 70px;"></div>
  </div>
  <div class="orbit" style="width: 180px; height: 180px;">
    <div class="planet earth" style="--distance: 90px;"></div>
  </div>
  <div class="orbit" style="width: 220px; height: 220px;">
    <div class="planet mars" style="--distance: 110px;"></div>
  </div>
</body>
</html>
