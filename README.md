<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Valentine Proposal 💖</title>
    <style>
        body {
            margin: 0;
            height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            background: linear-gradient(135deg, #ff758c, #ff7eb3);
            font-family: 'Poppins', sans-serif;
        }

        .card {
            background: #fff;
            width: 560px;
            padding: 50px 45px;
            border-radius: 28px;
            text-align: center;
            box-shadow: 0 25px 50px rgba(0,0,0,0.25);
            animation: pop 0.6s ease;
            position: relative;
        }

        @keyframes pop {
            0% { transform: scale(0.75); opacity: 0; }
            100% { transform: scale(1); opacity: 1; }
        }

        .emoji {
            font-size: 80px;
            margin-bottom: 15px;
        }

        h2 {
            color: #ff3366;
            margin: 14px 0;
            font-size: 30px;
        }

        p {
            color: #555;
            font-size: 19px;
            line-height: 1.6;
            margin-top: 10px;
        }

        .buttons {
            margin-top: 30px;
        }

        button {
            padding: 14px 34px;
            border: none;
            border-radius: 30px;
            font-size: 18px;
            cursor: pointer;
            transition: 0.3s;
            margin: 8px;
        }

        .yes {
            background: #ff3366;
            color: white;
        }

        .yes:hover {
            background: #e62e5c;
            transform: scale(1.08);
        }

        .no {
            background: #ddd;
            position: absolute;
        }
    </style>
</head>
<body>

<div class="card" id="card">
    <!-- FIRST PAGE -->
    <div class="emoji">😘😍🥰</div>
    <h2>Hey Babyyyyy ❤️💕</h2>
    <p>
        Babyyyyy 🥹<br><br>
        Every Valentine moment feels incomplete without you.<br><br>
        Will you accept my proposal to make this Valentine’s Day truly special? ❤️
    </p>

    <div class="buttons">
        <button class="yes" onclick="yesClicked()">Yes 😘🥰</button>
        <button class="no" id="noBtn" onmouseover="moveNo()">No 😡🙄</button>
    </div>
</div>

<script>
    function moveNo() {
        const btn = document.querySelector(".no");
        const card = document.querySelector(".card");

        const maxX = card.clientWidth - btn.offsetWidth - 20;
        const maxY = card.clientHeight - btn.offsetHeight - 20;

        btn.style.left = Math.random() * maxX + "px";
        btn.style.top = Math.random() * maxY + "px";
    }

    function yesClicked() {
        document.getElementById("card").innerHTML = `
            <div class="emoji">🥳🤩</div>
            <h2>I Knew It! 😍</h2>
            <p>
                You just made my day ❤️ even more special!<br><br>
                Every moment feels right with you.<br><br>
                I promise I will never leave you 🥹
            </p>
            <button class="yes" onclick="marriagePage()">
                Sweetheart, I have A one Question For You! 🧐🤨
            </button>
        `;
    }

    function marriagePage() {
        document.getElementById("card").innerHTML = `
            <div class="emoji">💍👰🤵</div>
            <h2>My Sweetheart 🥹❤️</h2>
            <p>
                From loving you… to choosing you…<br><br>
                Will you marry me and be mine forever? 💍💖
            </p>
            <div class="buttons">
                <button class="yes" onclick="finalPage()">YES 💞</button>
                <button class="no" onmouseover="moveNo()">NO 😝</button>
            </div>
        `;
    }

    function finalPage() {
        document.getElementById("card").innerHTML = `
            <div class="emoji">❤️💍💜</div>
            <h2>Forever Starts Now 😘😍</h2>
            <p>
                Thank you for choosing me 🥰<br><br>
                From Rose Day to Valentine’s Day,<br>
                From today tomorrow to forever I will alwaysssssss choose You My Bacchaa 😘😍
            </p>
        `;
    }
</script>

</body>
</html>
