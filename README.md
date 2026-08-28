<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Felipe Rua Braga - Portfólio</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background: linear-gradient(135deg, #1a1a2e 0%, #16213e 50%, #0f3460 100%);
            min-height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            overflow: hidden;
        }
        .container {
            text-align: center;
            padding: 40px;
            background: rgba(255, 255, 255, 0.1);
            border-radius: 20px;
            backdrop-filter: blur(10px);
            box-shadow: 0 8px 32px rgba(0, 0, 0, 0.3);
        }
        .name {
            font-size: 3.5em;
            color: #fff;
            margin-bottom: 40px;
            position: relative;
            animation: glow 2s ease-in-out infinite alternate;
        }
        .name span {
            display: inline-block;
            animation: wave 1.5s ease-in-out infinite;
        }
        .name span:nth-child(1) { animation-delay: 0s; }
        .name span:nth-child(2) { animation-delay: 0.1s; }
        .name span:nth-child(3) { animation-delay: 0.2s; }
        .name span:nth-child(4) { animation-delay: 0.3s; }
        .name span:nth-child(5) { animation-delay: 0.4s; }
        .name span:nth-child(6) { animation-delay: 0.5s; }
        .name span:nth-child(7) { animation-delay: 0.6s; }
        .name span:nth-child(8) { animation-delay: 0.7s; }
        .name span:nth-child(9) { animation-delay: 0.8s; }
        .name span:nth-child(10) { animation-delay: 0.9s; }
        .name span:nth-child(11) { animation-delay: 1s; }
        .name span:nth-child(12) { animation-delay: 1.1s; }
        .name span:nth-child(13) { animation-delay: 1.2s; }
        .name span:nth-child(14) { animation-delay: 1.3s; }
        .name span:nth-child(15) { animation-delay: 1.4s; }
        .name span:nth-child(16) { animation-delay: 1.5s; }
        @keyframes wave {
            0%, 100% {
                transform: translateY(0);
            }
            50% {
                transform: translateY(-20px);
            }
        }
        @keyframes glow {
            from {
                text-shadow: 0 0 10px #fff, 0 0 20px #fff, 0 0 30px #e60073, 0 0 40px #e60073;
            }
            to {
                text-shadow: 0 0 20px #fff, 0 0 30px #ff4da6, 0 0 40px #ff4da6, 0 0 50px #ff4da6;
            }
        }
        .skills-title {
            font-size: 1.8em;
            color: #fff;
            margin-bottom: 30px;
            opacity: 0;
            animation: fadeIn 1s ease-in-out 1s forwards;
        }
        .skills-container {
            display: flex;
            justify-content: center;
            gap: 20px;
            flex-wrap: wrap;
        }
        .skill-card {
            background: linear-gradient(145deg, rgba(255, 255, 255, 0.15), rgba(255, 255, 255, 0.05));
            padding: 25px 35px;
            border-radius: 15px;
            color: #fff;
            font-size: 1.3em;
            font-weight: bold;
            cursor: pointer;
            transition: all 0.3s ease;
            opacity: 0;
            animation: slideUp 0.8s ease-out forwards;
            border: 2px solid transparent;
        }
        .skill-card:hover {
            transform: translateY(-10px) scale(1.05);
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.4);
        }
        .skill-card:nth-child(1) { animation-delay: 1.5s; border-color: #f7df1e; }
        .skill-card:nth-child(2) { animation-delay: 1.7s; border-color: #00758f; }
        .skill-card:nth-child(3) { animation-delay: 1.9s; border-color: #e34c26; }
        .skill-card:nth-child(4) { animation-delay: 2.1s; border-color: #777bb4; }
        .skill-card.javascript:hover {
            background: linear-gradient(145deg, #f7df1e, #ffd700);
            color: #1a1a2e;
        }
        .skill-card.sql:hover {
            background: linear-gradient(145deg, #00758f, #0095b5);
            color: #fff;
        }
        .skill-card.html:hover {
            background: linear-gradient(145deg, #e34c26, #ff6b4a);
            color: #fff;
        }
        .skill-card.php:hover {
            background: linear-gradient(145deg, #777bb4, #8f93c9);
            color: #fff;
        }
        @keyframes fadeIn {
            to {
                opacity: 1;
            }
        }
        @keyframes slideUp {
            from {
                opacity: 0;
                transform: translateY(50px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }
        .particles {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            pointer-events: none;
            overflow: hidden;
            z-index: -1;
        }
        .particle {
            position: absolute;
            width: 10px;
            height: 10px;
            background: rgba(255, 255, 255, 0.3);
            border-radius: 50%;
            animation: float 15s infinite;
        }
        @keyframes float {
            0%, 100% {
                transform: translateY(100vh) rotate(0deg);
                opacity: 0;
            }
            10% {
                opacity: 1;
            }
            90% {
                opacity: 1;
            }
            100% {
                transform: translateY(-100vh) rotate(720deg);
                opacity: 0;
            }
        }
    </style>
</head>
<body>
    <div class="particles" id="particles"></div>
    <div class="container">
        <h1 class="name" id="animatedName"></h1>
        <h2 class="skills-title">Linguagens que domino</h2>
        <div class="skills-container">
            <div class="skill-card javascript">JavaScript</div>
            <div class="skill-card sql">SQL</div>
            <div class="skill-card html">HTML</div>
            <div class="skill-card php">PHP</div>
        </div>
    </div>
    <script>
        // Anima o nome letra por letra
        const name = "Felipe Rua Braga";
        const nameElement = document.getElementById("animatedName");
        name.split("").forEach((letter, index) => {
            const span = document.createElement("span");
            span.textContent = letter === " " ? "\u00A0" : letter;
            span.style.animationDelay = `${index * 0.1}s`;
            nameElement.appendChild(span);
        });
        const particlesContainer = document.getElementById("particles");
        for (let i = 0; i < 50; i++) {
            const particle = document.createElement("div");
            particle.className = "particle";
            particle.style.left = `${Math.random() * 100}%`;
            particle.style.animationDelay = `${Math.random() * 15}s`;
            particle.style.animationDuration = `${15 + Math.random() * 10}s`;
            particle.style.width = `${5 + Math.random() * 10}px`;
            particle.style.height = particle.style.width;
            particlesContainer.appendChild(particle);
        }
    </script>
</body>
</html>
