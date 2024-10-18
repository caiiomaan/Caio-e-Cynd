<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Nosso Amor</title>
    <style>
        body, html {
            margin: 0;
            padding: 0;
            width: 100%;
            height: 100%;
            display: flex;
            justify-content: center;
            align-items: center;
            background: url('cyndeeu.jpeg') no-repeat center center fixed;
            background-size: cover;
            color: white;
            text-align: center;
            font-family: Arial, sans-serif;
        }
        .container {
            background: rgba(0, 0, 0, 0.5);
            padding: 20px;
            border-radius: 15px;
        }
        .amor {
            font-size: 2em;
            margin-bottom: 10px;
        }
        .contador {
            font-size: 1.5em;
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="amor">Nosso amor cresce a cada segundo!</div>
        <div class="contador" id="contador"></div>
    </div>

    <script>
        function atualizarContador() {
            const dataInicio = new Date('2024-07-20T00:00:00');
            const agora = new Date();
            const diferenca = agora - dataInicio;

            const segundos = Math.floor(diferenca / 1000) % 60;
            const minutos = Math.floor(diferenca / 1000 / 60) % 60;
            const horas = Math.floor(diferenca / 1000 / 60 / 60);

            document.getElementById('contador').innerText = 
                `${horas} horas, ${minutos} minutos e ${segundos} segundos de namoro`;
        }

        setInterval(atualizarContador, 1000);
    </script>
</body>
</html>
