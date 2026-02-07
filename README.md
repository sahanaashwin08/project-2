##### What Language Is This?
The code you pasted is written using three web technologies:

# 1.HTML (HyperText Markup Language):
    This defines the structure of the web page:
         Example: <div>, <h1>, <button> are HTML tags.

# 2.CSS (Cascading Style Sheets):
      This controls the design and styling of the page.
          Example: background colors, fonts, button styles.

# 3.JavaScript (JS)
    This adds logic and interactivity.
       Example: showing questions, checking answers, updating score.

Together, these three are the core languages of web development.

 ## How Does It Run?
    **You don’t need any special compiler.**
    **Just save the code in a file with the extension .html (for example: quiz.html).**
    **Double-click the file or open it in any modern web browser (Chrome, Edge, Firefox, Safari).**
    **The browser itself understands HTML, CSS, and JavaScript, so it will render the page and run the quiz logic.**

## What Happens When You Run It?
     **HTML builds the quiz container (title, question area, options area, score area).**
     **CSS makes it look nice (gradient background, rounded buttons, hover effects).**
     **JavaScript loads questions one by one, creates option buttons dynamically, checks if your answer is correct, and finally shows your score.**
# Summary:
    **Language used: HTML + CSS + JavaScript**
    **Execution: Runs directly in a web browser (no extra software needed)** 
    

Output: A fully interactive quiz game with questions, options, and scoring
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Quiz Game</title>
  <style>
    body {
      font-family: 'Segoe UI', sans-serif;
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
      margin: 0;
      background: linear-gradient(135deg, #ff9a9e 0%, #fad0c4 100%);
    }

    .quiz-container {
      background: #fff;
      padding: 20px;
      border-radius: 15px;
      box-shadow: 0 0 20px rgba(0,0,0,0.3);
      width: 400px;
      text-align: center;
    }

    h1 {
      margin-bottom: 20px;
    }

    .question {
      font-size: 1.2em;
      margin-bottom: 15px;
    }

    .options {
      display: flex;
      flex-direction: column;
      gap: 10px;
    }

    button {
      padding: 10px;
      font-size: 1em;
      border: none;
      border-radius: 8px;
      cursor: pointer;
      background: #007bff;
      color: white;
      transition: background 0.3s;
    }

    button:hover {
      background: #0056b3;
    }

    #score {
      margin-top: 20px;
      font-weight: bold;
      font-size: 1.2em;
    }
  </style>
</head>
<body>
  <div class="quiz-container">
    <h1>Quiz Game</h1>
    <div id="quiz">
      <div class="question" id="question"></div>
      <div class="options" id="options"></div>
    </div>
    <div id="score"></div>
  </div>

  <script>
    const questions = [
      {
        question: "Which language runs in a web browser?",
        options: ["Java", "C", "Python", "JavaScript"],
        answer: "JavaScript"
      },
      {
        question: "What does CSS stand for?",
        options: ["Central Style Sheets", "Cascading Style Sheets", "Computer Style Sheets", "Creative Style System"],
        answer: "Cascading Style Sheets"
      },
      {
        question: "What does HTML stand for?",
        options: ["HyperText Markup Language", "Hyper Transfer Markup Language", "HighText Machine Language", "None of the above"],
        answer: "HyperText Markup Language"
      }
    ];

    let currentQuestion = 0;
    let score = 0;

    function loadQuestion() {
      if (currentQuestion < questions.length) {
        document.getElementById("question").textContent = questions[currentQuestion].question;
        const optionsDiv = document.getElementById("options");
        optionsDiv.innerHTML = "";
        questions[currentQuestion].options.forEach(option => {
          const btn = document.createElement("button");
          btn.textContent = option;
          btn.onclick = () => checkAnswer(option);
          optionsDiv.appendChild(btn);
        });
      } else {
        document.getElementById("quiz").innerHTML = "<h2>Quiz Completed!</h2>";
        document.getElementById("score").textContent = "Your Score: " + score + "/" + questions.length;
      }
    }

    function checkAnswer(selected) {
      if (selected === questions[currentQuestion].answer) {
        score++;
      }
      currentQuestion++;
      loadQuestion();
    }

    // Load first question after DOM ready
    window.onload = loadQuestion;
  </script>
</body>
</html>
# OTUPUT 
  http://127.0.0.1:5500/git/html-css-javascript-website/e-commer-website/index.html
