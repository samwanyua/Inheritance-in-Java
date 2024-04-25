# Inheritance-in-Java

Inheritance is a key feature of object-oriented programming (OOP) languages like Java. It allows a class (subclass or derived class) to inherit properties and behavior from another class (superclass or base class). This promotes code reusability, extensibility, and helps in creating a hierarchical relationship between classes.

## Table of Contents

- [Introduction to Inheritance](#introduction-to-inheritance)
- [Types of Inheritance](#types-of-inheritance)
  - [Single Inheritance](#single-inheritance)
  - [Multilevel Inheritance](#multilevel-inheritance)
  - [Hierarchical Inheritance](#hierarchical-inheritance)
  - [Multiple Inheritance (Through Interfaces)](#multiple-inheritance-through-interfaces)
- [Example Code](#example-code)
- [Benefits of Inheritance](#benefits-of-inheritance)
- [Conclusion](#conclusion)
- [Further Reading](#further-reading)

## Introduction to Inheritance

Inheritance allows a class to inherit properties and methods from another class. The class that is being inherited from is called the superclass or base class, and the class that inherits is called the subclass or derived class. In Java, inheritance is achieved using the `extends` keyword.

## Types of Inheritance

### Single Inheritance

Single inheritance occurs when a class inherits properties and behavior from only one superclass.

### Multilevel Inheritance

Multilevel inheritance involves a chain of inheritance, where a subclass inherits from a superclass, and then another subclass inherits from that subclass.

### Hierarchical Inheritance

Hierarchical inheritance involves multiple subclasses inheriting from a single superclass.

### Multiple Inheritance (Through Interfaces)

Java does not support multiple inheritance of classes to avoid the diamond problem, but it supports multiple inheritance through interfaces, where a class can implement multiple interfaces.

## Example Code

```java
// Superclass
class Vehicle {
    void drive() {
        System.out.println("Driving...");
    }
}

// Subclass inheriting from Vehicle
class Car extends Vehicle {
    void honk() {
        System.out.println("Honking...");
    }
}

// Subclass inheriting from Car
class SportsCar extends Car {
    void accelerate() {
        System.out.println("Accelerating...");
    }
}

public class Main {
    public static void main(String[] args) {
        SportsCar myCar = new SportsCar();
        myCar.drive();       // Output: Driving...
        myCar.honk();        // Output: Honking...
        myCar.accelerate();  // Output: Accelerating...
    }
}
