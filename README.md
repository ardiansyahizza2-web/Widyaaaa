#<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Maafin Aku, Sayang ❤️</title>
  <style>
    body {
      margin: 0;
      padding: 0;
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
      background: linear-gradient(135deg, #ff9a9e, #fad0c4);
      font-family: 'Poppins', sans-serif;
      text-align: center;
      overflow: hidden;
    }
    .card {
      background: white;
      padding: 30px;
      border-radius: 20px;
      box-shadow: 0 4px 20px rgba(0,0,0,0.2);
      max-width: 400px;
      animation: fadeIn 2s ease;
    }
    h1 {
      color: #ff4e78;
      font-size: 2rem;
    }
    p {
      font-size: 1.2rem;
      margin: 15px 0;
      color: #444;
    }
    button {
      background: #ff4e78;
      color: white;
      border: none;
      padding: 12px 25px;
      font-size: 1rem;
      border-radius: 25px;
      cursor: pointer;
      transition: 0.3s;
    }
    button:hover {
      background: #e63e67;
    }
    .hearts {
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      pointer-events: none;
      overflow: hidden;
    }
    .heart {
      position: absolute;
      color: #ff4e78;
      font-size: 20px;
      animation: float 5s linear infinite;
    }
    @keyframes fadeIn {
      from {opacity: 0; transform: translateY(30px);}
      to {opacity: 1; transform: translateY(0);}
    }
    @keyframes float {
      0% {transform: translateY(100vh) scale(0.5); opacity: 0;}
      50% {opacity: 1;}
      100% {transform: translateY(-10vh) scale(1.2); opacity: 0;}
    }
  </style>
</head>
<body>
  <div class="card">
    <h1>Maafin Aku ya, Sayang ❤️</h1>
    <p>Aku sadar aku udah bikin kamu kesal. Aku nggak bermaksud begitu. Semoga kamu mau maafin aku 🙏</p>
    <button onclick="alert('Makasih udah maafin aku, love you ❤️')">Maafin Aku</button>
  </div>
  <div class="hearts"></div>

  <!-- Musik Romantis -->
  <audio id="bg-music" autoplay loop>
    <source src="https://www.bensound.com/bensound-music/bensound-romantic.mp3" type="audio/mpeg">
  </audio>

  <script>
    function createHeart() {
      const heart = document.createElement("div");
      heart.classList.add("heart");
      heart.innerHTML = "❤️";
      heart.style.left = Math.random() * 100 + "vw";
      heart.style.fontSize = (Math.random() * 20 + 10) + "px";
      heart.style.animationDuration = (Math.random() * 3 + 3) + "s";
      document.querySelector(".hearts").appendChild(heart);

      setTimeout(() => {
        heart.remove();
      }, 5000);
    }
    setInterval(createHeart, 500);
  </script>
</body>
</html>
