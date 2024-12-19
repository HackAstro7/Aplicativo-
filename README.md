
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Calculadora Hacker - Double</title>
    <style>
        body {
            font-family: "Courier New", monospace;
            background-color: black;
            color: #00ff00;
            text-align: center;
            margin: 0;
            padding: 10px;
        }
        h1 {
            color: #00ff00;
            text-shadow: 0 0 10px #00ff00;
            margin-top: 5px;
            font-size: 30px;
        }
        .info-box {
            background: linear-gradient(135deg, #003300, #000000);
            color: #00ff00;
            border: 2px solid #00ff00;
            border-radius: 10px;
            padding: 15px;
            margin-bottom: 20px;
            font-size: 16px;
            box-shadow: 0 0 20px #00ff00;
        }
        .input-container {
            display: flex;
            justify-content: center;
            gap: 15px;
            margin-bottom: 15px;
        }
        input {
            width: 70px;
            height: 45px;
            text-align: center;
            font-size: 18px;
            border: 2px solid #00ff00;
            border-radius: 5px;
            background-color: black;
            color: #00ff00;
            box-shadow: 0 0 10px #00ff00;
        }
        button {
            background-color: #00ff00;
            color: black;
            border: 3px solid #00ff00;
            border-radius: 10px;
            padding: 10px 20px;
            font-size: 18px;
            font-weight: bold;
            cursor: pointer;
            box-shadow: 0 0 20px #00ff00;
            transition: all 0.3s ease-in-out;
            width: 200px;
            margin: 10px auto;
        }
        button:hover {
            background-color: #009900;
            color: white;
            box-shadow: 0 0 40px #00ff00;
        }
        .color-box {
            width: 100px;
            height: 100px;
            margin: 15px auto;
            border: 4px solid #00ff00;
            display: flex;
            align-items: center;
            justify-content: center;
            font-weight: bold;
            font-size: 24px;
            border-radius: 15px;
            box-shadow: 0 0 15px #00ff00;
            color: transparent;
            opacity: 0;
            transition: opacity 1s ease-in-out;
        }
        .message {
            margin-top: 15px;
            font-size: 20px;
            font-weight: bold;
        }
        .jetbet-title {
            margin-top: 20px;
            font-size: 22px;
            color: #00ff00;
            text-shadow: 0 0 15px #00ff00;
            font-weight: bold;
            opacity: 0;
            transition: opacity 1s ease-in-out;
        }
        iframe {
            margin-top: 30px;
            width: 100vw;
            height: 90vh;
            border: 4px solid #00ff00;
            border-radius: 15px;
            box-shadow: 0 0 25px #00ff00;
        }
        footer {
            margin-top: 30px;
            font-size: 14px;
            color: #555;
        }
    </style>
</head>
<body>
    <h1>🕵️ Calculadora Hacker - Double</h1>
    <div class="info-box">
        <p>Insira os últimos <strong>3 números</strong> que saíram no Double e clique em <strong>Calcular Entrada</strong>.</p>
        <p>⚠️ Este sistema só funciona na plataforma <strong>Jonbet</strong> abaixo!</p>
    </div>
    <div class="input-container">
        <input type="number" id="input1" min="0" max="14" required placeholder="">
        <input type="number" id="input2" min="0" max="14" required placeholder="">
        <input type="number" id="input3" min="0" max="14" required placeholder="">
    </div>
    <button onclick="calcularEntrada()">Calcular Entrada</button><div class="color-box" id="colorBox"></div>
    <div class="message" id="messageBox"></div>
    <div class="jetbet-title" id="jetbetMessage">🎲 Aposte Agora na jonbet ! 🎲</div>
    <iframe src="https://jon.ceo/r/vMzYw" title="JetBet365"></iframe>

    <footer>
        Desenvolvido com estilo hacker para análises 🔐 | JetBet365 Oficial
    </footer>

    <script>
        function calcularEntrada() {
            const n1 = parseInt(document.getElementById('input1').value) || 0;
            const n2 = parseInt(document.getElementById('input2').value) || 0;
            const n3 = parseInt(document.getElementById('input3').value) || 0;

            const colorBox = document.getElementById('colorBox');
            const messageBox = document.getElementById('messageBox');
            const jetbetMessage = document.getElementById('jetbetMessage');

            // Verificar se todos os números foram preenchidos
            if (!document.getElementById('input1').value || 
                !document.getElementById('input2').value || 
                !document.getElementById('input3').value) {
                // Tornar o quadro invisível
                colorBox.style.opacity = '0';
                colorBox.style.backgroundColor = 'transparent'; // Redefine a cor
                messageBox.innerText = "Preencha todos os números!";
                jetbetMessage.style.opacity = '0'; // Oculta a mensagem da JetBet365
                return;
            }

            const soma = n1 + n2 + n3;
            const isPar = soma % 2 === 0;

            // Efeito de suspense: Apagar a cor e exibir a mensagem
            colorBox.style.opacity = '0'; // Faz o quadrado desaparecer
            messageBox.innerText = "Calculando..."; // Mostra a mensagem de cálculo

            // Aguardar 1 segundo antes de mostrar a cor
            setTimeout(function() {
                if (isPar) {
                    colorBox.style.backgroundColor = "black";
                } else {
                    colorBox.style.backgroundColor = "red";
                }

                // Faz o quadrado reaparecer com a nova cor
                colorBox.style.opacity = '1';

                // Exibe a mensagem final
                messageBox.innerText = "Aposte até 2 gales no máximo!";

                // Exibe a mensagem da JetBet365
                jetbetMessage.style.opacity = '1';
            }, 1000); // 1 segundo de espera
        }
    </script>
</body>
</html>
