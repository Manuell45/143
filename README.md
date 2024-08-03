<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Animated Letter</title>
    <link href="https://fonts.googleapis.com/css2?family=Le+Fointe&display=swap" rel="stylesheet">
    <style>
        body {
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            background-color: #f0f8ff;
            margin: 0;
        }

        .envelope {
            position: relative;
            width: 300px;
            height: 200px;
            background: #fff;
            border: 2px solid #ccc;
            border-radius: 10px;
            overflow: hidden;
            cursor: pointer;
        }

        .top-flap {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 50%;
            background: #fff;
            border: 2px solid #ccc;
            border-bottom: 0;
            border-top-left-radius: 10px;
            border-top-right-radius: 10px;
            transform-origin: bottom;
            transition: transform 1s;
        }

        .bottom-flap {
            position: absolute;
            bottom: 0;
            left: 0;
            width: 100%;
            height: 50%;
            background: #fff;
            border: 2px solid #ccc;
            border-top: 0;
            border-bottom-left-radius: 10px;
            border-bottom-right-radius: 10px;
            transform-origin: top;
            transition: transform 1s;
        }

        .letter {
            display: none;
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            text-align: center;
            font-family: 'Le Fointe', cursive;
            font-size: 24px;
            opacity: 0;
        }

        .letter span {
            display: inline-block;
            opacity: 0;
            animation: fadeIn 1s forwards;
        }

        @keyframes fadeIn {
            from {
                opacity: 0;
            }
            to {
                opacity: 1;
            }
        }
    </style>
</head>
<body>

<div class="envelope" onclick="openEnvelope()">
    <div class="top-flap"></div>
    <div class="bottom-flap"></div>
    <div class="letter" id="letter">
        <span>You made me the happiest person</span><br>
        <span>I've ever been.</span>
    </div>
</div>

<script>
    function openEnvelope() {
        const topFlap = document.querySelector('.top-flap');
        const bottomFlap = document.querySelector('.bottom-flap');
        const letter = document.getElementById('letter');
        
        topFlap.style.transform = 'rotateX(180deg)';
        bottomFlap.style.transform = 'rotateX(-180deg)';
        
        setTimeout(() => {
            letter.style.display = 'block';
            letter.style.opacity = '1';
            const spans = letter.querySelectorAll('span');
            spans.forEach((span, index) => {
                span.style.animationDelay = `${index * 1}s`;
            });
        }, 1000);
    }
</script>

</body>
</html>
