# amemoduleexam.education
aircraft systems for ame
<!DOCTYPE html>
<html>
<head>
  <title>aircraft systems for ame</title>
  <script>
    // Function to validate login credentials
    function validateLogin() {
      var username = document.getElementById('username').value;
      var password = document.getElementById('password').value;

      if (username === 'aviolegis01' && password === '0101') {
        // Display the MCQ questions
        document.getElementById('loginContainer').style.display = 'none';
        document.getElementById('mcqContainer').style.display = 'block';
      } else {
        alert('Invalid login credentials. Please try again.');
      }
    }

    // Array of correct answers
    var correctAnswers = {
      q11: 'b',
      q12: 'a',
      q13: 'a'
    };

    // Function to calculate the total number of correct answers
    function calculateScore() {
      var score = 0;
      var questions = Object.keys(correctAnswers);

      // Loop through the questions and check if the selected answer is correct
      for (var i = 0; i < questions.length; i++) {
        var questionNumber = questions[i];
        var selectedAnswer = document.querySelector('input[name="' + questionNumber + '"]:checked').value;

        if (selectedAnswer === correctAnswers[questionNumber]) {
          score++;
        }
      }

      // Display the score
      document.getElementById('score').innerHTML = "Your score: " + score + "/" + questions.length;
    }
  </script>
  <style>
    #mcqContainer {
      display: none;
    }
  </style>
</head>
<body>
  <h1>MCQ Questions</h1>

  <div id="loginContainer">
    <label for="username">Username:</label>
    <input type="text" id="username"><br><br>

    <label for="password">Password:</label>
    <input type="password" id="password"><br><br>

    <button type="button" onclick="validateLogin()">Login</button>
  </div>

  <div id="mcqContainer">
    <form>
      <!-- Question 11 -->
      <h3>11. Which control surfaces are responsible for the directional control of a fixed-wing aircraft?</h3>
      <label>
        <input type="radio" name="q11" value="a"> a) Ailerons, elevators, and flaps
      </label><br>
      <label>
        <input type="radio" name="q11" value="b"> b) Ailerons, elevators, and rudders
      </label><br>
      <label>
        <input type="radio" name="q11" value="c"> c) Ailerons, flaps, and rudders
      </label><br>
      <label>
        <input type="radio" name="q11" value="d"> d) Elevators, flaps, and rudders
      </label><br>
      <br>

      <!-- Question 12 -->
      <h3>12. The primary flight control surfaces include which of the following?</h3>
      <label>
        <input type="radio" name="q12" value="a"> a) Ailerons, elevators, and flaps
      </label><br>
      <label>
        <input type="radio" name="q12" value="b"> b) Ailerons, elevators, and rudders
      </label><br>
      <label>
        <input type="radio" name="q12" value="c"> c) Flaps, elevators, and rudders
      </label><br>
      <label>
        <input type="radio" name="q12" value="d"> d) Ailerons, flaps, and rudders
      </label><br>
      <br>

      <!-- Question 13 -->
      <h3>13. The movement of ailerons causes the aircraft to rotate around which axis?</h3>
      <label>
        <input type="radio" name="q13" value="a"> a) Lateral axis
      </label><br>
      <label>
        <input type="radio" name="q13" value="b"> b) Longitudinal axis
      </label><br>
      <label>
        <input type="radio" name="q13" value="c"> c) Vertical axis
      </label><br>
      <label>
        <input type="radio" name="q13" value="d"> d) Horizontal axis
      </label><br>
      <br>

      <!-- Submit button -->
      <button type="button" onclick="calculateScore()">Submit</button>

      <!-- Score display -->
      <div id="score"></div>
    </form>
  </div>
</body>
</html>
