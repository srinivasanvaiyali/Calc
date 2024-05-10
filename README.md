# Ex.08 Design of a Standard Calculator
## Date:10/05/2024

## AIM:
To design a web application for a standard calculator with minimum five operations.

## DESIGN STEPS:

### Step 1:
Clone the github repository and create Django admin interface.

### Step 2:
Change settings.py file to allow request from all hosts.

### Step 3:
Use CSS for creating attractive colors.

### Step 4:
Write JavaScript program for implementing five different operations.

### Step 5:
Validate the HTML and CSS code.

### Step 6:
Publish the website in the given URL.

## PROGRAM :
```C
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <style>
    body {
      margin: 0;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      min-height: 100vh;
      background-color: #333;
      color: #fff;
      font-family: 'Arial', sans-serif;
    }
    #header {
      font-size: 24px;
      margin-bottom: 10px;
    }
    #calculator {
      background-color:lightgreen;
      border-radius: 10px;
      box-shadow: 0 0 10px rgba(0, 0, 0, 0.2);
      padding: 20px;
      text-align: center;
      margin-top: 20px;
    }
    input {
      width: 100%;
      margin-bottom: 10px;
      padding: 10px;
      font-size: 18px;
      background-color: #444;
      color: #000; /* Contrasting color for white background */
      border: none;
      border-radius: 5px;
    }
    button {
      width: 50px;
      height: 50px;
      margin: 5px;
      font-size: 18px;
      cursor: pointer;
      border: none;
      border-radius: 5px;
      background-color: #3498db;
      color: #fff;
    }
    button.operator {
      background-color: #e74c3c;
    }
    button.equal {
      background-color: #2ecc71;
    }
    button.clear {
      background-color: #95a5a6;
      color: #333;
    }
    button.extra {
      background-color: #f39c12;
    }
  </style>
</head>
<body>

<div id="header">STANDARD CALCULATOR
  <hr>
     SRINIVASAN.V(21222043008)</div>

<div id="calculator">
  <input type="text" id="display" disabled>
  <br>
  <button onclick="appendToDisplay('7')">7</button>
  <button onclick="appendToDisplay('8')">8</button>
  <button onclick="appendToDisplay('9')">9</button>
  <button class="operator" onclick="appendToDisplay('/')">/</button>
  <br>
  <button onclick="appendToDisplay('4')">4</button>
  <button onclick="appendToDisplay('5')">5</button>
  <button onclick="appendToDisplay('6')">6</button>
  <button class="operator" onclick="appendToDisplay('*')">*</button>
  <br>
  <button onclick="appendToDisplay('1')">1</button>
  <button onclick="appendToDisplay('2')">2</button>
  <button onclick="appendToDisplay('3')">3</button>
  <button class="operator" onclick="appendToDisplay('-')">-</button>
  <br>
  <button onclick="appendToDisplay('0')">0</button>
  <button class="clear" onclick="clearDisplay()">C</button>
  <button class="equal" onclick="calculateResult()">=</button>
  <button class="operator extra" onclick="appendToDisplay('%')">%</button>
  <br>
  <button class="extra" onclick="appendToDisplay('Math.sqrt(')">√</button>
  <button class="extra" onclick="appendToDisplay('Math.pow(')">x^y</button>
  <button class="extra" onclick="appendToDisplay('Math.sin(')">sin</button>
  <button class="extra" onclick="appendToDisplay('Math.cos(')">cos</button>
  <br>
  <button class="extra" onclick="appendToDisplay('Math.tan(')">tan</button>
  <button class="extra" onclick="appendToDisplay('Math.log10(')">log10</button>
  <button class="extra" onclick="appendToDisplay('Math.log(')">ln</button>
  <button class="extra" onclick="appendToDisplay('(')">(</button>
  <br>
  <button class="extra" onclick="appendToDisplay(')')">)</button>
  <button class="operator" onclick="appendToDisplay('+')">+</button>
  <button class="extra" onclick="appendToDisplay('Math.PI')">π</button>
  <button class="extra" onclick="appendToDisplay('Math.E')">e</button>
</div>

<script>
  function appendToDisplay(value) {
    document.getElementById('display').value += value;
  }

  function clearDisplay() {
    document.getElementById('display').value = '';
  }

  function calculateResult() {
    try {
      // Replace '^' with 'Math.pow'
      const expression = document.getElementById('display').value.replace(/\^/g, 'Math.pow');
      document.getElementById('display').value = eval(expression);
    } catch (error) {
      document.getElementById('display').value = 'Error';
    }
  }
</script>

</body>
</html>
```

## OUTPUT:
![Screenshot (73)](https://github.com/srinivasanvaiyali/Calc/assets/145117665/a3d8838b-6bf7-484b-b7fe-2e6d1c74908e)
![Screenshot (74)](https://github.com/srinivasanvaiyali/Calc/assets/145117665/3b01de56-ad6c-4f38-9232-2651a250a519)



## RESULT:
The program for designing a standard calculator using HTML and CSS is executed successfully.
