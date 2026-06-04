<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Avhijeet Loading...</title>
    <style>
        body { background-color: #000; color: #fff; text-align: center; font-family: 'Arial', sans-serif; display: flex; flex-direction: column; justify-content: center; height: 100vh; margin: 0; }
        .logo { font-size: 3rem; font-weight: bold; color: #ff0000; margin-bottom: 20px; }
        .progress-bar { width: 80%; height: 20px; background: #333; margin: 20px auto; border-radius: 10px; overflow: hidden; }
        .progress { width: 0%; height: 100%; background: #ff0000; transition: width 3s linear; }
        .text { font-size: 1.5rem; margin-top: 10px; }
    </style>
</head>
<body>
    <div class="logo">AVHIJEET IS BACK</div>
    <div class="progress-bar"><div class="progress" id="bar"></div></div>
    <div class="text" id="status">Loading 0%...</div>
    <script>
        let width = 0;
        let interval = setInterval(() => {
            if (width >= 95) {
                clearInterval(interval);
                document.getElementById('status').innerText = "95% ACCURACY - Ready!";
                setTimeout(() => { window.location.href = "YOUR_TELEGRAM_LINK_HERE"; }, 1000);
            } else {
                width++;
                document.getElementById('bar').style.width = width + '%';
                document.getElementById('status').innerText = "Loading " + width + "%...";
            }
        }, 50);
    </script>
</body>
</html>
