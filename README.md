# Fun.Webs

Fun websites- enjoy my friend

Random Jokes

HTML

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Random Jokes</title>
    <link rel="stylesheet" href="Fun1.css">
</head>
<body>
    <header>
        <h1>Random Jokes</h1>
    </header>
    <main>
        <div id="jokeDisplay">
            <p>Click the button to get a random joke:</p>
            <p id="jokeText"></p>
            <button id="jokeButton" onclick="getRandomJoke()">Get Joke</button>
        </div>
    </main>
    <footer>
        <p>&copy; 2023 Specter Website. All rights reserved.</p>
    </footer>
    <script src="Fun1.js"></script>
</body>
</html>

CSS

body {
    font-family: Arial, sans-serif;
    text-align: center;
    margin: 20px;
}

header {
    margin-bottom: 20px;
}

main {
    margin-bottom: 30px;
}

#jokeDisplay {
    padding: 20px;
    border: 2px solid #333;
    border-radius: 10px;
}

#jokeText {
    font-size: 18px;
    margin-bottom: 20px;
}

button {
    padding: 10px 20px;
    font-size: 16px;
    background-color: #007BFF;
    color: #fff;
    border: none;
    border-radius: 5px;
    cursor: pointer;
}

button:hover {
    background-color: #0056b3;
}

footer {
    background-color: #f0f0f0;
    padding: 10px;
}

JS

const jokes = [
    "Why don't scientists trust atoms? Because they make up everything!",
    "Why don't some couples go to the gym? Because some relationships don't work out!",
    "Did you hear about the mathematician who’s afraid of negative numbers? He’ll stop at nothing to avoid them!",
    "Why don't skeletons fight each other? They don't have the guts!",
    "Why did the scarecrow win an award? Because he was outstanding in his field!",
    "How do you organize a space party? You planet!",
    "Why was the math book sad? Because it had too many problems!",
    "Why did the tomato turn red? Because it saw the salad dressing!",
    "Why did the golfer bring two pairs of pants? In case he got a hole in one!",
    "Why do seagulls fly over the sea? Because if they flew over the bay, they’d be bagels!"
];

function getRandomJoke() {
    const jokeText = document.getElementById("jokeText");
    const randomIndex = Math.floor(Math.random() * jokes.length);
    jokeText.innerText = jokes[randomIndex];
}
