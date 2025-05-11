<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Algebra Questions</title>
  <style>
    body {
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      background: linear-gradient(135deg, #6dd5ed, #2193b0);
      color: #fff;
      text-align: center;
      margin: 0;
      padding: 0;
    }
    .container {
      padding: 60px 20px;
    }
    .question-box {
      background: rgba(255, 255, 255, 0.95);
      color: #333;
      margin: 0 auto;
      padding: 30px;
      width: 90%;
      max-width: 700px;
      border-radius: 15px;
      box-shadow: 0 8px 20px rgba(0,0,0,0.2);
      font-size: 22px;
      transition: all 0.3s ease;
    }
    h1 {
      font-size: 40px;
      margin-bottom: 20px;
    }
    button {
      margin-top: 30px;
      padding: 10px 20px;
      font-size: 18px;
      border: none;
      border-radius: 10px;
      background-color: #ff7e5f;
      color: white;
      cursor: pointer;
      transition: background 0.3s ease;
    }
    button:hover {
      background-color: #feb47b;
    }
  </style>
</head>
<body>
  <div class="container">
    <h1>Algebra Question</h1>
    <div class="question-box" id="questionBox">Loading question...</div>
    <button onclick="newQuestion()">New Question</button>
  </div>

  <script>
    const questions = [
      "Solve for x: 2x + 3 = 11",
      "Factor: x² - 5x + 6",
      "Simplify: (3x² - x + 2) - (x² + 2x - 1)",
      "What is the slope of the line y = 4x - 7?",
      "Solve: (x - 2)(x + 3) = 0"
    ];

    function getRandomQuestion() {
      const index = Math.floor(Math.random() * questions.length);
      return questions[index];
    }

    function newQuestion() {
      document.getElementById("questionBox").innerText = getRandomQuestion();
    }

    // Load first question on page load
    newQuestion();
  </script>
</body>
</html>
