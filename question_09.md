In JavaScript, a class is a template or blueprint that defines the structure and behavior of objects. It serves as a blueprint for creating instances of objects that share common properties and methods. Classes provide a way to implement object-oriented programming concepts such as encapsulation, inheritance, and polymorphism.

Introduced in ECMAScript 2015 (ES6), JavaScript classes provide a more convenient syntax for creating objects and working with prototypes. Despite being called "classes," they are syntactical sugar over the existing prototype-based inheritance model in JavaScript.

Here's an example of a class in JavaScript:

```
class Person {
  constructor(name, age) {
    this.name = name;
    this.age = age;
  }

  sayHello() {
    console.log(`Hello, my name is ${this.name}.`);
  }
}

// Creating instances of the Person class
const john = new Person("John", 25);
john.sayHello(); // Output: "Hello, my name is John."
```

In the example above, the `Person` class is defined using the `class` keyword. It has a constructor method that is called when a new instance of the class is created. The constructor initializes the `name` and `age` properties of the object using the provided arguments.

The `sayHello` method is defined within the class, which can be invoked on instances of the `Person` class. The `this` keyword refers to the current instance of the object, allowing access to its properties and methods.

It's important to note that JavaScript classes are syntactic sugar over prototypes. Under the hood, class definitions are converted into constructor functions and prototype-based inheritance. This means that the `class` keyword is essentially a more convenient way to work with JavaScript's existing prototype system.

JavaScript classes provide a clearer and more familiar syntax for working with objects in an object-oriented style. They help in organizing and structuring code, facilitating code reusability and maintaining a clean separation of concerns.