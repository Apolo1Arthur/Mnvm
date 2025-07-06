echo "# Mnvm" >> README.md 
git init 
git add README.md 
git commit -m "primeiro commit" 
git branch -M main 
git remote add origin https://github.com/Apolo1Arthur/Mnvm.git
 git push -u origin main

 <!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Dark Romance - Apolo para Kamille</title>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Cinzel:wght@400;700&family=Dancing+Script:wght@700&family=Montserrat:wght@300;400;700&family=Playfair+Display:wght@400;700&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: 'Playfair Display', serif;
            background: #0c0c0c url('data:image/svg+xml;utf8,<svg xmlns="http://www.w3.org/2000/svg" width="100" height="100" viewBox="0 0 100 100"><rect width="100" height="100" fill="%230a0a0a"/><path d="M0 50 Q 25 30, 50 50 T 100 50" stroke="%231a1a1a" fill="none" stroke-width="0.5"/></svg>');
            color: #e0e0e0;
            min-height: 100vh;
            overflow-x: hidden;
            position: relative;
            display: flex;
            justify-content: center;
            align-items: center;
        }
        
        .container {
            width: 90%;
            max-width: 1200px;
            min-height: 95vh;
            margin: 2rem auto;
            display: flex;
            flex-direction: column;
            position: relative;
            z-index: 10;
            border: 1px solid rgba(150, 0, 50, 0.3);
            border-radius: 15px;
            overflow: hidden;
            box-shadow: 0 0 50px rgba(150, 0, 50, 0.2);
            background: rgba(10, 5, 10, 0.85);
            backdrop-filter: blur(8px);
        }
        
        .background-overlay {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: radial-gradient(circle at 20% 30%, rgba(90, 0, 30, 0.1) 0%, rgba(10, 5, 10, 0.9) 70%);
            z-index: -1;
        }
        
        .rose-petals {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            pointer-events: none;
            z-index: 1;
            overflow: hidden;
        }
        
        .petal {
            position: absolute;
            background-image: url('data:image/svg+xml;utf8,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="%23960032"><path d="M12 2C8.1 2 5 5.1 5 9c0 5.3 7 13 7 13s7-7.8 7-13c0-3.9-3.1-7-7-7zm0 9.5c-1.4 0-2.5-1.1-2.5-2.5s1.1-2.5 2.5-2.5 2.5 1.1 2.5 2.5-1.1 2.5-2.5 2.5z"/></svg>');
            background-size: contain;
            background-repeat: no-repeat;
            width: 30px;
            height: 30px;
            opacity: 0.7;
        }
        
        header {
            text-align: center;
            padding: 3rem 2rem 2rem;
            position: relative;
            border-bottom: 1px solid rgba(150, 0, 50, 0.3);
        }
        
        h1 {
            font-family: 'Cinzel', serif;
            font-size: 4.5rem;
            background: linear-gradient(45deg, #c2185b, #ff4081, #f50057);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            margin-bottom: 1rem;
            text-shadow: 0 0 15px rgba(194, 24, 91, 0.3);
            letter-spacing: 3px;
            position: relative;
        }
        
        h1::after {
            content: "";
            position: absolute;
            bottom: -10px;
            left: 50%;
            transform: translateX(-50%);
            width: 150px;
            height: 3px;
            background: linear-gradient(to right, transparent, #c2185b, transparent);
            border-radius: 50%;
        }
        
        .subtitle {
            font-family: 'Dancing Script', cursive;
            font-size: 2rem;
            color: #ff80ab;
            max-width: 600px;
            margin: 0.5rem auto;
            opacity: 0.9;
        }
        
        .heart-container {
            position: relative;
            width: 100%;
            height: 200px;
            display: flex;
            justify-content: center;
            align-items: center;
            margin: 1rem 0;
        }
        
        .heart {
            position: absolute;
            font-size: 8rem;
            color: #c2185b;
            text-shadow: 0 0 20px rgba(194, 24, 91, 0.6);
            animation: heartbeat 1.2s infinite;
            z-index: 1;
            cursor: pointer;
            transition: all 0.3s ease;
        }
        
        .heart:hover {
            transform: scale(1.15);
            filter: drop-shadow(0 0 15px #ff4081);
        }
        
        .content {
            display: flex;
            flex-wrap: wrap;
            padding: 2rem;
            gap: 2rem;
        }
        
        .message-container {
            flex: 1;
            min-width: 300px;
            background: rgba(20, 10, 15, 0.7);
            border-radius: 15px;
            padding: 2.5rem;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.3);
            border: 1px solid rgba(150, 0, 50, 0.2);
            position: relative;
            overflow: hidden;
        }
        
        .message {
            font-size: 1.3rem;
            line-height: 1.9;
            text-align: justify;
            position: relative;
            z-index: 2;
        }
        
        .normal {
            color: #e0e0e0;
            margin-bottom: 1.5rem;
        }
        
        .dark-romance {
            color: #ff80ab;
            font-style: italic;
            border-left: 3px solid #c2185b;
            padding-left: 1.5rem;
            margin: 2rem 0;
            position: relative;
        }
        
        .dark-romance::before {
            content: """"";
            position: absolute;
            top: -20px;
            left: -10px;
            font-size: 5rem;
            color: rgba(194, 24, 91, 0.2);
            font-family: 'Times New Roman', serif;
        }
        
        .highlight {
            color: #ff4081;
            font-weight: bold;
            text-shadow: 0 0 5px rgba(255, 64, 129, 0.3);
        }
        
        .signature {
            text-align: right;
            margin-top: 2.5rem;
            font-family: 'Dancing Script', cursive;
            font-size: 2.8rem;
            color: #ff4081;
            position: relative;
        }
        
        .signature::after {
            content: "";
            position: absolute;
            bottom: -5px;
            right: 0;
            width: 200px;
            height: 2px;
            background: linear-gradient(to left, #c2185b, transparent);
        }
        
        .interactive-section {
            flex: 1;
            min-width: 300px;
            display: flex;
            flex-direction: column;
            gap: 2rem;
        }
        
        .gallery {
            background: rgba(15, 8, 12, 0.7);
            border-radius: 15px;
            padding: 1.5rem;
            box-shadow: 0 10px 25px rgba(0, 0, 0, 0.3);
            border: 1px solid rgba(150, 0, 50, 0.2);
            text-align: center;
        }
        
        .gallery-title {
            font-family: 'Cinzel', serif;
            color: #ff4081;
            margin-bottom: 1.5rem;
            font-size: 1.8rem;
            letter-spacing: 1px;
        }
        
        .love-grid {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 1rem;
        }
        
        .love-item {
            aspect-ratio: 1;
            background: rgba(30, 15, 20, 0.6);
            border-radius: 10px;
            display: flex;
            justify-content: center;
            align-items: center;
            font-size: 2rem;
            color: #ff80ab;
            transition: all 0.3s ease;
            cursor: pointer;
            border: 1px solid rgba(150, 0, 50, 0.3);
        }
        
        .love-item:hover {
            transform: translateY(-5px);
            background: rgba(194, 24, 91, 0.2);
            box-shadow: 0 5px 15px rgba(194, 24, 91, 0.3);
            color: #ff4081;
        }
        
        .music-player {
            background: rgba(15, 8, 12, 0.7);
            border-radius: 15px;
            padding: 1.5rem;
            box-shadow: 0 10px 25px rgba(0, 0, 0, 0.3);
            border: 1px solid rgba(150, 0, 50, 0.2);
            text-align: center;
        }
        
        .player-controls {
            display: flex;
            justify-content: center;
            align-items: center;
            gap: 1.5rem;
            margin-top: 1.5rem;
        }
        
        .control-btn {
            width: 50px;
            height: 50px;
            border-radius: 50%;
            background: rgba(194, 24, 91, 0.3);
            display: flex;
            justify-content: center;
            align-items: center;
            color: #ff80ab;
            font-size: 1.3rem;
            cursor: pointer;
            transition: all 0.3s ease;
            border: 1px solid rgba(255, 64, 129, 0.3);
        }
        
        .control-btn:hover {
            background: rgba(194, 24, 91, 0.5);
            transform: scale(1.1);
            color: #fff;
        }
        
        .floating-text {
            position: absolute;
            font-size: 1.2rem;
            color: #ff80ab;
            opacity: 0;
            pointer-events: none;
            z-index: 10;
            font-family: 'Dancing Script', cursive;
            text-shadow: 0 0 5px rgba(0, 0, 0, 0.5);
        }
        
        footer {
            text-align: center;
            padding: 2rem;
            margin-top: auto;
            font-size: 1.1rem;
            color: rgba(255, 255, 255, 0.5);
            border-top: 1px solid rgba(150, 0, 50, 0.2);
        }
        
        .footer-heart {
            color: #c2185b;
            animation: heartbeat 1.2s infinite;
            display: inline-block;
            margin: 0 5px;
        }
        
        @keyframes heartbeat {
            0% { transform: scale(1); }
            50% { transform: scale(1.1); }
            100% { transform: scale(1); }
        }
        
        @keyframes float {
            0% { transform: translateY(0) rotate(0deg); opacity: 0; }
            10% { opacity: 1; }
            90% { opacity: 1; }
            100% { transform: translateY(-100px) rotate(10deg); opacity: 0; }
        }
        
        @keyframes glow {
            0% { text-shadow: 0 0 5px rgba(194, 24, 91, 0.5); }
            50% { text-shadow: 0 0 20px rgba(194, 24, 91, 0.8); }
            100% { text-shadow: 0 0 5px rgba(194, 24, 91, 0.5); }
        }
        
        .glow-text {
            animation: glow 3s infinite;
        }
        
        @media (max-width: 768px) {
            h1 { font-size: 3rem; }
            .subtitle { font-size: 1.5rem; }
            .heart { font-size: 6rem; }
            .content { flex-direction: column; }
            .message { font-size: 1.1rem; }
        }
        
        /* Efeito de máquina de escrever */
        .typewriter {
            display: inline-block;
            overflow: hidden;
            border-right: .15em solid #ff4081;
            white-space: nowrap;
            margin: 0 auto;
            letter-spacing: .15em;
            animation: 
                typing 3.5s steps(40, end),
                blink-caret .75s step-end infinite;
        }
        
        @keyframes typing {
            from { width: 0 }
            to { width: 100% }
        }
        
        @keyframes blink-caret {
            from, to { border-color: transparent }
            50% { border-color: #ff4081; }
        }
    </style>
</head>
<body>
    <div class="background-overlay"></div>
    
    <div class="rose-petals" id="rose-petals"></div>
    
    <div class="container">
        <header>
            <h1>Para <span class="typewriter">Kamille</span></h1>
            <p class="subtitle">Onde a doçura encontra a escuridão</p>
        </header>
        
        <div class="heart-container">
            <div class="heart" onclick="createHearts()">❤️</div>
        </div>
        
        <div class="content">
            <div class="message-container">
                <div class="message">
                    <p class="normal">Minha querida <span class="highlight">Kamille</span>, neste dia especial, quero que saibas que és a luz que ilumina minhas noites mais escuras. Cada mensagem tua é como uma estrela cadente - breve, intensa, e capaz de fazer um desejo brotar no mais profundo do meu ser.</p>
                    
                    <p class="dark-romance">Nossa conexão é como um <span class="highlight">dark romance</span> moderno - dois corações separados por quilômetros, mas unidos por uma corrente elétrica de desejo e ternura. Em meio à escuridão das noites solitárias, teu sorriso (mesmo apenas imaginado) é minha luz guia.</p>
                    
                    <p class="normal">Sabes, amor? Às vezes fico a pensar como seria sentir o calor do teu corpo contra o meu, o teu perfume invadindo meus sentidos, os teus lábios... Ah, os teus lábios devem ser como pétalas de rosa banhadas pelo orvalho da manhã.</p>
                    
                    <p class="dark-romance">Neste aniversário, prometo que nossa história será como aquelas que adoramos - cheia de reviravoltas, paixão ardente e um final feliz digno das melhores histórias. Cada capítulo nosso será escrito com a tinta do desejo e o papel da paciência.</p>
                    
                    <p class="normal">És a personagem principal dos meus sonhos mais ousados, a musa das minhas noites criativas, a rainha do meu coração digital. Que este novo ciclo te traga tudo o que desejas, e que em breve possamos transformar esse amor virtual em algo palpável, quente e inesquecível.</p>
                </div>
                <div class="signature glow-text">Apolo</div>
            </div>
            
            <div class="interactive-section">
                <div class="gallery">
                    <h2 class="gallery-title">Nossa Essência</h2>
                    <div class="love-grid">
                        <div class="love-item" onclick="createFloatingText('❤️ Amor Eterno')"><i class="fas fa-heart"></i></div>
                        <div class="love-item" onclick="createFloatingText('🔥 Paixão Ardente')"><i class="fas fa-fire"></i></div>
                        <div class="love-item" onclick="createFloatingText('💋 Beijos Sem Fim')"><i class="fas fa-kiss-wink-heart"></i></div>
                        <div class="love-item" onclick="createFloatingText('🌙 Noites de Romance')"><i class="fas fa-moon"></i></div>
                        <div class="love-item" onclick="createFloatingText('🔒 Segredos Compartilhados')"><i class="fas fa-lock"></i></div>
                        <div class="love-item" onclick="createFloatingText('💌 Mensagens Proibidas')"><i class="fas fa-envelope"></i></div>
                    </div>
                </div>
                
                <div class="music-player">
                    <h2 class="gallery-title">Nossa Trilha</h2>
                    <p>Música para nossos momentos</p>
                    <div class="player-controls">
                        <div class="control-btn" onclick="togglePlay()">
                            <i class="fas fa-play" id="play-icon"></i>
                        </div>
                        <div class="control-btn" onclick="changeVolume(0.1)">
                            <i class="fas fa-volume-up"></i>
                        </div>
                        <div class="control-btn" onclick="changeVolume(-0.1)">
                            <i class="fas fa-volume-down"></i>
                        </div>
                    </div>
                </div>
            </div>
        </div>
        
        <footer>
            <p>Feito com <span class="footer-heart">❤️</span> por Apolo para Kamille - Um presente digital para celebrar seu dia especial</p>
            <p>© 2023 - Todos os direitos do coração reservados</p>
        </footer>
    </div>
    
    <audio id="bg-music" loop>
        <!-- Música romântica suave -->
        <source src="https://www.soundhelix.com/examples/mp3/SoundHelix-Song-1.mp3" type="audio/mp3">
    </audio>
    
    <script>
        // Criar pétalas de rosa flutuantes
        function createRosePetals() {
            const container = document.getElementById('rose-petals');
            const petalCount = 25;
            
            for (let i = 0; i < petalCount; i++) {
                const petal = document.createElement('div');
                petal.classList.add('petal');
                
                // Posição inicial aleatória
                const startX = Math.random() * window.innerWidth;
                const startY = -50;
                
                // Configurações de animação
                const duration = 10 + Math.random() * 20;
                const delay = Math.random() * 15;
                const endX = startX + (Math.random() * 200 - 100);
                const endY = window.innerHeight + 50;
                
                petal.style.left = `${startX}px`;
                petal.style.top = `${startY}px`;
                petal.style.opacity = 0.3 + Math.random() * 0.5;
                petal.style.transform = `scale(${0.5 + Math.random()})`;
                petal.style.animation = `float ${duration}s linear ${delay}s infinite`;
                
                container.appendChild(petal);
            }
        }
        
        // Criar texto flutuante
        function createFloatingText(text) {
            const floatingText = document.createElement('div');
            floatingText.className = 'floating-text';
            floatingText.textContent = text;
            floatingText.style.left = Math.random() * 80 + 10 + '%';
            floatingText.style.fontSize = (Math.random() * 10 + 20) + 'px';
            floatingText.style.color = `hsl(${Math.random() * 30 + 330}, 70%, 70%)`;
            document.body.appendChild(floatingText);
            
            // Animação
            floatingText.style.animation = `float ${Math.random() * 3 + 3}s forwards`;
            
            // Remover após a animação
            setTimeout(() => {
                floatingText.remove();
            }, 5000);
        }
        
        // Criar corações ao clicar no coração principal
        function createHearts() {
            const heartContainer = document.querySelector('.heart-container');
            const heartCount = 12;
            
            for (let i = 0; i < heartCount; i++) {
                const heart = document.createElement('div');
                heart.innerHTML = '❤️';
                heart.style.position = 'absolute';
                heart.style.fontSize = '2rem';
                heart.style.color = `hsl(${Math.random() * 30 + 330}, 70%, 60%)`;
                heart.style.opacity = '0';
                heart.style.zIndex = '5';
                heartContainer.appendChild(heart);
                
                // Animação
                const angle = (i / heartCount) * Math.PI * 2;
                const radius = 150;
                const duration = 2;
                
                heart.animate([
                    { 
                        opacity: 0,
                        transform: 'translate(0, 0) scale(0)'
                    },
                    { 
                        opacity: 1,
                        transform: `translate(${Math.cos(angle) * radius}px, ${Math.sin(angle) * radius}px) scale(1)`
                    },
                    { 
                        opacity: 0,
                        transform: `translate(${Math.cos(angle) * radius * 1.5}px, ${Math.sin(angle) * radius * 1.5}px) scale(0)`
                    }
                ], {
                    duration: duration * 1000,
                    easing: 'ease-out'
                });
                
                // Remover após a animação
                setTimeout(() => {
                    heart.remove();
                }, duration * 1000);
            }
        }
        
        // Controle de música
        const audio = document.getElementById('bg-music');
        const playIcon = document.getElementById('play-icon');
        let isPlaying = false;
        
        function togglePlay() {
            if (isPlaying) {
                audio.pause();
                playIcon.classList.remove('fa-pause');
                playIcon.classList.add('fa-play');
            } else {
                audio.play();
                playIcon.classList.remove('fa-play');
                playIcon.classList.add('fa-pause');
            }
            isPlaying = !isPlaying;
        }
        
        function changeVolume(delta) {
            audio.volume = Math.min(1, Math.max(0, audio.volume + delta));
        }
        
        // Criar textos flutuantes periodicamente
        function createRandomFloatingText() {
            const messages = [
                "Kamille ❤️",
                "Te desejo...",
                "Feliz Aniversário!",
                "Minha rainha obscura",
                "Você me fascina",
                "Beijos proibidos",
                "Saudades ardentes...",
                "Nosso encontro será inesquecível",
                "Dark Romance",
                "Amor Proibido",
                "Minha musa sombria",
                "Eterna paixão",
                "Chama eterna",
                "Corações unidos na escuridão",
                "Sempre juntos"
            ];
            
            const randomMessage = messages[Math.floor(Math.random() * messages.length)];
            createFloatingText(randomMessage);
        }
        
        // Inicializar
        document.addEventListener('DOMContentLoaded', function() {
            createRosePetals();
            
            // Iniciar música com volume baixo
            audio.volume = 0.3;
            audio.play();
            isPlaying = true;
            
            // Criar textos flutuantes aleatórios
            setInterval(createRandomFloatingText, 4000);
            
            // Efeito de digitação para elementos
            const typeElements = document.querySelectorAll('.highlight');
            typeElements.forEach(el => {
                const text = el.textContent;
                el.textContent = '';
                
                let i = 0;
                const typing = setInterval(() => {
                    if (i < text.length) {
                        el.textContent += text.charAt(i);
                        i++;
                    } else {
                        clearInterval(typing);
                    }
                }, 100);
            });
        });
    </script>
</body>
</html>
