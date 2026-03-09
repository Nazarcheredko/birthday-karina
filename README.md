<!DOCTYPE html>
<html lang="uk">
<head>
<meta charset="UTF-8">
<title>З Днем Народження, Каріно ❤️</title>

<style>
body {
  margin: 0;
  font-family: Arial, sans-serif;
  overflow: hidden;
}

.bg {
  position: fixed;
  width: 100%;
  height: 100%;
  background: url("karina.jpg") center/cover no-repeat;
  filter: brightness(0.7);
}

.center {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  text-align: center;
  color: white;
}

h1 {
  font-size: 55px;
}

button {
  padding: 15px 30px;
  font-size: 18px;
  border: none;
  border-radius: 30px;
  background: #ff4d6d;
  color: white;
  cursor: pointer;
}

.message {
  display: none;
  margin-top: 20px;
  font-size: 22px;
}

.heart {
  position: absolute;
  color: red;
  animation: fall 5s linear infinite;
}

@keyframes fall {
  0% {
    transform: translateY(-100px);
  }
  100% {
    transform: translateY(100vh);
  }
}
</style>
</head>

<body>

<div class="bg"></div>

<div class="center">
  <h1>🎂 З Днем Народження, Каріно! ❤️</h1>

  <button onclick="start()">Відкрити сюрприз</button>

  <div class="message" id="msg">
    Бажаю тобі море щастя, радості і здійснення всіх бажань! 
    Ти - найдорожча людина для мене ❤️
  </div>
</div>

<script>
function start() {
  document.getElementById("msg").style.display = "block";

  for (let i = 0; i < 40; i++) {
    let heart = document.createElement("div");
    heart.innerHTML = "❤️";
    heart.className = "heart";
    heart.style.left = Math.random() * 100 + "vw";
    heart.style.fontSize = Math.random() * 30 + 20 + "px";
    heart.style.animationDuration = 3 + Math.random() * 5 + "s";
    document.body.appendChild(heart);
  }
}
</script>

</body>
</html>
