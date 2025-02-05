<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Rodela's Portfolio</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: Arial, sans-serif;
            background-color: #f0f0f0;
            height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            flex-direction: column;
        }

        .container {
            text-align: center;
        }

        .rose-container {
            position: relative;
            width: 100px;
            height: 100px;
            margin-bottom: 20px;
            animation: bloom 5s ease-out forwards;
        }

        .rose {
            position: absolute;
            top: 50%;
            left: 50%;
            width: 20px;
            height: 20px;
            background-color: #ff007f;
            border-radius: 50%;
            transform: translate(-50%, -50%);
        }

        .petal {
            position: absolute;
            top: 50%;
            left: 50%;
            width: 30px;
            height: 10px;
            background-color: #ff007f;
            border-radius: 20px;
            transform-origin: center center;
            opacity: 0;
            transition: opacity 0.5s ease;
        }

        .petal:nth-child(1) {
            transform: translate(-50%, -50%) rotate(0deg);
        }

        .petal:nth-child(2) {
            transform: translate(-50%, -50%) rotate(90deg);
        }

        .petal:nth-child(3) {
            transform: translate(-50%, -50%) rotate(180deg);
        }

        .petal:nth-child(4) {
            transform: translate(-50%, -50%) rotate(270deg);
        }

        @keyframes bloom {
            0% {
                transform: scale(0);
                opacity: 0;
            }
            100% {
                transform: scale(1);
                opacity: 1;
            }
        }

        .rose-container.blooming .petal {
            opacity: 1;
            transform: translate(-50%, -50%) scale(1);
        }

        .intro-text h1 {
            font-size: 36px;
            color: #333;
        }

        .intro-text p {
            font-size: 18px;
            color: #777;
            margin-top: 10px;
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="rose-container">
            <div class="rose">
                <div class="petal"></div>
                <div class="petal"></div>
                <div class="petal"></div>
                <div class="petal"></div>
            </div>
        </div>
        <div class="intro-text">
            <h1>Welcome to Rodela's Portfolio</h1>
            <p>Explore my work, projects, and journey!</p>
        </div>
    </div>

    <script>
        window.onload = function() {
            const roseContainer = document.querySelector('.rose-container');
            roseContainer.classList.add('blooming');
        };
    </script>
</body>
</html>
