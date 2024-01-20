CODE USED TO CREATE CALCULATOR.



HTMl CODE :
<!DOCTYPE html>
<html>

<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width">
  <title>Calculate me! - A calculator made my me</title>
  <link href="styles.css" rel="stylesheet" type="text/css" />
  <link href="comp.css" rel="stylesheet" type="text/css" />
</head>

<body>
  <h1 class="text-center">BASIC-CALCULATOR</h1>
  <div class="container flex flex-col items-center mx-auto m-w-20">
    <div class="row">
      <input class="input" type="text"/>
    </div>
    <div class="row">
      <button class="button">C</button>
      <button class="button">%</button>
      <button class="button">M+</button>
      <button class="button">M-</button>
    </div>
    <div class="row">
      <button class="button">7</button>
      <button class="button">8</button>
      <button class="button">9</button>
      <button class="button">*</button>
    </div>
    <div class="row">
      <button class="button">4</button>
      <button class="button">5</button>
      <button class="button">6</button>
      <button class="button">/</button>
    </div>
    <div class="row">
      <button class="button">1</button>
      <button class="button">2</button>
      <button class="button">3</button>
      <button class="button">+</button>
    </div>
    <div class="row">
      <button class="button">0</button>
      <button class="button">.</button>
      <button class="button">=</button>
      <button class="button">-</button>
    </div>
  </div>
  <script src="script.js"></script>
</body>

</html>

CSS ADJUSTMENT CODE: 
.text-center{
    text-align: center;
    color: rgb(190, 107, 11);
    font-family: system-ui, -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
  }
  
  .bg-red{
    background: black;
  }
  
  .mx-auto{
    margin: auto;
  }
  
  .flex{
    display:flex;
  } 
  .flex-col{
    flex-direction: column;
  }
  
  .items-center{
    align-items: center;
  }

  CSS DESIGN CODE:
  html, body {
    height: 100%;
    width: 100%;
    font-family: system-ui, -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif; 
    background-color: rgb(8, 10, 10);
  }
  
  .button{
    width: 66px;
    padding: 23px;
    margin: 2px 4px;
    
    border-radius: 400px;
    cursor: pointer;
    color: rgb(190, 107, 11);
    background-color: black;
  }
  
  .row{
    margin: 8px 0;
  }
  .row input{
    width: 291px;
    font-size: 20px;
      margin: 0;
      padding: 10px 0px;
      border: 2px solid black;
      border-radius: 5px;
  }

  JAVASCRIPT CODE:
  let string = "";
let buttons = document.querySelectorAll('.button');
Array.from(buttons).forEach((button)=>{
  button.addEventListener('click', (e)=>{
    if(e.target.innerHTML == '='){
      string = eval(string);
      document.querySelector('input').value = string;
    }
    else if(e.target.innerHTML == 'C'){
      string = ""
      document.querySelector('input').value = string;
    }
    else{ 
    console.log(e.target)
    string = string + e.target.innerHTML;
    document.querySelector('input').value = string;
      }
  })
})
