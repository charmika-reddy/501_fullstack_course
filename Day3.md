<h1>NPM(Node Package Manager)</h1>

### Why there is need for library ecosystem

A library ecosystem is essential for modern software development because it provides reusable, modular, and well-tested code that simplifies the process of building and maintaining software. Here are the key reasons why a library ecosystem is important:

### What is NPM
NPM is a package manager for JavaScript programming language. It is the default package manager for the JavaScript runtime environment Node.js. It is used to install, update, and manage dependencies in a Node.js project. It is a command line tool to install the packages which is required to our project. This NPM is automaticall installed when we install the Node.js to check the version of the both node.js and npm we simply use this commands

- node --version We can get the Version of Node.js

- npm --version We can get the Version of NPM.

### What is NPM Scripts ?
NPM scripts are custom commands defined in the package.json file of a Node.js project. They allow developers to automate repetitive tasks like running tests, building code, starting a server, or even executing custom commands. NPM provides a simple way to define, run, and manage these tasks using the npm run command.

<h5>Example: "start":"node index.js" Which is used to run that app using the simple command called npm start.</h5>

### Built-in fs module

The `fs` module is a built-in Node.js module that provides an interface to the file system. It allows you to read and write files, as well as perform other operations on the files we can use this file system module to do all these operations on the file by using both synchronous and asynchronous files.

Node.js fs modules used for some common tasks like:

- Create files
- Read files
- Update files
- Delete files
- Rename files

### Stream in Node.js

In Node.js, streams are objects that allow you to read or write data sequentially. They are used to handle large data efficiently by processing it piece-by-piece instead of loading it all into memory.

Types of Streams:
- Readable Streams: Used for reading data, e.g., fs.createReadStream().
- Writable Streams: Used for writing data, e.g., fs.createWriteStream().
- Duplex Streams: Can both read and write, e.g., net.Socket.
- Transform Streams: A type of duplex stream that modifies data as it is read or written, e.g., zlib.createGzip().

### Accepting input from CLI

Node.js which is also provides the readline module whihc is allow the user to get input from a readable stream such as the `process.stdin` stream, which during the execution of a Node.js program this asks the input in the terminal input. This wil takes the input in one line only.

Example Code
```javascript
`const readline = require('node:readline');

const rl = readline.createInterface({
  input: process.stdin,
  output: process.stdout,
});

rl.question(`What's your name?\n`, name => {
  console.log(`Hi ${name}!`);
  rl.close();
});`
```

After run this it will take the input from the user then after it will gives the output as like below

Sample Output

```javascript
What is your name?
Charmika       <-----("You need to enter this.")
Hi Charmika!
```
### Using the Minimist to accept CLI input
The minimist module will analyze arguments we pass the command line. It provides the argument list into an array for the simple use. In this array we can use the index names aswell as the numbers to access the values.

Sample Code
```javascript
var argv = require('minimist')(process.argv.slice(2))
console.log(argv)
```
Sample Output

```javascript
{ _: [] }
```