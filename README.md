# html-calculator
<!DOCTYPE html>
<html>
<head>
    <title>Scientific Calculator</title>
    <style>
        /* CSS styling for the calculator layout */
        .calculator {
            width: 250px;
            padding: 10px;
            border: 1px solid #ccc;
            background-color: #f9f9f9;
        }

        .calculator input {
            width: 100%;
            margin-bottom: 5px;
        }

        .calculator .row {
            display: flex;
        }

        .calculator .row .button {
            flex: 1;
            margin-right: 5px;
        }
    </style>
</head>
<body>
    <div class="calculator">
        <input type="text" id="result" readonly>

        <div class="row">
            <input type="button" class="button" value="7" onclick="appendToResult('7')">
            <input type="button" class="button" value="8" onclick="appendToResult('8')">
            <input type="button" class="button" value="9" onclick="appendToResult('9')">
            <input type="button" class="button" value="/" onclick="appendToResult('/')">
        </div>

        <div class="row">
            <input type="button" class="button" value="4" onclick="appendToResult('4')">
            <input type="button" class="button" value="5" onclick="appendToResult('5')">
            <input type="button" class="button" value="6" onclick="appendToResult('6')">
            <input type="button" class="button" value="*" onclick="appendToResult('*')">
        </div>

        <div class="row">
            <input type="button" class="button" value="1" onclick="appendToResult('1')">
            <input type="button" class="button" value="2" onclick="appendToResult('2')">
            <input type="button" class="button" value="3" onclick="appendToResult('3')">
            <input type="button" class="button" value="-" onclick="appendToResult('-')">
        </div>

        <div class="row">
            <input type="button" class="button" value="0" onclick="appendToResult('0')">
            <input type="button" class="button" value="." onclick="appendToResult('.')">
            <input type="button" class="button" value="=" onclick="calculateResult()">
            <input type="button" class="button" value="+" onclick="appendToResult('+')">
        </div>

        <div class="row">
            <input type="button" class="button" value="sqrt" onclick="calculateSquareRoot()">
            <input type="button" class="button" value="^" onclick="appendToResult('**')">
            <input type="button" class="button" value="C" onclick="clearResult()">
        </div>
    </div>

    <script>
        // JavaScript code for calculator functionality
        function appendToResult(value) {
            document.getElementById("result").value += value;
        }

        function calculateResult() {
            var result = eval(document.getElementById("result").value);
            document.getElementById("result").value = result;
        }

        function calculateSquareRoot() {
            var result = Math.sqrt(eval(document.getElementById("result").value));
            document.getElementById("result").value = result;
        }

        function clearResult() {
            document.getElementById("result").value = "";
        }
    </script>
</body>
</html>
