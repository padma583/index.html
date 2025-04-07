<!DOCTYPE html>
<html lang="en">
  <head>
    <title>Digital Clock</title>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width" />
    <style>
      body {
    background: linear-gradient(45deg, #ff0000, #003cff);
}

.clock {
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translateX(-50%) translateY(-50%);
    color: 
#ffffff;
    font-size: 160px;
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    letter-spacing: 7px;
      </style>
  </head>
  <body>
    <div id="MyClockDisplay" class="clock" onload="showTime()"></div>
    <script>
      
Digital Clock Using HTML, CSS & JavaScript
Author Profile Photo
Jithu Thomas
Aug 20
12.2k
0
2
100
Article
DigitalClock.zip
An article for building a stylish, real-time digital clock using HTML, CSS, and JavaScript.

Step 1. Create a HTML front
Creating an HTML front using the code below.

<!DOCTYPE html>
<html lang="en">
  <head>
    <title>Digital Clock</title>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width" />
    <link rel='stylesheet' href='https://fonts.googleapis.com/css?family=Orbitron'>
    <link rel='stylesheet' href='https://fonts.googleapis.com/css?family=Aldrich'>
    <link rel="stylesheet" href="style.css" />
  </head>
  <body>
    <div id="MyClockDisplay" class="clock" onload="showTime()"></div>
    <script src="script.js"></script>
  </body>
</html>
Markup
Step 2. Style using css
Make the style using css as follows.

body {
    background: linear-gradient(45deg, #ff0000, #003cff);
}

.clock {
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translateX(-50%) translateY(-50%);
    color: 
#ffffff;
    font-size: 160px;
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    letter-spacing: 7px;
}
CSS
Step 3. BAckendJavaScript Code
The backend code for the JavaScript as follows.

function showTime() {
    let date = new Date();
    let h = date.getHours(); // 0 - 23
    let m = date.getMinutes(); // 0 - 59
    let s = date.getSeconds(); // 0 - 59
    let session = "AM";

    if (h == 0) {
        h = 12;
    }

    if (h > 12) {
        h = h - 12;
        session = "pm";
    }

    h = (h < 10) ? "0" + h : h;
    m = (m < 10) ? "0" + m : m;
    s = (s < 10) ? "0" + s : s;

    var time = h + ":" + m + ":" + s + " " + session;

    document.getElementById("MyClockDisplay").innerText = time;
    document.getElementById("MyClockDisplay").textContent = time;

    setTimeout(showTime, 1000);
}
    </script>
  </body>
</html>
