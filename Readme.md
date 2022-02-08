

# **DESIGN PATTERNS**


#### In the Software Engineering world, **Design patterns** are typical solutions to a common problems. They are like templates that we can use and customize to solve a design problem in our code.

#### The pattern is not a specific piece of code, but it is a general concept for solving a particular problem. We can follow the pattern details and build a solution that is required for our program in order to solve the problem.



#### lets talk a bit about ***Algorithm*** as it also helps one to solve problems and make programs using that.

#### If we talk about *Algorithm*, it is a sequence of operations which needs to be implemented in order to solve a specific problem. 

 > **An Algorithm can be expressed in a code but a Design Pattern can't be directly translated to code.**


---

#### **Lets talk about what patterns consists of**


#### Here are the sections that are usually present in a pattern description:


* **Intent** of the pattern briefly describes both the problem and the solution.
* **Motivation** further explains the problem and the solution the pattern makes possible.
* **Structure** of classes shows each part of the pattern and how they are related.
* **Code example** in one of the popular programming languages makes it easier to grasp the idea behind the pattern.
----

#### **Why one should learn** ***Design Patterns?***

 

*    Design patterns are a toolkit of tried and tested solutions to common problems in software design. Even if you never encounter these problems, knowing patterns is still useful because it teaches you how to solve all sorts of problems using principles of object-oriented design.

*    Design patterns define a common language that you and your teammates can use to communicate more efficiently. You can say, “Oh, just use a Singleton for that,” and everyone will understand the idea behind your suggestion. No need to explain what a singleton is if you know the pattern and its name.


---

# **Classification of Design Pattern**

#### Design patterns differ by their complexity, level of detail and scale of applicability to the entire system being designed. I like the analogy to road construction: you can make an intersection safer by either installing some traffic lights or building an entire multi-level interchange with underground passages for pedestrians.

#### The most basic and low-level patterns are often called idioms. They usually apply only to a single programming language.

#### The most universal and high-level patterns are architectural patterns. Developers can implement these patterns in virtually any language. Unlike other patterns, they can be used to design the architecture of an entire application.

#### In addition, all patterns can be categorized by their intent, or purpose. This book covers three main groups of patterns:

   * **Creational patterns** provide object creation mechanisms that increase flexibility and reuse of existing code.

   * **Structural patterns** explain how to assemble objects and classes into larger structures, while keeping the structures flexible and efficient.

  *  **Behavioral patterns** take care of effective communication and the assignment of responsibilities between objects.

---


># **Design Patterns in JavaScript**


### Following are the Design Patterns in JavaScipt:


## **1.**   **Constructor Design Pattern** 


#### This is a special method that is used to initialize the newly created objects once a memory is allocated.

```js
   //Code Example

   var newObject = {};


   var newObject = Object.create(Object.prototype);

   var newObject = newObject();

```
---

## **2.** **Prototype Pattern**

#### The prototype pattern is based on prototypical inheritance whereby objects created to act as prototypes for other objects. In reality, prototypes act as a blueprint for each object constructor created.

```js 
   //Code example

   var myCar= {
   name:"Ford",
   brake:function(){
   console.log("Stop! I am applying brakes");
   }
   Panic : function (){
   console.log ( "wait. how do you stop thuis thing?")
   }
   }
   var yourCar= object.create(myCar);
   console.log (yourCar.name);

 ```

 ---

 ## **3.** **Command Pattern**

 

#### The command design pattern encapsulates method invocation, operations, or requests into a single object so that we can pass method calls at our discretion. These commands are presented in **run()** and **execute()** format.



 ```js

   //Code Example

   (function(){

   var carManager = {

   requestInfo: function( model, id ){
   return "The information for " + model + " with ID " + id + " is foo bar";
   },

   buyVehicle: function( model, id ){
   return "You have successfully purchased Item " + id + ", a " + model;
   },

   arrangeViewing: function( model, id ){
   return "You have successfully booked a viewing of " + model + " ( " + id + " ) ";
   }
   };
   })();
```
---


 ## **4.** **Observer Pattern**

 #### The observer design pattern is handy in a place where objects communicate with other sets of objects simultaneously.

 ```js

   //Code Example


   function Observer() {
   this.observerContainer = [];
   }

   Observer.prototype.subscribe = function (element) {
   this.observerContainer.push(element);
   }


   Observer.prototype.unsubscribe = function (element) {

   const elementIndex = this.observerContainer.indexOf(element);
   if (elementIndex &gt; -1) {
   this.observerContainer.splice(elementIndex, 1);
   }
   }


   Observer.prototype.notifyAll = function (element) {
   this.observerContainer.forEach(function (observerElement) {
   observerElement(element);
   });
   }
```
---
 ## **5.** **Observer Pattern**

 #### This pattern is referred to as strict pattern, one drawback associated with this pattern is its daunting experience in testing because of its hidden dependencies objects which are not easily singled out for testing.


```js 

   //Code Example

   function DatabaseConnection () {

   let databaseInstance = null;

   let count = 0;

   function init() {
   console.log(`Opening database #${count + 1}`);
   }
   function createIntance() {
   if(databaseInstance == null) {
   databaseInstance = init();
   }
   return databaseInstance;
   }
   function closeIntance() {
   console.log('closing database');
   databaseInstance = null;
   }
   return {
   open: createIntance,
   close: closeIntance
   }
   }

   const database = DatabseConnection();
   database.open(); //Open database #1
   database.open(); //Open database #1
   database.open(); //Open database #1
   database.close(); //close database
```

---
---
#### **References Used In This Document**


* [Design Patterns](https://refactoring.guru/design-patterns)
* [JavaScript Design Patterns](https://codesource.io/javascript-design-patterns/)
