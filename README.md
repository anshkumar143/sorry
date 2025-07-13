<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>I'm Sorry ❤️</title>
  <style>
    body {
      margin: 0;
      font-family: 'Segoe UI', sans-serif;
      background: linear-gradient(to right, #ffafbd, #ffc3a0);
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      height: 100vh;
      overflow: hidden;
    }

    h1 {
      color: #fff;
      font-size: 3em;
      text-shadow: 2px 2px 4px rgba(0,0,0,0.3);
    }

    p {
      color: #fff;
      font-size: 1.5em;
      margin: 20px 30px;
      text-align: center;
    }

    button {
      background-color: #fff;
      color: #ff6f91;
      font-size: 1.2em;
      padding: 15px 30px;
      border: none;
      border-radius: 30px;
      cursor: pointer;
      box-shadow: 0 4px 8px rgba(0,0,0,0.2);
      transition: 0.3s ease;
    }

    button:hover {
      background-color: #ff6f91;
      color: #fff;
    }

    .hearts {
      position: absolute;
      width: 100%;
      height: 100%;
      top: 0;
      left: 0;
      pointer-events: none;
      overflow: hidden;
    }

    .heart {
      position: absolute;
      width: 20px;
      height: 20px;
      background: red;
      transform: rotate(45deg);
      animation: float 5s linear infinite;
    }

    .heart::before,
    .heart::after {
      content: '';
      position: absolute;
      width: 20px;
      height: 20px;
      background: red;
      border-radius: 50%;
    }

    .heart::before {
      top: -10px;
      left: 0;
    }

    .heart::after {
      left: -10px;
      top: 0;
    }

    @keyframes float {
      0% {
        transform: translateY(100vh) rotate(45deg);
        opacity: 1;
      }
      100% {
        transform: translateY(-10vh) rotate(45deg);
        opacity: 0;
      }
    }
  </style>
</head>
<body>
  <div class="hearts">
    <!-- Generate hearts dynamically -->
    <script>
      for(let i = 0; i < 30; i++) {
        const heart = document.createElement('div');
        heart.className = 'heart';
        heart.style.left = Math.random() * 100 + 'vw';
        heart.style.animationDuration = (Math.random() * 3 + 2) + 's';
        heart.style.opacity = Math.random();
        document.querySelector('.hearts').appendChild(heart);
      }
    </script>
  </div>

  <h1>I'm Really Sorry 😔</h1>
  <p>I know I made you upset, and it hurts me too. Please forgive me. You mean the world to me. 💕</p>
  <button onclick="alert('Thank you for forgiving me 😘')">Forgive Me?</button>
</body>
</html>
