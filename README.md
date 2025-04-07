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
    function showTime() {
    let date = new Date();
    let h = date.getHours(); // 0 - 23
    let m = date.getMinutes(); // 0 - 59
    let s = date.getSeconds(); // 0 - 59
    let session = "AM";

    
  
}
    </script>
  </body>
</html>
