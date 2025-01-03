<h1>Event Loop , Callback , Promises , closures , Async & Await. </h1>

### What is Event Loop ?
The event loop is a mechanism that allows JavaScript to handle multiple tasks concurrently.It is a centralized control structure that manages the execution of tasks, ensuring that each task is executed in a sequential manner, while allowing other tasks to be executed concurrently.

Example:
```javascript
javascript
Copy code
console.log("Start");

setTimeout(() => {
  console.log("This happens later");
}, 0);

console.log("End");
```
Output:
```javascript
Start
End
This happens later
```
In the above code ("This happens later") message wil prints after the completion of all the code execution and later it will take one second time to print this message because of the event loop mechanism.

### What is CallBack ?
A callback is a function that is passed as an argument to another function and is executed later, once a specific task or operation is complete. Callbacks are commonly used in asynchronous programming to handle the result of an operation after it has finished, without blocking the execution of other code.

Example :
```javascript
function greet(name, callback) {
  console.log("Hello " + name);
  callback();
}

function sayGoodbye() {
  console.log("Goodbye!");
}
greet("Alice", sayGoodbye);
```
Output:
```javascript
Hello Alice
Goodbye!
```
### What is a Promise?
A promise in JavaScript is an object that represents the eventual completion (or failure) of an asynchronous operation and its resulting value. It allows you to handle asynchronous operations in a more structured and readable way than using callbacks.

Example:
```javascript
const cleanRoom = new Promise((resolve, reject) => {
    let isClean = true;

    if (isClean) {
        resolve("Room is clean!");
    } else {
        reject("Room is still messy!");
    }
});

cleanRoom
    .then(message => console.log(message));
    .catch(error => console.log(error));  
```
Sample Output
```javascript

Room is clean!
```  
In the above code, a Promise is created with a resolve and reject function. The resolve function is called when the room is clean, and the reject function is called when the room is still messy.

### What is a Closure ?
A closure is a function that "remembers" its lexical scope (the environment in which it was created), even when the function is executed outside of that scope. In simple terms, a closure allows a function to access variables from its outer scope, even after the outer function has finished executing.

Example:
```javascript
function outerFunction(outerVariable) {
  return function innerFunction(innerVariable) {
    console.log("Outer variable: " + outerVariable);
    console.log("Inner variable: " + innerVariable);
  };
}

const closureExample = outerFunction("Hello");
closureExample("World");
```
Output:
```javascript
Outer variable: Hello
Inner variable: World
```

### What is Async & Await ?
async and await are used to work with promises in a cleaner, more readable way. async is used to define a function as asynchronous, and await is used inside an async function to wait for a promise to resolve before continuing the execution of the function.

Example:

```javascript
function delay(ms) {
  return new Promise(resolve => setTimeout(resolve, ms));
}

async function fetchData() {
  console.log("Fetching data...");
  await delay(2000); 
  console.log("Data fetched!");
}

fetchData();
```
Output:

```javascript
Fetching data...
(2 seconds delay)
Data fetched!
```
