# Standard Calculator

# Calc.html
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Calculator</title>
    <style>
    body {
        font-family: Arial, sans-serif;
        display: flex;
        align-items: center;
        justify-content: center;
        height: 100vh;
        background-color: #ffffff;
        flex-direction: column;
        background: url(img.jpg);
        background-size: cover;
    }

    #calculator {
        border: 2px solid #d0c60b;
        border-radius: 5px;
        padding: 60px;
        text-align: center;
        box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
        background-color: #3d749f;


    }

    input[type="text"] {
        width: 100%;
        padding: 10px;
        margin-bottom: 10px;
        font-size: 18px;
    
    }

    input[type="button"] {
        width: 60px;
        height: 60px;
        font-size: 25px;
        margin: 5px;
        cursor: pointer;
        border-radius: 10px;
        font-weight:bolder;
        

    }

    input[type="button"]:hover {
        background-color: #eee;
    }

    #clear {
        background-color: rgb(22, 46, 231);
        color: #fff;
    }
    #display{
        margin-right: 60px;
        border: 4px solid black;
    }
    .name{
        margin-bottom: 50px;
        }
    </style>
</head>
<body>
    <script>
        function addToDisplay(value) {
            document.getElementById('display').value += value;
            }

        function clearDisplay() {
            document.getElementById('display').value = '';
            }

        function calculate() {
            try {
                document.getElementById('display').value = eval(document.getElementById('display').value);
                } catch (error) {
                document.getElementById('display').value = 'Error';
                }
            }   
    </script>

<div id="calculator">
   
    <input type="text" id="display" >
    <br><br>
    <input type="button" value="7" onclick="addToDisplay('7')">
    <input type="button" value="8" onclick="addToDisplay('8')">
    <input type="button" value="9" onclick="addToDisplay('9')">
    <input type="button" value="/" onclick="addToDisplay('/')">
    <br>
    <input type="button" value="4" onclick="addToDisplay('4')">
    <input type="button" value="5" onclick="addToDisplay('5')">
    <input type="button" value="6" onclick="addToDisplay('6')">
    <input type="button" value="-" onclick="addToDisplay('-')">
    <br>
    <input type="button" value="1" onclick="addToDisplay('1')">
    <input type="button" value="2" onclick="addToDisplay('2')">
    <input type="button" value="3" onclick="addToDisplay('3')">
    <input type="button" value="+" onclick="addToDisplay('+')">
    <br>
    <input type="button" value="0" onclick="addToDisplay('0')">
    
    <input type="button" value="=" onclick="calculate()">
    <input type="button" value="*" onclick="addToDisplay('*')">
   
    <input type="button" value="%" onclick="addToDisplay('%')">
    <br>
    <input type="button" id="clear" value="C" onclick="clearDisplay()">
</div>
</body>
</html>

```
# Output:
![image](https://github.com/AadhithyaRaj/calculator/assets/128829484/faf3b79f-628c-4467-b5e6-9b6888b603bd)