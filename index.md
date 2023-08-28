---
layout: default
title: Student Blog
---




## Tarun's Page


## About Me

My name is Tarun and I am a sophmore at Del Norte High School. Things I like to do include coding, playing tennis, playing video games, and hanging out with friends. The classes I am taking this trimester include: AP Computer Science, AP Chemistry, World History 1, AP Calculus AB, and Spanish 3.

<img src="images/IMG_0886.PNG"  width="250" height="500">



## Picture of me (and my dog)

<img src="images/IMG_4992-preview.jpg"  width="350" height="500">

## My Class Schedule

| Period      | Class |
| ----------- | ----------- |
|1    | AP Computer Science       |
|2    | AP Chemistry        |
|3    | World History 1        |
|4    | AP Calculus AB        |
|5    | Spanish 3        |



## Go to My Page:


Go to my [Github account](https://github.com/Djxnxnx){:target="_blank"}

## Hacks

Make sure to run bundle install where the Gemfile is located. Download nbconvert and PyYaml to run your make command. Copy the link after running make. The file to change the blog page is index.md. You can use the notebooks to create other blogs which you can use. Use ls to list all the files in a directory. Use cd to change directories. Use pip3 install to download things. Use mkdir to create a directory. To check the version of something, put in the name and then --version.

## Calculator

<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<style>
  body {
    font-family: Arial, sans-serif;
  }

  .calculator {
    width: 250px;
    border: 1px solid #ccc;
    padding: 10px;
    border-radius: 5px;
    box-shadow: 0 0 10px rgba(0, 0, 0, 0.2);
    margin: 0 auto;
  }

  .output {
    display: flex;
    justify-content: flex-end;
    align-items: center;
    font-size: 24px;
    margin-bottom: 10px;
  }

  .buttons {
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    grid-gap: 5px;
  }

  button {
    padding: 10px;
    font-size: 18px;
    background-color: #f0f0f0;
    border: none;
    cursor: pointer;
  }
button:hover {
    background-color: #d0d0d0;
  }
</style>
<title>Calculator</title>
</head>
<body>
  <div class="calculator">
    <div class="output" id="output">0</div>
    <div class="buttons">
      <button onclick="appendToOutput('7')">7</button>
      <button onclick="appendToOutput('8')">8</button>
      <button onclick="appendToOutput('9')">9</button>
      <button onclick="appendToOutput('+')">+</button>
      <button onclick="appendToOutput('4')">4</button>
      <button onclick="appendToOutput('5')">5</button>
      <button onclick="appendToOutput('6')">6</button>
      <button onclick="appendToOutput('-')">-</button>
      <button onclick="appendToOutput('1')">1</button>
      <button onclick="appendToOutput('2')">2</button>
      <button onclick="appendToOutput('3')">3</button>
      <button onclick="appendToOutput('*')">x</button>
      <button onclick="appendToOutput('0')">0</button>
      <button onclick="calculate()">=</button>
      <button onclick="clearOutput()">C</button>
      <button onclick="appendToOutput('/')">/</button>
    </div>
  </div>

  <script>
    let outputElement = document.getElementById('output');
    let currentInput = '';

    function appendToOutput(value) {
      currentInput += value;
      outputElement.innerText = currentInput;
    }

    function calculate() {
      try {
        currentInput = eval(currentInput).toString();
        outputElement.innerText = currentInput;
      } catch (error) {
        outputElement.innerText = 'Error';
      }
    }

    function clearOutput() {
      currentInput = '';
      outputElement.innerText = '0';
    }
  </script>
</body>