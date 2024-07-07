<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Calculadora de Holding Time</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            margin-top: 50px;
        }
        h1 {
            color: #333;
        }
        .result {
            font-size: 18px;
            margin-top: 20px;
        }
    </style>
</head>
<body>
    <h1>Calculadora de Holding Time</h1>
    <div>
        <p>Clique no botão para calcular a hora atual mais 60 horas:</p>
        <button onclick="calcularHora()">Calcular</button>
        <p class="result" id="resultado"></p>
    </div>

    <script>
        function calcularHora() {
            // Obter a data e hora atual
            let agora = new Date();

            // Adicionar 60 horas
            agora.setHours(agora.getHours() + 60);

            // Formatar a data e hora
            let dataFormatada = agora.toLocaleString('pt-BR', {
                weekday: 'long',
                year: 'numeric',
                month: 'long',
                day: 'numeric',
                hour: 'numeric',
                minute: 'numeric',
                second: 'numeric'
            });

            // Exibir o resultado na página
            document.getElementById('resultado').textContent = `Hora atual mais 60 horas: ${dataFormatada}`;
        }
    </script>
</body>
</html>
