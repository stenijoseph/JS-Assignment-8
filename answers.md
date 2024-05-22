## 1.	Write short notes on the below with code examples

## • while loop The while loop loops through a block of code as long as a specified condition is true.

 ### Syntax:-while (condition) {
 ### // code block to be executed
 ### }
```js
 ex:- while (i < 10) {
 text += "The number is " + i;
 i++;
 }
```

## • do-while loop:The do while loop is a variant of the while loop. This loop will execute the code block once, before checking if the condition is true, then it will repeat the loop as long as the condition is true.
### Syntax:-do {
###  // code block to be executed
### }
### while (condition);
```js
 ex:-do {
    text += "The number is " + i;
 i++;
}
 while (i < 10);
```

## •for loop:The for statement creates a loop with 3 optional expressions:
### Syntax:for (expression 1; expression 2; expression 3) {
 ### // code block to be executed
### }
-  Expression 1 is executed (one time) before the execution of the code block.
- Expression 2 defines the condition for executing the code block.
- Expression 3 is executed (every time) after the code block has been executed.
```js
for (let i = 0; i < 5; i++) {
  text += "The number is " + i + "<br>";
}
```

## •for in loop:The JavaScript for in statement loops through the properties of an Object:
### Syntax:-for (key in object) {
 ### // code block to be executed
### }
```js
const person = {fname:"John", lname:"Doe", age:25};

let text = "";
for (let x in person) {
  text += person[x];
}
```

## •for of loop:The JavaScript for of statement loops through the values of an iterable object.
### Syntax:-for (variable of iterable) {
###  // code block to be executed
### }
 - variable - For every iteration the value of the next property is assigned to the variable. Variable can be declared with const, let, or var.
- iterable - An object that has iterable properties.
```js
const cars = ["BMW", "Volvo", "Mini"];

let text = "";
for (let x of cars) {
  text += x;
}
```
## 2.Explain the scope in Javascript.
## Ans:-Scope determines the accessibility (visibility) of variables.JavaScript variables have 3 types of scope:-
- Block scope
- Function scope
- Global scope

## Block Scope:-ES6 introduced two important new JavaScript keywords: let and const.These two keywords provide Block Scope in JavaScript.Variables declared inside a { } block cannot be accessed from outside the block:
```js
{
  let x = 2;
}
```
## Function Scope:-JavaScript has function scope: Each function creates a new scope.Variables defined inside a function are not accessible (visible) from outside the function.Variables declared with var, let and const are quite similar when declared inside a function.They all have Function Scope:
```js
function myFunction() {
  var carName = "Volvo"
}
```
## Global Scope:-A variable declared outside a function, becomes GLOBAL.
```js
let carName = "Volvo";
function myFunction() {

}
```
## Local Scope:-Variables declared within a JavaScript function, are LOCAL to the function. 
```js
function myFunction() {
  let carName = "Volvo";
  
}
```
## 3.What is a callback?
## Ans:-A callback is a function that is passed as an argument to another function, and is called after the main function has finished its execution. The main function is called with a callback function as its argument, and when the main function is finished, it calls the callback function to provide a result. Callbacks allow you to handle the results of an asynchronous operation in a non-blocking manner, which means that the program can continue to run while the operation is being executed.

## 4.Explain context in JavaScript?
## Ans:-In JavaScript, the environment that enables the JavaScript code to get executed is what we call JavaScript Execution Context. It is the execution context that decides which code section has access to the functions, variables, and objects used in the code. During the execution context, the specific code gets parsed line by line then the variables and functions are stored in the memory. An execution context is similar to a container that stores variables, and the code gets evaluated and then executed. Thus, it is the execution context that provides an environment for the specific code to get executed.


## 5.What is hoisting in JavaScript?

## Ans:-JavaScript Hoisting refers to the process whereby the interpreter appears to move the declaration of functions, variables, classes, or imports to the top of their scope, prior to execution of the code.

## 6.Explain lexical scope?

## Ans:-Lexical scope is a fundamental concept in programming that determines the accessibility of variables and functions within a program. In simple terms, the lexical scope is the scope of a variable or function based on where it is defined in the source code. The scope is determined by the placement of variables and functions in the code, and it remains the same throughout the execution of the program. Global variables can be accessed from anywhere within the program, while local variables can only be accessed within the function or block in which they are defined. The nested scope allows functions to access variables defined in parent functions, and block scope allows variables to have limited accessibility within a block of code.

## 7.What is scope chaining?

## Ans;-JavaScript engine uses scopes to find out the exact location or accessibility of variables and that particular process is known as Scope Chain.Scope Chain means that one variable has a scope (it may be global or local/function or block scope) is used by another variable or function having another scope (may be global or local/function or block scope).This complete chain formation goes on and stops when the user wishes to stop it according to the requirement.

## 8.Explain closure.

## Ans:-A closure is the combination of a function bundled together (enclosed) with references to its surrounding state (the lexical environment). When you create a closure, you gain access to an outer function’s scope from an inner function. Closures are automatically created every time a function is defined in JavaScript.


## 9.What is the difference between undefined and not defined in javascript?

## Ans:- - undefined: 
## 1.It is a JavaScript keyword that has a special meaning. Everything which gets a space in memory will contain undefined until we assign a value to that memory space.
## 2. It works like when we declared a variable in the code but did not assign the value before printing the variable value.

## not defined:
## 1.In JavaScript, it is one of the reference errors that JavaScript will throw when someone accesses the variable which is not inside the memory heap.
## 2.It works like when we did not declare the variable and try to call that variable.

## 10.Explain spread and rest operator?

## Ans:-Spread Operator:
## The spread operator, denoted by three consecutive dots (...), is primarily used for expanding iterables like arrays into individual elements. This operator allows us to efficiently merge, copy, or pass array elements to functions without explicitly iterating through them.
```js
const arr = [1, 2, 3];
const newArr = [5, 6, ...arr];
console.log("New array ", newArr);
```
## Rest Operator:
## While the spread operator expands elements, the rest operator condenses them into a single entity within function parameters or array destructuring. It collects remaining elements into a designated variable, facilitating flexible function definitions and array manipulation.

## 11.Explain ‘this’ keyword in Javascript.

## Ans:-This” keyword refers to an object that is executing the current piece of code. It references the object that is executing the current function. If the function being referenced is a regular function, “this” references the global object.