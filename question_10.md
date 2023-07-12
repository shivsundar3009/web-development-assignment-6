In JavaScript, the `super` keyword is used to call and access the parent class's constructor, properties, and methods from within a subclass. It provides a way to reference and invoke the parent class's functionality when extending or overriding it in a subclass.

The `super` keyword has two main uses:

1. Calling the Parent Class Constructor: In a subclass constructor, `super()` is used to call the constructor of the parent class. It is necessary to initialize the inherited properties from the parent class before adding or modifying them in the subclass.

   Example:

   ```
   class Parent {
     constructor(name) {
       this.name = name;
     }
   }

   class Child extends Parent {
     constructor(name, age) {
       super(name); // Call the Parent class constructor
       this.age = age;
     }
   }

   const child = new Child("John", 25);
   console.log(child.name); // Output: "John"
   ```

2. Calling Parent Class Methods: The `super` keyword is also used to access and call methods of the parent class within the subclass. It allows the subclass to override a method inherited from the parent class but still make use of the parent class's implementation.

   Example:

   ```
   class Parent {
     sayHello() {
       console.log("Hello from Parent");
     }
   }

   class Child extends Parent {
     sayHello() {
       super.sayHello(); // Call the Parent class method
       console.log("Hello from Child");
     }
   }

   const child = new Child();
   child.sayHello();
   // Output:
   // "Hello from Parent"
   // "Hello from Child"
   ```

In the example above, the `Child` class overrides the `sayHello()` method inherited from the `Parent` class. By using `super.sayHello()`, the parent class's implementation is invoked first, followed by the additional behavior defined in the subclass.

The `super` keyword is crucial for maintaining the inheritance chain and leveraging the functionalities provided by the parent class. It allows subclasses to extend and modify the behavior inherited from the parent class while reusing and building upon the existing implementation.