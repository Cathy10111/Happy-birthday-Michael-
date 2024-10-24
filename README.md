# Happy-birthday-Michael-
Birthday quiz 
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Michael's Special Quiz</title>
    <style>
        body {
            font-family: 'Arial', sans-serif;
            background: linear-gradient(to bottom right, #ff5f6d, #ffc371);
            text-align: center;
            padding: 50px;
            color: #fff;
        }
        h1 {
            color: #ffcccb;
            margin-bottom: 30px;
        }
        .question {
            background-color: rgba(255, 102, 153, 0.7);
            border-radius: 15px;
            padding: 20px;
            margin: 20px auto;
            width: 80%;
            max-width: 600px;
        }
        button {
            padding: 15px 30px;
            background-color: #ff6666;
            color: white;
            border: none;
            border-radius: 10px;
            cursor: pointer;
            font-size: 1.2em;
            margin: 10px;
            transition: background-color 0.3s;
        }
        button:hover {
            background-color: #ff4444;
        }
        #reward {
            font-size: 1.5em;
            margin-top: 20px;
            color: #fff;
        }
    </style>
</head>
<body>

    <h1>Michael's Special Quiz ❤️</h1>
    <div id="quiz-container">
        <div class="question" id="question1">
            <p><strong>1. What is your favorite color?</strong></p>
            <button onclick="showQuestion(2)">Red</button>
            <button onclick="showQuestion(2)">Blue</button>
        </div>

        <div class="question" id="question2" style="display:none;">
            <p><strong>2. What’s my favorite thing about you?</strong></p>
            <button onclick="showQuestion(3)">Your eyes</button>
            <button onclick="showQuestion(3)">Your smile</button>
        </div>

        <div class="question" id="question3" style="display:none;">
            <p><strong>3. When is our special day?</strong></p>
            <button onclick="showQuestion(4)">December</button>
            <button onclick="showQuestion(4)">March</button>
        </div>

        <div class="question" id="question4" style="display:none;">
            <p><strong>4. Where did we go on our first date?</strong></p>
            <button onclick="showQuestion(5)">RocoMamas</button>
            <button onclick="showQuestion(5)">The Ferris Wheel</button>
        </div>

        <div class="question" id="question5" style="display:none;">
            <p><strong>5. What is my favorite memory with you?</strong></p>
            <button onclick="showFinalMessage()">The Ferris Wheel</button>
            <button onclick="showFinalMessage()">Our anniversary</button>
        </div>
    </div>

    <div id="final-message" style="display:none;">
        <h2>Congratulations!</h2>
        <p>You completed the quiz! ❤️</p>
        <p id="reward">🎟️ As a reward, you get an aquarium ticket! Enjoy the colorful fish and aquatic adventures! 🎉</p>
        <p>“Every love story is beautiful, but ours is my favorite.” 💖</p>
        <button onclick="resetQuiz()">Play Again</button>
    </div>

    <script>
        function showQuestion(questionNumber) {
            const questions = document.querySelectorAll('.question');
            questions.forEach(q => q.style.display = 'none'); // Hide all questions
            document.getElementById('question' + questionNumber).style.display = 'block'; // Show the current question
        }

        function showFinalMessage() {
            document.getElementById('quiz-container').style.display = 'none'; // Hide the quiz
            document.getElementById('final-message').style.display = 'block'; // Show final message
        }

        function resetQuiz() {
            document.getElementById('final-message').style.display = 'none'; // Hide final message
            showQuestion(1); // Start the quiz over
        }

        // Start the quiz by showing the first question
        showQuestion(1);
    </script>

</body>
</html>
