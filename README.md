<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Happy Birthday Aspar</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <div id="container">
        <div id="page1">
            <h1>Happy Birthday Aspar</h1>
            <button onclick="nextPage(2)">Next</button>
        </div>

        <div id="page2" class="hidden">
            <h2>Do you love me?</h2>
            <button onclick="nextPage(3)">Yes</button>
            <button onclick="nextPage(4)">No</button>
        </div>

        <div id="page3" class="hidden">
            <h2>Awww, I love you too Aspar ❤️</h2>
        </div>

        <div id="page4" class="hidden">
            <h2>Think more...</h2>
            <button onclick="nextPage(5)">Yes</button>
            <button onclick="nextPage(6)">No</button>
        </div>

        <div id="page5" class="hidden">
            <h2>Yay! You changed your mind ❤️</h2>
        </div>

        <div id="page6" class="hidden">
            <h2>Uh oh...</h2>
            <iframe width="560" height="315" src="https://www.youtube.com/embed/8gVU1hvL5uI?autoplay=1" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>
        </div>
    </div>

    <script src="script.js"></script>
</body>
</html>
body {
    font-family: Arial, sans-serif;
    text-align: center;
    background-color: #ffe6f2;
    margin: 0;
    padding: 0;
}

#container {
    margin-top: 100px;
}

h1, h2 {
    color: #ff1493;
}

button {
    background-color: #ff1493;
    color: white;
    border: none;
    padding: 10px 20px;
    margin: 10px;
    font-size: 18px;
    cursor: pointer;
    border-radius: 5px;
}

button:hover {
    background-color: #ff69b4;
}

.hidden {
    display: none;
}
function nextPage(pageNumber) {
    document.querySelectorAll('div').forEach(div => div.classList.add('hidden'));
    document.getElementById(`page${pageNumber}`).classList.remove('hidden');
}
