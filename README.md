
<html lang="tr">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>You will explode :3</title>
  <style>
    body {
font-family: 'Roboto', sans-serif;
      text-align: center;
      background-color: hsl(0, 0%, 13%);
      margin-top: 100px;
    }
    h1 {
      font-size: 48px;
      color: hwb(113 6% 14%);
    }
    #countdown {
      font-size: 36px;
      margin-top: 20px;
      color: hsl(273, 94%, 38%);
    }
  </style>
</head>
<body>
  <h1>Bu geri sayım dolana kadar A2 seviyesinde olmanız gerekmektedir.
    Seviyenizi TAÜ A2 sınavı ile bizzat ben ölçeceğim.
  </h1>
  <div id="countdown">Yükleniyor...</div>

  <script>
    const targetDate = new Date("February 25, 2030 12:55:00").getTime();

    const countdownElement = document.getElementById("countdown");

    const updateCountdown = () => {
      const now = new Date().getTime();
      const timeLeft = targetDate - now;

      if (timeLeft < 0) {
        countdownElement.innerHTML = "Etkinlik başladı!";
        return;
      }

      const days = Math.floor(timeLeft / (1000 * 60 * 60 * 24));
      const hours = Math.floor((timeLeft % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
      const minutes = Math.floor((timeLeft % (1000 * 60 * 60)) / (1000 * 60));
      const seconds = Math.floor((timeLeft % (1000 * 60)) / 1000);

      countdownElement.innerHTML = `${days} gün ${hours} saat ${minutes} dakika ${seconds} saniye`;
    };

    updateCountdown();
    setInterval(updateCountdown, 1000);
  </script>
</body>
</html>
