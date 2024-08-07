<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Data e Hora Atuais</title>
</head>
<body>

<button onclick="mostrarInformacoes()">Que dia é hoje?</button>

<p id="informacao"></p>

<script>
  function mostrarInformacoes() {
    const agora = new Date();
    let diaDaSemana;
    switch (agora.getDay()) {
      case 0:
        diaDaSemana = 'Domingo';
        break;
      case 1:
        diaDaSemana = 'Segunda-feira';
        break;
      case 2:
        diaDaSemana = 'Terça-feira';
        break;
      case 3:
        diaDaSemana = 'Quarta-feira';
        break;
      case 4:
        diaDaSemana = 'Quinta-feira';
        break;
      case 5:
        diaDaSemana = 'Sexta-feira';
        break;
      case 6:
        diaDaSemana = 'Sábado';
        break;
    }

    const data = agora.toLocaleDateString('pt-BR');
    const horas = agora.getHours().toString().padStart(2, '0');
    const minutos = agora.getMinutes().toString().padStart(2, '0');
    const horario = ${horas}:${minutos};

    document.getElementById("informacao").innerHTML = Hoje é ${diaDaSemana}, ${data} e agora são ${horario}.;
  }
</script>

</body>
</html>
