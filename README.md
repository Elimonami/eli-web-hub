# index.html
This is my web site with a lot of stuff
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>Eli Hub</title>

<style>
body {
  margin: 0;
  font-family: Arial, sans-serif;
  background: linear-gradient(135deg, #0f0f1a, #1b1b2f);
  color: white;
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
  text-align: center;
  overflow: hidden;
}

/* Glow background */
body::before {
  content: "";
  position: absolute;
  width: 500px;
  height: 500px;
  background: rgba(88, 101, 242, 0.15);
  border-radius: 50%;
  filter: blur(120px);
  top: -100px;
  left: -100px;
}

/* Main container */
.container {
  display: flex;
  flex-direction: column;
  gap: 20px;
  z-index: 2;
}

h1 {
  margin: 0;
  font-size: 50px;
  letter-spacing: 2px;
  animation: glow 2s infinite alternate;
}

@keyframes glow {
  from {
    text-shadow: 0 0 10px #5865F2;
  }
  to {
    text-shadow: 0 0 25px #8ea1ff;
  }
}

p {
  color: #b5b5c3;
  margin-top: -10px;
}

/* Main button */
button {
  padding: 15px 25px;
  font-size: 16px;
  background: rgba(88, 101, 242, 0.15);
  border: 1px solid rgba(255,255,255,0.1);
  border-radius: 14px;
  color: white;
  cursor: pointer;
  transition: 0.25s;
  backdrop-filter: blur(8px);
  box-shadow: 0 0 15px rgba(88,101,242,0.25);
}

button:hover {
  transform: scale(1.07);
  background: rgba(88, 101, 242, 0.3);
  box-shadow: 0 0 25px rgba(88,101,242,0.6);
}

button:active {
  transform: scale(0.97);
}

/* Special TOS button */
.tos-button {
  position: absolute;
  bottom: 20px;
  right: 20px;
  padding: 12px 18px;
  font-size: 14px;
  border-radius: 999px;
  background: rgba(255,255,255,0.08);
  border: 1px solid rgba(255,255,255,0.12);
  color: #d7d7ff;
  box-shadow: 0 0 20px rgba(255,255,255,0.08);
}

.tos-button:hover {
  background: rgba(255,255,255,0.16);
  transform: scale(1.08);
  box-shadow: 0 0 30px rgba(255,255,255,0.2);
}
</style>

</head>
<body>

<div class="container">
  <h1>🚀 Eli Web Hub</h1>
  <p>One available experiment</p>

  <button onclick="goToSite1()">
    Discord IP Ban
  </button>
</div>

<!-- Special corner button -->
<button class="tos-button" onclick="openTOS()">
  📜 Terms Of Service
</button>

<script>
function goToSite1() {
  window.open("https://listmakerfordiscord.netlify.app/", "_blank");
}

function openTOS() {
  window.open("https://whattoknow.netlify.app/", "_blank");
}
</script>

</body>
</html>
