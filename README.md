<!DOCTYPE html>
<html lang="pt">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Calculadora Simples</title>
 
  <p>Calculadora Simples</p>
  <style>
 body {
  font-family: Arial, sans-serif;
}

.calculator {
  display: flex;
  flex-direction: column;
  width: 300px;
  margin: auto;
  border: 10px;
}

.display {
  margin-bottom: 20px;
  text-align: right;
  padding: 10px;
  background-color: #f2f2f2;
}

.buttons {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 5px;
}

button {
  padding: 10px;
  font-size: 15px;
}

.borda {
  margin: auto;
  width: 300px;
}

</style>
</head>
<body>
<div class="calculator">
  <input type="text" id="display" class="display" disabled>
  <div class="buttons">
    <button onclick="press('1')">1</button>
    <button onclick="press('2')">2</button>
    <button onclick="press('3')">3</button>
    <button onclick="press('+')">+</button>
    <button onclick="press('4')">4</button>
    <button onclick="press('5')">5</button>
    <button onclick="press('6')">6</button>
    <button onclick="press('-')">-</button>
    <button onclick="press('7')">7</button>
    <button onclick="press('8')">8</button>
    <button onclick="press('9')">9</button>
    <button onclick="press('')"></button>
    <button onclick="press('C')">C</button>
    <button onclick="press('0')">0</button>
    <button onclick="press('=')">=</button>
    <button onclick="press('/')">/</button>
  </div>
</div>
<script>
  let display = document.getElementById('display');

  function press(num) {
    if(num === '=') {
      display.value = eval(display.value);
    } else if(num === 'C') {
      display.value = '';
    } else {
      display.value += num;
    }
  }
</script>
</body>
</html>
