<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Python-style Calculator</title>
</head>
<body>
    <h1>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Calculator</h1>
    <br><br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 
    <input type="number" id="display" placeholder="           Enter Values"> 
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
    <input type="number" id="result" placeholder="                Result"><br><br>

<pre>
               <button onclick="clearDisplay()">C</button>       <button onclick="inputvalue('(')">(</button>        <button onclick="inputvalue(')')">)</button>         <button onclick="backspace()">⌫</button>



               <button onclick="inputvalue('0')">0</button>       <button onclick="inputvalue('1')">1</button>        <button onclick="inputvalue('2')">2</button>         <button onclick="inputvalue('*')">*</button><br>


               <button onclick="inputvalue('3')">3</button>       <button onclick="inputvalue('4')">4</button>        <button onclick="inputvalue('5')">5</button>         <button onclick="inputvalue('-')"><b>-</b></button><br>


               <button onclick="inputvalue('6')">6</button>       <button onclick="inputvalue('7')">7</button>        <button onclick="inputvalue('8')">8</button>         <button onclick="inputvalue('+')">+</button><br>


               <button onclick="inputvalue('9')">9</button>       <button onclick="inputvalue('.')"><b>.</b></button>        <button onclick="inputvalue('**')">**</button>         <button onclick="inputvalue('//')">//</button><br>


                    <button onclick="inputvalue('%')">%</button>       <button onclick="inputvalue('^')">^</button>        <button onclick="calculate()">=</button>
</pre>

<script>
let display = document.getElementById('display');
let resultBox = document.getElementById('result');

function inputvalue(value) {
    display.value += value; // append text
}

function clearDisplay() {
    display.value = "";
    resultBox.value = "";
}

function backspace() {
    display.value = display.value.slice(0, -1);
}

function calculate() {
    try {
        // Replace ^ with ** for JS evaluation
        let expr = display.value.replace(/\^/g, '**');
        // Replace // with Math.floor division
        expr = expr.replace(/(\d+)\/\/(\d+)/g, (_, a, b) => Math.floor(a / b));
        resultBox.value = eval(expr);
    } catch (error) {
        resultBox.value = "Error";
    }
}
</script>
</body>
</html>
