# JavaScript Basics: Complete Course Book

## Table of Contents

1. [Introduction to JavaScript](#1-introduction-to-javascript)
2. [Setting Up Your Development Environment](#2-setting-up-your-development-environment)
3. [Your First JavaScript Program](#3-your-first-javascript-program)
4. [Variables and Data Types](#4-variables-and-data-types)
5. [Operators](#5-operators)
6. [Control Structures](#6-control-structures)
7. [Functions](#7-functions)
8. [Objects and Arrays](#8-objects-and-arrays)
9. [Strings and String Methods](#9-strings-and-string-methods)
10. [Working with the DOM](#10-working-with-the-dom)
11. [Events and Event Handling](#11-events-and-event-handling)
12. [Asynchronous JavaScript](#12-asynchronous-javascript)
13. [Error Handling](#13-error-handling)
14. [Modern JavaScript (ES6+)](#14-modern-javascript-es6)
15. [Best Practices and Tips](#15-best-practices-and-tips)
16. [Final Project](#16-final-project)

---

## 1. Introduction to JavaScript

### What is JavaScript?

JavaScript is a high-level, interpreted programming language that was initially created to make web pages interactive. Today, JavaScript is used for:

- **Frontend Development**: Making websites interactive
- **Backend Development**: Server-side programming with Node.js
- **Mobile Apps**: React Native, Ionic
- **Desktop Apps**: Electron
- **Game Development**: Browser and mobile games

### Why Learn JavaScript?

1. **Easy to Learn**: Beginner-friendly syntax
2. **Versatile**: Works everywhere (web, mobile, desktop, server)
3. **High Demand**: Most popular programming language
4. **Active Community**: Huge ecosystem and support
5. **No Setup Required**: Runs in any web browser

### JavaScript vs Other Languages

```javascript
// JavaScript - Dynamic and flexible
let message = "Hello World";
console.log(message);

// Compared to Java - More verbose
public class HelloWorld {
    public static void main(String[] args) {
        System.out.println("Hello World");
    }
}
```

---

## 2. Setting Up Your Development Environment

### Option 1: Browser Console (Quick Start)

1. Open any web browser (Chrome, Firefox, Safari)
2. Right-click → "Inspect" or "Developer Tools"
3. Click "Console" tab
4. Start typing JavaScript!

### Option 2: Code Editor + Browser

**Recommended Code Editors:**
- Visual Studio Code (Free, most popular)
- Sublime Text
- Atom

**VS Code Setup:**
1. Download from [https://code.visualstudio.com/](https://code.visualstudio.com/)
2. Install useful extensions:
   - JavaScript (ES6) code snippets
   - Live Server
   - Prettier - Code formatter

### Creating Your First HTML File

Create a file called `index.html`:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>JavaScript Learning</title>
</head>
<body>
    <h1>JavaScript Course</h1>
    
    <!-- Internal JavaScript -->
    <script>
        console.log("Hello from internal script!");
    </script>
    
    <!-- External JavaScript -->
    <script src="script.js"></script>
</body>
</html>
```

Create `script.js`:

```javascript
console.log("Hello from external script!");
```

---

## 3. Your First JavaScript Program

### The Console

The console is your best friend for learning JavaScript:

```javascript
// This prints to the browser console
console.log("Hello, World!");

// You can print different types of data
console.log(42);
console.log(true);
console.log(["apple", "banana", "orange"]);
```

### Comments

Comments help you document your code:

```javascript
// This is a single-line comment

/*
This is a 
multi-line comment
*/

console.log("This code runs"); // Comment at end of line
// console.log("This code doesn't run");
```

### Basic Syntax Rules

```javascript
// JavaScript is case-sensitive
let name = "John";
let Name = "Jane"; // Different variable!

// Statements usually end with semicolons
console.log("Hello");
console.log("World");

// But semicolons are optional (automatic insertion)
console.log("Hello")
console.log("World")
```

### Your First Interactive Program

```javascript
// Get user input
let userName = prompt("What's your name?");

// Show a message
alert("Hello, " + userName + "!");

// Log to console
console.log("User entered:", userName);
```

---

## 4. Variables and Data Types

### What are Variables?

Variables are containers that store data values.

```javascript
// Think of variables like labeled boxes
let age = 25;        // Box labeled "age" contains 25
let name = "Alice";  // Box labeled "name" contains "Alice"
```

### Declaring Variables

```javascript
// Modern way (recommended)
let message = "Hello";
const PI = 3.14159;

// Old way (avoid in new code)
var oldVariable = "I'm old";

// Without declaration (creates global - avoid!)
globalVar = "Don't do this";
```

### Variable Rules

```javascript
// Valid variable names
let firstName = "John";
let age2 = 25;
let _private = "secret";
let $element = "jQuery style";

// Invalid variable names
// let 2age = 25;      // Can't start with number
// let first-name = "John"; // Can't use hyphens
// let let = "keyword";     // Can't use reserved words
```

### Data Types

#### 1. Numbers

```javascript
let integer = 42;
let decimal = 3.14159;
let negative = -17;
let scientific = 2.5e6; // 2,500,000

// Special number values
let infinity = Infinity;
let notANumber = NaN;

console.log(typeof 42);        // "number"
console.log(typeof 3.14);     // "number"
```

#### 2. Strings

```javascript
let singleQuotes = 'Hello';
let doubleQuotes = "World";
let backticks = `Template literal`;

// String concatenation
let greeting = "Hello" + " " + "World";
console.log(greeting); // "Hello World"

// Template literals (modern way)
let name = "Alice";
let age = 30;
let message = `My name is ${name} and I'm ${age} years old`;
console.log(message); // "My name is Alice and I'm 30 years old"
```

#### 3. Booleans

```javascript
let isTrue = true;
let isFalse = false;

// Boolean from comparisons
let isAdult = age >= 18;
let isEmpty = name === "";

console.log(typeof true);  // "boolean"
```

#### 4. Undefined and Null

```javascript
let notDefined;
console.log(notDefined); // undefined

let empty = null;
console.log(empty); // null

console.log(typeof undefined); // "undefined"
console.log(typeof null);      // "object" (this is a known quirk)
```

#### 5. Checking Data Types

```javascript
let value = 42;
console.log(typeof value);           // "number"
console.log(typeof "hello");         // "string"
console.log(typeof true);            // "boolean"
console.log(typeof undefined);       // "undefined"
console.log(typeof null);            // "object"
console.log(typeof [1, 2, 3]);      // "object"
console.log(typeof {name: "John"}); // "object"
```

### Type Conversion

```javascript
// String to Number
let strNumber = "123";
let num1 = Number(strNumber);        // 123
let num2 = parseInt(strNumber);      // 123
let num3 = parseFloat("123.45");     // 123.45
let num4 = +strNumber;               // 123 (unary plus)

// Number to String
let number = 123;
let str1 = String(number);           // "123"
let str2 = number.toString();        // "123"
let str3 = number + "";              // "123"

// Boolean Conversion
let bool1 = Boolean(1);              // true
let bool2 = Boolean(0);              // false
let bool3 = Boolean("hello");        // true
let bool4 = Boolean("");             // false
```

### Practice Exercises

```javascript
// Exercise 1: Create variables for a person
let firstName = "John";
let lastName = "Doe";
let age = 25;
let isStudent = true;
let favoriteColor = null; // unknown

console.log(`${firstName} ${lastName} is ${age} years old`);

// Exercise 2: Type conversion practice
let userInput = "25";
let userAge = Number(userInput);
let canVote = userAge >= 18;

console.log(`User can vote: ${canVote}`);

// Exercise 3: Variable reassignment
let score = 0;
console.log("Initial score:", score);

score = 10;
console.log("After scoring:", score);

score = score + 5;
console.log("Final score:", score);
```

---

## 5. Operators

### Arithmetic Operators

```javascript
let a = 10;
let b = 3;

console.log(a + b);  // 13 (addition)
console.log(a - b);  // 7  (subtraction)
console.log(a * b);  // 30 (multiplication)
console.log(a / b);  // 3.333... (division)
console.log(a % b);  // 1  (remainder/modulo)
console.log(a ** b); // 1000 (exponentiation)

// Increment and Decrement
let counter = 5;
counter++;           // counter becomes 6
counter--;           // counter becomes 5

// Pre vs Post increment
let x = 5;
console.log(x++);    // 5 (uses value, then increments)
console.log(x);      // 6

let y = 5;
console.log(++y);    // 6 (increments, then uses value)
console.log(y);      // 6
```

### Assignment Operators

```javascript
let num = 10;

num += 5;    // num = num + 5; (15)
num -= 3;    // num = num - 3; (12)
num *= 2;    // num = num * 2; (24)
num /= 4;    // num = num / 4; (6)
num %= 3;    // num = num % 3; (0)

console.log(num); // 0
```

### Comparison Operators

```javascript
let a = 10;
let b = "10";

// Equality (type coercion)
console.log(a == b);   // true (converts string to number)
console.log(a != b);   // false

// Strict equality (no type coercion)
console.log(a === b);  // false (different types)
console.log(a !== b);  // true

// Relational
console.log(5 > 3);    // true
console.log(5 < 3);    // false
console.log(5 >= 5);   // true
console.log(5 <= 3);   // false
```

### Logical Operators

```javascript
let age = 25;
let hasLicense = true;

// AND (&&) - both conditions must be true
let canDrive = age >= 18 && hasLicense;
console.log(canDrive); // true

// OR (||) - at least one condition must be true
let isWeekend = true;
let isHoliday = false;
let canSleep = isWeekend || isHoliday;
console.log(canSleep); // true

// NOT (!) - reverses the boolean value
let isWorking = false;
let isFree = !isWorking;
console.log(isFree); // true
```

### String Operators

```javascript
let firstName = "John";
let lastName = "Doe";

// Concatenation
let fullName = firstName + " " + lastName;
console.log(fullName); // "John Doe"

// Compound assignment with strings
let message = "Hello";
message += " World";
console.log(message); // "Hello World"

// Template literals (preferred modern way)
let greeting = `Hello, ${firstName} ${lastName}!`;
console.log(greeting); // "Hello, John Doe!"
```

### Operator Precedence

```javascript
// Mathematical order of operations applies
let result1 = 2 + 3 * 4;        // 14 (not 20)
let result2 = (2 + 3) * 4;      // 20

// Comparison before logical
let check = 5 > 3 && 2 < 4;     // true && true = true

// Use parentheses for clarity
let complex = (age >= 18) && (hasLicense === true);
```

### Practice Exercises

```javascript
// Exercise 1: Calculator
let num1 = 15;
let num2 = 4;

console.log(`${num1} + ${num2} = ${num1 + num2}`);
console.log(`${num1} - ${num2} = ${num1 - num2}`);
console.log(`${num1} * ${num2} = ${num1 * num2}`);
console.log(`${num1} / ${num2} = ${num1 / num2}`);
console.log(`${num1} % ${num2} = ${num1 % num2}`);

// Exercise 2: Age checker
let userAge = 17;
let hasParentPermission = true;

let canWatchMovie = userAge >= 18 || (userAge >= 13 && hasParentPermission);
console.log(`Can watch R-rated movie: ${canWatchMovie}`);

// Exercise 3: Even or odd
let number = 17;
let isEven = number % 2 === 0;
console.log(`${number} is ${isEven ? 'even' : 'odd'}`);
```

---

## 6. Control Structures

### If Statements

```javascript
// Basic if statement
let age = 18;

if (age >= 18) {
    console.log("You are an adult");
}

// If-else
let weather = "sunny";

if (weather === "sunny") {
    console.log("Let's go to the beach!");
} else {
    console.log("Maybe stay inside today");
}

// If-else if-else
let score = 85;

if (score >= 90) {
    console.log("Grade: A");
} else if (score >= 80) {
    console.log("Grade: B");
} else if (score >= 70) {
    console.log("Grade: C");
} else if (score >= 60) {
    console.log("Grade: D");
} else {
    console.log("Grade: F");
}
```

### Ternary Operator

```javascript
// Short form of if-else
let age = 20;
let message = age >= 18 ? "Adult" : "Minor";
console.log(message); // "Adult"

// Can be nested (but avoid complex nesting)
let score = 75;
let grade = score >= 90 ? "A" : score >= 80 ? "B" : "C";
console.log(grade); // "C"
```

### Switch Statements

```javascript
let day = "Monday";

switch (day) {
    case "Monday":
        console.log("Start of work week");
        break;
    case "Tuesday":
    case "Wednesday":
    case "Thursday":
        console.log("Midweek");
        break;
    case "Friday":
        console.log("TGIF!");
        break;
    case "Saturday":
    case "Sunday":
        console.log("Weekend!");
        break;
    default:
        console.log("Invalid day");
}

// Modern switch with return values
function getDayType(day) {
    switch (day) {
        case "Monday":
        case "Tuesday":
        case "Wednesday":
        case "Thursday":
        case "Friday":
            return "Weekday";
        case "Saturday":
        case "Sunday":
            return "Weekend";
        default:
            return "Invalid day";
    }
}
```

### Loops

#### For Loop

```javascript
// Basic for loop
for (let i = 0; i < 5; i++) {
    console.log(`Count: ${i}`);
}
// Output: Count: 0, Count: 1, Count: 2, Count: 3, Count: 4

// Loop through an array
let fruits = ["apple", "banana", "orange"];
for (let i = 0; i < fruits.length; i++) {
    console.log(`Fruit ${i + 1}: ${fruits[i]}`);
}

// For...of loop (modern way for arrays)
for (let fruit of fruits) {
    console.log(`I like ${fruit}`);
}

// For...in loop (for object properties)
let person = {name: "John", age: 30, city: "New York"};
for (let key in person) {
    console.log(`${key}: ${person[key]}`);
}
```

#### While Loop

```javascript
// While loop
let count = 0;
while (count < 3) {
    console.log(`Count: ${count}`);
    count++;
}

// Do-while loop (executes at least once)
let userInput;
do {
    userInput = prompt("Enter 'quit' to exit:");
    console.log(`You entered: ${userInput}`);
} while (userInput !== "quit");
```

#### Loop Control

```javascript
// Break - exit the loop
for (let i = 0; i < 10; i++) {
    if (i === 5) {
        break; // Exit loop when i equals 5
    }
    console.log(i); // Prints 0, 1, 2, 3, 4
}

// Continue - skip current iteration
for (let i = 0; i < 5; i++) {
    if (i === 2) {
        continue; // Skip when i equals 2
    }
    console.log(i); // Prints 0, 1, 3, 4
}
```

### Practice Exercises

```javascript
// Exercise 1: Number guessing game
let secretNumber = 7;
let guess = 5;

if (guess === secretNumber) {
    console.log("Correct! You guessed it!");
} else if (guess < secretNumber) {
    console.log("Too low!");
} else {
    console.log("Too high!");
}

// Exercise 2: Multiplication table
let number = 5;
console.log(`Multiplication table for ${number}:`);
for (let i = 1; i <= 10; i++) {
    console.log(`${number} × ${i} = ${number * i}`);
}

// Exercise 3: Sum of numbers
let sum = 0;
for (let i = 1; i <= 100; i++) {
    sum += i;
}
console.log(`Sum of 1 to 100: ${sum}`); // 5050

// Exercise 4: FizzBuzz
for (let i = 1; i <= 20; i++) {
    if (i % 3 === 0 && i % 5 === 0) {
        console.log("FizzBuzz");
    } else if (i % 3 === 0) {
        console.log("Fizz");
    } else if (i % 5 === 0) {
        console.log("Buzz");
    } else {
        console.log(i);
    }
}
```

---

## 7. Functions

### What are Functions?

Functions are reusable blocks of code that perform specific tasks.

```javascript
// Function declaration
function greet() {
    console.log("Hello, World!");
}

// Call the function
greet(); // Output: Hello, World!

// Function with parameters
function greetPerson(name) {
    console.log(`Hello, ${name}!`);
}

greetPerson("Alice"); // Output: Hello, Alice!
greetPerson("Bob");   // Output: Hello, Bob!
```

### Function Parameters and Arguments

```javascript
// Multiple parameters
function addNumbers(a, b) {
    let sum = a + b;
    console.log(`${a} + ${b} = ${sum}`);
}

addNumbers(5, 3); // Output: 5 + 3 = 8

// Default parameters
function greetWithDefault(name = "Friend") {
    console.log(`Hello, ${name}!`);
}

greetWithDefault();        // Output: Hello, Friend!
greetWithDefault("Alice"); // Output: Hello, Alice!
```

### Return Values

```javascript
// Function that returns a value
function multiply(a, b) {
    return a * b;
}

let result = multiply(4, 5);
console.log(result); // 20

// Function with multiple return statements
function getGrade(score) {
    if (score >= 90) return "A";
    if (score >= 80) return "B";
    if (score >= 70) return "C";
    if (score >= 60) return "D";
    return "F";
}

console.log(getGrade(85)); // "B"

// Early return pattern
function divide(a, b) {
    if (b === 0) {
        return "Cannot divide by zero";
    }
    return a / b;
}
```

### Function Expressions

```javascript
// Function expression
let sayHello = function(name) {
    return `Hello, ${name}!`;
};

console.log(sayHello("World")); // "Hello, World!"

// Arrow functions (ES6+)
let add = (a, b) => {
    return a + b;
};

// Short arrow function (implicit return)
let square = x => x * x;
let greet = name => `Hello, ${name}!`;

console.log(add(3, 4));    // 7
console.log(square(5));    // 25
console.log(greet("Bob")); // "Hello, Bob!"
```

### Function Scope

```javascript
let globalVar = "I'm global";

function testScope() {
    let localVar = "I'm local";
    console.log(globalVar); // Can access global
    console.log(localVar);  // Can access local
}

testScope();
// console.log(localVar); // Error: localVar is not defined

// Function parameters are local
function parameterTest(param) {
    param = "Changed";
    console.log(param); // "Changed"
}

let myVar = "Original";
parameterTest(myVar);
console.log(myVar); // Still "Original"
```

### Higher-Order Functions

```javascript
// Function that takes another function as parameter
function calculator(a, b, operation) {
    return operation(a, b);
}

function add(x, y) { return x + y; }
function multiply(x, y) { return x * y; }

console.log(calculator(5, 3, add));      // 8
console.log(calculator(5, 3, multiply)); // 15

// Using arrow functions
console.log(calculator(5, 3, (x, y) => x - y)); // 2
```

### Recursive Functions

```javascript
// Factorial function
function factorial(n) {
    if (n <= 1) {
        return 1; // Base case
    }
    return n * factorial(n - 1); // Recursive case
}

console.log(factorial(5)); // 120 (5 * 4 * 3 * 2 * 1)

// Fibonacci sequence
function fibonacci(n) {
    if (n <= 1) return n;
    return fibonacci(n - 1) + fibonacci(n - 2);
}

console.log(fibonacci(6)); // 8
```

### Practice Exercises

```javascript
// Exercise 1: Temperature converter
function celsiusToFahrenheit(celsius) {
    return (celsius * 9/5) + 32;
}

function fahrenheitToCelsius(fahrenheit) {
    return (fahrenheit - 32) * 5/9;
}

console.log(`20°C = ${celsiusToFahrenheit(20)}°F`);
console.log(`68°F = ${fahrenheitToCelsius(68)}°C`);

// Exercise 2: Number checker
function isEven(number) {
    return number % 2 === 0;
}

function isPositive(number) {
    return number > 0;
}

function numberInfo(num) {
    console.log(`${num} is ${isEven(num) ? 'even' : 'odd'}`);
    console.log(`${num} is ${isPositive(num) ? 'positive' : 'negative or zero'}`);
}

numberInfo(7);
numberInfo(-4);

// Exercise 3: Array utilities
function findMax(numbers) {
    let max = numbers[0];
    for (let i = 1; i < numbers.length; i++) {
        if (numbers[i] > max) {
            max = numbers[i];
        }
    }
    return max;
}

function sum(numbers) {
    let total = 0;
    for (let num of numbers) {
        total += num;
    }
    return total;
}

function average(numbers) {
    return sum(numbers) / numbers.length;
}

let scores = [85, 92, 78, 96, 87];
console.log(`Max: ${findMax(scores)}`);
console.log(`Sum: ${sum(scores)}`);
console.log(`Average: ${average(scores)}`);
```

---

## 8. Objects and Arrays

### Arrays

Arrays store multiple values in a single variable.

```javascript
// Creating arrays
let fruits = ["apple", "banana", "orange"];
let numbers = [1, 2, 3, 4, 5];
let mixed = ["hello", 42, true, null];

// Empty array
let empty = [];
let alsoEmpty = new Array();

// Accessing array elements
console.log(fruits[0]);    // "apple" (first element)
console.log(fruits[1]);    // "banana"
console.log(fruits[2]);    // "orange"
console.log(fruits[3]);    // undefined

// Array length
console.log(fruits.length); // 3

// Last element
console.log(fruits[fruits.length - 1]); // "orange"
```

#### Array Methods

```javascript
let fruits = ["apple", "banana"];

// Adding elements
fruits.push("orange");        // Add to end: ["apple", "banana", "orange"]
fruits.unshift("grape");      // Add to beginning: ["grape", "apple", "banana", "orange"]

// Removing elements
let lastFruit = fruits.pop();       // Remove from end: "orange"
let firstFruit = fruits.shift();    // Remove from beginning: "grape"

console.log(fruits); // ["apple", "banana"]

// Finding elements
let index = fruits.indexOf("banana");  // 1
let exists = fruits.includes("apple"); // true

// Slicing (doesn't modify original)
let numbers = [1, 2, 3, 4, 5];
let slice = numbers.slice(1, 4);    // [2, 3, 4]
console.log(numbers);               // [1, 2, 3, 4, 5] (unchanged)

// Splicing (modifies original)
let colors = ["red", "green", "blue", "yellow"];
let removed = colors.splice(1, 2);  // Remove 2 elements starting at index 1
console.log(colors);                // ["red", "yellow"]
console.log(removed);               // ["green", "blue"]

// Adding with splice
colors.splice(1, 0, "purple", "pink"); // Add at index 1
console.log(colors);                    // ["red", "purple", "pink", "yellow"]
```

#### Array Iteration

```javascript
let numbers = [1, 2, 3, 4, 5];

// For loop
for (let i = 0; i < numbers.length; i++) {
    console.log(numbers[i]);
}

// For...of loop (modern way)
for (let number of numbers) {
    console.log(number);
}

// forEach method
numbers.forEach(function(number, index) {
    console.log(`Index ${index}: ${number}`);
});

// Arrow function version
numbers.forEach((number, index) => {
    console.log(`Index ${index}: ${number}`);
});
```

#### Useful Array Methods

```javascript
let numbers = [1, 2, 3, 4, 5];

// Map - transform each element
let doubled = numbers.map(x => x * 2);
console.log(doubled); // [2, 4, 6, 8, 10]

// Filter - select elements that meet condition
let evens = numbers.filter(x => x % 2 === 0);
console.log(evens); // [2, 4]

// Find - first element that meets condition
let found = numbers.find(x => x > 3);
console.log(found); // 4

// Reduce - combine all elements into single value
let sum = numbers.reduce((total, current) => total + current, 0);
console.log(sum); // 15

// Some - check if any element meets condition
let hasEven = numbers.some(x => x % 2 === 0);
console.log(hasEven); // true

// Every - check if all elements meet condition
let allPositive = numbers.every(x => x > 0);
console.log(allPositive); // true
```

### Objects

Objects store data in key-value pairs.

```javascript
// Creating objects
let person = {
    name: "John Doe",
    age: 30,
    city: "New York",
    isStudent: false
};

// Accessing object properties
console.log(person.name);        // "John Doe" (dot notation)
console.log(person["age"]);      // 30 (bracket notation)

// Adding properties
person.email = "john@example.com";
person["phone"] = "123-456-7890";

// Modifying properties
person.age = 31;
person["city"] = "Los Angeles";

// Deleting properties
delete person.isStudent;

console.log(person);
```

#### Object Methods

```javascript
let calculator = {
    // Properties
    brand: "Scientific Calculator",
    
    // Methods
    add: function(a, b) {
        return a + b;
    },
    
    subtract: function(a, b) {
        return a - b;
    },
    
    // Modern method syntax (ES6+)
    multiply(a, b) {
        return a * b;
    },
    
    // Arrow functions don't work well as methods
    divide: (a, b) => a / b // Avoid this pattern
};

console.log(calculator.add(5, 3));      // 8
console.log(calculator.multiply(4, 2)); // 8
```

#### The 'this' Keyword

```javascript
let person = {
    firstName: "Alice",
    lastName: "Johnson",
    
    getFullName: function() {
        return this.firstName + " " + this.lastName;
    },
    
    introduce: function() {
        return `Hi, I'm ${this.getFullName()}`;
    }
};

console.log(person.getFullName()); // "Alice Johnson"
console.log(person.introduce());   // "Hi, I'm Alice Johnson"
```

#### Object Utilities

```javascript
let person = {
    name: "Bob",
    age: 25,
    city: "Boston"
};

// Get all keys
let keys = Object.keys(person);
console.log(keys); // ["name", "age", "city"]

// Get all values
let values = Object.values(person);
console.log(values); // ["Bob", 25, "Boston"]

// Get key-value pairs
let entries = Object.entries(person);
console.log(entries); // [["name", "Bob"], ["age", 25], ["city", "Boston"]]

// Check if property exists
console.log("name" in person);           // true
console.log(person.hasOwnProperty("age")); // true
```

#### Nested Objects and Arrays

```javascript
let student = {
    name: "Sarah",
    grades: [85, 92, 78, 96],
    address: {
        street: "123 Main St",
        city: "Springfield",
        zipCode: "12345"
    },
    courses: [
        { name: "Math", grade: 90 },
        { name: "English", grade: 88 },
        { name: "Science", grade: 94 }
    ]
};

// Accessing nested data
console.log(student.address.city);        // "Springfield"
console.log(student.grades[0]);           // 85
console.log(student.courses[1].name);     // "English"

// Modifying nested data
student.address.city = "New Springfield";
student.grades.push(89);
student.courses[0].grade = 92;
```

### Practice Exercises

```javascript
// Exercise 1: Student grade book
let student = {
    name: "Alex Smith",
    grades: [],
    
    addGrade: function(grade) {
        this.grades.push(grade);
    },
    
    getAverage: function() {
        if (this.grades.length === 0) return 0;
        let sum = this.grades.reduce((total, grade) => total + grade, 0);
        return sum / this.grades.length;
    },
    
    getLetterGrade: function() {
        let avg = this.getAverage();
        if (avg >= 90) return "A";
        if (avg >= 80) return "B";
        if (avg >= 70) return "C";
        if (avg >= 60) return "D";
        return "F";
    }
};

student.addGrade(85);
student.addGrade(92);
student.addGrade(78);
console.log(`${student.name}'s average: ${student.getAverage().toFixed(1)}`);
console.log(`Letter grade: ${student.getLetterGrade()}`);

// Exercise 2: Shopping cart
let cart = {
    items: [],
    
    addItem: function(name, price, quantity = 1) {
        this.items.push({ name, price, quantity });
    },
    
    removeItem: function(name) {
        this.items = this.items.filter(item => item.name !== name);
    },
    
    getTotal: function() {
        return this.items.reduce((total, item) => {
            return total + (item.price * item.quantity);
        }, 0);
    },
    
    displayCart: function() {
        console.log("Shopping Cart:");
        this.items.forEach(item => {
            console.log(`${item.name} - $${item.price} x ${item.quantity}`);
        });
        console.log(`Total: $${this.getTotal().toFixed(2)}`);
    }
};

cart.addItem("Apple", 0.99, 3);
cart.addItem("Bread", 2.50, 1);
cart.addItem("Milk", 3.25, 2);
cart.displayCart();

// Exercise 3: Array manipulation
let numbers = [3, 1, 4, 1, 5, 9, 2, 6, 5];

// Remove duplicates
let unique = [...new Set(numbers)];
console.log("Unique numbers:", unique);

// Sort in ascending order
let sorted = [...numbers].sort((a, b) => a - b);
console.log("Sorted:", sorted);

// Get even numbers
let evens = numbers.filter(n => n % 2 === 0);
console.log("Even numbers:", evens);

// Double all numbers
let doubled = numbers.map(n => n * 2);
console.log("Doubled:", doubled);
```

---

## 9. Strings and String Methods

### String Basics

```javascript
// Creating strings
let singleQuotes = 'Hello World';
let doubleQuotes = "Hello World";
let templateLiteral = `Hello World`;

// Multi-line strings
let multiLine = `This is a
multi-line
string`;

// Escape characters
let escaped = "He said, \"Hello!\"";
let newLine = "First line\nSecond line";
let tab = "Column1\tColumn2";
let backslash = "This is a backslash: \\";

console.log(escaped);   // He said, "Hello!"
console.log(newLine);   // First line (new line) Second line
```

### String Properties and Basic Methods

```javascript
let message = "Hello, World!";

// Length property
console.log(message.length); // 13

// Accessing characters
console.log(message[0]);        // "H"
console.log(message.charAt(0)); // "H"
console.log(message.charAt(7)); // "W"

// Case conversion
console.log(message.toUpperCase()); // "HELLO, WORLD!"
console.log(message.toLowerCase()); // "hello, world!"

// Original string is unchanged
console.log(message); // "Hello, World!"
```

### String Search Methods

```javascript
let text = "The quick brown fox jumps over the lazy dog";

// Finding substrings
console.log(text.indexOf("quick"));     // 4
console.log(text.indexOf("cat"));       // -1 (not found)
console.log(text.lastIndexOf("the"));   // 31

// Check if string contains substring
console.log(text.includes("fox"));      // true
console.log(text.includes("cat"));      // false

// Check start and end
console.log(text.startsWith("The"));    // true
console.log(text.endsWith("dog"));      // true

// Search with regular expressions
console.log(text.search(/fox/));        // 16
console.log(text.match(/the/gi));       // ["The", "the"] (global, case-insensitive)
```

### String Extraction Methods

```javascript
let text = "Hello, World!";

// Substring methods
console.log(text.slice(0, 5));          // "Hello"
console.log(text.slice(7));             // "World!"
console.log(text.slice(-6));            // "World!"
console.log(text.slice(-6, -1));        // "World"

console.log(text.substring(0, 5));      // "Hello"
console.log(text.substr(7, 5));         // "World" (deprecated)

// Character extraction
console.log(text.charAt(1));            // "e"
console.log(text.charCodeAt(1));        // 101 (ASCII code)
```

### String Modification Methods

```javascript
let text = "  Hello, World!  ";

// Trimming whitespace
console.log(text.trim());               // "Hello, World!"
console.log(text.trimStart());          // "Hello, World!  "
console.log(text.trimEnd());            // "  Hello, World!"

// Replacing text
let message = "Hello, World!";
console.log(message.replace("World", "JavaScript")); // "Hello, JavaScript!"
console.log(message.replaceAll("l", "L"));           // "HeLLo, WorLd!"

// Padding
let num = "5";
console.log(num.padStart(3, "0"));      // "005"
console.log(num.padEnd(3, "0"));        // "500"

// Repeating
console.log("Ha".repeat(3));            // "HaHaHa"
```

### String Splitting and Joining

```javascript
// Splitting strings
let csv = "apple,banana,orange,grape";
let fruits = csv.split(",");
console.log(fruits); // ["apple", "banana", "orange", "grape"]

let sentence = "The quick brown fox";
let words = sentence.split(" ");
console.log(words); // ["The", "quick", "brown", "fox"]

// Split with limit
let limited = sentence.split(" ", 2);
console.log(limited); // ["The", "quick"]

// Joining arrays
let joined = fruits.join(" | ");
console.log(joined); // "apple | banana | orange | grape"

let rejoined = words.join(" ");
console.log(rejoined); // "The quick brown fox"
```

### Template Literals (Advanced)

```javascript
let name = "Alice";
let age = 30;

// Basic template literal
let greeting = `Hello, my name is ${name} and I'm ${age} years old.`;

// Expressions in template literals
let message = `Next year I'll be ${age + 1} years old.`;

// Multi-line template literals
let html = `
    <div>
        <h1>Welcome, ${name}!</h1>
        <p>You are ${age} years old.</p>
    </div>
`;

// Function calls in template literals
function formatCurrency(amount) {
    return `$${amount.toFixed(2)}`;
}

let price = 19.99;
let product = `The product costs ${formatCurrency(price)}`;
console.log(product); // "The product costs $19.99"
```

### String Comparison

```javascript
let str1 = "apple";
let str2 = "banana";
let str3 = "Apple";

// Basic comparison
console.log(str1 === str2);  // false
console.log(str1 === str3);  // false (case-sensitive)

// Alphabetical comparison
console.log(str1 < str2);    // true (a comes before b)
console.log(str1 > str3);    // true (lowercase > uppercase in ASCII)

// Case-insensitive comparison
console.log(str1.toLowerCase() === str3.toLowerCase()); // true

// Locale-aware comparison
console.log(str1.localeCompare(str2)); // -1 (str1 comes before str2)
console.log(str2.localeCompare(str1)); // 1 (str2 comes after str1)
console.log(str1.localeCompare(str1)); // 0 (equal)
```

### Regular Expressions (Basic)

```javascript
let text = "The phone number is 123-456-7890";

// Test pattern
let phonePattern = /\d{3}-\d{3}-\d{4}/;
console.log(phonePattern.test(text)); // true

// Extract matches
let matches = text.match(phonePattern);
console.log(matches[0]); // "123-456-7890"

// Global search
let emailText = "Contact us at info@example.com or support@example.com";
let emailPattern = /\w+@\w+\.\w+/g;
let emails = emailText.match(emailPattern);
console.log(emails); // ["info@example.com", "support@example.com"]

// Replace with pattern
let cleanText = "Remove   extra    spaces";
let cleaned = cleanText.replace(/\s+/g, " ");
console.log(cleaned); // "Remove extra spaces"
```

### Practice Exercises

```javascript
// Exercise 1: String utilities
function stringUtils() {
    // Reverse a string
    function reverseString(str) {
        return str.split("").reverse().join("");
    }
    
    // Count vowels
    function countVowels(str) {
        let vowels = str.toLowerCase().match(/[aeiou]/g);
        return vowels ? vowels.length : 0;
    }
    
    // Capitalize first letter of each word
    function titleCase(str) {
        return str.split(" ")
                  .map(word => word.charAt(0).toUpperCase() + word.slice(1).toLowerCase())
                  .join(" ");
    }
    
    // Check if palindrome
    function isPalindrome(str) {
        let cleaned = str.toLowerCase().replace(/[^a-z]/g, "");
        return cleaned === cleaned.split("").reverse().join("");
    }
    
    return { reverseString, countVowels, titleCase, isPalindrome };
}

let utils = stringUtils();
console.log(utils.reverseString("hello"));           // "olleh"
console.log(utils.countVowels("JavaScript"));        // 3
console.log(utils.titleCase("hello world"));         // "Hello World"
console.log(utils.isPalindrome("A man a plan a canal Panama")); // true

// Exercise 2: Text processor
function processText(text) {
    let words = text.toLowerCase().split(/\s+/);
    
    // Word count
    let wordCount = words.length;
    
    // Character count (no spaces)
    let charCount = text.replace(/\s/g, "").length;
    
    // Most frequent word
    let wordFreq = {};
    words.forEach(word => {
        wordFreq[word] = (wordFreq[word] || 0) + 1;
    });
    
    let mostFrequent = Object.keys(wordFreq).reduce((a, b) => 
        wordFreq[a] > wordFreq[b] ? a : b
    );
    
    return {
        wordCount,
        charCount,
        mostFrequent,
        wordFrequency: wordFreq
    };
}

let analysis = processText("The quick brown fox jumps over the lazy dog. The dog was really lazy.");
console.log(analysis);

// Exercise 3: URL builder
function buildURL(base, params = {}) {
    let url = base;
    let queryParams = Object.keys(params)
        .map(key => `${encodeURIComponent(key)}=${encodeURIComponent(params[key])}`)
        .join("&");
    
    if (queryParams) {
        url += (base.includes("?") ? "&" : "?") + queryParams;
    }
    
    return url;
}

let url = buildURL("https://api.example.com/search", {
    q: "javascript",
    limit: 10,
    category: "programming"
});
console.log(url);
// "https://api.example.com/search?q=javascript&limit=10&category=programming"
```

---

## 10. Working with the DOM

### What is the DOM?

The Document Object Model (DOM) is a programming interface for HTML documents. It represents the page as a tree of objects that JavaScript can manipulate.

```html
<!DOCTYPE html>
<html>
<head>
    <title>DOM Example</title>
</head>
<body>
    <h1 id="main-title">Welcome to JavaScript</h1>
    <p class="intro">This is a paragraph.</p>
    <ul id="fruit-list">
        <li>Apple</li>
        <li>Banana</li>
        <li>Orange</li>
    </ul>
    <button id="change-btn">Click me!</button>
</body>
</html>
```

### Selecting Elements

```javascript
// Select by ID
let title = document.getElementById("main-title");
console.log(title); // <h1 id="main-title">Welcome to JavaScript</h1>

// Select by class name
let intro = document.getElementsByClassName("intro")[0]; // Returns array-like object
console.log(intro);

// Select by tag name
let allParagraphs = document.getElementsByTagName("p");
console.log(allParagraphs);

// Modern selectors (CSS-style)
let titleByQuery = document.querySelector("#main-title");      // First match
let introByQuery = document.querySelector(".intro");
let firstLi = document.querySelector("li");

// Select all matching elements
let allLis = document.querySelectorAll("li");               // NodeList
let allIntros = document.querySelectorAll(".intro");

// Advanced selectors
let secondLi = document.querySelector("li:nth-child(2)");
let lastLi = document.querySelector("li:last-child");
```

### Manipulating Content

```javascript
// Text content
let title = document.querySelector("#main-title");
console.log(title.textContent);        // "Welcome to JavaScript"
title.textContent = "Hello, DOM!";     // Changes text

// HTML content
let intro = document.querySelector(".intro");
console.log(intro.innerHTML);          // "This is a paragraph."
intro.innerHTML = "<strong>This is bold text!</strong>";

// Input values
// For <input type="text" id="user-input">
let input = document.querySelector("#user-input");
console.log(input.value);              // Gets input value
input.value = "New value";             // Sets input value
```

### Manipulating Attributes

```javascript
let title = document.querySelector("#main-title");

// Get attributes
console.log(title.id);                 // "main-title"
console.log(title.getAttribute("id")); // "main-title"

// Set attributes
title.setAttribute("class", "highlight");
title.id = "new-title";

// Remove attributes
title.removeAttribute("class");

// Check if attribute exists
if (title.hasAttribute("class")) {
    console.log("Has class attribute");
}

// Data attributes
// For <div data-user-id="123" data-role="admin">
let userDiv = document.querySelector("[data-user-id]");
console.log(userDiv.dataset.userId);   // "123"
console.log(userDiv.dataset.role);     // "admin"
userDiv.dataset.status = "active";     // Sets data-status="active"
```

### Manipulating Styles

```javascript
let title = document.querySelector("#main-title");

// Inline styles
title.style.color = "blue";
title.style.fontSize = "24px";
title.style.backgroundColor = "yellow";

// Multiple styles
title.style.cssText = "color: red; font-size: 28px; font-weight: bold;";

// CSS classes
title.classList.add("highlight");          // Add class
title.classList.remove("old-style");       // Remove class
title.classList.toggle("active");          // Toggle class
title.classList.contains("highlight");     // Check if class exists

// Replace class
title.className = "new-class another-class";

// Computed styles (read-only)
let computedStyle = window.getComputedStyle(title);
console.log(computedStyle.color);
console.log(computedStyle.fontSize);
```

### Creating and Modifying Elements

```javascript
// Create new elements
let newParagraph = document.createElement("p");
newParagraph.textContent = "This is a new paragraph";
newParagraph.className = "dynamic-content";

let newImage = document.createElement("img");
newImage.src = "image.jpg";
newImage.alt = "Description";

// Create element with HTML
let container = document.createElement("div");
container.innerHTML = `
    <h3>New Section</h3>
    <p>This is dynamically created content.</p>
`;

// Add elements to DOM
let body = document.body;
body.appendChild(newParagraph);              // Add to end
body.insertBefore(container, newParagraph); // Insert before

// More insertion methods
let list = document.querySelector("#fruit-list");
let newItem = document.createElement("li");
newItem.textContent = "Grape";

list.appendChild(newItem);                   // Add to end
list.insertAdjacentHTML("beforeend", "<li>Mango</li>");

// Insert positions for insertAdjacentHTML:
// "beforebegin" - before the element
// "afterbegin" - inside, before first child
// "beforeend" - inside, after last child  
// "afterend" - after the element
```

### Removing Elements

```javascript
// Remove element
let elementToRemove = document.querySelector(".old-content");
if (elementToRemove) {
    elementToRemove.remove();               // Modern way
    // elementToRemove.parentNode.removeChild(elementToRemove); // Old way
}

// Remove all children
let list = document.querySelector("#fruit-list");
list.innerHTML = "";                        // Quick way
// Or loop through and remove each child

// Replace element
let oldElement = document.querySelector("#old-element");
let newElement = document.createElement("div");
newElement.textContent = "New content";
oldElement.parentNode.replaceChild(newElement, oldElement);
```

### Navigating the DOM

```javascript
let list = document.querySelector("#fruit-list");

// Parent navigation
console.log(list.parentNode);              // Parent element
console.log(list.parentElement);           // Same as parentNode (usually)

// Children navigation
console.log(list.children);                // HTML elements only
console.log(list.childNodes);              // All nodes (including text)
console.log(list.firstElementChild);       // First HTML element child
console.log(list.lastElementChild);        // Last HTML element child

// Sibling navigation
let firstItem = list.firstElementChild;
console.log(firstItem.nextElementSibling); // Next sibling element
console.log(firstItem.previousElementSibling); // Previous sibling

// Check relationships
console.log(list.contains(firstItem));     // true
```

### Form Manipulation

```javascript
// Working with forms
let form = document.querySelector("#contact-form");
let nameInput = document.querySelector("#name");
let emailInput = document.querySelector("#email");
let submitBtn = document.querySelector("#submit-btn");

// Get form data
function getFormData() {
    return {
        name: nameInput.value,
        email: emailInput.value
    };
}

// Set form data
function setFormData(data) {
    nameInput.value = data.name;
    emailInput.value = data.email;
}

// Form validation
function validateForm() {
    let isValid = true;
    
    if (nameInput.value.trim() === "") {
        nameInput.classList.add("error");
        isValid = false;
    } else {
        nameInput.classList.remove("error");
    }
    
    if (!emailInput.value.includes("@")) {
        emailInput.classList.add("error");
        isValid = false;
    } else {
        emailInput.classList.remove("error");
    }
    
    return isValid;
}

// Reset form
function resetForm() {
    form.reset();                           // Built-in method
    // Or manually:
    // nameInput.value = "";
    // emailInput.value = "";
}
```

### Practice Exercises

```javascript
// Exercise 1: Dynamic list manager
function createListManager() {
    let list = document.querySelector("#task-list");
    let input = document.querySelector("#task-input");
    let addBtn = document.querySelector("#add-task");
    
    function addTask() {
        let taskText = input.value.trim();
        if (taskText === "") return;
        
        let listItem = document.createElement("li");
        listItem.innerHTML = `
            <span>${taskText}</span>
            <button class="delete-btn">Delete</button>
        `;
        
        // Add delete functionality
        let deleteBtn = listItem.querySelector(".delete-btn");
        deleteBtn.addEventListener("click", () => {
            listItem.remove();
        });
        
        list.appendChild(listItem);
        input.value = "";
    }
    
    addBtn.addEventListener("click", addTask);
    
    input.addEventListener("keypress", (e) => {
        if (e.key === "Enter") {
            addTask();
        }
    });
}

// Exercise 2: Image gallery
function createImageGallery() {
    let gallery = document.querySelector("#gallery");
    let mainImage = document.querySelector("#main-image");
    
    let images = [
        { src: "image1.jpg", alt: "Image 1" },
        { src: "image2.jpg", alt: "Image 2" },
        { src: "image3.jpg", alt: "Image 3" }
    ];
    
    // Create thumbnails
    images.forEach((img, index) => {
        let thumbnail = document.createElement("img");
        thumbnail.src = img.src;
        thumbnail.alt = img.alt;
        thumbnail.classList.add("thumbnail");
        
        thumbnail.addEventListener("click", () => {
            mainImage.src = img.src;
            mainImage.alt = img.alt;
            
            // Update active thumbnail
            document.querySelectorAll(".thumbnail").forEach(thumb => {
                thumb.classList.remove("active");
            });
            thumbnail.classList.add("active");
        });
        
        gallery.appendChild(thumbnail);
    });
    
    // Set first image as default
    if (images.length > 0) {
        mainImage.src = images[0].src;
        mainImage.alt = images[0].alt;
        gallery.firstChild.classList.add("active");
    }
}

// Exercise 3: Theme switcher
function createThemeSwitcher() {
    let themeBtn = document.querySelector("#theme-toggle");
    let currentTheme = localStorage.getItem("theme") || "light";
    
    // Apply saved theme
    document.body.classList.add(currentTheme + "-theme");
    updateThemeButton();
    
    function toggleTheme() {
        if (currentTheme === "light") {
            currentTheme = "dark";
        } else {
            currentTheme = "light";
        }
        
        // Update DOM
        document.body.classList.remove("light-theme", "dark-theme");
        document.body.classList.add(currentTheme + "-theme");
        
        // Save preference
        localStorage.setItem("theme", currentTheme);
        updateThemeButton();
    }
    
    function updateThemeButton() {
        themeBtn.textContent = currentTheme === "light" ? "🌙" : "☀️";
        themeBtn.title = `Switch to ${currentTheme === "light" ? "dark" : "light"} theme`;
    }
    
    themeBtn.addEventListener("click", toggleTheme);
}
```

---

## 11. Events and Event Handling

### What are Events?

Events are actions that happen in the browser - user clicks, page loads, forms submit, etc. JavaScript can "listen" for these events and respond to them.

### Adding Event Listeners

```javascript
// Method 1: addEventListener (recommended)
let button = document.querySelector("#my-button");
button.addEventListener("click", function() {
    console.log("Button was clicked!");
});

// Method 2: Arrow function
button.addEventListener("click", () => {
    console.log("Button clicked with arrow function!");
});

// Method 3: Named function
function handleClick() {
    console.log("Button clicked with named function!");
}
button.addEventListener("click", handleClick);

// Method 4: HTML attribute (not recommended)
// <button onclick="handleClick()">Click me</button>

// Method 5: DOM property (not recommended)
button.onclick = handleClick;
```

### Common Events

```javascript
let input = document.querySelector("#text-input");
let form = document.querySelector("#my-form");
let link = document.querySelector("#my-link");

// Mouse events
button.addEventListener("click", () => console.log("Clicked"));
button.addEventListener("dblclick", () => console.log("Double clicked"));
button.addEventListener("mousedown", () => console.log("Mouse down"));
button.addEventListener("mouseup", () => console.log("Mouse up"));
button.addEventListener("mouseenter", () => console.log("Mouse entered"));
button.addEventListener("mouseleave", () => console.log("Mouse left"));
button.addEventListener("mouseover", () => console.log("Mouse over"));

// Keyboard events
input.addEventListener("keydown", () => console.log("Key pressed down"));
input.addEventListener("keyup", () => console.log("Key released"));
input.addEventListener("keypress", () => console.log("Key pressed")); // Deprecated

// Form events
form.addEventListener("submit", () => console.log("Form submitted"));
input.addEventListener("change", () => console.log("Input changed"));
input.addEventListener("input", () => console.log("Input value changed"));
input.addEventListener("focus", () => console.log("Input focused"));
input.addEventListener("blur", () => console.log("Input lost focus"));

// Window events
window.addEventListener("load", () => console.log("Page loaded"));
window.addEventListener("resize", () => console.log("Window resized"));
window.addEventListener("scroll", () => console.log("Page scrolled"));
```

### Event Object

```javascript
button.addEventListener("click", function(event) {
    console.log("Event type:", event.type);           // "click"
    console.log("Target element:", event.target);     // The clicked element
    console.log("Current target:", event.currentTarget); // Element with listener
    console.log("Mouse position:", event.clientX, event.clientY);
    console.log("Timestamp:", event.timeStamp);
    
    // Prevent default behavior
    event.preventDefault();
    
    // Stop event from bubbling up
    event.stopPropagation();
});

// Keyboard events
input.addEventListener("keydown", function(event) {
    console.log("Key pressed:", event.key);           // "a", "Enter", "Shift"
    console.log("Key code:", event.code);             // "KeyA", "Enter", "ShiftLeft"
    console.log("Ctrl pressed:", event.ctrlKey);      // true/false
    console.log("Shift pressed:", event.shiftKey);    // true/false
    console.log("Alt pressed:", event.altKey);        // true/false
});

// Mouse events
button.addEventListener("click", function(event) {
    console.log("Button pressed:", event.button);     // 0=left, 1=middle, 2=right
    console.log("Click position:", event.pageX, event.pageY);
    console.log("Relative to element:", event.offsetX, event.offsetY);
});
```

### Event Delegation

```javascript
// Instead of adding listeners to each item
let list = document.querySelector("#item-list");

// Add single listener to parent
list.addEventListener("click", function(event) {
    // Check if clicked element is a list item
    if (event.target.tagName === "LI") {
        console.log("List item clicked:", event.target.textContent);
        event.target.classList.toggle("selected");
    }
    
    // Check if clicked element is a delete button
    if (event.target.classList.contains("delete-btn")) {
        event.target.parentElement.remove();
    }
});

// This works even for dynamically added items!
function addNewItem(text) {
    let newItem = document.createElement("li");
    newItem.innerHTML = `
        ${text} 
        <button class="delete-btn">Delete</button>
    `;
    list.appendChild(newItem);
}
```

### Removing Event Listeners

```javascript
function handleClick() {
    console.log("Button clicked!");
}

// Add listener
button.addEventListener("click", handleClick);

// Remove listener (must be same function reference)
button.removeEventListener("click", handleClick);

// Anonymous functions can't be removed
button.addEventListener("click", function() {
    console.log("This can't be removed!");
});

// Solution: Store function reference
let myHandler = function() {
    console.log("This can be removed!");
};
button.addEventListener("click", myHandler);
button.removeEventListener("click", myHandler);
```

### Event Options

```javascript
// Event listener options
button.addEventListener("click", handleClick, {
    once: true,       // Run only once
    passive: true,    // Never calls preventDefault
    capture: true     // Capture phase instead of bubbling
});

// Older syntax (boolean for capture)
button.addEventListener("click", handleClick, true);
```

### Custom Events

```javascript
// Create custom event
let customEvent = new CustomEvent("userLoggedIn", {
    detail: {
        username: "john_doe",
        timestamp: Date.now()
    }
});

// Listen for custom event
document.addEventListener("userLoggedIn", function(event) {
    console.log("User logged in:", event.detail.username);
    console.log("At:", new Date(event.detail.timestamp));
});

// Dispatch custom event
document.dispatchEvent(customEvent);

// Custom event on specific element
let widget = document.querySelector("#my-widget");
widget.addEventListener("dataUpdated", function(event) {
    console.log("Widget data updated:", event.detail);
});

// Trigger custom event
widget.dispatchEvent(new CustomEvent("dataUpdated", {
    detail: { newData: [1, 2, 3] }
}));
```

### Practical Examples

```javascript
// Example 1: Form validation with events
function setupFormValidation() {
    let form = document.querySelector("#registration-form");
    let emailInput = document.querySelector("#email");
    let passwordInput = document.querySelector("#password");
    let confirmInput = document.querySelector("#confirm-password");
    
    // Real-time validation
    emailInput.addEventListener("blur", validateEmail);
    passwordInput.addEventListener("input", validatePassword);
    confirmInput.addEventListener("input", validatePasswordMatch);
    
    // Form submission
    form.addEventListener("submit", function(event) {
        event.preventDefault(); // Stop form submission
        
        if (validateForm()) {
            console.log("Form is valid - would submit here");
            // Actually submit form or send AJAX request
        }
    });
    
    function validateEmail() {
        let email = emailInput.value;
        let isValid = email.includes("@") && email.includes(".");
        
        if (isValid) {
            emailInput.classList.remove("error");
            emailInput.classList.add("valid");
        } else {
            emailInput.classList.remove("valid");
            emailInput.classList.add("error");
        }
        
        return isValid;
    }
    
    function validatePassword() {
        let password = passwordInput.value;
        let isValid = password.length >= 8;
        
        passwordInput.classList.toggle("error", !isValid);
        passwordInput.classList.toggle("valid", isValid);
        
        // Also revalidate confirm password
        validatePasswordMatch();
        
        return isValid;
    }
    
    function validatePasswordMatch() {
        let password = passwordInput.value;
        let confirm = confirmInput.value;
        let isValid = password === confirm && confirm.length > 0;
        
        confirmInput.classList.toggle("error", !isValid);
        confirmInput.classList.toggle("valid", isValid);
        
        return isValid;
    }
    
    function validateForm() {
        return validateEmail() && validatePassword() && validatePasswordMatch();
    }
}

// Example 2: Interactive dropdown menu
function createDropdown() {
    let dropdown = document.querySelector("#dropdown");
    let trigger = dropdown.querySelector(".dropdown-trigger");
    let menu = dropdown.querySelector(".dropdown-menu");
    
    // Toggle dropdown
    trigger.addEventListener("click", function(event) {
        event.stopPropagation();
        menu.classList.toggle("show");
    });
    
    // Close dropdown when clicking outside
    document.addEventListener("click", function() {
        menu.classList.remove("show");
    });
    
    // Prevent closing when clicking inside menu
    menu.addEventListener("click", function(event) {
        event.stopPropagation();
    });
    
    // Handle menu item selection
    menu.addEventListener("click", function(event) {
        if (event.target.classList.contains("dropdown-item")) {
            trigger.textContent = event.target.textContent;
            menu.classList.remove("show");
            
            // Trigger custom event
            dropdown.dispatchEvent(new CustomEvent("selectionChanged", {
                detail: { value: event.target.dataset.value }
            }));
        }
    });
}

// Example 3: Drag and drop
function setupDragAndDrop() {
    let draggables = document.querySelectorAll(".draggable");
    let dropZones = document.querySelectorAll(".drop-zone");
    
    // Make elements draggable
    draggables.forEach(item => {
        item.addEventListener("dragstart", function(event) {
            event.dataTransfer.setData("text/plain", item.id);
            item.classList.add("dragging");
        });
        
        item.addEventListener("dragend", function() {
            item.classList.remove("dragging");
        });
    });
    
    // Setup drop zones
    dropZones.forEach(zone => {
        zone.addEventListener("dragover", function(event) {
            event.preventDefault(); // Allow drop
            zone.classList.add("drag-over");
        });
        
        zone.addEventListener("dragleave", function() {
            zone.classList.remove("drag-over");
        });
        
        zone.addEventListener("drop", function(event) {
            event.preventDefault();
            zone.classList.remove("drag-over");
            
            let draggedId = event.dataTransfer.getData("text/plain");
            let draggedElement = document.getElementById(draggedId);
            
            if (draggedElement) {
                zone.appendChild(draggedElement);
            }
        });
    });
}
```

### Practice Exercises

```javascript
// Exercise 1: Image carousel
function createCarousel() {
    let carousel = document.querySelector("#carousel");
    let images = carousel.querySelectorAll("img");
    let prevBtn = document.querySelector("#prev-btn");
    let nextBtn = document.querySelector("#next-btn");
    let currentIndex = 0;
    
    function showImage(index) {
        images.forEach((img, i) => {
            img.style.display = i === index ? "block" : "none";
        });
    }
    
    function nextImage() {
        currentIndex = (currentIndex + 1) % images.length;
        showImage(currentIndex);
    }
    
    function prevImage() {
        currentIndex = (currentIndex - 1 + images.length) % images.length;
        showImage(currentIndex);
    }
    
    // Event listeners
    nextBtn.addEventListener("click", nextImage);
    prevBtn.addEventListener("click", prevImage);
    
    // Keyboard navigation
    document.addEventListener("keydown", function(event) {
        if (event.key === "ArrowLeft") prevImage();
        if (event.key === "ArrowRight") nextImage();
    });
    
    // Auto-play
    setInterval(nextImage, 3000);
    
    // Initialize
    showImage(0);
}

// Exercise 2: Modal dialog
function createModal() {
    let modal = document.querySelector("#modal");
    let openBtn = document.querySelector("#open-modal");
    let closeBtn = document.querySelector("#close-modal");
    let overlay = document.querySelector("#modal-overlay");
    
    function openModal() {
        modal.style.display = "block";
        document.body.style.overflow = "hidden"; // Prevent scrolling
    }
    
    function closeModal() {
        modal.style.display = "none";
        document.body.style.overflow = ""; // Restore scrolling
    }
    
    // Event listeners
    openBtn.addEventListener("click", openModal);
    closeBtn.addEventListener("click", closeModal);
    overlay.addEventListener("click", closeModal);
    
    // Close with Escape key
    document.addEventListener("keydown", function(event) {
        if (event.key === "Escape" && modal.style.display === "block") {
            closeModal();
        }
    });
}

// Exercise 3: Search with live results
function createSearchBox() {
    let searchInput = document.querySelector("#search-input");
    let resultsContainer = document.querySelector("#search-results");
    
    // Sample data
    let data = [
        "JavaScript", "Java", "Python", "C++", "Ruby", "PHP", 
        "Swift", "Kotlin", "Go", "Rust", "TypeScript"
    ];
    
    let searchTimeout;
    
    searchInput.addEventListener("input", function() {
        clearTimeout(searchTimeout);
        
        // Debounce search (wait for user to stop typing)
        searchTimeout = setTimeout(() => {
            let query = searchInput.value.toLowerCase().trim();
            
            if (query === "") {
                resultsContainer.innerHTML = "";
                return;
            }
            
            // Filter data
            let filtered = data.filter(item => 
                item.toLowerCase().includes(query)
            );
            
            // Display results
            if (filtered.length > 0) {
                resultsContainer.innerHTML = filtered
                    .map(item => `<div class="search-result">${item}</div>`)
                    .join("");
            } else {
                resultsContainer.innerHTML = "<div class='no-results'>No results found</div>";
            }
        }, 300); // Wait 300ms after user stops typing
    });
    
    // Handle result selection
    resultsContainer.addEventListener("click", function(event) {
        if (event.target.classList.contains("search-result")) {
            searchInput.value = event.target.textContent;
            resultsContainer.innerHTML = "";
        }
    });
}
```

---

## 12. Asynchronous JavaScript

### Understanding Synchronous vs Asynchronous

```javascript
// Synchronous code - runs line by line
console.log("First");
console.log("Second");
console.log("Third");
// Output: First, Second, Third

// Asynchronous code - doesn't block execution
console.log("First");
setTimeout(() => {
    console.log("Second (after delay)");
}, 1000);
console.log("Third");
// Output: First, Third, Second (after delay)
```

### setTimeout and setInterval

```javascript
// setTimeout - run once after delay
let timeoutId = setTimeout(() => {
    console.log("This runs after 2 seconds");
}, 2000);

// Cancel timeout
clearTimeout(timeoutId);

// setInterval - run repeatedly
let intervalId = setInterval(() => {
    console.log("This runs every second");
}, 1000);

// Cancel interval
setTimeout(() => {
    clearInterval(intervalId);
    console.log("Interval stopped");
}, 5000);

// Practical example: Countdown timer
function createCountdown(seconds) {
    let remaining = seconds;
    
    let interval = setInterval(() => {
        console.log(`${remaining} seconds remaining`);
        remaining--;
        
        if (remaining < 0) {
            clearInterval(interval);
            console.log("Time's up!");
        }
    }, 1000);
}

createCountdown(5);
```

### Callbacks

```javascript
// Function that takes a callback
function fetchData(callback) {
    console.log("Fetching data...");
    
    setTimeout(() => {
        let data = { id: 1, name: "John Doe" };
        callback(data);
    }, 2000);
}

// Using the callback
fetchData(function(result) {
    console.log("Data received:", result);
});

// Callback hell (avoid this pattern)
function step1(callback) {
    setTimeout(() => {
        console.log("Step 1 complete");
        callback();
    }, 1000);
}

function step2(callback) {
    setTimeout(() => {
        console.log("Step 2 complete");
        callback();
    }, 1000);
}

function step3(callback) {
    setTimeout(() => {
        console.log("Step 3 complete");
        callback();
    }, 1000);
}

// Nested callbacks (hard to read and maintain)
step1(() => {
    step2(() => {
        step3(() => {
            console.log("All steps complete");
        });
    });
});
```

### Promises

```javascript
// Creating a Promise
let myPromise = new Promise((resolve, reject) => {
    let success = true;
    
    setTimeout(() => {
        if (success) {
            resolve("Operation successful!");
        } else {
            reject("Operation failed!");
        }
    }, 2000);
});

// Using a Promise
myPromise
    .then(result => {
        console.log("Success:", result);
    })
    .catch(error => {
        console.log("Error:", error);
    })
    .finally(() => {
        console.log("Promise completed");
    });

// Promise states
console.log(myPromise); // Promise { <pending> }

// Chaining Promises
function fetchUser(id) {
    return new Promise((resolve, reject) => {
        setTimeout(() => {
            if (id > 0) {
                resolve({ id: id, name: `User ${id}` });
            } else {
                reject("Invalid user ID");
            }
        }, 1000);
    });
}

function fetchUserPosts(user) {
    return new Promise((resolve) => {
        setTimeout(() => {
            resolve([
                { title: "Post 1", author: user.name },
                { title: "Post 2", author: user.name }
            ]);
        }, 1000);
    });
}

// Promise chaining
fetchUser(1)
    .then(user => {
        console.log("User:", user);
        return fetchUserPosts(user);
    })
    .then(posts => {
        console.log("Posts:", posts);
    })
    .catch(error => {
        console.log("Error:", error);
    });
```

### Promise Utilities

```javascript
// Promise.all - wait for all promises
let promise1 = Promise.resolve(3);
let promise2 = new Promise(resolve => setTimeout(() => resolve('foo'), 1000));
let promise3 = Promise.resolve(42);

Promise.all([promise1, promise2, promise3])
    .then(values => {
        console.log(values); // [3, 'foo', 42]
    });

// Promise.allSettled - wait for all, regardless of outcome
let promises = [
    Promise.resolve('Success'),
    Promise.reject('Error'),
    Promise.resolve('Another success')
];

Promise.allSettled(promises)
    .then(results => {
        console.log(results);
        // [
        //   { status: 'fulfilled', value: 'Success' },
        //   { status: 'rejected', reason: 'Error' },
        //   { status: 'fulfilled', value: 'Another success' }
        // ]
    });

// Promise.race - first one to complete wins
let fastPromise = new Promise(resolve => setTimeout(() => resolve('Fast'), 100));
let slowPromise = new Promise(resolve => setTimeout(() => resolve('Slow'), 1000));

Promise.race([fastPromise, slowPromise])
    .then(result => {
        console.log(result); // 'Fast'
    });

// Promise.any - first one to succeed wins
Promise.any([
    Promise.reject('Error 1'),
    Promise.resolve('Success'),
    Promise.reject('Error 2')
])
.then(result => {
    console.log(result); // 'Success'
});
```

### Async/Await

```javascript
// Converting Promise chain to async/await
async function fetchUserData(id) {
    try {
        let user = await fetchUser(id);
        console.log("User:", user);
        
        let posts = await fetchUserPosts(user);
        console.log("Posts:", posts);
        
        return { user, posts };
    } catch (error) {
        console.log("Error:", error);
        throw error; // Re-throw if needed
    }
}

// Using async function
fetchUserData(1)
    .then(result => {
        console.log("Complete data:", result);
    })
    .catch(error => {
        console.log("Failed to fetch data:", error);
    });

// Async/await with multiple operations
async function processMultipleUsers() {
    try {
        // Sequential (one after another)
        let user1 = await fetchUser(1);
        let user2 = await fetchUser(2);
        
        // Parallel (at the same time)
        let [posts1, posts2] = await Promise.all([
            fetchUserPosts(user1),
            fetchUserPosts(user2)
        ]);
        
        return {
            user1: { ...user1, posts: posts1 },
            user2: { ...user2, posts: posts2 }
        };
    } catch (error) {
        console.log("Error processing users:", error);
    }
}

// Top-level await (in modules)
// const userData = await fetchUserData(1);
```

### Fetch API

```javascript
// Basic fetch
fetch('https://jsonplaceholder.typicode.com/posts/1')
    .then(response => response.json())
    .then(data => console.log(data))
    .catch(error => console.log('Error:', error));

// Fetch with async/await
async function fetchPost(id) {
    try {
        let response = await fetch(`https://jsonplaceholder.typicode.com/posts/${id}`);
        
        if (!response.ok) {
            throw new Error(`HTTP error! status: ${response.status}`);
        }
        
        let data = await response.json();
        return data;
    } catch (error) {
        console.log('Fetch error:', error);
        throw error;
    }
}

// POST request with fetch
async function createPost(postData) {
    try {
        let response = await fetch('https://jsonplaceholder.typicode.com/posts', {
            method: 'POST',
            headers: {
                'Content-Type': 'application/json',
            },
            body: JSON.stringify(postData)
        });
        
        if (!response.ok) {
            throw new Error(`HTTP error! status: ${response.status}`);
        }
        
        let data = await response.json();
        return data;
    } catch (error) {
        console.log('Error creating post:', error);
        throw error;
    }
}

// Using the functions
async function example() {
    try {
        // Fetch a post
        let post = await fetchPost(1);
        console.log('Fetched post:', post);
        
        // Create a new post
        let newPost = await createPost({
            title: 'My New Post',
            body: 'This is the content of my new post.',
            userId: 1
        });
        console.log('Created post:', newPost);
    } catch (error) {
        console.log('Example error:', error);
    }
}
```

### Error Handling in Async Code

```javascript
// Error handling with Promises
function riskyOperation() {
    return new Promise((resolve, reject) => {
        let random = Math.random();
        
        setTimeout(() => {
            if (random > 0.5) {
                resolve("Success!");
            } else {
                reject(new Error("Random failure"));
            }
        }, 1000);
    });
}

// Promise error handling
riskyOperation()
    .then(result => {
        console.log("Result:", result);
    })
    .catch(error => {
        console.log("Caught error:", error.message);
    });

// Async/await error handling
async function handleRiskyOperation() {
    try {
        let result = await riskyOperation();
        console.log("Result:", result);
    } catch (error) {
        console.log("Caught error:", error.message);
    }
}

// Global error handling
window.addEventListener('unhandledrejection', event => {
    console.log('Unhandled promise rejection:', event.reason);
    event.preventDefault(); // Prevent default browser error handling
});

// Timeout wrapper
function withTimeout(promise, timeoutMs) {
    return Promise.race([
        promise,
        new Promise((_, reject) => 
            setTimeout(() => reject(new Error('Timeout')), timeoutMs)
        )
    ]);
}

// Usage
withTimeout(fetchPost(1), 5000)
    .then(post => console.log('Post:', post))
    .catch(error => console.log('Error or timeout:', error.message));
```

### Practice Exercises

```javascript
// Exercise 1: Simple loading system
async function createLoader() {
    let loader = document.querySelector("#loader");
    let content = document.querySelector("#content");
    
    async function showLoading() {
        loader.style.display = "block";
        content.style.display = "none";
    }
    
    async function hideLoading() {
        loader.style.display = "none";
        content.style.display = "block";
    }
    
    async function loadData() {
        showLoading();
        
        try {
            // Simulate API call
            await new Promise(resolve => setTimeout(resolve, 2000));
            
            content.innerHTML = "<h2>Data loaded successfully!</h2>";
        } catch (error) {
            content.innerHTML = `<h2>Error: ${error.message}</h2>`;
        } finally {
            hideLoading();
        }
    }
    
    return { loadData };
}

// Exercise 2: Progress tracker
async function createProgressTracker() {
    let progressBar = document.querySelector("#progress");
    let statusText = document.querySelector("#status");
    
    async function simulateTask(name, duration) {
        statusText.textContent = `Processing ${name}...`;
        
        return new Promise(resolve => {
            let progress = 0;
            let interval = setInterval(() => {
                progress += 10;
                progressBar.style.width = `${progress}%`;
                
                if (progress >= 100) {
                    clearInterval(interval);
                    resolve();
                }
            }, duration / 10);
        });
    }
    
    async function runTasks() {
        let tasks = [
            { name: "Initializing", duration: 1000 },
            { name: "Loading data", duration: 2000 },
            { name: "Processing", duration: 1500 },
            { name: "Finalizing", duration: 800 }
        ];
        
        for (let task of tasks) {
            await simulateTask(task.name, task.duration);
            progressBar.style.width = "0%";
        }
        
        statusText.textContent = "All tasks completed!";
    }
    
    return { runTasks };
}

// Exercise 3: API data fetcher with caching
function createAPIClient() {
    let cache = new Map();
    
    async function fetchWithCache(url, cacheTime = 60000) { // 1 minute default
        // Check cache
        if (cache.has(url)) {
            let cached = cache.get(url);
            if (Date.now() - cached.timestamp < cacheTime) {
                console.log("Returning cached data");
                return cached.data;
            }
        }
        
        // Fetch fresh data
        console.log("Fetching fresh data");
        try {
            let response = await fetch(url);
            if (!response.ok) {
                throw new Error(`HTTP ${response.status}`);
            }
            
            let data = await response.json();
            
            // Cache the result
            cache.set(url, {
                data: data,
                timestamp: Date.now()
            });
            
            return data;
        } catch (error) {
            console.error("Fetch error:", error);
            throw error;
        }
    }
    
    async function fetchMultipleEndpoints(urls) {
        try {
            let promises = urls.map(url => fetchWithCache(url));
            let results = await Promise.allSettled(promises);
            
            return results.map((result, index) => ({
                url: urls[index],
                success: result.status === 'fulfilled',
                data: result.status === 'fulfilled' ? result.value : null,
                error: result.status === 'rejected' ? result.reason.message : null
            }));
        } catch (error) {
            console.error("Error fetching multiple endpoints:", error);
            throw error;
        }
    }
    
    function clearCache() {
        cache.clear();
    }
    
    return { fetchWithCache, fetchMultipleEndpoints, clearCache };
}

// Usage example
async function demonstrateAsyncPatterns() {
    let api = createAPIClient();
    
    try {
        // Single request
        let post = await api.fetchWithCache('https://jsonplaceholder.typicode.com/posts/1');
        console.log('Single post:', post);
        
        // Multiple requests
        let results = await api.fetchMultipleEndpoints([
            'https://jsonplaceholder.typicode.com/posts/1',
            'https://jsonplaceholder.typicode.com/posts/2',
            'https://jsonplaceholder.typicode.com/users/1'
        ]);
        
        console.log('Multiple results:', results);
    } catch (error) {
        console.error('Demo error:', error);
    }
}
```

---

## 13. Error Handling

### Types of Errors

```javascript
// Syntax Error - code won't run
// console.log("missing quote);

// Reference Error - variable doesn't exist
// console.log(nonExistentVariable);

// Type Error - wrong data type
// let num = 5;
// num.toUpperCase(); // TypeError: num.toUpperCase is not a function

// Range Error - number out of range
// let arr = new Array(-1); // RangeError: Invalid array length
```

### Try-Catch-Finally

```javascript
// Basic try-catch
try {
    let result = riskyOperation();
    console.log("Result:", result);
} catch (error) {
    console.log("An error occurred:", error.message);
}

// Try-catch-finally
try {
    let data = JSON.parse('{"name": "John"}');
    console.log("Parsed:", data);
} catch (error) {
    console.log("JSON parsing failed:", error.message);
} finally {
    console.log("This always runs");
}

// Catching specific error types
try {
    let obj = null;
    console.log(obj.property);
} catch (error) {
    if (error instanceof TypeError) {
        console.log("Type error occurred:", error.message);
    } else if (error instanceof ReferenceError) {
        console.log("Reference error occurred:", error.message);
    } else {
        console.log("Unknown error:", error.message);
    }
}
```

### Throwing Custom Errors

```javascript
// Throwing basic errors
function divide(a, b) {
    if (b === 0) {
        throw new Error("Cannot divide by zero");
    }
    return a / b;
}

try {
    let result = divide(10, 0);
} catch (error) {
    console.log("Error:", error.message);
}

// Custom error classes
class ValidationError extends Error {
    constructor(message, field) {
        super(message);
        this.name = "ValidationError";
        this.field = field;
    }
}

class NetworkError extends Error {
    constructor(message, statusCode) {
        super(message);
        this.name = "NetworkError";
        this.statusCode = statusCode;
    }
}

// Using custom errors
function validateUser(user) {
    if (!user.name) {
        throw new ValidationError("Name is required", "name");
    }
    if (!user.email || !user.email.includes("@")) {
        throw new ValidationError("Valid email is required", "email");
    }
    if (user.age < 0 || user.age > 150) {
        throw new ValidationError("Age must be between 0 and 150", "age");
    }
}

try {
    validateUser({ name: "", email: "invalid", age: -5 });
} catch (error) {
    if (error instanceof ValidationError) {
        console.log(`Validation error in ${error.field}: ${error.message}`);
    } else {
        console.log("Unexpected error:", error.message);
    }
}
```

### Error Handling in Functions

```javascript
// Error handling with return values
function safeParseJSON(jsonString) {
    try {
        return {
            success: true,
            data: JSON.parse(jsonString),
            error: null
        };
    } catch (error) {
        return {
            success: false,
            data: null,
            error: error.message
        };
    }
}

let result = safeParseJSON('{"name": "John"}');
if (result.success) {
    console.log("Parsed data:", result.data);
} else {
    console.log("Parse error:", result.error);
}

// Error handling with callbacks
function processDataWithCallback(data, callback) {
    try {
        // Simulate processing
        if (!data) {
            throw new Error("No data provided");
        }
        
        let processed = data.toUpperCase();
        callback(null, processed); // null for error, data for success
    } catch (error) {
        callback(error, null); // error for error, null for data
    }
}

processDataWithCallback("hello", (error, result) => {
    if (error) {
        console.log("Error:", error.message);
    } else {
        console.log("Result:", result);
    }
});
```

### Async Error Handling

```javascript
// Promise error handling
function fetchDataPromise(url) {
    return new Promise((resolve, reject) => {
        // Simulate API call
        setTimeout(() => {
            if (url.includes("error")) {
                reject(new NetworkError("Failed to fetch data", 500));
            } else {
                resolve({ data: "Some data" });
            }
        }, 1000);
    });
}

fetchDataPromise("https://api.example.com/data")
    .then(result => {
        console.log("Success:", result);
    })
    .catch(error => {
        if (error instanceof NetworkError) {
            console.log(`Network error ${error.statusCode}: ${error.message}`);
        } else {
            console.log("Unknown error:", error.message);
        }
    });

// Async/await error handling
async function fetchAndProcessData(url) {
    try {
        let response = await fetch(url);
        
        if (!response.ok) {
            throw new NetworkError(
                `HTTP ${response.status}: ${response.statusText}`,
                response.status
            );
        }
        
        let data = await response.json
