# index.html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Login</title>
  <style>
    * { box-sizing: border-box; }
    body {
      margin: 0;
      min-height: 100vh;
      display: flex;
      justify-content: center;
      align-items: center;
      font-family: Arial, sans-serif;
      background: linear-gradient(135deg, #101827, #263c5a);
    }
    .login-box {
      width: min(90%, 360px);
      padding: 30px;
      background: white;
      border-radius: 16px;
      box-shadow: 0 12px 35px #0005;
    }
    h2 { text-align: center; margin-bottom: 24px; }
    input {
      width: 100%;
      padding: 12px;
      margin-bottom: 14px;
      border: 1px solid #ccc;
      border-radius: 8px;
    }
    button {
      width: 100%;
      padding: 12px;
      border: none;
      border-radius: 8px;
      background: #1769ff;
      color: white;
      font-size: 16px;
      cursor: pointer;
    }
    button:hover { background: #0d4ec7; }
    #message { text-align: center; font-size: 14px; }
  </style>
</head>
<body>
  <main class="login-box">
    <h2>Welcome</h2>
    <form id="loginForm">
      <input type="text" id="username" placeholder="Username" autocomplete="username" required>
      <input type="password" id="password" placeholder="Password" autocomplete="current-password" required>
      <button type="submit">Login</button>
      <p id="message" aria-live="polite"></p>
    </form>
  </main>
  <script>
    const form = document.getElementById("loginForm");
    const message = document.getElementById("message");
    form.addEventListener("submit", function (event) {
      event.preventDefault();
      message.textContent = "Demo only: connect a secure authentication system to log in.";
      message.style.color = "#b45309";
    });
  </script>
</body>
</html>
