<!DOCTYPE html><html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>FF panel</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background: #f4f4f9;
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
    }
    .panel, .welcome {
      background: white;
      padding: 20px 30px;
      border-radius: 12px;
      box-shadow: 0 4px 10px rgba(0,0,0,0.1);
      text-align: center;
      width: 320px;
    }
    h1, h2, h3 {
      color: #333;
    }
    .input-box {
      margin: 10px 0;
      text-align: left;
    }
    label {
      display: block;
      font-weight: bold;
      margin-bottom: 5px;
    }
    input {
      width: 100%;
      padding: 8px;
      border: 1px solid #ccc;
      border-radius: 8px;
    }
    button {
      margin-top: 15px;
      width: 100%;
      padding: 10px;
      border: none;
      border-radius: 8px;
      background: #007bff;
      color: white;
      font-size: 16px;
      cursor: pointer;
    }
    button:hover {
      background: #0056b3;
    }
    .toggle-btn {
      background: #28a745;
    }
    .toggle-btn.off {
      background: #dc3545;
    }
    .welcome {
      display: none;
    }
    .active-msg {
      margin-top: 10px;
      color: green;
      font-weight: bold;
      display: none;
    }
  </style>
</head>
<body>
  <div class="panel" id="loginPanel">
    <h1>FF panel</h1>
    <div class="input-box">
      <label for="username">Username:</label>
      <input type="text" id="username" placeholder="Enter Username">
    </div>
    <div class="input-box">
      <label for="password">Password:</label>
      <input type="password" id="password" placeholder="Enter Password">
    </div>
    <button onclick="login()">Login</button>
  </div>  <div class="welcome" id="welcomePage">
    <h2>Made by BISMIL</h2>
    <h1>Welcome Bismil!</h1>
    <p>You have successfully logged in 🚀</p><div>
  <h3>Auto Drag Head</h3>
  <button id="toggleBtn" class="toggle-btn" onclick="toggleAutoDrag()">ON</button>
</div>

<div>
  <h3>Bypass</h3>
  <button onclick="bypass()">Activate Bypass</button>
  <div id="bypassMsg" class="active-msg">Active ✅</div>
</div>

<div>
  <h3>Free Fire Max</h3>
  <button onclick="openFF()">Open Play Store</button>
</div>

<div>
  <h3>Download Panel</h3>
  <button onclick="downloadPanel()">Download</button>
</div>

  </div>  <script>
    function login() {
      const user = document.getElementById('username').value;
      const pass = document.getElementById('password').value;
      
      if(user === "BISMIL" && pass === "991021") {
        document.getElementById("loginPanel").style.display = "none";
        document.getElementById("welcomePage").style.display = "block";
      } else {
        alert("Invalid Username or Password!");
      }
    }

    function toggleAutoDrag() {
      const btn = document.getElementById("toggleBtn");
      if(btn.innerText === "ON") {
        btn.innerText = "OFF";
        btn.classList.add("off");
      } else {
        btn.innerText = "ON";
        btn.classList.remove("off");
      }
    }

    function bypass() {
      document.getElementById("bypassMsg").style.display = "block";
    }

    function openFF() {
      window.open("https://play.google.com/store/apps/details?id=com.dts.freefiremax", "_blank");
    }

    function downloadPanel() {
      window.open("https://www.mediafire.com/file/tyo7w2tc7senlt7/GREEN_ENEMY_%252B_DRAG_50%2525_BY_MANISH_MODS.7z/file?dkey=o13qmd0h4cd&r=9", "_blank");
    }
  </script></body>
</html>
