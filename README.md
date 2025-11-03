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
<head
\\\
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>AMER's GitHub Profile</title>
  <style>
    body {
      background-color: black;
      color: white;
      font-family: sans-serif;
      text-align: center;
      margin: 0;
      padding: 20px;
    }
    .profile-img {
      width: 250px;
      border-radius: 10px;
    }
    .badges span {
      display: inline-block;
      padding: 8px 16px;
      margin: 5px;
      border-radius: 5px;
      color: white;
      font-weight: bold;
    }
    .cpp { background-color: #00599C; }
    .cs { background-color: #68217A; }
    .java { background-color: #B22222; }
    .python { background-color: #3776AB; }

    .clock {
      position: relative;
      width: 200px;
      height: 200px;
      border: 8px solid white;
      border-radius: 50%;
      margin: 40px auto;
    }
    .hand {
      position: absolute;
      bottom: 50%;
      left: 50%;
      transform-origin: bottom;
      background: white;
    }
    .hour { width: 6px; height: 50px; }
    .minute { width: 4px; height: 70px; }
    .second { width: 2px; height: 90px; background: red; }

    .time-text {
      font-size: 24px;
      margin-top: 10px;
    }
  </style>
</head>
<body>

  <h1>👋 Hello, I'm AMER</h1>
  <img src="YOUR_IMAGE_URL_HERE" alt="Anime Character" class="profile-img">

  <p>A systems developer specialized in:<br>
     Operating systems · Web applications · Android mobile apps</p>

  <div class="badges">
    <span class="cpp">C++</span>
    <span class="cs">C#</span>
    <span class="java">Java</span>
    <span class="python">Python</span>
  </div>

  <div class="clock">
    <div class="hand hour" id="hour"></div>
    <div class="hand minute" id="minute"></div>
    <div class="hand second" id="second"></div>
  </div>
  <div class="time-text" id="timeText"></div>

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

      document.getElementById('timeText').textContent = `${String(h).padStart(2, '0')}:${String(m).padStart(2, '0')}:${String(s).padStart(2, '0')} (Jordan Time)`;
    }

    setInterval(updateClock, 1000);
    updateClock();
  </script>

</body>
</html>
p.type
30
