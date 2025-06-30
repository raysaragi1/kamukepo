<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8">
  <title>Aku Sayang Kamu, Aya 💖</title>
  <style>
    body {
      background: linear-gradient(to bottom right, pink, lightblue);
      font-family: 'Courier New', monospace;
      text-align: center;
      padding-top: 100px;
      color: #fff;
      overflow-x: hidden;
    }

    h1 {
      font-size: 3em;
      animation: fadeIn 3s ease-in-out;
    }

    p {
      font-size: 1.5em;
      margin: 20px;
    }

    button {
      font-size: 1.3em;
      padding: 10px 25px;
      margin: 10px;
      border: none;
      border-radius: 10px;
      color: white;
      cursor: pointer;
      animation: pulse 2s infinite;
    }

    .yes {
      background-color: #28a745;
    }

    .no {
      background-color: #dc3545;
    }

    @keyframes fadeIn {
      from { opacity: 0; transform: scale(0.9); }
      to { opacity: 1; transform: scale(1); }
    }

    @keyframes pulse {
      0% { transform: scale(1); }
      50% { transform: scale(1.1); }
      100% { transform: scale(1); }
    }

    .heart {
      font-size: 5em;
      color: red;
      animation: pulse 1.5s infinite;
    }

    .message {
      font-size: 1.8em;
      margin-top: 30px;
    }

    .snowflake {
      position: fixed;
      top: -10px;
      z-index: 9999;
      user-select: none;
      color: white;
      font-size: 1.5em;
      animation: fall linear infinite;
    }

    @keyframes fall {
      0% { transform: translateY(0); }
      100% { transform: translateY(100vh); }
    }
  </style>
</head>
<body>

  <div class="heart">❤️</div>
  <h1>Hai Aya...</h1>
  <p>Aku punya sesuatu yang mau aku bilang dari hati yang terdalam...</p>
  <p>Setelah waktu yang kita lewati bersama...</p>
  <h1>✨ Mau gak kamu jadi pacarku? ✨</h1>

  <!-- Tombol pilihan -->
  <button class="yes" onclick="jawaban('ya')">💖 Aku Mau</button>
  <button class="no" onclick="jawaban('tidak')">💔 Maaf ya</button>

  <!-- Tempat muncul jawaban -->
  <div class="message" id="hasilJawaban"></div>

  <!-- Embed YouTube Musik Romantis (Off My Face - Justin Bieber) -->
  <iframe width="0" height="0" 
    src="https://www.youtube.com/watch?v=p7CMx_N0Wbw&list=RDp7CMx_N0Wbw&start_radio=1&ab_channel=MAXIMA" 
    frameborder="0" allow="autoplay"></iframe>

  <!-- Efek salju cinta -->
  <script>
    function createSnowflake() {
      const snowflake = document.createElement("div");
      snowflake.classList.add("snowflake");
      snowflake.style.left = Math.random() * window.innerWidth + "px";
      snowflake.style.animationDuration = 5 + Math.random() * 5 + "s";
      snowflake.innerHTML = "❄️";
      document.body.appendChild(snowflake);
      setTimeout(() => {
        snowflake.remove();
      }, 10000);
    }

    setInterval(createSnowflake, 300);

    function jawaban(pilihan) {
      const hasil = document.getElementById('hasilJawaban');
      if (pilihan === 'ya') {
        hasil.innerHTML = "💖 YES! Aku bahagia banget! Terima kasih Aya, kamu udah bikin hariku sempurna! 💑";
      } else {
        hasil.innerHTML = "💔 Gak apa-apa Aya... yang penting kamu tahu perasaanku. Aku tetap doain yang terbaik buatmu 🙏";
      }
    }
  </script>

</body>
</html>
