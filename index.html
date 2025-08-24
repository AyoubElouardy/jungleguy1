# jungleguy1
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Jungle Adventure - Enhanced 3D Pixel Edition</title>
    <script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            image-rendering: pixelated;
        }
        
        body {
            background: linear-gradient(to bottom, #1a5f7a, #159895);
            min-height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            color: white;
            overflow: hidden;
        }
        
        #game-container {
            width: 900px;
            max-width: 95%;
            position: relative;
        }
        
        #game-canvas {
            background: #2a7a52;
            border: 4px solid #2C394B;
            border-radius: 10px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.4);
            display: block;
            margin: 0 auto;
        }
        
        #ui-container {
            display: flex;
            justify-content: space-between;
            padding: 10px 20px;
            background: rgba(44, 57, 75, 0.8);
            border-radius: 10px;
            margin-bottom: 10px;
            font-size: 20px;
            font-weight: bold;
            text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.5);
        }
        
        #level-display { color: #FFD700; }
        #timer { color: #FF5722; }
        #score { color: #4CAF50; }
        #lives { color: #FF5252; }
        #powerup-timer { color: #9C27B0; }
        #boss-health { color: #FF5252; display: none; }
        
        #boss-health-bar {
            width: 200px;
            height: 15px;
            background: #444;
            border-radius: 10px;
            overflow: hidden;
            margin-left: 10px;
        }
        
        #boss-health-fill {
            height: 100%;
            background: linear-gradient(to right, #FF5252, #FF0000);
            width: 100%;
            transition: width 0.3s;
        }
        
        #start-screen, #level-complete, #game-over, #leaderboard, #boss-intro {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(28, 40, 54, 0.95);
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            border-radius: 10px;
            text-align: center;
            padding: 20px;
            z-index: 10;
        }
        
        #boss-intro { background: rgba(0, 0, 0, 0.9); }
        #leaderboard { display: none; }
        
        h1 {
            font-size: 48px;
            color: #FFD700;
            text-shadow: 3px 3px 0 #FF5722;
            margin-bottom: 20px;
        }
        
        h2 {
            font-size: 36px;
            color: #4CAF50;
            margin-bottom: 20px;
        }
        
        p {
            font-size: 20px;
            margin-bottom: 15px;
            max-width: 80%;
        }
        
        button {
            background: #FF5722;
            color: white;
            border: none;
            padding: 15px 40px;
            font-size: 20px;
            border-radius: 50px;
            cursor: pointer;
            box-shadow: 0 4px 0 #D84315;
            transition: all 0.2s;
            margin-top: 20px;
            font-weight: bold;
        }
        
        button:hover {
            background: #FF7043;
            transform: translateY(-2px);
            box-shadow: 0 6px 0 #D84315;
        }
        
        button:active {
            transform: translateY(2px);
            box-shadow: 0 2px 0 #D84315;
        }
        
        .instructions {
            background: rgba(255, 255, 255, 0.1);
            padding: 20px;
            border-radius: 10px;
            margin: 20px 0;
            text-align: center;
            max-width: 80%;
        }
        
        .key {
            display: inline-block;
            background: rgba(255, 255, 255, 0.2);
            padding: 5px 10px;
            border-radius: 5px;
            margin: 0 5px;
            font-weight: bold;
        }
        
        #leaderboard-list {
            list-style-type: none;
            width: 80%;
            margin: 20px 0;
            max-height: 200px;
            overflow-y: auto;
            background: rgba(255, 255, 255, 0.1);
            border-radius: 10px;
            padding: 10px;
        }
        
        #leaderboard-list li {
            padding: 10px;
            border-bottom: 1px solid rgba(255, 255, 255, 0.2);
            display: flex;
            justify-content: space-between;
        }
        
        #leaderboard-list li:first-child {
            color: #FFD700;
            font-weight: bold;
            font-size: 1.2em;
        }
        
        #name-input {
            background: rgba(255, 255, 255, 0.2);
            border: 2px solid #FF5722;
            border-radius: 50px;
            padding: 12px 20px;
            color: white;
            font-size: 18px;
            text-align: center;
            margin-top: 10px;
            width: 250px;
        }
        
        #name-input::placeholder {
            color: rgba(255, 255, 255, 0.7);
        }
        
        .powerup-active {
            animation: glow 0.5s infinite alternate;
        }
        
        @keyframes glow {
            from { box-shadow: 0 0 5px #fff, 0 0 10px #fff, 0 0 15px #9C27B0, 0 0 20px #9C27B0; }
            to { box-shadow: 0 0 10px #fff, 0 0 20px #fff, 0 0 30px #9C27B0, 0 0 40px #9C27B0; }
        }
        
        .coin-counter {
            position: absolute;
            top: 10px;
            right: 10px;
            background: rgba(0, 0, 0, 0.5);
            padding: 5px 10px;
            border-radius: 20px;
            font-size: 16px;
            color: #FFD700;
        }
        
        .boss-title {
            font-size: 60px;
            color: #FF0000;
            text-shadow: 0 0 10px #FF9800;
            animation: bossPulse 2s infinite;
        }
        
        @keyframes bossPulse {
            0% { transform: scale(1); }
            50% { transform: scale(1.1); }
            100% { transform: scale(1); }
        }
        
        .pixel-art {
            image-rendering: pixelated;
        }
        
        #stats-canvas {
            max-width: 100%;
            margin-top: 20px;
        }
    </style>
</head>
<body>
    <div id="game-container">
        <div id="ui-container">
            <div>Level: <span id="level-display">1</span></div>
            <div>Time: <span id="timer">00:00</span></div>
            <div>Score: <span id="score">0</span></div>
            <div>Lives: <span id="lives">3</span></div>
            <div>Powerup: <span id="powerup-timer">0s</span></div>
            <div id="boss-health">Boss: 
                <div id="boss-health-bar">
                    <div id="boss-health-fill"></div>
                </div>
            </div>
        </div>
        
        <canvas id="game-canvas" width="900" height="500"></canvas>
        <div class="coin-counter">Coins until extra life: <span id="coins-to-life">50</span></div>
        
        <div id="start-screen">
            <h1>Jungle Adventure - Enhanced</h1>
            <div class="instructions">
                <p>Help Alex escape the perilous jungle!</p>
                <p>Use <span class="key">←</span> <span class="key">→</span> or <span class="key">A</span> <span class="key">D</span> to move</p>
                <p>Use <span class="key">Space</span> or <span class="key">W</span> to jump</p>
                <p>Climb vines with <span class="key">↑</span> or <span class="key">W</span></p>
                <p>Collect coins and bananas for super speed!</p>
                <p>Watch out for crocodiles and breakable platforms!</p>
                <p>Defeat the bear boss in the final level!</p>
            </div>
            <button id="start-button">Start Game</button>
        </div>
        
        <div id="level-complete" style="display: none;">
            <h2>Level Complete!</h2>
            <p>Your time: <span id="level-time">00:00</span></p>
            <p>Total score: <span id="total-score">0</span></p>
            <button id="next-level">Next Level</button>
        </div>
        
        <div id="game-over" style="display: none;">
            <h2>Game Over</h2>
            <p>You were caught by crocodiles!</p>
            <p>Final score: <span id="final-score">0</span></p>
            <button id="restart-button">Play Again</button>
        </div>
        
        <div id="boss-intro" style="display: none;">
            <h1 class="boss-title">BOSS BATTLE</h1>
            <h2>Defeat the Giant Bear!</h2>
            <p>Jump on the bear's head to damage it!</p>
            <p>Dodge its powerful attacks!</p>
            <button id="start-boss">Start Battle</button>
        </div>
        
        <div id="leaderboard">
            <h2>Leaderboard</h2>
            <p>Fastest completions:</p>
            <ul id="leaderboard-list">
                <li>Loading...</li>
            </ul>
            <canvas id="stats-canvas" width="600" height="300"></canvas>
            <input type="text" id="name-input" placeholder="Enter your name">
            <button id="submit-score">Submit Score</button>
        </div>
    </div>

    <script>
        // Game variables
        const canvas = document.getElementById('game-canvas');
        const ctx = canvas.getContext('2d');
        const scoreElement = document.getElementById('score');
        const livesElement = document.getElementById('lives');
        const levelDisplay = document.getElementById('level-display');
        const timerElement = document.getElementById('timer');
        const powerupTimerElement = document.getElementById('powerup-timer');
        const coinsToLifeElement = document.getElementById('coins-to-life');
        const bossHealthElement = document.getElementById('boss-health');
        const bossHealthFill = document.getElementById('boss-health-fill');
        const startScreen = document.getElementById('start-screen');
        const levelCompleteScreen = document.getElementById('level-complete');
        const gameOverScreen = document.getElementById('game-over');
        const bossIntroScreen = document.getElementById('boss-intro');
        const leaderboardScreen = document.getElementById('leaderboard');
        const startButton = document.getElementById('start-button');
        const nextLevelButton = document.getElementById('next-level');
        const restartButton = document.getElementById('restart-button');
        const startBossButton = document.getElementById('start-boss');
        const submitScoreButton = document.getElementById('submit-score');
        const nameInput = document.getElementById('name-input');
        const leaderboardList = document.getElementById('leaderboard-list');
        const levelTimeElement = document.getElementById('level-time');
        const totalScoreElement = document.getElementById('total-score');
        const finalScoreElement = document.getElementById('final-score');
        const statsCanvas = document.getElementById('stats-canvas');
        
        // Game state
        let gameRunning = false;
        let currentLevel = 1;
        let score = 0;
        let lives = 3;
        let levelTime = 0;
        let totalTime = 0;
        let timerInterval;
        let playerName = "Player";
        let coinsCollected = 0;
        let powerupActive = false;
        let powerupTimeLeft = 0;
        let powerupEffect = null;
        let levelScores = [0, 0, 0, 0, 0]; // Track scores per level
        let parallaxOffset = 0;
        let particles = [];
        
        // Player properties
        const player = {
            x: 50,
            y: 400,
            width: 35,
            height: 55,
            speed: 5,
            jumpForce: 12,
            velocityY: 0,
            jumping: false,
            direction: 1,
            frame: 0,
            frameCounter: 0,
            onVine: false,
            vineClimbSpeed: 4
        };
        
        // Boss properties
        const boss = {
            x: 700,
            y: 380,
            width: 120,
            height: 100,
            speed: 2.5,
            direction: -1,
            health: 100,
            maxHealth: 100,
            attackCooldown: 0,
            jumpCooldown: 0,
            isAttacking: false,
            attackType: null,
            attackTimer: 0,
            projectiles: []
        };
        
        // Game objects
        let platforms = [];
        let coins = [];
        let bananas = [];
        let crocodiles = [];
        let trees = [];
        let rocks = [];
        let vines = [];
        let levelGoal = { x: 0, y: 0, width: 40, height: 40 };
        let waterAreas = [];
        
        // Key states
        const keys = {};
        
        // Leaderboard data
        let leaderboard = [];
        
        // Textures and images
        const textures = {
            player: [], // Array for animated sprites
            crocodile: [],
            boss: [],
            grass: createGrassTexture(),
            tree: createTreeTexture(),
            water: createWaterTexture(),
            rock: createRockTexture(),
            jungleBgFar: createJungleBackgroundFar(),
            jungleBgMid: createJungleBackgroundMid(),
            jungleBgNear: createJungleBackgroundNear(),
            coin: createCoinTexture(),
            banana: createBananaTexture(),
            goal: createGoalTexture(),
            projectile: createProjectileTexture(),
            vine: createVineTexture()
        };
        
        // Create texture functions
        function createPlayerTexture() {
            const frames = [];
            for (let i = 0; i < 4; i++) {
                const canvas = document.createElement('canvas');
                canvas.width = 35;
                canvas.height = 55;
                const ctx = canvas.getContext('2d');
                
                // Base color with more detail
                ctx.fillStyle = '#3564FC';
                ctx.fillRect(5, 15, 25, 30); // Body
                
                // Head
                ctx.fillStyle = '#F4D47C';
                ctx.fillRect(10, 5, 15, 15);
                
                // Eyes
                ctx.fillStyle = 'white';
                ctx.fillRect(15 + (i % 2), 10, 3, 3);
                ctx.fillRect(22 + (i % 2), 10, 3, 3);
                
                // Pants
                ctx.fillStyle = '#294ECC';
                ctx.fillRect(5, 40, 25, 10);
                
                // Arms and legs (animation)
                ctx.fillStyle = '#3564FC';
                const armOffset = i % 2 === 0 ? 0 : 2;
                ctx.fillRect(2, 20 + armOffset, 5, 15); // Left arm
                ctx.fillRect(28, 20 - armOffset, 5, 15); // Right arm
                ctx.fillRect(10 + (i % 2), 45, 5, 10); // Left leg
                ctx.fillRect(20 - (i % 2), 45, 5, 10); // Right leg
                
                // Shading
                ctx.fillStyle = 'rgba(0, 0, 0, 0.3)';
                ctx.fillRect(5, 15, 5, 30);
                ctx.fillRect(30, 15, 5, 30);
                
                // Highlights
                ctx.fillStyle = 'rgba(255, 255, 255, 0.3)';
                ctx.fillRect(10, 15, 3, 30);
                
                // Hat for detail
                ctx.fillStyle = '#FF5722';
                ctx.fillRect(8, 2, 19, 5);
                
                frames.push(canvas);
            }
            return frames;
        }
        
        function createCrocodileTexture() {
            const frames = [];
            for (let i = 0; i < 2; i++) {
                const canvas = document.createElement('canvas');
                canvas.width = 60;
                canvas.height = 30;
                const ctx = canvas.getContext('2d');
                
                ctx.fillStyle = '#4CAF50';
                ctx.fillRect(5, 10, 50, 15); // Body
                ctx.fillRect(0, 5, 15, 20); // Head
                ctx.fillRect(50, 5, 10, 20); // Tail
                
                // Eyes
                ctx.fillStyle = 'white';
                ctx.fillRect(5 + (i % 2), 8, 5, 5);
                ctx.fillStyle = 'black';
                ctx.fillRect(7 + (i % 2), 10, 2, 2);
                
                // Teeth
                ctx.fillStyle = 'white';
                for (let j = 0; j < 3; j++) {
                    ctx.fillRect(12 + j*5, 20 + (i % 2), 3, 5);
                }
                
                // Scales
                ctx.fillStyle = '#3E8E41';
                for (let j = 0; j < 8; j++) {
                    ctx.fillRect(10 + j*5, 12 + (i % 2), 3, 3);
                }
                
                // Shading
                ctx.fillStyle = 'rgba(0, 0, 0, 0.3)';
                ctx.fillRect(5, 10, 3, 15);
                
                // Highlights
                ctx.fillStyle = 'rgba(255, 255, 255, 0.3)';
                ctx.fillRect(10, 10, 2, 15);
                
                frames.push(canvas);
            }
            return frames;
        }
        
        function createBossTexture() {
            const frames = [];
            for (let i = 0; i < 2; i++) {
                const canvas = document.createElement('canvas');
                canvas.width = 120;
                canvas.height = 100;
                const ctx = canvas.getContext('2d');
                
                ctx.fillStyle = '#8B4513';
                ctx.fillRect(30, 40, 60, 40); // Body
                ctx.fillRect(40, 10, 40, 40); // Head
                ctx.fillRect(20, 40, 15, 20); // Left arm
                ctx.fillRect(85, 40, 15, 20); // Right arm
                ctx.fillRect(40, 80, 20, 20); // Left leg
                ctx.fillRect(60, 80, 20, 20); // Right leg
                
                // Ears
                ctx.fillStyle = '#6B3410';
                ctx.fillRect(35, 5, 10, 10);
                ctx.fillRect(75, 5, 10, 10);
                
                // Eyes
                ctx.fillStyle = 'red';
                ctx.fillRect(50 + (i % 2), 25, 5, 5);
                ctx.fillRect(65 + (i % 2), 25, 5, 5);
                
                // Nose
                ctx.fillStyle = 'black';
                ctx.fillRect(55, 35, 10, 5);
                
                // Mouth
                ctx.strokeStyle = 'black';
                ctx.lineWidth = 2;
                ctx.beginPath();
                ctx.moveTo(50, 45 + (i % 2));
                ctx.lineTo(70, 45 + (i % 2));
                ctx.stroke();
                
                // Claws
                ctx.fillStyle = 'white';
                for (let j = 0; j < 3; j++) {
                    ctx.fillRect(20, 55 + j*3, 3, 5);
                    ctx.fillRect(97, 55 + j*3, 3, 5);
                }
                
                // Fur
                ctx.fillStyle = '#6B3410';
                for (let j = 0; j < 5; j++) {
                    ctx.fillRect(35 + j*10, 15 + (i % 2), 5, 3);
                }
                
                // Shading
                ctx.fillStyle = 'rgba(0, 0, 0, 0.3)';
                ctx.fillRect(30, 40, 5, 40);
                
                // Highlights
                ctx.fillStyle = 'rgba(255, 255, 255, 0.3)';
                ctx.fillRect(85, 40, 5, 40);
                
                frames.push(canvas);
            }
            return frames;
        }
        
        function createGrassTexture() {
            const canvas = document.createElement('canvas');
            canvas.width = 50;
            canvas.height = 50;
            const ctx = canvas.getContext('2d');
            
            ctx.fillStyle = '#7CB342';
            ctx.fillRect(0, 0, 50, 50);
            
            // Grass blades
            ctx.fillStyle = '#5D8C2B';
            for (let i = 0; i < 30; i++) {
                const x = Math.random() * 50;
                const height = 8 + Math.random() * 12;
                ctx.fillRect(x, 50 - height, 3, height);
            }
            
            // Dirt
            ctx.fillStyle = '#5D4037';
            for (let i = 0; i < 15; i++) {
                const x = Math.random() * 50;
                const y = Math.random() * 50;
                ctx.fillRect(x, y, 3, 3);
            }
            
            return canvas;
        }
        
        function createTreeTexture() {
            const canvas = document.createElement('canvas');
            canvas.width = 80;
            canvas.height = 120;
            const ctx = canvas.getContext('2d');
            
            // Trunk
            ctx.fillStyle = '#8B4513';
            ctx.fillRect(35, 40, 10, 80);
            
            // Leaves
            ctx.fillStyle = '#2E8B57';
            ctx.fillRect(10, 5, 60, 40); // Bottom layer
            ctx.fillRect(20, 15, 40, 30); // Middle layer
            ctx.fillRect(30, 25, 20, 20); // Top layer
            
            // Shading
            ctx.fillStyle = 'rgba(0, 0, 0, 0.3)';
            ctx.fillRect(10, 5, 10, 40);
            
            // Highlights
            ctx.fillStyle = 'rgba(255, 255, 255, 0.3)';
            ctx.fillRect(60, 5, 10, 40);
            
            return canvas;
        }
        
        function createWaterTexture() {
            const canvas = document.createElement('canvas');
            canvas.width = 50;
            canvas.height = 50;
            const ctx = canvas.getContext('2d');
            
            ctx.fillStyle = '#1E90FF';
            ctx.fillRect(0, 0, 50, 50);
            
            // Waves
            ctx.fillStyle = 'rgba(255, 255, 255, 0.5)';
            for (let i = 0; i < 6; i++) {
                const y = 10 + i * 8;
                for (let x = 0; x < 50; x += 6) {
                    ctx.fillRect(x, y + Math.sin((x + Date.now() / 1000) / 10) * 3, 4, 2);
                }
            }
            
            return canvas;
        }
        
        function createRockTexture() {
            const canvas = document.createElement('canvas');
            canvas.width = 50;
            canvas.height = 50;
            const ctx = canvas.getContext('2d');
            
            ctx.fillStyle = '#708090';
            ctx.fillRect(5, 5, 40, 40);
            
            // Details
            ctx.fillStyle = '#5A6672';
            for (let i = 0; i < 12; i++) {
                const x = 10 + Math.random() * 30;
                const y = 10 + Math.random() * 30;
                ctx.fillRect(x, y, 3, 3);
            }
            
            // Shading
            ctx.fillStyle = 'rgba(0, 0, 0, 0.3)';
            ctx.fillRect(5, 5, 5, 40);
            
            return canvas;
        }
        
        function createJungleBackgroundFar() {
            const canvas = document.createElement('canvas');
            canvas.width = 900;
            canvas.height = 500;
            const ctx = canvas.getContext('2d');
            
            // Sky
            const skyGradient = ctx.createLinearGradient(0, 0, 0, 300);
            skyGradient.addColorStop(0, '#87CEEB');
            skyGradient.addColorStop(1, '#98FB98');
            ctx.fillStyle = skyGradient;
            ctx.fillRect(0, 0, 900, 300);
            
            // Mountains
            ctx.fillStyle = '#2F4F4F';
            for (let i = 0; i < 18; i++) {
                const x = i * 50;
                const height = 80 + Math.random() * 100;
                ctx.fillRect(x, 300 - height, 50, height);
            }
            
            return canvas;
        }
        
        function createJungleBackgroundMid() {
            const canvas = document.createElement('canvas');
            canvas.width = 900;
            canvas.height = 500;
            const ctx = canvas.getContext('2d');
            
            // Mid-layer trees
            ctx.fillStyle = '#006400';
            for (let i = 0; i < 20; i++) {
                const x = Math.random() * 900;
                const height = 100 + Math.random() * 120;
                ctx.fillRect(x, 300 - height, 40, height);
            }
            
            return canvas;
        }
        
        function createJungleBackgroundNear() {
            const canvas = document.createElement('canvas');
            canvas.width = 900;
            canvas.height = 500;
            const ctx = canvas.getContext('2d');
            
            // Near-layer foliage
            ctx.fillStyle = '#228B22';
            for (let i = 0; i < 15; i++) {
                const x = Math.random() * 900;
                const height = 120 + Math.random() * 80;
                ctx.fillRect(x, 300 - height, 50, height);
            }
            
            return canvas;
        }
        
        function createCoinTexture() {
            const canvas = document.createElement('canvas');
            canvas.width = 20;
            canvas.height = 20;
            const ctx = canvas.getContext('2d');
            
            ctx.fillStyle = '#FFD700';
            ctx.fillRect(2, 2, 16, 16);
            
            // Shine
            ctx.fillStyle = '#FFFF00';
            ctx.fillRect(5, 5, 10, 10);
            
            // Highlight
            ctx.fillStyle = 'rgba(255, 255, 255, 0.8)';
            ctx.fillRect(7, 7, 5, 5);
            
            return canvas;
        }
        
        function createBananaTexture() {
            const canvas = document.createElement('canvas');
            canvas.width = 25;
            canvas.height = 35;
            const ctx = canvas.getContext('2d');
            
            ctx.fillStyle = '#FFEB3B';
            ctx.fillRect(5, 5, 15, 25);
            
            // Stem
            ctx.fillStyle = '#8BC34A';
            ctx.fillRect(20, 5, 5, 8);
            
            // Shading
            ctx.fillStyle = 'rgba(0, 0, 0, 0.3)';
            ctx.fillRect(5, 5, 3, 25);
            
            return canvas;
        }
        
        function createGoalTexture() {
            const canvas = document.createElement('canvas');
            canvas.width = 40;
            canvas.height = 40;
            const ctx = canvas.getContext('2d');
            
            ctx.fillStyle = '#FF5722';
            ctx.fillRect(5, 5, 30, 30);
            
            // Flag pole
            ctx.fillStyle = '#795548';
            ctx.fillRect(15, 5, 5, 30);
            
            // Flag
            ctx.fillStyle = '#FFD700';
            ctx.fillRect(5, 5, 15, 15);
            
            return canvas;
        }
        
        function createProjectileTexture() {
            const canvas = document.createElement('canvas');
            canvas.width = 15;
            canvas.height = 15;
            const ctx = canvas.getContext('2d');
            
            ctx.fillStyle = '#708090';
            ctx.fillRect(3, 3, 9, 9);
            
            // Shading
            ctx.fillStyle = 'rgba(0, 0, 0, 0.3)';
            ctx.fillRect(3, 3, 3, 9);
            
            return canvas;
        }
        
        function createVineTexture() {
            const canvas = document.createElement('canvas');
            canvas.width = 20;
            canvas.height = 100;
            const ctx = canvas.getContext('2d');
            
            ctx.fillStyle = '#4B2E0B';
            ctx.fillRect(8, 0, 4, 100);
            
            // Leaves
            ctx.fillStyle = '#2E8B57';
            for (let i = 0; i < 5; i++) {
                ctx.fillRect(0, 10 + i * 20, 8, 8);
                ctx.fillRect(12, 15 + i * 20, 8, 8);
            }
            
            return canvas;
        }
        
        // Initialize textures
        textures.player = createPlayerTexture();
        textures.crocodile = createCrocodileTexture();
        textures.boss = createBossTexture();
        
        // Particle system
        function createParticle(x, y, color) {
            return {
                x: x,
                y: y,
                vx: (Math.random() - 0.5) * 4,
                vy: (Math.random() - 0.5) * 4,
                size: 5 + Math.random() * 5,
                life: 20,
                color: color
            };
        }
        
        function updateParticles() {
            particles = particles.filter(p => p.life > 0);
            particles.forEach(p => {
                p.x += p.vx;
                p.y += p.vy;
                p.life--;
                p.size *= 0.95;
            });
        }
        
        function renderParticles() {
            particles.forEach(p => {
                ctx.fillStyle = p.color;
                ctx.fillRect(p.x, p.y, p.size, p.size);
            });
        }
        
        // Event listeners
        window.addEventListener('keydown', (e) => {
            keys[e.key] = true;
            if (e.key === 'a' || e.key === 'A') keys['ArrowLeft'] = true;
            if (e.key === 'd' || e.key === 'D') keys['ArrowRight'] = true;
            if (e.key === 'w' || e.key === 'W') keys['ArrowUp'] = true;
            if (e.key === ' ') keys['ArrowUp'] = true;
        });
        
        window.addEventListener('keyup', (e) => {
            keys[e.key] = false;
            if (e.key === 'a' || e.key === 'A') keys['ArrowLeft'] = false;
            if (e.key === 'd' || e.key === 'D') keys['ArrowRight'] = false;
            if (e.key === 'w' || e.key === 'W') keys['ArrowUp'] = false;
            if (e.key === ' ') keys['ArrowUp'] = false;
        });
        
        startButton.addEventListener('click', startGame);
        nextLevelButton.addEventListener('click', loadNextLevel);
        restartButton.addEventListener('click', restartGame);
        startBossButton.addEventListener('click', startBossBattle);
        submitScoreButton.addEventListener('click', submitScore);
        
        // Chart.js for stats
        let statsChart;
        function updateStatsChart() {
            if (statsChart) statsChart.destroy();
            statsChart = new Chart(statsCanvas, {
                type: 'bar',
                data: {
                    labels: ['Level 1', 'Level 2', 'Level 3', 'Level 4', 'Boss'],
                    datasets: [{
                        label: 'Score per Level',
                        data: levelScores,
                        backgroundColor: 'rgba(76, 175, 80, 0.7)',
                        borderColor: '#4CAF50',
                        borderWidth: 2
                    }]
                },
                options: {
                    scales: {
                        y: { beginAtZero: true, title: { display: true, text: 'Score' } },
                        x: { title: { display: true, text: 'Level' } }
                    },
                    plugins: {
                        legend: { display: true },
                        title: { display: true, text: 'Your Performance' }
                    }
                }
            });
        }
        
        // Leaderboard
        function loadLeaderboard() {
            const savedLeaderboard = localStorage.getItem('jungleLeaderboard');
            if (savedLeaderboard) {
                leaderboard = JSON.parse(savedLeaderboard);
            } else {
                leaderboard = [
                    { name: "Jungle Master", time: 120, score: 3000 },
                    { name: "Croc Hunter", time: 180, score: 2500 },
                    { name: "Adventurer", time: 240, score: 2000 },
                    { name: "Explorer", time: 300, score: 1500 },
                    { name: "Beginner", time: 360, score: 1000 }
                ];
            }
            updateLeaderboardDisplay();
        }
        
        function updateLeaderboardDisplay() {
            leaderboardList.innerHTML = '';
            leaderboard.sort((a, b) => a.time - b.time).forEach(entry => {
                const li = document.createElement('li');
                const minutes = Math.floor(entry.time / 60);
                const seconds = entry.time % 60;
                li.innerHTML = `${entry.name} - ${minutes.toString().padStart(2, '0')}:${seconds.toString().padStart(2, '0')} - ${entry.score} pts`;
                leaderboardList.appendChild(li);
            });
        }
        
        function startGame() {
            loadLeaderboard();
            startScreen.style.display = 'none';
            currentLevel = 1;
            score = 0;
            lives = 3;
            coinsCollected = 0;
            totalTime = 0;
            levelScores = [0, 0, 0, 0, 0];
            updateCoinsToLife();
            loadLevel(currentLevel);
        }
        
        function loadLevel(level) {
            if (level === 5) {
                bossIntroScreen.style.display = 'flex';
                return;
            }
            
            const config = levelConfigs[level - 1];
            platforms = JSON.parse(JSON.stringify(config.platforms));
            coins = JSON.parse(JSON.stringify(config.coins));
            bananas = JSON.parse(JSON.stringify(config.bananas));
            crocodiles = JSON.parse(JSON.stringify(config.crocodiles));
            trees = JSON.parse(JSON.stringify(config.trees || []));
            rocks = JSON.parse(JSON.stringify(config.rocks || []));
            vines = JSON.parse(JSON.stringify(config.vines || []));
            levelGoal = JSON.parse(JSON.stringify(config.goal));
            waterAreas = JSON.parse(JSON.stringify(config.waterAreas));
            
            // Initialize breakable platforms
            platforms.forEach(p => {
                p.breakTimer = p.breakable ? 120 : null;
            });
            
            // Initialize crocodiles
            crocodiles.forEach(croc => {
                croc.initialX = croc.x;
                croc.emergeTimer = Math.random() * 60;
            });
            
            // Reset player
            player.x = 50;
            player.y = 400;
            player.velocityY = 0;
            player.jumping = false;
            player.speed = 5;
            player.frame = 0;
            player.frameCounter = 0;
            player.onVine = false;
            
            // Reset powerup
            powerupActive = false;
            powerupTimeLeft = 0;
            powerupEffect = null;
            powerupTimerElement.textContent = "0s";
            document.getElementById('game-container').classList.remove('powerup-active');
            
            // Hide boss health
            bossHealthElement.style.display = 'none';
            
            // Update UI
            levelDisplay.textContent = level;
            updateScore();
            updateLives();
            
            // Start timer
            levelTime = 0;
            clearInterval(timerInterval);
            timerInterval = setInterval(() => {
                levelTime++;
                totalTime++;
                updateTimer();
                
                if (powerupActive) {
                    powerupTimeLeft--;
                    powerupTimerElement.textContent = `${powerupTimeLeft}s`;
                    if (powerupTimeLeft <= 0) {
                        endPowerup();
                    }
                }
                
                updateCrocodiles();
            }, 1000);
            
            gameRunning = true;
            gameLoop();
        }
        
        function startBossBattle() {
            bossIntroScreen.style.display = 'none';
            
            platforms = [
                { x: 0, y: 460, width: 900, height: 40, breakable: false },
                { x: 200, y: 350, width: 100, height: 20, breakable: true },
                { x: 400, y: 350, width: 100, height: 20, breakable: true },
                { x: 600, y: 350, width: 100, height: 20, breakable: true }
            ];
            
            coins = [];
            bananas = [];
            crocodiles = [];
            trees = [];
            rocks = [];
            vines = [];
            waterAreas = [];
            
            // Reset boss
            boss.health = boss.maxHealth;
            boss.x = 700;
            boss.y = 380;
            boss.direction = -1;
            boss.attackCooldown = 0;
            boss.jumpCooldown = 0;
            boss.isAttacking = false;
            boss.attackType = null;
            boss.attackTimer = 0;
            boss.projectiles = [];
            
            // Reset player
            player.x = 100;
            player.y = 400;
            player.velocityY = 0;
            player.jumping = false;
            player.speed = 5;
            player.frame = 0;
            player.frameCounter = 0;
            player.onVine = false;
            
            // Show boss health
            bossHealthElement.style.display = 'flex';
            updateBossHealth();
            
            levelDisplay.textContent = 5;
            
            // Start timer
            levelTime = 0;
            clearInterval(timerInterval);
            timerInterval = setInterval(() => {
                levelTime++;
                totalTime++;
                updateTimer();
                updateBoss();
            }, 1000);
            
            gameRunning = true;
            gameLoop();
        }
        
        function updateBoss() {
            boss.x += boss.speed * boss.direction;
            if (boss.x <= 200 || boss.x + boss.width >= 850) {
                boss.direction *= -1;
            }
            
            if (boss.attackCooldown > 0) {
                boss.attackCooldown--;
            }
            
            if (boss.jumpCooldown > 0) {
                boss.jumpCooldown--;
            }
            
            if (boss.isAttacking) {
                boss.attackTimer--;
                if (boss.attackType === 'charge') {
                    boss.speed = 7;
                    if (boss.attackTimer <= 0) {
                        boss.speed = 2.5;
                        boss.isAttacking = false;
                        boss.attackCooldown = 60;
                    }
                } else if (boss.attackType === 'jump') {
                    if (boss.attackTimer === 30) {
                        boss.y = 280;
                    } else if (boss.attackTimer <= 0) {
                        boss.y = 380;
                        boss.isAttacking = false;
                        boss.jumpCooldown = 120;
                        // Shake effect
                        particles.push(...Array(20).fill().map(() => createParticle(boss.x + boss.width / 2, boss.y + boss.height, '#8B4513')));
                    }
                } else if (boss.attackType === 'projectile') {
                    if (boss.attackTimer % 15 === 0) {
                        boss.projectiles.push({
                            x: boss.x + (boss.direction > 0 ? boss.width : -15),
                            y: boss.y + 40,
                            width: 15,
                            height: 15,
                            speed: 6 * boss.direction
                        });
                    }
                    if (boss.attackTimer <= 0) {
                        boss.isAttacking = false;
                        boss.attackCooldown = 90;
                    }
                }
            }
            
            if (!boss.isAttacking && boss.attackCooldown <= 0) {
                const attackTypes = ['charge', 'jump', 'projectile'];
                boss.attackType = attackTypes[Math.floor(Math.random() * attackTypes.length)];
                boss.isAttacking = true;
                
                if (boss.attackType === 'charge') {
                    boss.attackTimer = 60;
                } else if (boss.attackType === 'jump') {
                    boss.attackTimer = 60;
                } else if (boss.attackType === 'projectile') {
                    boss.attackTimer = 60;
                }
            }
            
            for (let i = boss.projectiles.length - 1; i >= 0; i--) {
                const proj = boss.projectiles[i];
                proj.x += proj.speed;
                if (proj.x < -50 || proj.x > canvas.width + 50) {
                    boss.projectiles.splice(i, 1);
                }
            }
        }
        
        function updateCrocodiles() {
            for (const croc of crocodiles) {
                if (croc.inWater) {
                    croc.waterTimer--;
                    croc.emergeTimer--;
                    if (croc.emergeTimer <= 0) {
                        croc.inWater = false;
                        croc.y = 410;
                        croc.emergeTimer = 60 + Math.random() * 60;
                    }
                } else {
                    croc.x += croc.speed * croc.direction;
                    if (croc.direction > 0 && croc.x > croc.initialX + croc.moveDistance) {
                        croc.direction *= -1;
                    } else if (croc.direction < 0 && croc.x < croc.initialX) {
                        croc.direction *= -1;
                    }
                    if (Math.random() < 0.05) {
                        croc.inWater = true;
                        croc.waterTimer = 2 + Math.floor(Math.random() * 3);
                        croc.y = 480;
                    }
                }
            }
        }
        
        function loadNextLevel() {
            levelScores[currentLevel - 1] = score - levelScores.slice(0, currentLevel - 1).reduce((a, b) => a + b, 0);
            currentLevel++;
            if (currentLevel <= 5) {
                levelCompleteScreen.style.display = 'none';
                loadLevel(currentLevel);
            } else {
                gameComplete();
            }
        }
        
        function gameComplete() {
            clearInterval(timerInterval);
            gameRunning = false;
            levelScores[currentLevel - 1] = score - levelScores.slice(0, currentLevel - 1).reduce((a, b) => a + b, 0);
            updateStatsChart();
            leaderboardScreen.style.display = 'flex';
            finalScoreElement.textContent = score;
        }
        
        function restartGame() {
            gameOverScreen.style.display = 'none';
            startGame();
        }
        
        function submitScore() {
            const name = nameInput.value.trim() || playerName;
            leaderboard.push({ name, time: totalTime, score });
            localStorage.setItem('jungleLeaderboard', JSON.stringify(leaderboard));
            updateLeaderboardDisplay();
            leaderboardScreen.style.display = 'none';
            startScreen.style.display = 'flex';
            startButton.textContent = 'Play Again';
        }
        
        function gameLoop() {
            if (!gameRunning) return;
            
            update();
            render();
            requestAnimationFrame(gameLoop);
        }
        
        function update() {
            // Update parallax
            parallaxOffset += player.direction * 0.5;
            if (parallaxOffset > 900) parallaxOffset -= 900;
            if (parallaxOffset < -900) parallaxOffset += 900;
            
            // Apply gravity
            if (!player.onVine) {
                player.velocityY += 0.4; // Reduced gravity for smoother jumps
            }
            
            // Move player
            const currentSpeed = powerupEffect === 'speed' ? player.speed * 1.8 : player.speed;
            let moving = false;
            
            if (player.onVine) {
                if (keys['ArrowUp'] || keys['w'] || keys['W']) {
                    player.y -= player.vineClimbSpeed;
                }
                if (keys['ArrowDown']) {
                    player.y += player.vineClimbSpeed;
                }
                if (keys[' '] && !player.jumping) {
                    player.velocityY = -player.jumpForce;
                    player.jumping = true;
                    player.onVine = false;
                }
            } else {
                if (keys['ArrowLeft'] || keys['a'] || keys['A']) {
                    player.x -= currentSpeed;
                    player.direction = -1;
                    moving = true;
                }
                if (keys['ArrowRight'] || keys['d'] || keys['D']) {
                    player.x += currentSpeed;
                    player.direction = 1;
                    moving = true;
                }
                
                // Jump
                if ((keys['ArrowUp'] || keys['w'] || keys['W'] || keys[' ']) && !player.jumping) {
                    player.velocityY = -player.jumpForce;
                    player.jumping = true;
                }
            }
            
            // Animation
            if (moving || player.onVine) {
                player.frameCounter++;
                if (player.frameCounter >= 8) {
                    player.frame = (player.frame + 1) % 4;
                    player.frameCounter = 0;
                }
            } else {
                player.frame = 0;
                player.frameCounter = 0;
            }
            
            // Apply velocity
            player.y += player.velocityY;
            
            // Check vine collisions
            player.onVine = false;
            for (const vine of vines) {
                if (
                    player.x < vine.x + vine.width &&
                    player.x + player.width > vine.x &&
                    player.y < vine.y + vine.height &&
                    player.y + player.height > vine.y
                ) {
                    player.onVine = true;
                    player.velocityY = 0;
                    player.jumping = false;
                    player.y = Math.max(vine.y, Math.min(player.y, vine.y + vine.height - player.height));
                    break;
                }
            }
            
            // Check platform collisions
            player.jumping = true;
            for (let i = platforms.length - 1; i >= 0; i--) {
                const platform = platforms[i];
                if (
                    player.x < platform.x + platform.width &&
                    player.x + player.width > platform.x &&
                    player.y + player.height > platform.y &&
                    player.y + player.height <= platform.y + platform.height + player.velocityY &&
                    player.velocityY >= 0
                ) {
                    player.y = platform.y - player.height;
                    player.velocityY = 0;
                    player.jumping = false;
                    if (platform.breakable) {
                        platform.breakTimer--;
                        if (platform.breakTimer <= 0) {
                            platforms.splice(i, 1);
                            particles.push(...Array(10).fill().map(() => createParticle(platform.x + platform.width / 2, platform.y, '#7CB342')));
                        }
                    }
                }
            }
            
            // Screen boundaries
            if (player.x < 0) player.x = 0;
            if (player.x + player.width > canvas.width) player.x = canvas.width - player.width;
            
            // Check if player fell
            if (player.y > canvas.height) {
                loseLife();
                resetPlayer();
            }
            
            // Update crocodiles
            if (currentLevel < 5) {
                for (const croc of crocodiles) {
                    if (!croc.inWater) {
                        croc.x += croc.speed * croc.direction;
                        if (croc.direction > 0 && croc.x > croc.initialX + croc.moveDistance) {
                            croc.direction *= -1;
                        } else if (croc.direction < 0 && croc.x < croc.initialX) {
                            croc.direction *= -1;
                        }
                        
                        if (
                            player.x < croc.x + croc.width &&
                            player.x + player.width > croc.x &&
                            player.y < croc.y + croc.height &&
                            player.y + player.height > croc.y
                        ) {
                            if (player.velocityY > 0 && player.y + player.height < croc.y + croc.height / 2) {
                                croc.x = -200;
                                player.velocityY = -8;
                                score += 100;
                                updateScore();
                                particles.push(...Array(5).fill().map(() => createParticle(croc.x + croc.width / 2, croc.y, '#4CAF50')));
                            } else {
                                loseLife();
                                resetPlayer();
                            }
                        }
                    }
                }
            }
            
            // Boss battle
            if (currentLevel === 5) {
                if (
                    player.x < boss.x + boss.width &&
                    player.x + player.width > boss.x &&
                    player.y < boss.y + boss.height &&
                    player.y + player.height > boss.y
                ) {
                    if (player.velocityY > 0 && player.y + player.height < boss.y + boss.height / 2) {
                        boss.health -= 10;
                        updateBossHealth();
                        player.velocityY = -10;
                        score += 50;
                        updateScore();
                        particles.push(...Array(10).fill().map(() => createParticle(boss.x + boss.width / 2, boss.y, '#8B4513')));
                        if (boss.health <= 0) {
                            score += 500;
                            updateScore();
                            levelComplete();
                        }
                    } else {
                        loseLife();
                        resetPlayer();
                    }
                }
                
                for (let i = boss.projectiles.length - 1; i >= 0; i--) {
                    const proj = boss.projectiles[i];
                    if (
                        player.x < proj.x + proj.width &&
                        player.x + player.width > proj.x &&
                        player.y < proj.y + proj.height &&
                        player.y + player.height > proj.y
                    ) {
                        boss.projectiles.splice(i, 1);
                        loseLife();
                        resetPlayer();
                    }
                }
            }
            
            // Check coin collisions
            for (const coin of coins) {
                if (
                    !coin.collected &&
                    player.x < coin.x + coin.width &&
                    player.x + player.width > coin.x &&
                    player.y < coin.y + coin.height &&
                    player.y + player.height > coin.y
                ) {
                    coin.collected = true;
                    score += 50;
                    coinsCollected++;
                    updateScore();
                    updateCoinsToLife();
                    particles.push(...Array(5).fill().map(() => createParticle(coin.x + coin.width / 2, coin.y + coin.height / 2, '#FFD700')));
                    if (coinsCollected % 50 === 0) {
                        lives++;
                        updateLives();
                    }
                }
            }
            
            // Check banana collisions
            for (const banana of bananas) {
                if (
                    !banana.collected &&
                    player.x < banana.x + banana.width &&
                    player.x + player.width > banana.x &&
                    player.y < banana.y + banana.height &&
                    player.y + player.height > banana.y
                ) {
                    banana.collected = true;
                    activatePowerup('speed');
                    score += 30;
                    updateScore();
                    particles.push(...Array(5).fill().map(() => createParticle(banana.x + banana.width / 2, banana.y + banana.height / 2, '#FFEB3B')));
                }
            }
            
            // Check goal
            if (currentLevel < 5 &&
                player.x < levelGoal.x + levelGoal.width &&
                player.x + player.width > levelGoal.x &&
                player.y < levelGoal.y + levelGoal.height &&
                player.y + player.height > levelGoal.y
            ) {
                levelComplete();
            }
            
            // Update particles
            updateParticles();
        }
        
        function updateBossHealth() {
            const healthPercent = (boss.health / boss.maxHealth) * 100;
            bossHealthFill.style.width = `${healthPercent}%`;
        }
        
        function activatePowerup(type) {
            powerupActive = true;
            powerupTimeLeft = 5;
            powerupEffect = type;
            powerupTimerElement.textContent = `${powerupTimeLeft}s`;
            document.getElementById('game-container').classList.add('powerup-active');
        }
        
        function endPowerup() {
            powerupActive = false;
            powerupEffect = null;
            powerupTimerElement.textContent = "0s";
            document.getElementById('game-container').classList.remove('powerup-active');
        }
        
        function updateCoinsToLife() {
            const coinsNeeded = 50 - (coinsCollected % 50);
            coinsToLifeElement.textContent = coinsNeeded;
        }
        
        function render() {
            ctx.clearRect(0, 0, canvas.width, canvas.height);
            
            // Draw parallax background
            ctx.drawImage(textures.jungleBgFar, -parallaxOffset * 0.2, 0);
            ctx.drawImage(textures.jungleBgFar, 900 - parallaxOffset * 0.2, 0);
            ctx.drawImage(textures.jungleBgMid, -parallaxOffset * 0.5, 0);
            ctx.drawImage(textures.jungleBgMid, 900 - parallaxOffset * 0.5, 0);
            ctx.drawImage(textures.jungleBgNear, -parallaxOffset * 0.8, 0);
            ctx.drawImage(textures.jungleBgNear, 900 - parallaxOffset * 0.8, 0);
            
            // Simulate lighting
            const gradient = ctx.createRadialGradient(450, 250, 100, 450, 250, 500);
            gradient.addColorStop(0, 'rgba(255, 255, 255, 0.2)');
            gradient.addColorStop(1, 'rgba(0, 0, 0, 0.3)');
            ctx.fillStyle = gradient;
            ctx.fillRect(0, 0, canvas.width, canvas.height);
            
            // Draw water
            waterAreas.forEach(water => {
                const waterPattern = ctx.createPattern(textures.water, 'repeat');
                ctx.fillStyle = waterPattern;
                ctx.fillRect(water.x, water.y, water.width, water.height);
            });
            
            // Draw platforms
            platforms.forEach(platform => {
                const grassPattern = ctx.createPattern(textures.grass, 'repeat');
                ctx.fillStyle = platform.breakable ? 'rgba(124, 179, 66, 0.7)' : grassPattern;
                ctx.fillRect(platform.x, platform.y, platform.width, platform.height);
            });
            
            // Draw trees
            trees.forEach(tree => {
                ctx.drawImage(textures.tree, tree.x, tree.y - 80, 80, 120);
            });
            
            // Draw rocks
            rocks.forEach(rock => {
                ctx.drawImage(textures.rock, rock.x, rock.y, 40, 40);
            });
            
            // Draw vines
            vines.forEach(vine => {
                ctx.drawImage(textures.vine, vine.x, vine.y, vine.width, vine.height);
            });
            
            // Draw coins
            coins.forEach(coin => {
                if (!coin.collected) {
                    ctx.drawImage(textures.coin, coin.x, coin.y, coin.width, coin.height);
                }
            });
            
            // Draw bananas
            bananas.forEach(banana => {
                if (!banana.collected) {
                    ctx.drawImage(textures.banana, banana.x, banana.y, banana.width, banana.height);
                }
            });
            
            // Draw crocodiles
            crocodiles.forEach(croc => {
                if (!croc.inWater) {
                    ctx.drawImage(textures.crocodile[Math.floor(croc.frame) % 2], croc.x, croc.y, croc.width, croc.height);
                    croc.frame = (croc.frame || 0) + 0.1;
                }
            });
            
            // Draw boss
            if (currentLevel === 5) {
                ctx.drawImage(textures.boss[Math.floor(boss.frame) % 2], boss.x, boss.y, boss.width, boss.height);
                boss.frame = (boss.frame || 0) + 0.1;
                
                boss.projectiles.forEach(proj => {
                    ctx.drawImage(textures.projectile, proj.x, proj.y, proj.width, proj.height);
                });
            }
            
            // Draw goal
            if (currentLevel < 5) {
                ctx.drawImage(textures.goal, levelGoal.x, levelGoal.y, levelGoal.width, levelGoal.height);
            }
            
            // Draw player
            ctx.drawImage(textures.player[player.frame], player.x, player.y, player.width, player.height);
            
            // Draw particles
            renderParticles();
        }
        
        function updateScore() {
            scoreElement.textContent = score;
        }
        
        function updateLives() {
            livesElement.textContent = lives;
        }
        
        function updateTimer() {
            const minutes = Math.floor(levelTime / 60);
            const seconds = levelTime % 60;
            timerElement.textContent = `${minutes.toString().padStart(2, '0')}:${seconds.toString().padStart(2, '0')}`;
        }
        
        function loseLife() {
            lives--;
            updateLives();
            if (lives <= 0) {
                gameOver();
            }
        }
        
        function resetPlayer() {
            player.x = currentLevel === 5 ? 100 : 50;
            player.y = 400;
            player.velocityY = 0;
            player.onVine = false;
            endPowerup();
        }
        
        function levelComplete() {
            clearInterval(timerInterval);
            gameRunning = false;
            const timeBonus = Math.max(0, 300 - levelTime) * 2;
            score += timeBonus;
            levelScores[currentLevel - 1] = score - levelScores.slice(0, currentLevel - 1).reduce((a, b) => a + b, 0);
            
            const minutes = Math.floor(levelTime / 60);
            const seconds = levelTime % 60;
            levelTimeElement.textContent = `${minutes.toString().padStart(2, '0')}:${seconds.toString().padStart(2, '0')}`;
            totalScoreElement.textContent = score;
            levelCompleteScreen.style.display = 'flex';
        }
        
        function gameOver() {
            clearInterval(timerInterval);
            gameRunning = false;
            levelScores[currentLevel - 1] = score - levelScores.slice(0, currentLevel - 1).reduce((a, b) => a + b, 0);
            updateStatsChart();
            gameOverScreen.style.display = 'flex';
            finalScoreElement.textContent = score;
        }
        
        // Level configurations
        const levelConfigs = [
            {
                platforms: [
                    { x: 0, y: 460, width: 900, height: 40, breakable: false },
                    { x: 200, y: 350, width: 150, height: 20, breakable: true },
                    { x: 400, y: 250, width: 150, height: 20, breakable: true },
                    { x: 600, y: 350, width: 150, height: 20, breakable: false },
                    { x: 750, y: 250, width: 100, height: 20, breakable: true }
                ],
                coins: [
                    { x: 230, y: 320, width: 20, height: 20, collected: false },
                    { x: 430, y: 220, width: 20, height: 20, collected: false },
                    { x: 630, y: 320, width: 20, height: 20, collected: false },
                    { x: 780, y: 220, width: 20, height: 20, collected: false },
                    { x: 500, y: 400, width: 20, height: 20, collected: false },
                    { x: 300, y: 400, width: 20, height: 20, collected: false },
                    { x: 550, y: 150, width: 20, height: 20, collected: false }
                ],
                bananas: [
                    { x: 350, y: 310, width: 25, height: 35, collected: false },
                    { x: 550, y: 210, width: 25, height: 35, collected: false }
                ],
                crocodiles: [
                    { x: 300, y: 410, width: 60, height: 30, speed: 1.5, direction: 1, moveDistance: 200, inWater: false, waterTimer: 0 }
                ],
                trees: [
                    { x: 100, y: 460 }, { x: 500, y: 460 }, { x: 800, y: 460 }
                ],
                rocks: [
                    { x: 50, y: 420 }, { x: 850, y: 420 }
                ],
                vines: [
                    { x: 400, y: 150, width: 20, height: 100 }
                ],
                waterAreas: [
                    { x: 250, y: 460, width: 300, height: 40 }
                ],
                goal: { x: 830, y: 210, width: 40, height: 40 }
            },
            // Additional levels follow similar structure with added vines and breakable platforms
        ];
        
        // Initialize the game
        loadLeaderboard();
    </script>
</body>
</html>
