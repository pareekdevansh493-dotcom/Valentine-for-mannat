# Valentine-for-<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>For Mannat ❤️</title>
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      font-family: 'Poppins', sans-serif;
    }

    body {
      height: 100vh;
      background: linear-gradient(135deg, #ff758c, #ff7eb3);
      display: flex;
      justify-content: center;
      align-items: center;
      overflow: hidden;
      color: white;
    }

    .container {
      text-align: center;
      padding: 30px;
      animation: fadeIn 2s ease;
    }

    h1 {
      font-size: 2.6rem;
      margin-bottom: 15px;
    }

    p {
      font-size: 1.2rem;
      margin-bottom: 30px;
      opacity: 0.95;
    }

    .buttons {
      display: flex;
      gap: 20px;
      justify-content: center;
      position: relative;
    }

    button {
      padding: 15px 35px;
      font-size: 1.1rem;
      border: none;
      border-radius: 50px;
      cursor: pointer;
      transition: all 0.3s ease;
      font-weight: 600;
    }

    .yes {
      background: white;
      color: #ff4d6d;
    }

    .yes:hover {
      transform: scale(1.2);
      background: #ffe6eb;
    }

    .obviously {
      background: #ff4d6d;
      color: white;
    }

    .obviously:hover {
      transform: scale(1.15) rotate(-2deg);
      background: #ff1e4d;
    }

    .hidden {
      display: none;
    }

    .message {
      animation: fadeIn 1.5s ease;
    }

    .message h2 {
      font-size: 2.3rem;
      margin-bottom: 15px;
    }

    .message p {
      font-size: 1.2rem;
      line-height: 1.7;
    }

    .hearts {
      position: absolute;
      width: 100%;
      height: 100%;
      top: 0;
      left: 0;
      pointer-events: none;
    }

    .heart {
      position: absolute;
      color: rgba(255, 255, 255, 0.8);
      font-size: 20px;
      animation: float 6s linear infinite;
    }

    @keyframes fadeIn {
      from { opacity: 0; transform: translateY(20px); }
      to { opacity: 1; transform: translateY(0); }
    }

    @keyframes float {
      from { transform: translateY(100vh) scale(0.5); opacity: 1; }
      to { transform: translateY(-10vh) scale(1.2); opacity: 0; }
    }
  </style>
  <audio id="bgMusic" loop>
    <source src="https://cdn.pixabay.com/download/audio/2022/03/15/audio_6b2b6a6f89.mp3" type="audio/mpeg">
  </audio>
</head>
<body>

  <div class="hearts" id="hearts"></div>

  <div class="container" id="question">
    <h1>Mannat ❤️</h1>
    <p>You make my ordinary days feel extraordinary…</p>
    <h1>Will you be my Valentine? 💖</h1>
    <div class="buttons">
      <button class="yes" onclick="showLove(); playMusic();()">Yes 💕</button>
      <button class="obviously" onclick="showLove(); playMusic();()">Obviously 😌</button>
    </div>
  </div>

  <div class="container hidden message" id="loveMessage">
    <h2>You chose me 🥹💘</h2>
    <p>
      Mannat, you are my happiest thought and my safest place.<br />
      Every smile of yours feels like a blessing I never asked for but always needed.<br /><br />
      I promise to stand by you, laugh with you,
      hold your hand on hard days,
      and love you a little more every single day. ✨<br /><br />
      Happy Valentine’s, my love ❤️<br /><br />
      — Devansh 💖<br /><br />Come here… I owe you the warmest hug 🤍
    </p>
  </div>

  <script>
    function showLove() {
      document.getElementById('question').classList.add('hidden');
      document.getElementById('loveMessage').classList.remove('hidden');
      createHearts();
    }

    function playMusic() {
      const music = document.getElementById('bgMusic');
      music.volume = 0.6;
      music.play();
    }

    function createHearts()() {
      const heartsContainer = document.getElementById('hearts');
      for (let i = 0; i < 40; i++) {
        const heart = document.createElement('div');
        heart.className = 'heart';
        heart.innerHTML = '❤';
        heart.style.left = Math.random() * 100 + 'vw';
        heart.style.animationDuration = 3 + Math.random() * 3 + 's';
        heart.style.fontSize = 16 + Math.random() * 26 + 'px';
        heartsContainer.appendChild(heart);

        setTimeout(() => heart.remove(), 6000);
      }
    }
  </script>

</body>
</html>
