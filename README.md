# Valentine
Valentine 
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Be My Valentine?</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <div class="container">
        <div id="valentine-card">
            <img id="display-image" src="https://media.giphy.com/media/v1.Y2lkPTc5MGI3NjExOHp1eHByZzR0bmZ6bmZ6bmZ6bmZ6bmZ6bmZ6bmZ6bmZ6bmZ6JmVwPXYxX2ludGVybmFsX2dpZl9ieV9pZCZjdD1z/3ohzdIuqJoo8QdJJnm/giphy.gif" alt="Cute Cat">
            <h1 id="question">Chandan, will you be my valentine?</h1>
            <div class="buttons">
                <button id="yesBtn">Yes</button>
                <button id="noBtn">No</button>
            </div>
        </div>
    </div>
    <script src="script.js"></script>
</body>
</html>

body {
    background-color: #ffebee;
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
    margin: 0;
    font-family: 'Arial', sans-serif;
}

.container {
    text-align: center;
    background: white;
    padding: 50px;
    border-radius: 20px;
    box-shadow: 0 10px 25px rgba(0,0,0,0.1);
}

img {
    width: 150px;
    margin-bottom: 20px;
}

.buttons {
    margin-top: 20px;
    position: relative;
    height: 50px;
}

button {
    padding: 10px 25px;
    font-size: 18px;
    border-radius: 10px;
    border: none;
    cursor: pointer;
    transition: 0.3s;
}

#yesBtn {
    background-color: #ff4081;
    color: white;
}

#noBtn {
    background-color: #eeeeee;
    position: absolute;
}

const noBtn = document.getElementById('noBtn');
const yesBtn = document.getElementById('yesBtn');
const question = document.getElementById('question');
const image = document.getElementById('display-image');

// Make the No button run away
noBtn.addEventListener('mouseover', () => {
    const x = Math.random() * (window.innerWidth - noBtn.offsetWidth);
    const y = Math.random() * (window.innerHeight - noBtn.offsetHeight);
    
    noBtn.style.left = `${x}px`;
    noBtn.style.top = `${y}px`;
});

// What happens when they click Yes
yesBtn.addEventListener('click', () => {
    question.innerHTML = "YAY! See you then! 🎆";
    image.src = "https://media.giphy.com/media/v1.Y2lkPTc5MGI3NjExNHp1eHByZzR0bmZ6bmZ6bmZ6bmZ6bmZ6bmZ6bmZ6bmZ6bmZ6JmVwPXYxX2ludGVybmFsX2dpZl9ieV9pZCZjdD1z/l41lTfWxy9HHoXv6E/giphy.gif"; // Success GIF
    noBtn.style.display = 'none';
});


