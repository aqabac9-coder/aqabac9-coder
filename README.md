<p align="center">
  <img src="https://copilot.microsoft.com/th/id/BCO.8450ccf7-b6ff-4b4f-a7c9-9e79e3dbc6a6.png" alt="AMER Character" width="300"/>
</p>

<h1 align="center">👋 Hello, I'm AMER</h1>

<p align="center">
  A systems developer specialized in:<br>
  Operating systems · Web applications · Android mobile apps
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Python-blue?style=for-the-badge&logo=python&logoColor=white"/>
  <img src="https://img.shields.io/badge/C++-darkblue?style=for-the-badge&logo=c%2B%2B&logoColor=white"/>
  <img src="https://img.shields.io/badge/C%23-purple?style=for-the-badge&logo=csharp&logoColor=white"/>
  <img src="https://img.shields.io/badge/Java-red?style=for-the-badge&logo=java&logoColor=white"/>
</p>

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Jordan Clock</title>
  <style>
    body {
      background-color: black;
      color: white;
      text-align: center;
      font-family: sans-serif;
    }
    .clock {
      position: relative;
      width: 200px;
      height: 200px;
      border: 8px solid white;
      border-radius: 50%;
      margin: 50px auto;
    }
    .hand {
      position: absolute;
      bottom: 50%;
      left: 50%;
      transform-origin: bottom;
      background: white;
    }
    .hour {
      width: 6px;
      height: 50px;
    }
    .minute {
      width: 4px;
      height: 70px;
    }
    .second {
      width: 2px;
      height: 90px;
      background: red;
    }
  </style>
</head>
<body>
  <h1>🕰️ Jordan Local Time</h1>
  <div class="clock">
    <div class="hand hour" id="hour"></div>
    <div class="hand minute" id="minute"></div>
    <div class="hand second" id="second"></div>
  </div>

  <script>
    function updateClock() {
      const now = new Date();
      const jordanTime = new Intl.DateTimeFormat('en-US', {
        timeZone: 'Asia/Amman',
        hour: 'numeric',
        minute: 'numeric',
        second: 'numeric',
        hour12: false
      }).formatToParts(now);

      const h = parseInt(jordanTime.find(p => p.type === 'hour').value);
      const m = parseInt(jordanTime.find(p => p.type === 'minute').value);
      const s = parseInt(jordanTime.find(p => p.type === 'second').value);

      document.getElementById('hour').style.transform = `rotate(${(h % 12) * 30 + m / 2}deg)`;
      document.getElementById('minute').style.transform = `rotate(${m * 6}deg)`;
      document.getElementById('second').style.transform = `rotate(${s * 6}deg)`;
    }

    setInterval(updateClock, 1000);
    updateClock();
  </script>
</body>
</html>
p.type
30
