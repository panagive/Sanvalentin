<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>San Valentín</title>
    <style>
        body {
            text-align: center;
            font-family: Arial, sans-serif;
            background-color: #ffccdd; /* Rosa pastel */
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
            background-image: radial-gradient(circle, rgba(255, 192, 203, 0.5) 10%, transparent 10%), 
                              radial-gradient(circle, rgba(255, 105, 180, 0.5) 10%, transparent 10%);
            background-size: 50px 50px;
            background-position: 0 0, 25px 25px;
        }
        .container {
            background-color: white;
            padding: 30px;
            border-radius: 15px;
            box-shadow: 0px 0px 10px rgba(0, 0, 0, 0.1);
            width: 80%;
            max-width: 400px;
        }
        img {
            width: 200px;
            border-radius: 10px;
        }
        .buttons {
            margin-top: 20px;
        }
        button {
            font-size: 20px;
            padding: 10px 20px;
            margin: 10px;
            cursor: pointer;
            border: none;
            border-radius: 5px;
        }
        #yes {
            background-color: #ff66b2;
            color: white;
        }
        #no {
            background-color: #666;
            color: white;
            position: absolute;
        }
        #message, #messageNo {
            font-size: 24px;
            color: red;
            display: none;
        }
    </style>
</head>
<body>

    <div class="container">
        <h1>¿Quieres ser mi San Valentín? ❤️</h1>
        <img src="gatitos.png" alt="Gatitos">
        <div class="buttons">
            <button id="yes" onclick="showLove()">Sí</button>
            <button id="no" onmouseover="moveNo()" onclick="noClicked()">No</button>
        </div>
        <p id="message">¡Sabía que dirías que sí! ❤️</p>
        <p id="messageNo">¡No es una opción! 😆</p>
    </div>

    <script>
        function showLove() {
            document.getElementById("message").style.display = "block";
            document.getElementById("no").style.display = "none";
        }

        function moveNo() {
            let button = document.getElementById("no");
            let x = Math.random() * (window.innerWidth - 100);
            let y = Math.random() * (window.innerHeight - 50);
            button.style.left = x + "px";
            button.style.top = y + "px";
        }

        function noClicked() {
            document.getElementById("messageNo").style.display = "block";
            document.getElementById("no").style.display = "none";
        }
    </script>

</body>
</html>
