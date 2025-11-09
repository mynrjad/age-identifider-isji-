<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Isjianne Dumlao - Age Checker</title>
  <style>
    body {
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      background-color: #1e1e1e;
      color: #ffffff;
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
      padding: 20px;
    }

    .container {
      max-width: 500px;
      text-align: center;
      background-color: #2c2c2c;
      padding: 30px;
      border-radius: 10px;
    }

    h1 {
      font-size: 2rem;
      margin-bottom: 10px;
    }

    p {
      margin-bottom: 20px;
      font-size: 1rem;
      color: #cccccc;
    }

    input[type="number"] {
      padding: 10px;
      font-size: 1rem;
      border-radius: 5px;
      border: none;
      margin-bottom: 15px;
      width: 80%;
    }

    button {
      padding: 10px 20px;
      font-size: 1rem;
      border-radius: 5px;
      border: none;
      background-color: #4a90e2;
      color: #ffffff;
      cursor: pointer;
    }

    button:hover {
      background-color: #357ab8;
    }

    .result {
      margin-top: 20px;
      font-size: 1.1rem;
      background-color: #3a3a3a;
      padding: 15px;
      border-radius: 5px;
    }
  </style>
</head>
<body>
  <div class="container">
    <h1>Isjianne Dumlao - Age Checker</h1>
    <p>Enter the age of your favorite artist:</p>
    <input type="number" id="ageInput" placeholder="Enter age...">
    <br>
    <button onclick="checkAge()">Check Age</button>
    <div class="result" id="result"></div>
  </div>

  <script>
    const ageInput = document.getElementById('ageInput');
    const result = document.getElementById('result');

    function checkAge() {
      const age = parseInt(ageInput.value);

      if (!age) {
        result.textContent = "Please enter a valid age!";
        return;
      }

      if (age < 25) {
        result.textContent = `They are ${age}, and they're younger than Google.`;
      } else if (age === 25) {
        result.textContent = `They are ${age}, and they're as old as Google.`;
      } else {
        result.textContent = `They are ${age}, and they're older than Google.`;
      }
    }
  </script>
</body>
</html>
