<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=5.0">
    <title>Valentine's Day Invite - Hugguland 💕</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Arial', sans-serif;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            min-height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            overflow: hidden;
            padding: 10px;
            width: 100%;
        }

        .falling-hearts {
            position: fixed;
            width: 100%;
            height: 100%;
            top: 0;
            left: 0;
            pointer-events: none;
            z-index: 1;
        }

        .heart {
            position: absolute;
            width: 30px;
            height: 30px;
            opacity: 0.6;
            animation: fall linear infinite;
            font-size: 30px;
            display: flex;
            align-items: center;
            justify-content: center;
        }

        @keyframes fall {
            to {
                transform: translateY(100vh) rotate(360deg);
                opacity: 0;
            }
        }

        .container {
            background: white;
            border-radius: 20px;
            padding: 40px 20px;
            box-shadow: 0 20px 60px rgba(0, 0, 0, 0.3);
            width: 100%;
            max-width: 600px;
            position: relative;
            z-index: 2;
            animation: slideIn 0.8s ease-out;
            max-height: 85vh;
            overflow-y: auto;
            -webkit-overflow-scrolling: touch;
        }

        @keyframes slideIn {
            from {
                opacity: 0;
                transform: translateY(30px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        .main-heart {
            font-size: clamp(50px, 15vw, 80px);
            text-align: center;
            margin-bottom: 20px;
            animation: heartbeat 1.2s ease-in-out infinite;
        }

        @keyframes heartbeat {
            0%, 100% {
                transform: scale(1);
            }
            25% {
                transform: scale(1.1);
            }
            50% {
                transform: scale(1.2);
            }
            75% {
                transform: scale(1.1);
            }
        }

        h1 {
            color: #ff1744;
            font-size: clamp(1.5em, 7vw, 2.5em);
            margin-bottom: 10px;
            text-align: center;
            animation: fadeInDown 0.8s ease-out;
            word-wrap: break-word;
        }

        h2 {
            color: #ff1744;
            font-size: clamp(1.2em, 5vw, 1.5em);
            margin-bottom: 20px;
            text-align: center;
        }

        .subtitle {
            color: #666;
            font-size: clamp(0.95em, 4vw, 1.1em);
            text-align: center;
            margin-bottom: 30px;
            animation: fadeInUp 0.8s ease-out 0.2s both;
            line-height: 1.6;
        }

        @keyframes fadeInDown {
            from {
                opacity: 0;
                transform: translateY(-20px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        @keyframes fadeInUp {
            from {
                opacity: 0;
                transform: translateY(20px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        .content-section {
            display: none;
            animation: fadeIn 0.8s ease-out;
            position: relative;
        }

        .content-section.active {
            display: block;
        }

        @keyframes fadeIn {
            from {
                opacity: 0;
            }
            to {
                opacity: 1;
            }
        }

        .content-text {
            color: #333;
            font-size: clamp(0.95em, 4vw, 1.05em);
            line-height: 1.8;
            margin: 20px 0;
            text-align: center;
            white-space: pre-line;
            word-wrap: break-word;
        }

        .welcome-wrapper {
            text-align: center;
        }

        .message-text {
            font-size: clamp(0.95em, 4vw, 1.1em);
            color: #666;
            margin: 15px 0;
            line-height: 1.6;
            animation: fadeInUp 0.8s ease-out 0.4s both;
            word-wrap: break-word;
        }

        .photo-collage {
            position: relative;
            width: 100%;
            height: clamp(200px, 60vw, 320px);
            margin: 30px 0;
            animation: fadeInUp 0.8s ease-out 0.6s both;
            border-radius: 15px;
            border: 5px solid white;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.2);
            overflow: hidden;
            background-color: #f0f0f0;
        }

        .photo-collage img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            display: block;
        }

        .heart-deco {
            position: absolute;
            font-size: clamp(1.5em, 5vw, 2em);
            animation: heart-float 3s ease-in-out infinite;
            z-index: 10;
        }

        .heart-deco-1 {
            top: 20px;
            right: 20px;
            animation-delay: 0s;
        }

        .heart-deco-2 {
            bottom: 40px;
            left: 15px;
            animation-delay: 0.3s;
        }

        .heart-deco-3 {
            top: 50%;
            right: -20px;
            animation-delay: 0.6s;
        }

        @keyframes heart-float {
            0%, 100% {
                transform: translateY(0px) scale(1);
                opacity: 0.7;
            }
            50% {
                transform: translateY(-20px) scale(1.1);
                opacity: 1;
            }
        }

        .creative-subtitle {
            font-size: clamp(0.95em, 4vw, 1.1em);
            color: #666;
            font-weight: 500;
            margin: 20px 0 10px 0;
            animation: fadeInUp 0.8s ease-out 0.7s both;
            line-height: 1.6;
            word-wrap: break-word;
        }

        .buttons {
            margin-top: 30px;
            display: flex;
            gap: 10px;
            justify-content: center;
            flex-wrap: wrap;
            position: relative;
            width: 100%;
        }

        .proposal-buttons {
            margin-top: 30px;
            display: flex;
            gap: 10px;
            justify-content: center;
            flex-wrap: wrap;
            position: relative;
            width: 100%;
        }

        button {
            padding: clamp(10px, 2vw, 12px) clamp(20px, 4vw, 30px);
            font-size: clamp(0.85em, 3.5vw, 1em);
            border: none;
            border-radius: 50px;
            cursor: pointer;
            transition: all 0.3s ease;
            font-weight: bold;
            text-transform: uppercase;
            letter-spacing: 0.5px;
            white-space: nowrap;
            min-height: 44px;
            touch-action: manipulation;
        }

        .primary-btn {
            background: linear-gradient(135deg, #ff1744, #ff5252);
            color: white;
            box-shadow: 0 5px 15px rgba(255, 23, 68, 0.4);
            flex: 1;
            min-width: 100px;
        }

        .primary-btn:hover,
        .primary-btn:active {
            transform: scale(1.05);
            box-shadow: 0 8px 20px rgba(255, 23, 68, 0.6);
        }

        .primary-btn:active {
            transform: scale(0.98);
        }

        .secondary-btn {
            background: #f0f0f0;
            color: #333;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
            position: static;
            z-index: 10;
            flex: 1;
            min-width: 100px;
        }

        .secondary-btn:hover {
            background: #e0e0e0;
        }

        .no-btn {
            background: linear-gradient(135deg, #667eea, #764ba2);
            color: white;
            box-shadow: 0 5px 15px rgba(102, 126, 234, 0.4);
            position: fixed;
            z-index: 10;
            touch-action: none;
        }

        .no-btn:hover {
            background: linear-gradient(135deg, #764ba2, #667eea);
            box-shadow: 0 8px 20px rgba(102, 126, 234, 0.6);
        }

        .next-btn {
            background: linear-gradient(135deg, #ff1744, #ff5252);
            color: white;
            animation: fadeInUp 0.8s ease-out 0.8s both;
            width: 100%;
        }

        .next-btn:hover,
        .next-btn:active {
            transform: scale(1.05);
        }

        .next-btn:active {
            transform: scale(0.98);
        }

        .response {
            display: none;
            margin-top: 30px;
            font-size: clamp(1.1em, 5vw, 1.3em);
            font-weight: bold;
            text-align: center;
            animation: pop 0.5s ease-out;
            word-wrap: break-word;
        }

        @keyframes pop {
            0% {
                transform: scale(0);
                opacity: 0;
            }
            50% {
                transform: scale(1.1);
            }
            100% {
                transform: scale(1);
                opacity: 1;
            }
        }

        .yes-response {
            color: #ff1744;
        }

        .confetti {
            position: fixed;
            width: 10px;
            height: 10px;
            pointer-events: none;
            z-index: 3;
        }

        @keyframes confetti-fall {
            to {
                transform: translateY(100vh) rotate(720deg);
                opacity: 0;
            }
        }

        .section-title {
            color: #ff1744;
            font-size: clamp(1.2em, 5vw, 1.5em);
            margin-bottom: 20px;
            text-align: center;
        }

        .info-box {
            background: #f9f9f9;
            padding: clamp(12px, 3vw, 15px);
            border-radius: 10px;
            margin: 15px 0;
            border-left: 4px solid #ff1744;
            word-wrap: break-word;
        }

        .info-box p {
            color: #666;
            margin: 8px 0;
            font-size: clamp(0.9em, 4vw, 1em);
            line-height: 1.6;
        }

        .emoji {
            margin-right: 8px;
            font-size: 1.3em;
        }

        .heart-jump {
            position: fixed;
            font-size: clamp(40px, 12vw, 60px);
            pointer-events: none;
            z-index: 9;
            display: none;
        }

        @keyframes heart-bounce {
            0%, 100% {
                transform: translateY(0) rotate(0deg);
            }
            25% {
                transform: translateY(-40px) rotate(-10deg);
            }
            50% {
                transform: translateY(-80px) rotate(5deg);
            }
            75% {
                transform: translateY(-40px) rotate(-10deg);
            }
        }

        .heart-jump.active {
            display: block;
            animation: heart-bounce 0.8s ease-in-out;
        }

        .page-heart {
            position: absolute;
            font-size: clamp(30px, 8vw, 45px);
            pointer-events: none;
            z-index: 5;
        }

        @keyframes heart-float-deco {
            0%, 100% {
                transform: translateY(0) rotate(0deg);
            }
            50% {
                transform: translateY(-15px) rotate(5deg);
            }
        }

        @keyframes heart-wiggle {
            0%, 100% {
                transform: translateX(0) rotate(0deg);
            }
            25% {
                transform: translateX(-5px) rotate(-2deg);
            }
            75% {
                transform: translateX(5px) rotate(2deg);
            }
        }

        @keyframes heart-dance {
            0%, 100% {
                transform: rotate(0deg) scale(1);
            }
            25% {
                transform: rotate(-5deg) scale(1.05);
            }
            50% {
                transform: rotate(5deg) scale(1.1);
            }
            75% {
                transform: rotate(-5deg) scale(1.05);
            }
        }

        .heart-top-left {
            top: 10px;
            left: 10px;
            animation: heart-float-deco 3s ease-in-out infinite;
        }

        .heart-top-right {
            top: 10px;
            right: 10px;
            animation: heart-float-deco 3.5s ease-in-out infinite reverse;
        }

        .heart-bottom-left {
            bottom: 10px;
            left: 10px;
            animation: heart-dance 2.5s ease-in-out infinite;
        }

        .heart-bottom-right {
            bottom: 10px;
            right: 10px;
            animation: heart-wiggle 2.5s ease-in-out infinite reverse;
        }

        /* Disable animations on low-power devices */
        @media (prefers-reduced-motion: reduce) {
            * {
                animation: none !important;
                transition: none !important;
            }
        }

        @media (max-width: 480px) {
            body {
                padding: 5px;
            }

            .container {
                padding: 25px 15px;
                border-radius: 15px;
                max-height: 90vh;
            }

            h1 {
                margin-bottom: 15px;
            }

            .buttons,
            .proposal-buttons {
                gap: 8px;
            }

            button {
                flex: 1;
                min-width: 80px;
            }

            .no-btn {
                font-size: 0.8em;
                padding: 8px 16px;
            }

            .photo-collage {
                margin: 20px 0;
            }

            .info-box {
                margin: 12px 0;
                padding: 10px;
            }

            .page-heart {
                display: none;
            }

            .heart-deco {
                font-size: clamp(1em, 4vw, 1.5em);
            }
        }

        @media (max-width: 360px) {
            .container {
                padding: 20px 12px;
            }

            button {
                padding: 8px 12px;
                font-size: 0.8em;
            }

            .emoji {
                margin-right: 4px;
            }
        }

        /* Landscape orientation */
        @media (max-height: 600px) {
            .container {
                max-height: 95vh;
                padding: 30px 15px;
            }

            .photo-collage {
                height: 150px;
                margin: 15px 0;
            }

            .main-heart {
                font-size: 50px;
                margin-bottom: 10px;
            }

            h1 {
                margin-bottom: 5px;
            }
        }
    </style>
</head>
<body>
    <div class="falling-hearts" id="fallingHearts"></div>
    <div class="heart-jump" id="heart">💖</div>
    <audio id="boinkSound" preload="auto">
        <source src="https://assets.mixkit.co/active_storage/sfx/2869/2869-preview.mp3" type="audio/mpeg">
    </audio>

    <div class="container">
        <!-- SCREEN 1: CREATIVE GREETING WITH PHOTO COLLAGE -->
        <div id="screen1" class="content-section active">
            <div class="page-heart heart-top-left">💕</div>
            <div class="page-heart heart-top-right">💖</div>
            <div class="welcome-wrapper">
                <h1>Hi Chotiiiii</h1>
                
                <p class="message-text">
                    Sorry for being away for the last 3 weeks 💔
                </p>

                <!-- Photo Collage with Decorations -->
                <div class="photo-collage">
                    <img src="https://i.ibb.co/nNwyz1dp/image.jpg" alt="Special moment">
                    <!-- Heart Decorations -->
                    <div class="heart-deco heart-deco-1">💕</div>
                    <div class="heart-deco heart-deco-2">💖</div>
                    <div class="heart-deco heart-deco-3">💗</div>
                </div>

                <p class="creative-subtitle">But trying to make it up with a little something</p>

                <div class="buttons">
                    <button class="next-btn" onclick="showSection('screen2')">Continue →</button>
                </div>
            </div>
            <div class="page-heart heart-bottom-left">💗</div>
            <div class="page-heart heart-bottom-right">💓</div>
        </div>

        <!-- SCREEN 2: MESSAGE -->
        <div id="screen2" class="content-section">
            <div class="page-heart heart-top-left">💕</div>
            <div class="page-heart heart-bottom-right">💖</div>
            <div class="main-heart">💕</div>
            <h2 class="section-title">A Message For You</h2>
            <p class="content-text">
Chotu mera baccha hai, baccha bada shaitan hai, shaitani iski door bhagao, isko apna valentine banao
            </p>
            <div class="buttons">
                <button class="next-btn" onclick="showSection('screen3')">Next →</button>
            </div>
            <div class="page-heart heart-bottom-left">💗</div>
        </div>

        <!-- SCREEN 3: PROPOSAL -->
        <div id="screen3" class="content-section">
            <div class="page-heart heart-top-left">💓</div>
            <div class="page-heart heart-top-right">💕</div>
            <div class="main-heart">💕</div>
            <h2 class="section-title">Will You Be My Valentine?</h2>
            <div class="proposal-buttons">
                <button class="primary-btn" onclick="handleYes()">Yes! 💖</button>
                <button class="no-btn" id="noBtn" onmouseover="moveButtonAndShowHeart()" onmouseout="" ontouchstart="moveButtonAndShowHeart()" onmousemove="moveButtonAndShowHeart()" onclick="moveButtonAndShowHeart(event)">No 💔</button>
            </div>
            <div id="response" class="response"></div>
            <div class="page-heart heart-bottom-left">💖</div>
            <div class="page-heart heart-bottom-right">💗</div>
        </div>

        <!-- SCREEN 4: DETAILS (Shows after Yes) -->
        <div id="screen4" class="content-section">
            <div class="page-heart heart-top-left">💕</div>
            <div class="page-heart heart-top-right">💓</div>
            <div class="main-heart">💕</div>
            <h2 class="section-title">Event Details 🏰</h2>
            
            <div class="info-box">
                <p><span class="emoji">📅</span><strong>Date:</strong> 14th Feb 2026</p>
            </div>

            <div class="info-box">
                <p><span class="emoji">⏰</span><strong>Time:</strong> Full day for princess treatment</p>
            </div>

            <div class="info-box">
                <p><span class="emoji">📍</span><strong>Location:</strong> Hugguland</p>
            </div>

            <div class="info-box">
                <p><span class="emoji">💝</span><strong>What to Expect:</strong> Lots of hugus, kissus, puuchi and less pitti</p>
            </div>
            <div class="page-heart heart-bottom-left">💖</div>
            <div class="page-heart heart-bottom-right">💗</div>
        </div>
    </div>

    <script>
        // Detect touch device
        const isTouchDevice = () => {
            return (('ontouchstart' in window) || (navigator.maxTouchPoints > 0) || (navigator.msMaxTouchPoints > 0));
        };

        // Create falling hearts
        function createFallingHearts() {
            const container = document.getElementById('fallingHearts');
            const hearts = ['❤️', '💕', '💖', '💗', '💓', '💞'];
            
            setInterval(() => {
                const heart = document.createElement('div');
                heart.className = 'heart';
                heart.textContent = hearts[Math.floor(Math.random() * hearts.length)];
                heart.style.left = Math.random() * 100 + '%';
                heart.style.animationDuration = (Math.random() * 3 + 5) + 's';
                heart.style.fontSize = (Math.random() * 20 + 20) + 'px';
                container.appendChild(heart);
                
                setTimeout(() => heart.remove(), 8000);
            }, 300);
        }

        // Create confetti
        function createConfetti() {
            const colors = ['#ff1744', '#ff5252', '#ff6e40', '#ffb74d', '#ffd54f', '#ff69b4'];
            for (let i = 0; i < 50; i++) {
                const confetti = document.createElement('div');
                confetti.className = 'confetti';
                confetti.style.left = Math.random() * 100 + '%';
                confetti.style.top = '0';
                confetti.style.background = colors[Math.floor(Math.random() * colors.length)];
                confetti.style.animation = `confetti-fall ${Math.random() * 3 + 3}s ease-out forwards`;
                document.body.appendChild(confetti);
                
                setTimeout(() => confetti.remove(), 5000);
            }
        }

        // Play boink sound
        function playBoinkSound() {
            const sound = document.getElementById('boinkSound');
            sound.currentTime = 0;
            sound.play().catch(err => {
                console.log('Audio playback failed:', err);
            });
        }

        // Move the No button and show heart
        function moveButtonAndShowHeart(event) {
            if (event && event.preventDefault) {
                event.preventDefault();
            }
            
            playBoinkSound();
            
            const noBtn = document.getElementById('noBtn');
            const heart = document.getElementById('heart');
            
            // Get viewport dimensions for safer repositioning
            const vw = window.innerWidth;
            const vh = window.innerHeight;
            
            // Move the button to random position within viewport
            const randomX = (Math.random() - 0.5) * Math.min(vw * 0.8, 200);
            const randomY = (Math.random() - 0.5) * Math.min(vh * 0.4, 200);
            
            noBtn.style.transform = `translate(${randomX}px, ${randomY}px)`;
            
            // Position heart near the button
            const btnRect = noBtn.getBoundingClientRect();
            heart.style.left = (btnRect.left + btnRect.width / 2 - 30) + 'px';
            heart.style.top = (btnRect.top - 80) + 'px';
            
            // Remove active class and re-add it to trigger animation
            heart.classList.remove('active');
            void heart.offsetWidth;
            heart.classList.add('active');
            
            setTimeout(() => {
                heart.classList.remove('active');
            }, 800);
        }

        // Show section
        function showSection(sectionId) {
            const sections = document.querySelectorAll('.content-section');
            sections.forEach(section => section.classList.remove('active'));
            document.getElementById(sectionId).classList.add('active');
            
            const noBtn = document.getElementById('noBtn');
            if (noBtn) {
                noBtn.style.transform = 'translate(0, 0)';
            }
            
            const heart = document.getElementById('heart');
            heart.classList.remove('active');
            
            const response = document.getElementById('response');
            response.style.display = 'none';
            
            document.querySelector('.container').scrollIntoView({ behavior: 'smooth' });
        }

        // Handle Yes response
        function handleYes() {
            createConfetti();
            const response = document.getElementById('response');
            response.textContent = '🎉 Yayyyyy, welcome to Huggulanddddd 🎉';
            response.className = 'response yes-response';
            response.style.display = 'block';
            
            for (let i = 0; i < 10; i++) {
                setTimeout(createConfetti, i * 100);
            }
            
            setTimeout(() => {
                showSection('screen4');
            }, 2000);
        }

        // Initialize
        window.addEventListener('load', createFallingHearts);
    </script>
</body>
</html>
