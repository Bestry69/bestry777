<!DOCTYPE html>
<html lang="th">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Mini Game by Gemini</title>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Kanit:wght@400;600&display=swap" rel="stylesheet">
    
    <style>
        /* --- การตั้งค่าโดยรวม --- */
        body {
            margin: 0;
            font-family: 'Kanit', sans-serif;
            overflow: hidden; /* ซ่อน scrollbar */
            color: #fff;
            text-align: center;
        }

        .page {
            width: 100vw;
            height: 100vh;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            position: absolute;
            top: 0;
            left: 0;
            transition: opacity 0.5s ease-in-out, transform 0.5s ease-in-out;
        }

        /* --- หน้าหลัก --- */
        #home {
            background: linear-gradient(45deg, #2c3e50, #3498db, #2980b9);
            background-size: 300% 300%;
            animation: gradient-animation 15s ease infinite;
            z-index: 2;
        }

        #home h1 {
            font-size: 4rem;
            text-shadow: 2px 2px 8px rgba(0,0,0,0.3);
            margin-bottom: 10px;
        }

        #home p {
            font-size: 1.2rem;
            margin-bottom: 30px;
        }

        .play-button {
            padding: 15px 40px;
            font-size: 1.5rem;
            font-family: 'Kanit', sans-serif;
            border: 2px solid #fff;
            border-radius: 50px;
            background-color: transparent;
            color: #fff;
            cursor: pointer;
            transition: all 0.3s ease;
            box-shadow: 0 4px 15px rgba(0,0,0,0.2);
        }

        .play-button:hover {
            background-color: #fff;
            color: #2c3e50;
            transform: translateY(-5px);
            box-shadow: 0 8px 20px rgba(0,0,0,0.3);
        }

        /* --- หน้าเกม --- */
        #game-page {
            background-color: #1a1a2e;
            opacity: 0;
            transform: translateY(100%);
            z-index: 1;
        }
        
        #game-container {
            width: 80%;
            max-width: 600px;
            height: 70vh;
            background-color: #16213e;
            border: 3px solid #0f3460;
            border-radius: 20px;
            position: relative;
            box-shadow: 0 0 20px rgba(224, 16, 105, 0.5);
            overflow: hidden;
        }

        #stats-bar {
            display: flex;
            justify-content: space-around;
            padding: 15px;
            font-size: 1.5rem;
            background-color: rgba(0,0,0,0.2);
        }

        #target {
            width: 60px;
            height: 60px;
            background-color: #e94560;
            border-radius: 50%;
            position: absolute;
            cursor: pointer;
            transition: all 0.1s ease-out;
            box-shadow: 0 0 15px #e94560, inset 0 0 10px rgba(255,255,255,0.5);
        }

        #target:hover {
            transform: scale(1.1);
        }
        
        #game-over-screen {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(26, 26, 46, 0.9);
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            opacity: 0;
            visibility: hidden;
            transition: opacity 0.4s ease;
        }

        #game-over-screen h2 {
            font-size: 3.5rem;
            color: #e94560;
        }

        #game-over-screen p {
            font-size: 1.8rem;
        }
        
        .hidden {
            display: none;
        }

        /* --- อนิเมชันพื้นหลัง --- */
        @keyframes gradient-animation {
            0% { background-position: 0% 50%; }
            50% { background-position: 100% 50%; }
            100% { background-position: 0% 50%; }
        }
    </style>
</head>
<body>

    <div id="home" class="page">
        <h1>ยินดีต้อนรับ</h1>
        <p>ทดสอบความไวของคุณในเกมคลิกเกอร์</p>
        <button id="startGameBtn" class="play-button">เริ่มเกม!</button>
    </div>

    <div id="game-page" class="page">
        <div id="stats-bar">
            <span>คะแนน: <span id="score">0</span></span>
            <span>เวลา: <span id="time">15</span></span>
        </div>
        <div id="game-container">
            <div id="target"></div>
            
            <div id="game-over-screen">
                <h2>หมดเวลา!</h2>
                <p>คะแนนสุดท้ายของคุณ: <span id="final-score">0</span></p>
                <button id="playAgainBtn" class="play-button">เล่นอีกครั้ง</button>
            </div>
        </div>
         <button id="backToHomeBtn" class="play-button" style="margin-top:20px; padding: 10px 25px; font-size: 1rem;">กลับหน้าหลัก</button>
    </div>

    <script>
        // --- ตัวแปรอ้างอิง Element ---
        const homePage = document.getElementById('home');
        const gamePage = document.getElementById('game-page');
        const startGameBtn = document.getElementById('startGameBtn');
        const playAgainBtn = document.getElementById('playAgainBtn');
        const backToHomeBtn = document.getElementById('backToHomeBtn');

        const scoreDisplay = document.getElementById('score');
        const timeDisplay = document.getElementById('time');
        const target = document.getElementById('target');
        const gameContainer = document.getElementById('game-container');
        
        const gameOverScreen = document.getElementById('game-over-screen');
        const finalScoreDisplay = document.getElementById('final-score');

        // --- ตัวแปรสำหรับเกม ---
        let score = 0;
        let timeLeft = 15;
        let timerId = null;

        // --- ฟังก์ชันสลับหน้า ---
        function showGamePage() {
            homePage.style.opacity = '0';
            homePage.style.transform = 'translateY(-100%)';
            gamePage.style.opacity = '1';
            gamePage.style.transform = 'translateY(0)';
            startGame();
        }

        function showHomePage() {
            gamePage.style.opacity = '0';
            gamePage.style.transform = 'translateY(100%)';
            homePage.style.opacity = '1';
            homePage.style.transform = 'translateY(0)';
        }

        // --- ฟังก์ชันหลักของเกม ---
        function startGame() {
            // รีเซ็ตค่าเริ่มต้น
            score = 0;
            timeLeft = 15;
            scoreDisplay.textContent = score;
            timeDisplay.textContent = timeLeft;
            
            // ซ่อนหน้าจอ Game Over
            gameOverScreen.style.opacity = '0';
            gameOverScreen.style.visibility = 'hidden';
            target.style.display = 'block';

            moveTarget();

            // เริ่มนับเวลาถอยหลัง
            timerId = setInterval(updateTimer, 1000);
        }

        function updateTimer() {
            timeLeft--;
            timeDisplay.textContent = timeLeft;
            if (timeLeft === 0) {
                endGame();
            }
        }

        function endGame() {
            clearInterval(timerId); // หยุดนับเวลา
            target.style.display = 'none'; // ซ่อนเป้า
            finalScoreDisplay.textContent = score;
            gameOverScreen.style.opacity = '1';
            gameOverScreen.style.visibility = 'visible';
        }

        function moveTarget() {
            const containerWidth = gameContainer.clientWidth;
            const containerHeight = gameContainer.clientHeight;
            const targetSize = target.clientWidth;

            const randomX = Math.floor(Math.random() * (containerWidth - targetSize));
            const randomY = Math.floor(Math.random() * (containerHeight - targetSize));

            target.style.left = `${randomX}px`;
            target.style.top = `${randomY}px`;
        }

        function onTargetClick() {
            if (timeLeft > 0) {
                score++;
                scoreDisplay.textContent = score;
                moveTarget();
            }
        }

        // --- การผูก Event Listener ---
        startGameBtn.addEventListener('click', showGamePage);
        playAgainBtn.addEventListener('click', startGame);
        backToHomeBtn.addEventListener('click', showHomePage);
        target.addEventListener('click', onTargetClick);

    </script>
</body>
</html>
