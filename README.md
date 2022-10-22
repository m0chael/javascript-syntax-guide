# Javascript Syntax Guide

This is a **Javascript Syntax Guide** written from scratch and can be used as basic guidelines for programming fundamentals.

## Usage
In the editor of your choice, follow the guidelines for Javascript in this syntax guide.
- [Tab Indentation](#tab-indentation)
- [Trailing Whitespace](#trailing-whitespace)
- [JavaScript Variables](#javascript-variables)
- [JavaScript Comparison Statements](#javascript-comparison-statements)
- [JavaScript Boolean Statements](#javascript-boolean-statements)
- [JavaScript Arrays](#javascript-arrays)
- [JavaScript Objects](#javascript-objects)
- [JavaScript Functions](#javascript-functions)
- [JavaScript Functions & Parameters](#javascript-functions-and-parameters)
- [JavaScript Loops](#javascript-loops)
- [JavaScript Data Types](#javascript-data-types)
- [JavaScript Comments](#javascript-comments)

## Tab Indentation
Should use spacing of 2 spaces.

## Trailing Whitespace
Should be removed.

## Javascript Variables
There are three types of variable declarations in Javascript which are detailed below. `var` is an older version and it is preferred to use `let` and `const` type of declarations.
```js
// An older ES5 version of declaring a variable
var someVar = 1;

// Syntax in ES6 for declaring a variable in JS
let someLet = 1;

// ES6 to declare constant, should be put in CAPITAL_LETTERS with underscore spacing
const SOME_CONST = 1;
```

## Javascript Comparison Statements
There are various comparison statments which are detailed in this section in Javascript. Each comparison is essentially an operator that will equate to either `true` or `false`.
```js
// Results false because 2 does not equal 5
let someEqualComparison = (2 == 5);

// Results true because 2 does not equal 5
let someNotEqualComparison = ( 2 != 5);

// Results true because 2 is less than 5
let someLessThanComparison = (2 < 5);

// Results false becasue 2 is not greater than 5
let someGreaterThanComparison = (2 > 5);

// Results true because it is less than or equal to
let lessOrEqualComparison = (2 <= 2);

// Results true ecause 7 is greater than or equal to 5
let greaterThanOrEqualComparison = (7 >= 5);
```

## Javascript Boolean Statements
There are various boolean statement possibilities in Javascript. This outlines the various types and how to use them. There is `&&` (AND), `||` (OR) and `==` (EQUALITY), which compares booleans.
```js
// Results as true, as it is declared
let someTruthy = true;

// Results as false, as it is declared
let someFalsey = false;

// Results in true as it will choose the true statement with ||
let someBooleanCheck = true || false;

// Results in true because someTruthy was declared as true
let whatIsTheResult = (someTruthy == true);

// Checks AND comparison, resulting in false because it requires both values to be true for &&
let checkingAndStatment = (someFalsy && someTruthy);
```

## Javascript Arrays
Javascript arrays are essentially `lists` of items. They can hold numbers, strings, booleans, other arrays even (2D arrays), or objects. Below is a guide for how to do the syntax of arrays. There are 3 main methods for arrays which are `pop`, `push` and `splice`.
```js
// Declare an empty array
let someEmptyArray = [];

// Assign an array with 3 booleans of true or false
let someBooleanArray = [false, true, false];

// Declare an array with mixed values, which is allowed in Javascript
let someMixedArray = ["TextInsert", 3, false];

// Pop an array which returns the last item in the array and removes it from the array
let whatIsTheResult = someMixedArray.pop();

// This will render false, as it was returned from the pop() method
console.log(whatIsTheResult);

// Push into the end of an array using push() method
someMixedArray.push(true);

// This array will now display ["TextInsert", 3, true] because it added true
console.log(someMixedArray);

// Splice will remove an element from an array at a specific index
// This means at position 0, remove 1 element
someMixedArray.splice(0, 1);

// This will render [3, true], because it removed the first element of the array with splice.
console.log(someMixedArray);
```

## Javascript Objects
Javascript objects can represent a large variety of data contained into one entity. It's also possible to have arrays of objects themselves! Below describes how to define and use Javascript Objects.
```js
// This is how to define an object in Javascript. This is the method where keys are assigned to values using string notation
let someBookObject = {
  "title": "Some Javascript Book",
  "date": "October 21, 2022",
  "introduction": "A javascript syntax book which goes over the various fundamentals of the language",
  "pages": 5,
  "read": true
};

// This is also how to define an object in Javascript. This is the method where keys are assigned to values using object notation
let someBookObjectNotation = {
  title: "Some Javascript Book",
  date: "October 21, 2022",
  introduction: "A javascript syntax book which goes over the various fundamentals of the language",
  date: 5,
  read: true
};

// Parameters from both notations can be accessed using the dot notation
console.log(someBookObjectNotation.introduction);

// Or they can also be accessed similar to an array item, both are equivalent and valid syntax
console.log(someBookObject["introduction"]);

// To get the keys from a Javascript object as an array
let theseKeys = Object.keys(someBookObject);

// To get the values from a Javascript object as an array
let theseValues = Object.values(someBookObject);

// To loop through a Javacript object by it's keys can be done using a for-in loop
for (let key in someBookObject) {
  console.log(key); // This will print out the key
  console.log(someBookObject[key]); // This will print out the value of the object at the specific key
}
```

## Javascript Functions
Javascript Functions are assigned in a variety of ways. Below describes the syntax for defining and using a function in Javascript.
```js
// This is a function declaration
function thisIsMyFunction(){
  console.log("I'm inside a function!");
}

// This is a declaration using arrow functions which is ES6
const thisIsMyOtherFunction = () => {
  console.log("I'm inside an arrow function!");
};

// Calling a function works like this
thisIsMyFunction();

// Which also works for the arrow function
thisIsMyOtherFunction();
```

## Javascript Functions And Parameters
Javascript Functions can be passed parameters. Below describes the syntax for defining functions with parameters and how to pass data to a function.
```js
// Declaring a function with parameters to pass inside
function functionWithParameters(incoming) {
  console.log("I'm inside an arrow function for: " + incoming);
};

// Calling a function and passing parameters will bring the values inside the function's scope
functionWithParameters("This Javascript Syntax Guide");

// A function can receive multiple parameters seperated by commas
// This function prints out the incomingText the number of times passed by incomingNumber
function printOutMultipleTimes(incomingNumber, incomingText) {
  for (let i = 0; i < incomingNumber; i++) {
    console.log(incomingText);
  }
};

printOutMultipleTimes(3, "Printed out three times!");
```

## Javascript Loops
Javascript loops can be defined in a number of ways. For loops, for each loops and while loops. Careful while making loops as it may crash the browser if not handled properly.
```js
// this is the syntax of a for loop. It is generally a good idea to label the element that is being looped over to be descriptive
let incomingNumber = 3;
let incomingText = "The Javascript Syntax Guide";

for (let index = 0; index < incomingNumber; index++) {
  console.log(incomingText);
}

// This is the syntax of a for each loop, which uses an interable object to loop through, in this case an array
let someIterable = ["apple", "banana", "orange"];

// Inside the function of a foreach loop, it will pass the element and index seperated by comma notation
someIterable.forEach(function(elementInArray, indexInArray){
  console.log("The index of " + indexInArray + " is " + elementInArray);
});
```

## Javascript Data Types
Javascript has various data types such as strings, decimal place numbers or integers, objects, booleans, and arrays. Below gives an example of the different data types.
```js
// String scan be declared by using double quotes
let someString = "Some String As Text";

// Or single quotes work too for strings
let someOtherString = 'Or single quotes';

// Integers can be declared like this
let someInteger = 3;

// Floats are numbers too
let someFloat = 2.25

// Javascript is able to detect that both are numbers and will add them together. This results in 5.25
let someAddition = someInteger + someFloat;

// A boolean as described in an earlier section can be declared like this
let someBoolean = true;

// Arrays are a data type which hold a list of items, described in an earlier section
let someArray = ["cat", "dog", "fish"];

// An empty object is an object type too
let someObject = {};
```

## Javascript Comments
Javascript comments can be used by doing the following:
```js
// Comments with double slashes

/*
  Multi line comments
  can be made
  like this
*/
```