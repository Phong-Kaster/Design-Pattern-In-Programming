<h1 align="center">Design Pattern in Programming<br/>
    Everything you had better know about design pattern
</h1>

<p align="center">
    <img src="./photo/cover.jpg" width="1280" />
</p>


# [**Table Of Content**](#table-of-content)
- [**Table Of Content**](#table-of-content)
- [**What is Design Pattern ?**](#what-is-design-pattern-)
- [**Why shall we use Design Pattern ?**](#why-shall-we-use-design-pattern-)
- [**When shall we take advance of Design Pattern ?**](#when-shall-we-take-advance-of-design-pattern-)
- [**What you need to prepare before learning Design pattern ?**](#what-you-need-to-prepare-before-learning-design-pattern-)
- [**Types of design pattern**](#types-of-design-pattern)
  - [**Creational**](#creational)
    - [**Creational - Factory Method**](#creational---factory-method)
    - [**Creational - Abstract Method**](#creational---abstract-method)
    - [**Creational - Singleton**](#creational---singleton)
    - [**Creational - Builder**](#creational---builder)
    - [**Creational - Prototype**](#creational---prototype)
  - [**Structural**](#structural)
    - [**Structural - Adapter**](#structural---adapter)
    - [**Structural - Bridge**](#structural---bridge)
    - [**Structural - Composite**](#structural---composite)
    - [**Structural - Decorator**](#structural---decorator)
    - [**Structural - Facade**](#structural---facade)
    - [**Structural - Flyweight**](#structural---flyweight)
    - [**Structural - Proxy**](#structural---proxy)
  - [**Behavioural**](#behavioural)
    - [**Behavioural - Chain of responsibility**](#behavioural---chain-of-responsibility)
    - [**Behavioural - Command**](#behavioural---command)
    - [**Behavioural - Iterator**](#behavioural---iterator)
    - [**Behavioural - Mediator**](#behavioural---mediator)
    - [**Behavioural - Memento**](#behavioural---memento)
    - [**Behavioural - Observer**](#behavioural---observer)
    - [**Behavioural - State**](#behavioural---state)
    - [**Behavioural - Strategy**](#behavioural---strategy)
    - [**Behavioural - Template Method**](#behavioural---template-method)
    - [**Behavioural - Visitor**](#behavioural---visitor)
    - [**Behavioural - Interpreter**](#behavioural---interpreter)
- [**Another Specific Terms**](#another-specific-terms)
  - [**What is an abstract class ?**](#what-is-an-abstract-class-)
  - [**What is a concrete class ?**](#what-is-a-concrete-class-)
- [**My Mentors**](#my-mentors)
- [**Made with 💘**](#made-with-)

# [**What is Design Pattern ?**](#what-is-design-pattern)
Software development is an iterative process and there are many problems which developers has to face up to many times. Programmers could come up with an idea for addressing the problem yet it isn't the most effective. Design pattern supplies best optimized "samples" (or maybe "patterns") in getting programming with OOP.

Design patterns are the solution for software problems that we copes fluently.

The outstanding thing of design pattern is reusable.

# [**Why shall we use Design Pattern ?**](#why-shall-we-use-design-pattern)

Design patterns can speed up the development process by providing tested, proven development paradigms. Effective software design requires considering issues that may not become visible until later in the implementation. Reusing design patterns helps to prevent subtle issues that can cause major problems and improves code readability for coders and architects familiar with the patterns.

Often, people only understand how to apply certain software design techniques to certain problems. These techniques are difficult to apply to a broader range of problems. Design patterns provide general solutions, documented in a format that doesn't require specifics tied to a particular problem.

In addition, patterns allow developers to communicate using well-known, well understood names for software interactions. Common design patterns can be improved over time, making them more robust than ad-hoc designs.

# [**When shall we take advance of Design Pattern ?**](#when-shall-we-take-advance-of-design-pattern)

If you desires your application more simpler as more as possible. Implementing **Design Pattern** save our time & efforts to figure out solution to problems having correct way to fix.

# [**What you need to prepare before learning Design pattern ?**](#what-you-need-to-prepare-before-learning-design-pattern)

You must understand deeply 4 principles in [**Object-Oriented Programming**](https://www.techtarget.com/searchapparchitecture/definition/object-oriented-programming-OOP)(OOP). They includes: 

1. Inheritance

2. Encapsulation

3. Abstraction

4. Polymorphism

In addition, you have to identify `Interface` & `Abstraction` 

100% thinking by OOP

# [**Types of design pattern**](#types-of-design-pattern)

There are 3 types of design pattern that we usually utilize. They comprise:

- Creational

- Structural

- Behavioural


## [**Creational**](#creational)

<p align="center">
    <img src="./photo/creational.png" width="640" />
</p>
<h3 align="center">

***CREATIONAL PATTERN INCLUDES 5 SAMPLES***
</h3>

Creational pattern comprise 5 prototypes: 

1. Factory Method

2. Abstract Method

3. Singleton

4. Builder

5. Prototype


Instead of creating an object with `new` method, creational pattern provides a solution to instantiate an object & hide the logical way to create it. This way makes an application more flexible when it determines which objects will be created depend on what situation happens.

These patterns are used for instantiation of classes. They are concerned with the way of creating objects. Normally object creation happens in the below way by using the new keyword.

    Student myStudent = new Student();

The above code is more than enough for object instantiation, but in some cases `the object must be changed according to the nature of the program in runtime`, in such cases, creational design patterns will be useful.

### [**Creational - Factory Method**](#creational---factory-method)

- Fluency of use: ⭐ ⭐ ⭐ ⭐ ⭐ 

Factory Method is a creational design pattern that Define an interface for creating an object, but let subclasses decide which class to instantiate. Factory Method lets a class defer instantiation to subclasses.

Factory Method is a factory explicitly. This "factory" manufactures objects which we need only.

In Factory Method, it consist of 3 basic components:

1. Super Class: a super class could be interface, abstract & normal class.

2. Sub Class: classes which implements all methods from super class according to its own business.

3. Factory Class: a class is in charge of instantiate subclass's objects basing on passed parameters.

>Note: Factory class could be `Singleton` or any class providing a `public static` method for querying or creating an objects. It is said that factory uses `if-else` or `switch-case` so as to decide output subclass.

Example: We own a Mobile Money application for mobile device(Momo, Zalo and so forth). There are many financial organizations as ARGIBANK, BIDV, VIETCOMBANK,.... They are able to supply us a restfulAPI to use their services. The point in this scenario is how we don't need to change our core source code to use their restfulAPI if we want to cope with other businesses..... The answer for the problem is taking advantage of `Factory Method`


<p align="center">
    <img src="./photo/factory-example.png" width="640" />
</p>
<h3 align="center">

***WE DON'T WANT TO MODIFY / EXTEND CODE FOR EACH BANKS WE INCORPORATE? FACTORY METHOD IS THE KEY TO ADDRESS***
</h3>

First, create super class:

    public interface Bank{

        String getName();
        String getAddress();

        #do what you want
    }

Second, create 2 subclass which implements `Bank` interface 

- TPBank Class:
  
        package com.gpcoder.patterns.creational.factorymethod;
 
        public class TPBank implements Bank {
 
            @Override
            public String getName() {
                return "TPBank - A deeper understanding";
            }
 
            @Override
            public String getAddress()
            {
                return "49 Mac Dinh Chi, District 1, TP.HCM, Vietnam"
            }

            # any method/ functions are able to declare below.
        }

- Vietcombak Class

        package com.gpcoder.patterns.creational.factorymethod;
 
        public class Vietcombank implements Bank {
 
            @Override
            public String getName() {
                return "Vietcombank - Together for the future";
            }

            @Override
            public String getAddress()
            {
                return "125 Oktoberfest, District Deutschland, Berlin, Germany"
            }

            # any method/ functions are able to declare below.
        }

Third, instantiating `enum BankName`, the enum stores constant through our application. To manage easier with our customers, `ENUM` is chosen to store banks name.

        public enum BankName{

            # you can add more bank name if needed
            TPBANK, VIETCOMBANK
            BIDV, AGRIBANK,
            LienVietPostBank;

        }

Fourth, creating Factory Method. In this example, it is called `BankFactory`.

        public class BankFactory {
 

            # Constructor
            private BankFactory() {
            }
        


            # "getBank" method create an instance depending on @parameter BankName
            public static final Bank getBank(BankName bankName) {
                switch (bankName) {
        
                case TPBANK:
                    return new TPBank();
        
                case VIETCOMBANK:
                    return new Vietcombank();

                default:
                    throw new IllegalArgumentException("This bank is unsupported");
                }
            }
        
        }
Final, call `BankFactory` in our application"

    public class Client {
 
        public static void main(String[] args) {

            Bank bank = BankFactory.getBank(BankType.Vietcombank);

            String name = bank.getName();
            String address = bank.getAddress();


            System.out.println("One of our customer is " + content);
            System.out.println("Their headquarter is in " + address);
        }
    }

The output is absolutely as

    One of our customer is Vietcombank - Together for the future

    Their headquarter is in 125 Oktoberfest, District Deutschland, Berlin, Germany

### [**Creational - Abstract Method**](#creational---abstract-method)

- Fluency of use: ⭐ ⭐ ⭐ ⭐ 

Abstract Factory is a creational design pattern that provide an interface for creating families of  related or dependent objects without specifying their concrete classes.

>From my point of view, an Abstract (Factory) Method is a Factory method whose ability is to create a Factory Method.

Abstract Factory is the way to create a Super Factory. A `Super Factory` is eligible for creating a [**Factory Method**](#creational---factory-method)

In other word, Abstract Factory is a higher level of Factory Method. You could assume that Abstract Factory is an enormous factory. The enormous(Abstract Factory) factory comprises a number of small factory. Each small factory(Factory Method) specializes its own business.

Example: 

<p align="center">
    <img src="./photo/abstract-method-sample.png" width="640" />
</p>
<h3 align="center">

***A BUSINESS HAS 2 FACTORY SPECIALIZED FOR EACH MATERIALS***
</h3>

You are the chairman of GeoComply group - a furniture manufacturer. Your business supplies Table & Chair which is made from Wood or Plastic. However, manufacturing Wood furnitures & Plastic furnitures is different 100%. Therefore, you need 2 different factories to create them. Your customers can make orders which include both wood & plastic furnitures. Both of 2 factories will make process to fulfill your customers's order.



### [**Creational - Singleton**](#creational---singleton)

- Fluency of use: ⭐ ⭐ ⭐ ⭐ 

### [**Creational - Builder**](#creational---builder)

- Fluency of use: ⭐ ⭐ 
   
### [**Creational - Prototype**](#creational---prototype)

- Fluency of use: ⭐ ⭐ ⭐

## [**Structural**](#structural)

<p align="center">
    <img src="./photo/structural.png" width="640" />
</p>
<h3 align="center">

***THERE ARE 7 SAMPLES IN STRUCTURAL PATTERN***
</h3>

When it comes to **structural pattern**, it consists:

1. Adapter

2. Bridge

3. Composite

4. Decorator

5. Facade

6. Flyweight

7. Proxy
Structural pattern relates to class and object's components. It is used to define relationship between 2 or more classes.

Structural design patterns are concerned with how objects and classes are composed. This pattern helps in simplifying the structure by identifying the relationships. It focuses on `how classes inherit from each other and how they are composed from other classes`.

The main goal is to `increase or extend the functionalities` of the class `without changing its composition`.

### [**Structural - Adapter**](#structural---adapter)

- Fluency of use: ⭐ ⭐ ⭐ ⭐

### [**Structural - Bridge**](#structural---bridge)

- Fluency of use: ⭐ ⭐ ⭐

### [**Structural - Composite**](#structural---composite)

- Fluency of use: ⭐ ⭐ ⭐ ⭐

### [**Structural - Decorator**](#structural---decorator)

- Fluency of use: ⭐ ⭐ ⭐

### [**Structural - Facade**](#structural-facade)

- Fluency of use: ⭐ ⭐ ⭐ ⭐ ⭐ 

### [**Structural - Flyweight**](#structural---flyweight)

- Fluency of use: ⭐

### [**Structural - Proxy**](#structural---proxy)

- Fluency of use: ⭐ ⭐ ⭐ ⭐

## [**Behavioural**](#behavioural)

<p align="center">
    <img src="./photo/behavioural.png" width="640" />
</p>
<h3 align="center">

***THERE ARE 11 SAMPLES IN BEHAVIOURAL PATTERN***
</h3>

Behavioural pattern consists: 

1. Chain of responsibility

2. Command

3. Iterator

4. Mediator

5. Memento

6. Observer

7. State

8. Strategy

9. Template method

10. Visitor

11. Interpreter

They are used to take actions with objects, communication among objects.

### [**Behavioural - Chain of responsibility**](#behavioural---chain-of-responsibility)

- Fluency of use: ⭐ ⭐

### [**Behavioural - Command**](#behavioural---command)

- Fluency of use: ⭐ ⭐ ⭐ ⭐

### [**Behavioural - Iterator**](#behavioural---iterator)

- Fluency of use: ⭐ ⭐ ⭐ ⭐ ⭐ 

### [**Behavioural - Mediator**](#behavioural---mediator)

- Fluency of use: ⭐ ⭐

### [**Behavioural - Memento**](#behavioural---memento)

- Fluency of use: ⭐

### [**Behavioural - Observer**](#behavioural---observer)

- Fluency of use: ⭐ ⭐ ⭐ ⭐ ⭐ 

### [**Behavioural - State**](#behavioural---state)

- Fluency of use: ⭐ ⭐ ⭐

### [**Behavioural - Strategy**](#behavioural--strategy)

- Fluency of use: ⭐ ⭐ ⭐ ⭐

### [**Behavioural - Template Method**](#behavioural---template-method)

- Fluency of use: ⭐ ⭐ ⭐

### [**Behavioural - Visitor**](#behavioural---visitor)

- Fluency of use: ⭐

### [**Behavioural - Interpreter**](#behavioural---interpreter)

- Fluency of use: ⭐

# [**Another Specific Terms**](#other-terms-to-know)

## [**What is an abstract class ?**](#what-is-an-abstract-class)

Abstract class means `hiding the implementation` and just `showing the function definition` to the user. Abstract classes `cannot be instantiated`, it should be inherited and then instantiation should be done for the subclass. It can `have both abstract and non-abstract methods`.

## [**What is a concrete class ?**](#what-is-a-concrete-class)

A concrete class is a class which has implementation for all of its methods. It cannot have any unimplemented methods. It is simply the sub class which is inherited from an abstract class.

<p align="center">
    <img src="./photo/concrete.png" width="640" />
</p>
<h3 align="center">

***BOTH RECTANGLE AND CIRCLE ARE CONCRETE CLASS***
</h3>

# [**My Mentors**](#my-mentors)

<table>
        <tr>
            <td align="center">
                <a href="#">
                    <img src="./photo/mentor.jpeg" width="100px;" alt=""/>
                    <br />
                    <sub><b>Nguyễn Đăng Phát</b></sub>
                </a>
            </td>
            <td align="center">
                <a href="#">
                    <img src="./photo/mentor-2.jpeg" width="100px;" alt=""/>
                    <br />
                    <sub><b>Nguyễn Phúc Thảo</b></sub>
                </a>
            </td>
        </tr>
</table>
 
# [**Made with 💘**](#made-with-love-and-php)