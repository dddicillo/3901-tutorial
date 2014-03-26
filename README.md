# 3901-tutorial

This tutorial aims to provide a thorough explanation of three key elements related to web development: HTML/CSS, Javascript, and Ruby. Programmers with little to no web development experience should find this tutorial helpful, however, those without prior programming experience should first consult an introductory tutorial first, in order to learn the basic concepts of computer programming.

## HTML/CSS

## JavaScript

Once again, this tutorial assumes a certain amount of proficiency in computer programming. The JavaScript section will thus focus mainly on the differences between JavaScript and other common languages. There are many quirks and best practices unique to JavaScript. They will be covered here.

#### The Basics

##### Objects

JavaScript is an **Object-Based** language, which means it supports the creation of objects, but does not use classes like an **Object-Oriented** language would.

Several objects are implicitly defined by the browser, such as `Document` and `Window`. These objects can be used to interact with the core elements of the web page. For a detailed list of their associated members, check [here][DocumentObj] for the `Document` object or [here][WindowObj] for the `Window` object.

Object members can be accessed using the `.` operator much like in Java. For example, the following code snippet would display a popup window using the `alert` method of the `window` object.

	window.alert("Hello, World!");

##### Variables

JavaScript assigns variables on the basis of **dynamic typing**, meaning the type of a variable is determined at runtime. What this means for the programmer is that data types are not specified in the code. Additionally, the type of a variable may change throughout the course of execution. For example:

	var x = 10 // x is and integer
	...
	... // Some code
	...
	x = "Ten" // Now x is a string

Notice how the `int` keyword commonly used in other languages does not appear. Instead, the `var` keyword is used. This keyword just specifies that `x` is a local variable. Were the `var` keyword not used, `x` would be defined as a global variable by default. It is considered best practice to make variables local unless global scope is required for the script to function.

Another feature unique to JavaScript is the existence of the `undefined` type. This type is assigned by default to a variable that has not yet been assigned a value. For example: 

	typeof x; // #=> undefined

> Note: `typeof` is an operator, which will be explained later on in the tutorial.

Another distinction made when dealing with variables is whether they are **primitive** or **reference** types. Primitive types in JavaScript include booleans, numbers, strings, null, and undefined. Reference types include arrays and objects. Reference types behave as they do in most popular languages such as Java in regards to argument passing (pass by reference) and equality checking (check equality based on reference location when using the `==` operator).

##### Operators

This tutorial will not cover basic use of operators such as `+`, `-`, `*`, `/`, etc... Instead, it will focus on those operators which are unique to JavaScript or behave differently than expected. For a more in-depth explanation of the operators, check [here][Operators].

###### Assignment Operators

> JavaScript has all of the shorthand assignment operators common in most other languages. i.e. `+=`, `-=`, `*=`, `/=`, etc...

###### Comparison Operators

> JavaScript has all of the common comparison operators. i.e. `==`, `!=`, `<`, `<=`, etc...

A comparison operator unique to JavaScript is the `===` operator. This operator functions similarly to the `==`, but while the `==` operator will attempt to use **type coercion** to test the equality of two variables, the `===` operator requires that the two variables are of the same type (`!==` works similarly). For example:

	1 == "1"	// #=> true
	1 === "1"	// #=> false

###### Arithmetic Operators

> JavaScript has all of the common arithmetic operators. i.e.`+`, `-`, `*`, `/`, etc...

> JavaScript also includes the common unary operators. i.e. `++` and `--`.

When performing arithmetic operations, the JavaScript interpreter will use type coercion where appropriate in order to complete the operation. This means that the type of certain variables may be automatically changed in some cases. For example:

	var x = 1;
	var y = "Hello";

	x + y; // #=> "1Hello"

> Note: In this example, the type of `x` is promoted to `string` in order to perform the operation. `x` will return to a number upon completion of the operation.

###### Logical Operators

> JavaScript has all of the basic logical operators as well as bitwise logical operators. i.e. `&&`, `||`, `!`, etc...

###### Unique Operators

- `delete` - Removes a property from an object
- `in` - Determines whether or not a given object contains a given property
- `instanceof` - Deteremines whether or not a given object is an instance of another given object
- `new` - Creates a new object based on the object's constructor
- `typeof` - Returns the type of the given object in string format
- `void` - Ignores an expressions return value

##### Literals

**__I MIGHT JUST IGNORE THIS SECTION. WE'LL SEE__**

##### Arrays

Arrays are defined in the same way as Java, however, one key difference is that they may hold multiple different data types. For example:

	var arr = [1, 3.14, "Hello"];
	// or
	var arr = new Array(1, 3.14, "Hello");

Another distinction of JavaScript arrays is that they are dynamic structures. The length of the array can be adjusted manually by editing the `Array.length` property. Because arrays are reference types, they also have numerous methods which allow for convenient manipulation. For example:

	var arr = new Array();
	arr.push(1, 2, 3);
	var x = arr.pop(); // #=> 3

The above code uses the `push` and `pop` methods to add and remove elements from the array dynamically. For a comprehensive list of all of the methods and properties associated with JavaScript arrays, look [here][Arrays].

#### Control Flow

The control flow implemented in JavaScript is almost identical to that of Java, so this section of the tutorial will only cover basic examples of each. For a more in-depth explanation of JavaScript control flow, check [here][ControlFlow].

##### If/Then

	var x = 5
	if (x < 5) {
		console.log("x is less than five!");
	} else if (x == 5) {
		console.log("x equals five!");
	} else {
		console.log("x is greater than five!");
	}

##### Switch/Case

	var x = 3
	switch (x) {
		case 1:
			console.log("x equals one!");
			break;
		case 2:
			console.log("x equals two!");
			break;
		case 3:
			console.log("x equals three!");
			break;
		default:
			console.log("I don't know what is x!")
			break;
	}

##### For Loops

	for (var i = 0; i < 10; i++) {
		console.log("i is now " + i);
	}

##### While Loops

	var x = 10
	while (x > 5) {
		console.log("x is now " + x);
		x--;
	}

> Note: Do...While loops are also valid in JavaScript

#### Functions

##### Anonymity

##### Closure

#### Events

Every HTML element has a set of attributes that allow for the execution of JavaScript when certain events happen.


##Ruby

The Ruby section of this tutorial will focus on introducing the basics of Ruby as well as the differences between Ruby and other similar languages. Ruby is a easy to learn yet powerful programing language.

#### Object-Oriented


 Ruby is a pure **Object-Oriented** programing language. This means that Ruby supports the creation of objects as well as classes. 

[DocumentObj]: https://developer.mozilla.org/en-US/docs/Web/API/document
[WindowObj]: https://developer.mozilla.org/en-US/docs/Web/API/Window
[Operators]: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators
[Arrays]: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array
[ControlFlow]: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Statements