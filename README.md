<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Happy Birthday Aspar</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      text-align: center;
      background-color: #f9f9f9;
      margin: 0;
      padding: 0;
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
      overflow: hidden;
    }
    .slide {
      display: none;
      width: 100%;
      height: 100%;
      position: absolute;
      top: 0;
      left: 0;
      justify-content: center;
      align-items: center;
      flex-direction: column;
    }
    .slide.active {
      display: flex;
    }
    h1, h2 {
      color: #333;
    }
    button {
      padding: 10px 20px;
      font-size: 16px;
      margin: 10px;
      cursor: pointer;
      border: none;
      background-color: #ff6f61;
      color: white;
      border-radius: 5px;
    }
    button:hover {
      background-color: #ff3b2f;
    }
  </style>
</head>
<body>
  <div class="slide active" id="slide1">
    <h1>Happy Birthday Aspar!</h1>
    <button onclick="nextSlide()">Next</button>
  </div>

  <div class="slide" id="slide2">
    <h2>Do you love me?</h2>
    <button onclick="showLoveMessage()">Yes</button>
    <button onclick="nextSlide()">No</button>
  </div>

  <div class="slide" id="slide3">
    <h2>Awww I love you too Aspar ❤️</h2>
  </div>

  <div class="slide" id="slide4">
    <h2>Think more... Yes or No?</h2>
    <button onclick="showLoveMessage()">Yes</button>
    <button onclick="nextSlide()">No</button>
  </div>

  <div class="slide" id="slide5">
    <h2>Okay, I'll wait until you say Yes 😊</h2>
  </div>

  <script>
    let currentSlide = 1;

    function nextSlide() {
      document.getElementById(`slide${currentSlide}`).classList.remove('active');
      currentSlide++;
      if (currentSlide > 5) currentSlide = 5; // Prevent going beyond the last slide
      document.getElementById(`slide${currentSlide}`).classList.add('active');
    }

    function showLoveMessage() {
      document.getElementById(`slide${currentSlide}`).classList.remove('active');
      currentSlide = 3; // Go to the "Awww I love you too" slide
      document.getElementById(`slide${currentSlide}`).classList.add('active');
    }
  </script>
</body>
</html>
