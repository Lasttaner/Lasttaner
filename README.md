<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Dijital Saat</title>
  <style>
    #saat {
      font-size: 2em;
      text-align: center;
      margin: 50px;
    }
  </style>
</head>
<body>
  <div id="saat"></div>

  <script>
    function saatGuncelle() {
      var saatDiv = document.getElementById('saat');
      var simdikiZaman = new Date();
      var saat = simdikiZaman.getHours();
      var dakika = simdikiZaman.getMinutes();
      var saniye = simdikiZaman.getSeconds();

      saat = saat < 10 ? '0' + saat : saat;
      dakika = dakika < 10 ? '0' + dakika : dakika;
      saniye = saniye < 10 ? '0' + saniye : saniye;

      var saatMetni = saat + ':' + dakika + ':' + saniye;
      saatDiv.textContent = saatMetni;
    }

    setInterval(saatGuncelle, 1000);
    saatGuncelle(); // Sayfa yüklendiğinde saat güncellenmiş olsun diye
  </script>
</body>
</html>
