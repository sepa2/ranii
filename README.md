<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8">
  <title>Cie abis ospek</title>
  <style>
    body {
      font-family: 'Segoe UI', sans-serif;
      background-color: #2b00d8;
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
      margin: 0;
    }

    .login-box, .message-box {
      background: white;
      padding: 30px;
      border-radius: 20px;
      box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
      text-align: center;
      width: 300px;
      opacity: 1;
      transition: opacity 1s ease-in-out;
    }

    input {
      padding: 10px;
      margin: 10px 0;
      width: 100%;
      border-radius: 10px;
      border: 1px solid #ccc;
    }

    button {
      padding: 10px 20px;
      background-color: #ff66a3;
      color: white;
      border: none;
      border-radius: 10px;
      cursor: pointer;
      font-weight: bold;
    }

    h2 {
      color: #ff3399;
    }

    .fade-in {
      animation: fadeIn 1s ease-in-out;
    }

    @keyframes fadeIn {
      from { opacity: 0; transform: scale(0.95); }
      to { opacity: 1; transform: scale(1); }
    }
  </style>
</head>
<body>

<div class="login-box" id="loginBox">
  <h2>Login</h2>
  <input type="text" id="username" placeholder="Nama kamu">
  <input type="password" id="password" placeholder="Password rahasia">
  <button onclick="login()">Masuk</button>
</div>

<div class="message-box" id="messageBox" style="display:none;">
  <h2>Hii, Rani!</h2>
  <p>Selamat, karena sudah berhasil melewati hari yang melelahkan 🤩</p>
  <p>nanti kita maen ya, kalo gua ke nangor lagi ✌️</p>
</div>

<script>
  function login() {
    const user = document.getElementById("username").value.trim();
    const pass = document.getElementById("password").value;

    const correctUser = "Rani";
    const correctPass = "2206";

    if (user === correctUser && pass === correctPass) {
      const loginBox = document.getElementById("loginBox");
      const messageBox = document.getElementById("messageBox");

      loginBox.style.opacity = 0;
      setTimeout(() => {
        loginBox.style.display = "none";
        messageBox.style.display = "block";
        messageBox.classList.add("fade-in");
      }, 1000);
    } else {
      alert("Nama atau password salah, coba lagi ya 🥺");
    }
  }
</script>

</body>
</html>
