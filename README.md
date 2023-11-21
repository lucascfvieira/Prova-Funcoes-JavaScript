<!DOCTYPE html>
<html lang="pt-br">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Calculadora de IMC</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      text-align: center;
      margin: 50px;
    }
  </style>
</head>
<body>

  <h2>Calculadora de IMC</h2>

  <label for="peso">Peso (kg): </label>
  <input type="number" id="peso" placeholder="Informe o peso" required>
  <br>

  <label for="altura">Altura (m): </label>
  <input type="number" id="altura" placeholder="Informe a altura" required>
  <br>

  <button onclick="calcularIMC()">Calcular IMC</button>
  
  <h3>Resultado do IMC: <span id="resultado"></span></h3>

  <script>
    function calcularIMC() {
      // Obtém os valores dos inputs
      var peso = document.getElementById('peso').value;
      var altura = document.getElementById('altura').value;

      // Verifica se os campos foram preenchidos
      if (peso === '' || altura === '') {
        alert('Por favor, preencha todos os campos.');
        return;
      }

      // Calcula o IMC
      var imc = peso / (altura * altura);

      // Exibe o resultado na tela
      document.getElementById('resultado').textContent = imc.toFixed(2);
    }
  </script>

</body>
</html>
