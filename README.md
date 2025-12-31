# Surprise-
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Happy New Year ❤️</title>
    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Poppins', sans-serif;
        }

        body {
            background: linear-gradient(135deg, #0f2027, #203a43, #2c5364);
            color: white;
            min-height: 100vh;
            text-align: center;
            overflow-x: hidden;
        }

        .container {
            padding: 40px 20px;
            max-width: 900px;
            margin: auto;
        }

        h1 {
            font-size: 3rem;
            margin-bottom: 10px;
            animation: fadeIn 2s ease;
        }

        h2 {
            font-weight: 300;
            margin-bottom: 30px;
            animation: fadeIn 3s ease;
        }

        .heart {
            font-size: 60px;
            animation: pulse 1.5s infinite;
            margin-bottom: 20px;
        }

        .countdown {
            display: flex;
            justify-content: center;
            gap: 15px;
            margin: 30px 0;
        }

        .time-box {
            background: rgba(255,255,255,0.15);
            padding: 15px 20px;
            border-radius: 10px;
            min-width: 80px;
        }

        .time-box span {
            font-size: 2rem;
            font-weight: bold;
        }

        .time-box p {
            font-size: 0.8rem;
            opacity: 0.8;
        }

        .message {
            margin: 40px 0;
            font-size: 1.2rem;
            line-height: 1.8;
            animation: fadeInUp 2s ease;
        }

        button {
            background: #ff4b5c;
            color: white;
            border: none;
            padding: 15px 30px;
            font-size: 1rem;
            border-radius: 30px;
            cursor: pointer;
            transition: 0.3s;
        }

        button:hover {
            background: #ff1e38;
            transform: scale(1.05);
        }

        .letter {
            display: none;
            margin-top: 30px;
            background: rgba(0,0,0,0.4);
            padding: 25px;
            border-radius: 15px;
            animation: fadeInUp 1.5s ease;
        }

        footer {
            margin-top: 60px;
            font-size: 0.8rem;
            opacity: 0.6;
        }

        @keyframes pulse {
            0% { transform: scale(1); }
            50% { transform: scale(1.2); }
            100% { transform: scale(1); }
        }

        @keyframes fadeIn {
            from { opacity: 0; }
            to { opacity: 1; }
        }

        @keyframes fadeInUp {
            from { opacity: 0; transform: translateY(30px); }
            to { opacity: 1; transform: translateY(0); }
        }
    </style>
</head>
<body>

<div class="container">

    <div class="heart">❤️</div>

    <h1>Happy New Year, My Love</h1>
    <h2>Another year, still choosing you.</h2>

    <div class="countdown">
        <div class="time-box">
            <span id="days">00</span>
            <p>Days</p>
        </div>
        <div class="time-box">
            <span id="hours">00</span>
            <p>Hours</p>
        </div>
        <div class="time-box">
            <span id="minutes">00</span>
            <p>Minutes</p>
        </div>
        <div class="time-box">
            <span id="seconds">00</span>
            <p>Seconds</p>
        </div>
    </div>

    <div class="message">
        This year gave me memories, lessons, and moments—  
        but the best part of it was **you**.  
        <br><br>
        I don’t know what the future holds,  
        but I know who I want in it.
    </div>

    <button onclick="showLetter()">Click for my heart 💌</button>

    <div class="letter" id="letter">
        <p>
            My love,<br><br>
            As this year ends, I just want you to know—  
            you are my safest place, my favorite thought,  
            and the reason I believe in tomorrow.  
            <br><br>
            I promise to love you harder,  
            listen better, and choose you every single day.  
            <br><br>
            Happy New Year ❤️  
            Here’s to us, and everything we’re yet to become.
        </p>
    </div>

    <footer>
        Made with love, just for you ✨
    </footer>

</div>

<script>
    function showLetter() {
        document.getElementById("letter").style.display = "block";
    }

    // Countdown Timer
    const newYear = new Date("January 1, 2026 00:00:00").getTime();

    setInterval(() => {
        const now = new Date().getTime();
        const distance = newYear - now;

        const days = Math.floor(distance / (1000 * 60 * 60 * 24));
        const hours = Math.floor((distance % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
        const minutes = Math.floor((distance % (1000 * 60 * 60)) / (1000 * 60));
        const seconds = Math.floor((distance % (1000 * 60)) / 1000);

        document.getElementById("days").innerText = days;
        document.getElementById("hours").innerText = hours;
        document.getElementById("minutes").innerText = minutes;
        document.getElementById("seconds").innerText = seconds;
    }, 1000);
</script>

</body>
</html>
