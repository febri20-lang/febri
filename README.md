<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Ucapan Valentine</title>
    <style>
        body {
            background-color: pink;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
            font-family: Arial, sans-serif;
        }

        .envelope {
            width: 200px;
            height: 120px;
            background-color: white;
            border: 2px solid #ccc;
            border-radius: 5px;
            position: relative;
            cursor: pointer;
            transition: transform 0.3s;
        }

        .envelope:before {
            content: '';
            position: absolute;
            top: -20px;
            left: 0;
            width: 0;
            height: 0;
            border-left: 100px solid transparent;
            border-right: 100px solid transparent;
            border-bottom: 20px solid white;
        }

        .message {
            display: none;
            text-align: center;
            margin-top: 20px;
            font-size: 20px;
            color: #ff69b4;
        }

        .envelope.open {
            transform: translateY(-20px);
        }
    </style>
</head>
<body>

    <div class="envelope" onclick="openEnvelope(this)">
        <div class="message">Happy Valentine's Day Widya</div>
    </div>

    <script>
        function openEnvelope(element) {
            element.classList.toggle('open');
            const message = element.querySelector('.message');
            message.style.display = message.style.display === 'block' ? 'none' : 'block';
        }
    </script>

</body>
</html>
