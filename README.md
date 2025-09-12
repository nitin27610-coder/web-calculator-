# web-calculator-
web calculator using HTML + JAVA SCRPT
<!DOCTYPE html>
<html lang="en"
<head>
    <meta chargeset="UTF-8"
    <meta name="viewport"
    content="width=device-width,initial-scale=1.0">
    <title> APNA CALCULATOR </title>
    <head>
        <body>
<pre><h1><strong><BIG><header>                 CALCULATOR </header></strong></h1></pre>
    <ul><br><li> Welcome to<strong> APNA CALCULATOR</strong></li><br><li>Stop counting on fingers, Start using APNA CALCULATOR</li><br><li>Your Pocket-Friendly Math Assistant</li></ul>
    <input id="num1" type="number"
       placeholder="enter the first number">
    <input type="number" id="Num2"
    placeholder="enter the second number">
    <select id="operation">
    <option value="+">+</option>
        <option value="-">-</option>
            <option value="*">*</option>
                <option value="/">/</option>
                    <option value="**">**</option>
                        <option value="%">%</option>
                            </select>
                            <br><br><button onclick="calculate()">calculate</button>
                            <P id="result"></P>

                            <script>
                                function calculate() {
                            let num1 = parsefloat(document.getElementById("num1").value);
let num2 = parsefloat(documen.getElementById("num2").value);
let operation = document.getElementById("operation").value;
if (operation === "+") {
    result=num1+num2;
} else if (operation === "-") {
    result=num1-num2;
} else if (operation === "*") {
    result=num1*num2;
} else if (operation === "/") {
    result=num1/num2;
} else if (operation === "**") {
    result=num1**num2;
} else if (operation === "//") {
    result=num1//num2;
} else if (operation === "%") {
    result=num1%num2;
}else{
    result="invalid operation";
}
document.getElementById("result").innerText = "result:" + result;
                                }
                                </scrpt>
                                </body>
                                </html>
