# Momo-Birthday
# Happiestttt b'day to my momo💚🥟💋 
# Wishing-you-happy-birthday 

<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>For My MOMO🥟</title>
    <link href="https://fonts.googleapis.com/css2?family=Dancing+Script:wght@700&family=Poppins:wght@300;400;600&display=swap" rel="stylesheet">
    <style>
        :root {
            --pink: #ff85a1;
            --dark-pink: #ff4d7d;
            --soft-white: #fff5f7;
        }

        * { box-sizing: border-box; }

        body, html {
            margin: 0; padding: 0;
            min-height: 100%;
            font-family: 'Poppins', sans-serif;
            background-color: var(--soft-white);
            text-align: center;
            overflow-x: hidden;
        }

        .animation-overlay {
            position: fixed; top: 0; left: 0; width: 100%; height: 100%;
            pointer-events: none; z-index: 100;
        }

        .page {
            display: none;
            min-height: 100vh;
            width: 100vw;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            padding: 40px 20px;
            transition: all 0.5s ease;
        }

        .active { display: flex; animation: fadeIn 0.8s ease-out; }

        @keyframes fadeIn { 
            from { opacity: 0; transform: translateY(10px); } 
            to { opacity: 1; transform: translateY(0); } 
        }

        h1 { 
            font-family: 'Dancing Script', cursive; 
            color: var(--pink); 
            font-size: clamp(1.8rem, 8vw, 2.5rem); 
            text-shadow: 2px 2px #fff;
            margin: 15px 0;
        }

        .bhondu-img { 
            width: 85%; 
            max-width: 300px; 
            height: auto;
            max-height: 35vh;
            border-radius: 20px; 
            border: 6px solid white;
            box-shadow: 0 10px 25px rgba(255,133,161,0.2);
            object-fit: cover; 
            margin: 20px auto;
            animation: float 4s ease-in-out infinite;
        }

        @keyframes float {
            0%, 100% { transform: translateY(0) rotate(-1deg); }
            50% { transform: translateY(-12px) rotate(1deg); }
        }

        .collage-img {
            width: 90%;
            max-width: 450px;
            border-radius: 15px;
            border: 5px solid white;
            box-shadow: 0 8px 20px rgba(0,0,0,0.1);
            margin-bottom: 20px;
        }

        button, input {
            padding: 14px 28px; 
            border-radius: 30px;
            border: 2px solid var(--pink); 
            margin: 10px;
            font-size: 1rem; 
            outline: none;
            font-family: 'Poppins', sans-serif;
        }

        button {
            background: var(--pink); 
            color: white;
            cursor: pointer; 
            transition: 0.3s; 
            font-weight: 600;
            box-shadow: 0 4px 15px rgba(255,133,161,0.3);
        }

        button:hover { transform: scale(1.05); background: var(--dark-pink); }

        .gift-box { 
            font-size: 100px; 
            cursor: pointer; 
            animation: wobble 1.5s infinite; 
            margin: 30px 0;
        }

        @keyframes wobble {
            0%, 100% { transform: scale(1); }
            50% { transform: scale(1.1) rotate(5deg); }
        }

        .letter-container {
            background: rgba(255, 255, 255, 0.9);
            padding: 25px; 
            border-radius: 20px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.05);
            max-width: 500px; 
            width: 90%;
            line-height: 1.7; 
            border: 2px dashed var(--pink);
            margin-bottom: 20px;
        }

        .hindi-text { 
            font-size: 1.1rem; 
            color: #444; 
            padding: 0 15px; 
            font-weight: 500; 
            font-style: italic;
        }

        ::placeholder { color: #ccb; font-size: 0.9rem; }
    </style>
</head>
<body>

    <audio id="bg-music" loop>
        <source src="https://www.image2url.com/r2/default/audio/1778595272095-cfca3431-0cec-483e-80fd-d893a70b3caf.mp3" type="audio/mpeg">
    </audio>

    <div class="animation-overlay" id="anime"></div>

    <div class="page active" id="page1">
        <h1>For My Momooooooo... 🥟🥟</h1>
        <img src="https://i.postimg.cc/zB4r82QQ/Whats-App-Image-2026-05-12-at-19-48-55.jpg" class="bhondu-img" alt="Bhondu">
        <div style="width: 100%;">
            <input type="password" id="pass" placeholder="Secret code is 'momo'...">
            <br>
            <button onclick="checkPassword()">Unlock My Heart 🔑</button>
        </div>
    </div>

    <div class="page" id="page2">
        <h1>Happy Birthday! 🎂</h1>
        <img src="https://i.postimg.cc/m22cPtp8/Whats-App-Image-2026-05-12-at-20-00-27.jpg" class="collage-img" alt="Collage">
        <button onclick="nextPage(3)">See More ❤️</button>
    </div>

    <div class="page" id="page3">
        <h1 id="gift-msg">You have a gift!</h1>
        <div class="gift-box" id="box" onclick="openGift()">🎁</div>
        <div id="gift-content" style="display:none;">
            <img src="https://i.postimg.cc/cJN08z4v/Whats-App-Image-2026-05-12-at-19-48-54.jpg" class="bhondu-img" alt="Surprise">
            <p style="font-size: 1.2rem; color: var(--dark-pink); font-weight: 600;">my fav face in the world! ✨</p>
            <button onclick="nextPage(4)">Continue...</button>
        </div>
    </div>

    <div class="page" id="page4">
        <img src="https://i.postimg.cc/9FZWFVcj/Whats-App-Image-2026-05-12-at-19-48-56.jpg" class="momo-img" alt="Beauty">
        <div class="letter-container" style="border: none; background: none; box-shadow: none;">
            <p class="f-text">"To me you’re genuinely only and only most most most most special people of mine ever♾️.There’s something about you that makes me feel attached to you in a way I can’t even explain properly💚. Your presence feels comforting, your voice feels familiar, and even your smallest attention means a lot to me🥹. Without you things and days feel incomplete. You complete me♥️ 
You may not realize it, but you have this effect on me where my mood instantly changes because of you🫠. Out of everyone, you became the person I care about the most, the person I wait for, think about, miss and feel safest with💗.
To the world you may just be another person, but to me you’re my favourite feeling, safe spot, comfort person and tbh you are my  everything. 
I love you forever♥️💚"</p>
        </div>
        <button onclick="nextPage(5)">Finally, My Letter ✉️</button>
    </div>

    <div class="page" id="page5">
        <div class="letter-container">
            <p style="color: var(--dark-pink); font-size: 1.2rem;"><strong>Happy 20 baby♥️</strong></p>
            
            <p>
Honestly sometimes i still think about how crazy it is that someone living so far away became such an important part of my life..like you’re not even physically here but somehow you’re there in every part of my day🫠. every call, every random text, every little fight and every late night conversation means everything🥹. i don’t even know how to explain what you mean to me anymore because it’s so so so much more than just words now✨. I hope you feel so loved today because you genuinely deserve it😘. thank you for being in my life and being the biggest part of it 💋. I love you forever and endlessly i wish we celebrate all our b'days and special days together forever ♾️.
Happiest birthday to my mostttt favorite person ever💚</p>
        </div>
        <button onclick="location.reload()">Replay the Magic 🔄</button>
    </div>

    <script>
        function checkPassword() {
            const p = document.getElementById('pass').value;
            const music = document.getElementById('bg-music'); // Get audio element

            if(p.toLowerCase() === "momo") {
                // Play music when the button is clicked
                music.play().catch(e => console.log("Audio play failed:", e));
                nextPage(2);
            } else {
                alert("Wrong password! Hint: It's a food... momo🐼");
            }
        }

        function nextPage(num) {
            document.querySelectorAll('.page').forEach(p => p.classList.remove('active'));
            const next = document.getElementById('page' + num);
            next.classList.add('active');
            window.scrollTo(0, 0);
        }

        function openGift() {
            document.getElementById('box').style.display = 'none';
            document.getElementById('gift-msg').innerText = "Surprise for You!";
            document.getElementById('gift-content').style.display = 'block';
        }

        function createEmoji() {
            const emojis = ['❤️', '🥟', '💖', '✨', '🌸', '🐾'];
            const e = document.createElement('div');
            e.innerHTML = emojis[Math.floor(Math.random() * emojis.length)];
            e.style.position = 'fixed';
            e.style.left = Math.random() * 100 + 'vw';
            e.style.top = '110vh';
            e.style.fontSize = Math.random() * 20 + 15 + 'px';
            e.style.opacity = '0.8';
            e.style.transition = 'transform 6s linear, opacity 6s';
            e.style.zIndex = '100';
            document.getElementById('anime').appendChild(e);

            setTimeout(() => {
                e.style.transform = `translateY(-125vh) rotate(${Math.random() * 360}deg)`;
                e.style.opacity = '0';
            }, 100);

            setTimeout(() => e.remove(), 6500);
        }
        setInterval(createEmoji, 500);
    </script>
</body>
</html>
