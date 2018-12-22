# 33-js-concepts
Personal notes from reading: [GitHub - leonardomso/33-js-concepts: 📜 33 concepts every JavaScript developer should know.](https://github.com/leonardomso/33-js-concepts)

## 1. Call Stack
* A list of function invocations.  Last in, First Out.
* Helpful for debugging
* Ordered set of stack frames
* Most recently invoked function is on the top of the stack
* The bottom of the stack is the first function invoked
* JavaScript is single threaded, one thing is happening at a time.
* The stack is processed from top to bottom

* You blow the stack when you exceed the number of frames the browser allows in the call stack. e.g. infinite loop

* `function: main`  represents the javascript file and gets added to the stack before any function call. `main` = `anonymous`  in Chrome.

* Stack Frames Contents
	* The function that was invoked
	* The parameters that were passed to the function
	* Current line number

## 2. Primitive Types (Scalar)
* String, Number, Boolean, Undefined, Null, Symbol

* Primitives are copied by their value

## 3. Reference Types (Complex)
* Object, Function, Array

* Objects are copied by their reference

* A variable that contains a copy of an object is pointing to the same location in memory. 
```javascript
// Object is not stored in x, it is stored somewhere else in memory and the address to its location is stored in x
let x = { name: 'Daniel' };

let y = x;

x.name // Daniel
y.name // Daniel

// changing the value of x also changes the value of y since x and y both point to the same address of the object in memory
x.name = 'David'

x // { name: 'David' }
y // { name: 'Daniel' }
```

## 4. Implicit, Explicit, Nominal, Structural and Duck Typing
* JavaScript is dynamically typed
* Type conversion can happen in two ways:
	* Explicit
		* `parsInt(215)`
	* Implicit
		* Type coercion
		* `if (arr.length) {} // coerces Number to Boolean` 
* Type coercion in JavaScript
	* `=== & !===` No type coercion is done
	* Types must be the same initially in order to be considered equal
* Perform explicit type conversion
* [JS Equality Comparison Table](https://dorey.github.io/JavaScript-Equality-Table/)
* Duck Typing
	* An operation doest not formally specify the requirements that its operands have to meet, but just **tries it out** with what is given.
	* Dynamically typed languages like JavaScript or Python will just try to see if anything works, and if it doesn’t, will crash at runtime.
* Nominal vs Structural Typing
	* Nominal
		* Error will be thrown if when names of classes don’t match
		* C++, Java, Swift
	* Structural
		* Error will be thrown if structure of classes don’t match
		* OCaml, Haskell, Elm

## 5. == vs === vs typeof
## 6. Function Scope, Block Scope and Lexical Scope
## 7. Expression vs Statement
## 8. IIFE, Modules and Namespaces
## 9. Message Queue and Event Loop
## 10. setTimeout, setInterval and requestAnimationFrame
## 11. JavaScript Engines
## 12. Bitwise Operators, Type Array and Array Buffers
## 13. DOM and Layout Trees
## 14. Factories and Classes
## 15. this, call, apply and bind
## 16. new, Constructor, instanceof and Instances
## 17. Prototype Inheritance and Prototype Chain
## 18. Object.create and Object.assign
## 19. map, reduce, filter
## 20. Pure Functions, Side Effects and State Mutation
## 21. Closures
## 22. High Order Functions
## 23. Recursion
## 24. Collections and Generators
## 25. Promises
## 26. async/await
## 27.  Data Structures
## 28.  Expensive Operation and Big O Notation
## 29. Algorithms
## 30. Inheritance, Polymorphism and Code Reuse
## 31. Design Patterns
A design pattern is a term used in software engineering for a general reusable solution to a commonly occurring problem in software design.
[JavaScript Design Patterns – Beginner’s Guide to Mobile Web Development – Medium](https://medium.com/beginners-guide-to-mobile-web-development/javascript-design-patterns-25f0faaaa15)

## 32. Partial Applications, Currying, Compose and Pipe
* Partial Application is the term used more in conversation at work
	* You may want to partially apply a this function
* Currying is  generally something you say once 
	* All functions in Elm are curried

## 33. Clean Code