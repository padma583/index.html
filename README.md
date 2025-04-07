<!DOCTYPE html>
<html>
<head>
  <title>Digital Clock</title>
  <style>
    .clock {
  font-size: 4em;
  text-align: center;
  padding-top: 20px;
}

#time {
  font-weight: bold;
}
  </style>
</head>
<body>
  <div class="clock">
    <div id="time">00:00:00</div>
  </div>
  <script>
    function updateTime() {
  const now = new Date();
  let hours = now.getHours();
  let minutes = now.getMinutes();
  let seconds = now.getSeconds();

  // Add leading zeros if needed
  hours = hours < 10 ? "0" + hours : hours;
  minutes = minutes < 10 ? "0" + minutes : minutes;
  seconds = seconds < 10 ? "0" + seconds : seconds;

  const timeString = `${hours}:${minutes}:${seconds}`;
  document.getElementById("time").textContent = timeString;
}

// Update the time every second
setInterval(updateTime, 1000);
  </script>
</body>
</html>
