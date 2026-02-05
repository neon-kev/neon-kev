<!-- index.html -->
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>My Banner</title>
  <style>
    body {
      margin: 0;
      font-family: 'Arial', sans-serif;
    }
    .banner {
      position: relative;
      height: 300px;
      background: linear-gradient(135deg, #6a11cb, #2575fc);
      display: flex;
      justify-content: center;
      align-items: center;
      color: white;
      font-size: 2.5rem;
      overflow: hidden;
    }
    .banner span {
      position: absolute;
      animation: float 5s infinite linear;
    }
    @keyframes float {
      0% { transform: translateY(0); }
      50% { transform: translateY(-20px); }
      100% { transform: translateY(0); }
    }
  </style>
</head>
<body>
  <div class="banner">
    <span>🚀 Welcome to My GitHub!</span>
  </div>
  <script>
    // Optional JS: Change banner text dynamically
    const banner = document.querySelector('.banner span');
    const messages = ["🚀 Welcome!", "💻 Code & Coffee", "✨ Explore Projects"];
    let i = 0;
    setInterval(() => {
      i = (i + 1) % messages.length;
      banner.textContent = messages[i];
    }, 3000);
  </script>
</body>
</html>


