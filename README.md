<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Love Letter</title>
    <style>
        body {
            font-family: 'Georgia', serif;
            background-color: #f7e7ce;
            color: #333;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
            text-align: center;
        }

        .letter {
            background: #fff;
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0 4px 10px rgba(0, 0, 0, 0.2);
            max-width: 600px;
            width: 100%;
        }

        h1 {
            font-size: 2em;
            color: #e60073;
        }

        p {
            font-size: 1.2em;
            line-height: 1.6em;
        }

        .message {
            margin: 20px 0;
        }

        button {
            background-color: #e60073;
            color: #fff;
            border: none;
            padding: 10px 20px;
            font-size: 1.5em;
            border-radius: 50px;
            cursor: pointer;
            transition: background-color 0.3s ease;
        }

        button:hover {
            background-color: #ff66a3;
        }

        .hidden-message {
            display: none;
            margin-top: 20px;
            font-style: italic;
            color: #333;
        }
    </style>
</head>
<body>
    <div class="letter">
        <h1>To My Love</h1>
        <p class="intro">I wanted to write you a little something...</p>
        <div class="message">
            <p>Click the heart below to reveal my true feelings.</p>
        </div>
        <button id="revealButton">❤️</button>
        <p class="hidden-message" id="hiddenMessage">
            hiii matty, i know its been on and off lately. at this day i asked you to be my boyfriend. its been 4.43 weeks, 774 hrs, and 44,640 mins. 
            that i meet you. and i did not regret doing that. you made me feel alive again that day. even everything
            were so random, i still got your hands. never afraid to show your love on mine. 
            im bless to have you sana ikaw rin sa akin. you mean so much to me. and always choose to choose you. mwuaaaaa
        </p>
    </div>
    <script>
        document.getElementById('revealButton').addEventListener('click', function() {
            const hiddenMessage = document.getElementById('hiddenMessage');
            hiddenMessage.style.display = 'block';
        });
    </script>
</body>
</html>
