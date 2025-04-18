DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Happy Birthday Zubia!</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <div class="container">
        <h1 class="title">Happy Birthday, Zubia!</h1>
        <p class="message">Wishing you a day filled with love, joy, and wonderful surprises!</p>
        <div class="balloons">
            <div class="balloon balloon1"></div>
            <div class="balloon balloon2"></div>
            <div class="balloon balloon3"></div>
            <div class="balloon balloon4"></div>
        </div>
        <button class="wish-button" onclick="showWish()">Click for a Special Wish!</button>
        <div class="wish" id="wish"></div>
    </div>
    <script src="script.js"></script>
</body>
</html>

body {
    background-color: #f0e68c;
    font-family: 'Arial', sans-serif;
    overflow: hidden;
    margin: 0;
    padding: 0;
}

.container {
    text-align: center;
    position: relative;
    padding: 50px;
}

.title {
    font-size: 3em;
    color: #ff6f61;
    animation: fadeIn 2s;
}

.message {
    font-size: 1.5em;
    color: #333;
    margin: 20px 0;
    animation: fadeIn 2s 0.5s;
}

.balloons {
    position: absolute;
    bottom: 0;
    left: 50%;
    transform: translateX(-50%);
}

.balloon {
    width: 50px;
    height: 80px;
    background-color: #ff6f61;
    border-radius: 25px 25px 0 0;
    position: relative;
    display: inline-block;
    margin: 0 10px;
    animation: float 3s infinite;
}

.balloon1 { background-color: #ff6f61; }
.balloon2 { background-color: #6fa3ff; }
.balloon3 { background-color: #ffcc5c; }
.balloon4 { background-color: #88d8b0; }.balloon:after {
    content: '';
    width: 10px;
    height: 10px;
    background-color: #333;
    border-radius: 50%;
    position: absolute;
    bottom: -10px;
    left: 50%;
    transform: translateX(-50%);
}

.wish-button {
    padding: 10px 20px;
    font-size: 1.2em;
    background-color: #ff6f61;
    color: white;
    border: none;
    border-radius: 5px;
    cursor: pointer;
    margin-top: 20px;
    animation: fadeIn 2s 1s;
}

.wish {
    margin-top: 20px;
    font-size: 1.5em;
    color: #333;
    display: none;
}

@keyframes float {
    0% { transform: translateY(0); }
    50% { transform: translateY(-20px); }
    100% { transform: translateY(0); }
}

@keyframes fadeIn {
    from { opacity: 0; }
    to { opacity: 1; }
}

function showWish() {
    const wishElement = document.getElementById('wish');
    wishElement.innerHTML = "May all your dreams come true! 🎉";
    wishElement.style.display = "block";
    wishElement.style.animation = "fadeIn 2s";
}
