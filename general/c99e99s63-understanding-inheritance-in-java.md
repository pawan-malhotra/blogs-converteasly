---
title: "understanding the concept of inheritance in java with application"
date: '13 feb, 2024'
category: 'general'
---

Inheritance is a fundamental concept in Java (and in object-oriented programming in general) that allows classes to inherit properties and behaviors from other classes. Let's dive into concept of inheritance more deeply with a lots of examples.

## What is Inheritance ?

In Java, inheritance refers to the mechanism by which a class can inherit properties and methods from another class. The class from which properties and methods are inherited is called the superclass or parent class or base class, and the class that inherits those properties and method is called the subclass or child class.

### Example:

```powershell
// parent class or base class
public class Animal {
    public void eat(){
        System.out.println("eating....");
    }
    }
    // child class or subclass
    public class Dogs extends Animal {
    public void bark(){
        System.out.println("Dog is barking");
    }
}
// Main.java
public class Main {
    public static void main(String[] args) {
    Dogs dog =new Dogs();
       dog.eat();
       dog.bark();
    }
}
```

```powershell
Output
eating....
Dog is barking
```
**Note**:  Extend keywords are used to inherit the properties of the class.

## Types of Inheritance:

#### 1.Single Inheritance

#### 2.Multilevel inheritance

#### 3.Hierarchical Inheritance

#### 4.Hybrid Inheritance 

## Single Inheritance

A class can inherit attributes and methods from only one parent class. In other words, a subclass can extend only one superclass.

<img src="./pics/single inheritance.png"
     alt="single inheritance"
     style="float: left; margin-right: 10px;" />



### Example:

```powershell
// parent class or base class
public class Animal {
    public void eat(){
        System.out.println("eating....");
    }
    }
    // child class or subclass
    public class Dogs extends Animal {
    public void bark(){
        System.out.println("Dog is barking");
    }
}
// Main.java
public class Main {
    public static void main(String[] args) {
    Dogs dog =new Dogs();
       dog.eat();
       dog.bark();
    }
}
```

```powershell
Output
eating....
Dog is barking
```

## Multilevel Inheritance

The Inheritance in which class inherits methods and properties from a class that is already deriving from another class is called multilevel inheritance.

<img src="./pics/multilevel inheritance.png"
     alt="multilevel inheritance"
     style="float: left; margin-right: 10px;" />


### Example:

```powershell
// Parent class
public class Animal {
    public void eat(){
        System.out.println("eating....");
    }
    }
//    subclass of Animal  
    public class Dogs extends Animal {
    public void bark(){
        System.out.println("Dog is barking");
    }
    public void greeting(){
        System.out.println("welcome to animAL family");
    }
}

// subclass of Dogs
public class cat extends Dogs {
    public void sound(){
        System.out.println("Meow...");
    }
    }

// Main.java
    public class Main {
    public static void main(String[] args) {

       cat Cat=new cat();
       Cat.eat();
       Cat.sound();
       Cat.greeting();
    }
}

```

```powershell
Output
eating....
Meow...
welcome to animAL family


```
## Hierarchical Inheritance

In Hierarchical inheritance, more than one sub-class inherits the property of a single base class. There is one base class and multiple derived classes.

<img src="./pics/Hierchial inheritance.png"
     alt="single hierachial inheritance"
     style="float: left; margin-right: 10px;" />


```powershell
// Parent class or base class
public class Vehicle {
    void speedUp() {
        System.out.println("Speeding up...");
    }

    void brake() {
        System.out.println("Braking...");
    }
}

// Subclass of Vehicle
public class Car extends Vehicle{
    public void Greeting(){
        System.out.println("Hello I am Car");
    }
}

// Subclass of Vehicle
public class Bike extends Vehicle {

    public void Greeting(){
        System.out.println("Hello I am Bike");
    }
}

// Subclass of Vehicle
public class Truck extends Vehicle {

    public void Greeting(){
        System.out.println("Hello I am Truck");
    }
}

```

```powershell
output
Braking...
Hello I am Car
Speeding up...
Hello I am Bike
Speeding up...
Braking...
Hello I am Truck
```

## Hybrid Inheritance

It is a mix of two or more  types of inheritance.Since java doesn't support multiple inheritance with classes. It can be achieved through a combination of Multilevel Inheritance and Hierarchical Inheritance with classes, Hierarchical and Single Inheritance with classes.

<img src="./pics/hybrid inheritance.png"
     alt="hybrid inheritance"
     style="float: left; margin-right: 10px;" />

```powershell
// Parent class or Base class

public class Vehicle {
    void speedUp() {
        System.out.println("Speeding up...");
    }

    void brake() {
        System.out.println("Braking...");
    }
}

// subclass  of  Truck

public class Car extends Truck{
    public void Greeting(){
        System.out.println("Hello I am Car");
    }
}

// subclass of Vehicle

public class Truck extends Vehicle {

    public void Greeting(){
        System.out.println("Hello I am Truck");
    }
    public void Brand(){
        System.out.println("TATA");
    }
}

// Main.java

public class Main {
    public static void main(String[] args) {

       cat Cat=new cat();
       Cat.eat();
       Cat.sound();
       Cat.greeting();
    }
}
```

```powershell
Output

Braking...
Hello I am Car
TATA
Speeding up...
TATA

```




