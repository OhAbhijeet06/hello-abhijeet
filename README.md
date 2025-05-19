
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Hello, I am Abhijeet</title>
  <style>
    body {
      margin: 0;
      height: 100vh;
      background: linear-gradient(to bottom, #f9c5d1, #ffe1f0);
      overflow: hidden;
      display: flex;
      justify-content: center;
      align-items: center;
      font-family: 'Segoe UI', sans-serif;
    }

    h1 {
      position: absolute;
      color: #fff;
      font-size: 3em;
      text-shadow: 2px 2px 5px #e91e63;
    }

    .flower {
      position: absolute;
      top: -50px;
      font-size: 24px;
      animation: fall linear infinite;
    }

    @keyframes fall {
      to {
        transform: translateY(110vh) rotate(360deg);
        opacity: 0;
      }
    }
  </style>
</head>
<body>
  <h1>Hello, I am Abhijeet</h1>
  <script>
    function createFlower() {
      const flower = document.createElement('div');
      flower.className = 'flower';
      flower.innerHTML = '❀';
      flower.style.left = Math.random() * 100 + 'vw';
      flower.style.animationDuration = (Math.random() * 3 + 2) + 's';
      document.body.appendChild(flower);

      setTimeout(() => {
        flower.remove();
      }, 5000);
    }

    setInterval(createFlower, 300);
  </script>
</body>
</html>
