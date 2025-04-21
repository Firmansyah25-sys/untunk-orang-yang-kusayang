<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Untuk Kamu, Sayang 💖</title>
  <style>
    body {
      margin: 0;
      padding: 0;
      font-family: 'Comic Sans MS', cursive;
      background: #ffe6f0;
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
      flex-direction: column;
      overflow: hidden;
    }
    h1 {
      color: #d63384;
      text-align: center;
    }
    .btn {
      padding: 10px 20px;
      margin: 10px;
      background-color: #ff99cc;
      border: none;
      border-radius: 20px;
      color: white;
      font-size: 18px;
      cursor: pointer;
      transition: 0.3s;
    }
    .btn:hover {
      background-color: #ff66b2;
    }
    #output {
      margin-top: 20px;
      font-size: 20px;
      color: #d63384;
    }
    .heart {
      position: absolute;
      color: #ff4da6;
      animation: floatUp 2s ease-in-out forwards;
    }
    @keyframes floatUp {
      0% {
        opacity: 1;
        transform: translateY(0);
      }
      100% {
        opacity: 0;
        transform: translateY(-150px);
      }
    }
  </style>
</head>
<body>
  <h1>Hai, Sayang 💖</h1>
  <button class="btn" onclick="showMessage('Aku sayang kamu banget 😘')">Bilang Sayang</button>
  <button class="btn" onclick="showMessage('Peluk erat buat kamu 🤗')">Peluk</button>
  <button class="btn" onclick="showMessage('Ini bunga untuk kamu 🌹')">Kasih Bunga</button>
  <button class="btn" onclick="showMessage('Aku bakal selalu ada buat kamu 💕')">Selamanya</button>

  <div id="output"></div>

  <script>
    function showMessage(msg) {
      const output = document.getElementById('output');
      output.textContent = msg;

      // Bikin hati-hati muncul
      const heart = document.createElement('div');
      heart.textContent = '💖';
      heart.className = 'heart';
      heart.style.left = Math.random() * 100 + 'vw';
      heart.style.top = '80vh';
      document.body.appendChild(heart);

      setTimeout(() => {
        heart.remove();
      }, 2000);
    }
  </script>
</body>
</html>
