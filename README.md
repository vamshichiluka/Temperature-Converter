# Temperature-Converter
This is a simple Temperature Converter web application built using HTML5, CSS3, and JavaScript. The app allows users to easily convert temperatures between Celsius and Fahrenheit with a single click.

<!DOCTYPE html>
<html>
<head>
    <title>Temperature Converter</title>
</head>
<body>

    <h2>Temperature Converter</h2>
    
    <label>Enter Temperature:</label>
    <input type="number" id="tempInput">
    
    <select id="conversionType">
        <option value="CtoF">Celsius to Fahrenheit</option>
        <option value="FtoC">Fahrenheit to Celsius</option>
    </select>

    <button onclick="convertTemperature()">Convert</button>

    <p id="result"></p>

    <script>
        function convertTemperature() {
            let temp = parseFloat(document.getElementById("tempInput").value);
            let conversionType = document.getElementById("conversionType").value;
            let result;

            if (isNaN(temp)) {
                result = "Please enter a valid number.";
            } else if (conversionType === "CtoF") {
                result = temp + "°C = " + ((temp * 9/5) + 32).toFixed(2) + "°F";
            } else {
                result = temp + "°F = " + ((temp - 32) * 5/9).toFixed(2) + "°C";
            }

            document.getElementById("result").innerText = result;
        }
    </script>

</body>
</html>
