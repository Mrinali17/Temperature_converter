# Temperature_converter
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="style1.css" />

    <title>Temperature Converter</title>
    
</head>
<body>
            <h1>Temperature Converter</h1>
            <div id="container">
                <div class="input-div">
                    <label >Celsius</label><br>
                    <input type="number" value="0"  id="cel" class="inp">
                </div>
                <div class="input-div">
                    <label >Fahrenheit</label><br>
                    <input type="number" value="32" id="fah" class="inp">
                </div>
            </div>   
            
            <script>
                var cel = document.getElementById("cel");
                var fah = document.getElementById("fah");

                cel.addEventListener('input', function(){
                    let c = this.value;
                    let f = (c * 9/5) + 32;
                    if(!Number.isInteger(f)){
                        f = f.toFixed(2);
                    }
                    fah.value = f;

                });

                fah.addEventListener('input', function(){
                    let f = this.value;
                    let c = (f - 32) * 5/9;
                    if(!Number.isInteger(c)){
                        c = c.toFixed(2);
                    }
                    cel.value = c;


                });


            </script>
</body>
</html>   

<style1.css>
body{
    background-color: antiquewhite;
    padding: 50px 100px;
}
h1{
    text-align: center;
}
#container{
    text-align: center;
    background: #498080;
    box-shadow: 0px 0px 15px 3px rgba(44, 39, 39, 0.4);
    padding: 50px;
}
.input-div{
    display: inline-block;
}
.inp{
    padding: 5px 10px;
    margin: 10px;
    font-size: 30px;
    font-weight: bold;
    text-align: center;
}
label{
    font-size: 22px;
    color: rgb(36, 35, 34);
}

