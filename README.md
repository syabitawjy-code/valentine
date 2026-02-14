<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Ruang Kenangan Cinta - Hadiah Valentine</title>
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600&display=swap" rel="stylesheet">
    <style>
        body {
            font-family: 'Poppins', sans-serif;
            background: linear-gradient(to bottom, #FFF8DC, #FFB6C1);
            color: #8B0000;
            margin: 0;
            padding: 0;
            overflow-x: hidden;
        }
        .container {
            max-width: 800px;
            margin: 0 auto;
            padding: 20px;
            text-align: center;
        }
        .section {
            opacity: 0;
            transform: translateY(50px);
            transition: all 1s ease;
            margin-bottom: 50px;
        }
        .section.visible {
            opacity: 1;
            transform: translateY(0);
        }
        .mystery-message {
            font-size: 2em;
            font-weight: 600;
            margin: 50px 0;
            animation: fadeIn 2s ease-in;
        }
        @keyframes fadeIn {
            from { opacity: 0; }
            to { opacity: 1; }
        }
        .story, .moments, .notes, .messages {
            background: rgba(255, 255, 255, 0.8);
            border-radius: 15px;
            padding: 20px;
            box-shadow: 0 4px 8px rgba(0,0,0,0.1);
        }
        .moment {
            margin: 10px 0;
            cursor: pointer;
            transition: transform 0.3s;
        }
        .moment:hover {
            transform: scale(1.05);
        }
        .surprise {
            display: none;
            background: #8B0000;
            color: #FFF8DC;
            padding: 20px;
            border-radius: 15px;
            margin-top: 50px;
        }
        .surprise.visible {
            display: block;
        }
        button {
            background: #FFB6C1;
            border: none;
            padding: 10px 20px;
            border-radius: 10px;
            cursor: pointer;
            font-weight: 600;
            transition: background 0.3s;
        }
        button:hover {
            background: #8B0000;
            color: white;
        }
        .heart {
            color: #8B0000;
            font-size: 1.5em;
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="section mystery-message">
            <p>Psst... Ada sesuatu yang spesial niiichh. klikk disinii yaww cayang. siap? â¤ï¸</p>
            <button onclick="startJourney()">Mulai Perjalanan</button>
        </div>

        <div id="story" class="section story">
            <h2>Perjalanan Cinta Kita</h2>
            <p>Dari pertemuan pertama kita yg di primadini, we notice each other eyes and thats it.We have our story in bogor ð</p>
        </div>

        <div id="moments" class="section moments">
            <h2>Momen-Momen Bermakna</h2>
            <div class="moment" onclick="revealMoment(this)">Waktu kita di ancol hehe itu funn sii dan waktu kita ldr 5 bulan, we've been through a lot yaa honey :( but we did itt !</div>
            <div class="moment" onclick="revealMoment(this)">Sarapan pagi bareng, kamu masakin ayam, makan nasi kak sri, kita masakk barengg.</div>
            <div class="moment" onclick="revealMoment(this)">aku kangen kita yg di apart , kalo bisaaa pengenn kalii kuulangg lagii wkwkw, kamuu gituu gaa.</div>
        </div>

        <div id="notes" class="section notes">
            <h2>Hal-Hal yang Aku Sukai dari Dirimu</h2>
            <p>gantenggg, my typeee and ngertiin aku kaliii, talentedd,kamu yg ngasih tau kalo gapapa ga harus selalu kuatt. makasii ya sayanggg. ð</p>
        </div>

        <div id="messages" class="section messages">
            <h2>Pesan dari Hati</h2>
            <p>Aku ga jago ngomong romantis, tapi aku mau bilang: u are my home. with u, everything feels right . Aku cinta kamu, lebih dari kata-kata bisa kubilang. yokk, lanjut ke surprise?</p>
            <button onclick="showSurprise()">Klik untuk Surprise!</button>
        </div>

        <div id="surprise" class="section surprise">
            <h2>Surprise! â¤ï¸</h2>
            <p>Wow, kamu sampai sini! Aku mau bilang, masa depan kita bakal banyak adventure lagi. I hope kita bisa terus ketawa, saling dukung, and bikin kenangan baru. Makasii karena kamu ada, cus trust me. U are my biggest gift. Happy Valentine, sayang. I love foreverr. ð</p>
        </div>
    </div>

    <script>
        let sections = document.querySelectorAll('.section');
        let surprise = document.getElementById('surprise');

        function startJourney() {
            sections.forEach((section, index) => {
                setTimeout(() => {
                    section.classList.add('visible');
                }, index * 1000);
            });
        }

        function revealMoment(element) {
            element.innerHTML += ' <span class="heart">â¤ï¸</span>';
        }

        function showSurprise() {
            surprise.classList.add('visible');
        }

        // Auto-reveal on scroll to bottom
        window.addEventListener('scroll', () => {
            if (window.innerHeight + window.scrollY >= document.body.offsetHeight) {
                surprise.classList.add('visible');
            }
        });
    </script>
</body>
</html>+

