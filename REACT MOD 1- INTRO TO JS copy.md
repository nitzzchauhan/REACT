<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>HTML Module 4</title>
    <style>
        body {
            background-color: black;
            color: white;
        }
        h1, h2, h3, h4, h5, h6 {
            color: white;
        }
    </style>
</head>
<body>
## Module 1: Introduction to JavaScript (ES5 and ES6)

### Basic JavaScript
JavaScript is a high-level, interpreted programming language commonly used for web development. It is versatile and allows you to create dynamic and interactive web pages.

#### Example
```javascript
// Variables
var message = 'Hello, World!';
console.log(message);

// Functions
function greet(name) {
    return 'Hello, ' + name + '!';
}
console.log(greet('Alice'));

// Loops
for (var i = 0; i < 5; i++) {
    console.log(i);
}
```

### Object-Based JavaScript
JavaScript is an object-oriented language, allowing you to create objects to store data and methods.

#### Example
```javascript
// Creating an object
var person = {
    firstName: 'John',
    lastName: 'Doe',
    age: 30,
    fullName: function() {
        return this.firstName + ' ' + this.lastName;
    }
};
console.log(person.fullName());
```

### Introduction to ES6
ES6 (ECMAScript 2015) introduced several new features and syntactical improvements to JavaScript.

### JavaScript Helpers (forEach, filter, map, every, some)
JavaScript provides several array methods to perform common tasks.

#### forEach
Executes a provided function once for each array element.

```javascript
let numbers = [1, 2, 3, 4, 5];
numbers.forEach(function(number) {
    console.log(number);
});
```

#### filter
Creates a new array with all elements that pass the test implemented by the provided function.

```javascript
let evenNumbers = numbers.filter(function(number) {
    return number % 2 === 0;
});
console.log(evenNumbers);
```

#### map
Creates a new array with the results of calling a provided function on every element in the calling array.

```javascript
let doubledNumbers = numbers.map(function(number) {
    return number * 2;
});
console.log(doubledNumbers);
```

#### every
Tests whether all elements in the array pass the test implemented by the provided function.

```javascript
let allEven = numbers.every(function(number) {
    return number % 2 === 0;
});
console.log(allEven); // false
```

#### some
Tests whether at least one element in the array passes the test implemented by the provided function.

```javascript
let someEven = numbers.some(function(number) {
    return number % 2 === 0;
});
console.log(someEven); // true
```

### String Literals
In ES6, template literals provide an easier way to create multiline strings and perform string interpolation.

```javascript
let name = 'Alice';
let greeting = `Hello, ${name}!`;
console.log(greeting);
```

### Destructuring
Destructuring assignment syntax allows you to unpack values from arrays or properties from objects into distinct variables.

#### Array Destructuring
```javascript
let [a, b] = [1, 2];
console.log(a, b);
```

#### Object Destructuring
```javascript
let person = {firstName: 'John', lastName: 'Doe'};
let {firstName, lastName} = person;
console.log(firstName, lastName);
```

### Rest Parameters & Spread Operator
Rest parameters allow you to represent an indefinite number of arguments as an array. The spread operator allows an iterable to expand in places where multiple arguments or elements are expected.

#### Rest Parameters
```javascript
function sum(...numbers) {
    return numbers.reduce((total, number) => total + number);
}
console.log(sum(1, 2, 3)); // 6
```

#### Spread Operator
```javascript
let arr = [1, 2, 3];
let newArr = [...arr, 4, 5];
console.log(newArr); // [1, 2, 3, 4, 5]
```

### Arrow Functions
Arrow functions provide a shorter syntax for writing function expressions and lexically bind the `this` value.

```javascript
let add = (a, b) => a + b;
console.log(add(2, 3)); // 5
```

### Default Parameters
Default function parameters allow named parameters to be initialized with default values if no value or `undefined` is passed.

```javascript
function greet(name = 'World') {
    return `Hello, ${name}!`;
}
console.log(greet()); // Hello, World!
```

### Class: Inheritance, Constructor
ES6 introduced a new syntax for creating classes and handling inheritance.

#### Example
```javascript
class Animal {
    constructor(name) {
        this.name = name;
    }
    speak() {
        console.log(`${this.name} makes a noise.`);
    }
}

class Dog extends Animal {
    constructor(name, breed) {
        super(name);
        this.breed = breed;
    }
    speak() {
        console.log(`${this.name} barks.`);
    }
}

let dog = new Dog('Rex', 'German Shepherd');
dog.speak(); // Rex barks.
```

### Promises
Promises provide a way to handle asynchronous operations. A promise represents a value that may be available now, in the future, or never.

#### Example
```javascript
let promise = new Promise((resolve, reject) => {
    let success = true;
    if (success) {
        resolve('Promise fulfilled!');
    } else {
        reject('Promise rejected.');
    }
});

promise
    .then(message => {
        console.log(message);
    })
    .catch(error => {
        console.log(error);
    });
```

## Interview Questions and Answers

1. **What is the difference between `var`, `let`, and `const` in JavaScript?**
   - **Answer:** `var` is function-scoped and can be re-declared and updated. `let` and `const` are block-scoped. `let` can be updated but not re-declared, whereas `const` cannot be updated or re-declared.

2. **Explain how arrow functions differ from regular functions.**
   - **Answer:** Arrow functions have a shorter syntax and lexically bind the `this` value. They cannot be used as constructors and do not have their own `this`, `arguments`, `super`, or `new.target`.

3. **What are template literals and how do they differ from regular strings?**
   - **Answer:** Template literals are enclosed by backticks (`` ` ``) and allow for multiline strings and string interpolation using `${expression}` syntax, unlike regular strings which are enclosed by single or double quotes.

4. **What is the purpose of the spread operator and how is it used?**
   - **Answer:** The spread operator (`...`) allows an iterable such as an array to be expanded in places where zero or more arguments or elements are expected. It is used for copying arrays, merging arrays, and spreading elements in function calls.

5. **How do you handle asynchronous operations in JavaScript using Promises?**
   - **Answer:** Promises provide a way to handle asynchronous operations by representing a value that may be available now, in the future, or never. Promises have `then` and `catch` methods to handle resolved and rejected cases respectively.
   - **Code Example:**
     ```javascript
     let promise = new Promise((resolve, reject) => {
         let success = true;
         if (success) {
             resolve('Promise fulfilled!');
         } else {
             reject('Promise rejected.');
         }
     });

     promise
         .then(message => {
             console.log(message);
         })
         .catch(error => {
             console.log(error);
         });
     ```

These notes, interview questions, and code examples provide a comprehensive overview of JavaScript basics, ES5 features, and ES6 enhancements.