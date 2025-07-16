<!DOCTYPE html>
<html>
  <head>
    <title>  ELITE WORLD </title>
    <link rel="stylesheet" href="styles.css" />
  </head>
  <body>
      <h1 class="title"> ELITE WORLD 
      </h1>
      <p id="currentTime"></p>
      <script src="script.js"></script>
  </body>
</html><!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <title>ELITE EARNING POINT</title>
  <style>
    body {
      background: #0f172a;
      color: #fff;
      font-family: Arial, sans-serif;
      text-align: center;
      padding: 40px;
    }
    h1 {
      color: #00ff99;
    }
    a {
      color: #00ccff;
      text-decoration: none;
      font-size: 20px;
    }
    .box {
      background: #1e293b;
      padding: 20px;
      border-radius: 12px;
      box-shadow: 0 0 20px #00ff99;
      display: inline-block;
      margin-top: 20px;
      width: 300px;
    }
    input {
      width: 90%;
      padding: 10px;
      margin: 8px 0;
      border: none;
      border-radius: 8px;
    }
    button {
      padding: 10px 20px;
      border: none;
      border-radius: 8px;
      background-color: #00ff99;
      color: #000;
      font-weight: bold;
      cursor: pointer;
      transition: background-color 0.3s ease;
    }
    button.applied {
      background-color: #009944;
      color: #fff;
    }
    .toggle-link {
      color: #ccc;
      font-size: 14px;
      cursor: pointer;
    }
    .telegram-box {
      margin-top: 40px;
    }
    #eliteAnimation {
      font-size: 40px;
      font-weight: bold;
      color: #00ff99;
      animation: glow 1.5s ease-in-out infinite alternate;
      display: none;
      margin-top: 30px;
    }
    @keyframes glow {
      from {
        text-shadow: 0 0 10px #00ff99, 0 0 20px #00ff99;
      }
      to {
        text-shadow: 0 0 20px #00ffff, 0 0 40px #00ffff;
      }
    }
    .jobs {
      display: none;
      margin-top: 30px;
    }
    .job-card {
      background: #1e293b;
      border: 1px solid #00ff99;
      border-radius: 12px;
      padding: 20px;
      margin: 10px auto;
      width: 90%;
      max-width: 400px;
    }
  </style>
</head>
<body>
  <h1>💸 ELITE EARNING POINT 💸</h1>

  <div class="box" id="loginBox">
    <h2>Login</h2>
    <input type="email" placeholder="Email" id="email" /><br />
    <input type="password" placeholder="Password" id="password" /><br />
    <button onclick="handleLogin()">Login</button>
    <p class="toggle-link" onclick="toggleForm()"
      >Don't have an account? Sign Up</p
    >
  </div>

  <div class="box" id="signupBox" style="display:none;">
    <h2>Sign Up</h2>
    <input type="text" placeholder="Full Name" /><br />
    <input type="email" placeholder="Email" /><br />
    <input type="password" placeholder="Password" /><br />
    <button>Sign Up</button>
    <p class="toggle-link" onclick="toggleForm()">Already have an account? Login</p>
  </div>

  <div class="telegram-box">
    <p>👉 Join our Telegram for daily updates:</p>
    <a href="https://t.me/eliteearning75" target="_blank">🔗 Join Now</a>
  </div>

  <div id="eliteAnimation">✨ ELITE EARNING POINT ✨</div>

  <div class="jobs" id="jobSection">
    <div class="job-card">
      <h3>📄 Typing Survey</h3>
      <p>Earn money by filling out simple typing forms daily.</p>
      <button class="apply-btn" onclick="toggleApply(this)">Apply Now</button>
    </div>
    <div class="job-card">
      <h3>💼 Data Entry Job</h3>
      <p>Get paid weekly for entering basic data online.</p>
      <button class="apply-btn" onclick="toggleApply(this)">Apply Now</button>
    </div>
  </div>

  <script>
    function toggleForm() {
      const loginBox = document.getElementById("loginBox");
      const signupBox = document.getElementById("signupBox");
      loginBox.style.display = loginBox.style.display === "none" ? "block" : "none";
      signupBox.style.display = signupBox.style.display === "none" ? "block" : "none";
    }

    function handleLogin() {
      document.getElementById("loginBox").style.display = "none";
      document.getElementById("signupBox").style.display = "none";
      document.getElementById("eliteAnimation").style.display = "block";

      // Show jobs after animation (2 seconds delay)
      setTimeout(() => {
        document.getElementById("eliteAnimation").style.display = "none";
        document.getElementById("jobSection").style.display = "block";
      }, 2000);
    }

    function toggleApply(btn) {
      if (btn.classList.contains("applied")) {
        btn.classList.remove("applied");
        btn.textContent = "Apply Now";
      } else {
        btn.classList.add("applied");
        btn.textContent = "Applied";
      }
    }
  </script>
</body>
</html>
