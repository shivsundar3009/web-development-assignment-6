In JavaScript, the `call()`, `apply()`, and `bind()` methods are used to explicitly set the value of `this` within a function. They provide control over the context in which a function is executed. Here's an explanation of each method and the differences between them:

1. `call()`: The `call()` method is used to invoke a function immediately with a specified `this` value and optional arguments provided individually. The first argument passed to `call()` sets the value of `this`, and subsequent arguments are passed as individual parameters to the function.

   Syntax: `function.call(thisArg, arg1, arg2, ...)`

   Example:
   ```
   function greet() {
     console.log("Hello, my name is " + this.name);
   }

   var john = { name: "John" };

   greet.call(john); // Output: "Hello, my name is John"
   ```

2. `apply()`: The `apply()` method is similar to `call()`, but it takes an array-like or iterable object as the second argument. The first argument sets the value of `this`, and the second argument is an array or array-like object containing the function's arguments.

   Syntax: `function.apply(thisArg, [argsArray])`

   Example:
   ```
   function greet(message) {
     console.log(message + ", my name is " + this.name);
   }

   var john = { name: "John" };
   var args = ["Hello"];

   greet.apply(john, args); // Output: "Hello, my name is John"
   ```

3. `bind()`: The `bind()` method returns a new function with a permanently bound `this` value. It allows you to create a new function that, when called, has a specified `this` value. Unlike `call()` and `apply()`, `bind()` does not invoke the function immediately but returns a new function with the desired context.

   Syntax: `function.bind(thisArg, arg1, arg2, ...)`

   Example:
   ```
   function greet() {
     console.log("Hello, my name is " + this.name);
   }

   var john = { name: "John" };
   var greetJohn = greet.bind(john);

   greetJohn(); // Output: "Hello, my name is John"
   ```

The main difference between `call()` and `apply()` is how the arguments are passed. `call()` accepts individual arguments, while `apply()` takes an array-like object of arguments. Both methods immediately invoke the function.

On the other hand, `bind()` returns a new function with the bound `this` value but does not invoke the function immediately. The returned function can be invoked later.

These methods are useful when you want to control the value of `this` explicitly or when you want to borrow methods from one object and apply them to another object with a different context.