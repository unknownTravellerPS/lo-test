
<!DOCTYPE html>
<html>
<head>
    <title>Yousef Calculator</title>
    <meta charset="utf-8" />
</head>
<body>
<h1>Welcome to Yousef Abu Al- felat Calculator Test</h1>

<p>n1</p>
<input type="number" id="one" />
<p>n2</p>
<input type="number" id="two" />
<p>n3</p>
<input type="number" id="three" />
<p>n4</p>
<input type="number" id="four" />

<br><br>

<button onclick="calculate('add')">Sum</button>
<button onclick="calculate('subtract')">Subtract</button>
<button onclick="calculate('multiply')">Multiply</button>
<button onclick="calculate('divide')">Divide</button>

<script>
    function calculate(operation) {
        // Get input values and convert to numbers
        var one = Number(document.getElementById("one").value) || 0;
        var two = Number(document.getElementById("two").value) || 0;
        var three = Number(document.getElementById("three").value) || 0;
        var four = Number(document.getElementById("four").value) || 0;

        var result;

        if (operation === "add") {
            result = one + two + three + four;
        } else if (operation === "subtract") {
            result = one - two - three - four;
        } else if (operation === "multiply") {
            result = one * two * three * four;
        } else if (operation === "divide") {
            // Treat blank values as 1 to avoid infinity
            one = one || 1;
            two = two || 1;
            three = three || 1;
            four = four || 1;
            result = one / two / three / four;
        }

        alert("Result: " + result);
    }
</script>
</body>
</html>
