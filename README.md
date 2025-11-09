<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <title>Isjianne Dumlao</title>

  <style>
    body {
      font-family: Arial, sans-serif;
      background: #0d0d0d;
      color: #f0f0f0;
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
      margin: 0;
    }

    .container {
      background: #181818;
      padding: 30px;
      width: 350px;
      border-radius: 12px;
      text-align: center;
      animation: fadeIn 0.5s ease forwards;
      opacity: 0;
    }

    input {
      width: 80%;
      padding: 10px;
      border-radius: 8px;
      border: 1px solid #333;
      background: #111;
      color: white;
      margin-bottom: 15px;
    }

    button {
      padding: 10px 20px;
      border: none;
      background: #4da3ff;
      color: white;
      border-radius: 8px;
      cursor: pointer;
    }

    #result {
      margin-top: 15px;
      font-size: 16px;
      opacity: 0;
      animation: fadeIn 0.5s ease forwards;
      min-height: 20px;
    }

    @keyframes fadeIn {
      from { opacity: 0; }
      to { opacity: 1; }
    }
  </style>
</head>

<body>
  <div class="container">
    <h2>Artist Age Checker</h2>

    <input id="artistAge" type="number" placeholder="Enter age" />
    <button onclick="checkAge()">Check</button>

    <div id="result"></div>
  </div>

  <script>
    function checkAge() {
      const age = Number(document.getElementById("artistAge").value);
      const googleAge = 25;
      let message = "";

      if (!age && age !== 0) {
        message = "Please enter a valid age.";
      } else if (age < googleAge) {
        message = `They are ${age}, and they're younger than Google.`;
      } else if (age === googleAge) {
        message = `They are ${age}, and they're as old as Google.`;
      } else {
        message = `They are ${age}, and they're older than Google.`;
      }

      const result = document.getElementById("result");
      result.textContent = message;

      result.style.opacity = "0";
      setTimeout(() => {
        result.style.opacity = "1";
      }, 10);
    }
  </script>
</body>
</html>
