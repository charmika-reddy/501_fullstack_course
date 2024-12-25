<h1>Introduction to Node.js</h1>

### What is Node.js
Node.js is a runtime environment that lets you run JavaScript outside the browser. While JavaScript traditionally ran only in browsers for front-end web pages, Node.js allows it to be used for backend development, servers, and more.

#### *Example*:

Think of JavaScript as a chef limited to working in a browser (a kitchen). Node.js gives the chef a mobile kitchen, enabling them to work anywhere, like creating backend servers or command-line tools.

### Key Features of Node.js

1. *Fast and Lightweight*: Built on Google Chrome’s V8 JavaScript engine.
1. *Non-Blocking I/O*: Processes tasks without waiting, making it efficient.
1. *npm*: A built-in package manager for installing libraries.
1. *Full-Stack Development*: Powers frameworks like Express.js (backend) and works with front-end tools like React.

### Installation of Node.js

Visit the [Official Node.js](https://nodejs.org/en/download/package-manager) Webpage and select the file as per your system type & install it. After that finish the setup and next check it whether it is installed successfully or not by chrecking its version in terminal or powershell.

### What is Server

A server that which stores the information and shares it with other devices when it get request. It is always ready to give the responses for the requests from other computers, Phone or any other devices.

#### Example:

Imagine a restaurant:

- The server is like a waiter who takes orders (requests) and brings food (responses).
- The clients are the customers who request food (data).

### Frist Node.js Program

Here the sample node.js program to run the node.js program file we need to run this command node filename.js

#### index.js

```javascript
function hello(){
    console.log("Hello, World!");
}
hello();
```

### Node.js REPL

The Node.js REPL stands for Read-Eval-Print Loop, and it’s like a playground where you can quickly try out JavaScript code in real-time. To start the REPL, simply type node in your terminal or command prompt and press Enter.

1. Read : It reads the code you type.
1. Eval : It evaluates (runs) your code.
1. Print : It prints the result.
1. Loop : It does this again and again until you quit.

### Code Quality using ESLint

[Visual Studio Code](https://code.visualstudio.com/) providing many builtin features to increase the speed at which we write code. By installing the extensions that may help in code quality and readability.

- **ESLint** :

    [ESLint](https://eslint.org/) is a tool or Extenssion for the Visual Studio Code for identifying and reporting on problems patterns found in JavaScript it may helps to write the cde in propper manner aswell as it would be make sure useful to improve the quality of code while writing the code. If any error in the code it will directly shows that in the terminal.