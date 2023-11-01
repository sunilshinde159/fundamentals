# Access Modifiers
Access modifiers in Java are keywords that determine the accessibility or visibility of classes, methods, and variables within a program. They control the level of access that other parts of the program have to these elements.
There are four types of access modifiers in Java:
1. Public: The public access modifier allows unrestricted access to the class, method, or variable from any other part of the program.
2. Private: The private access modifier restricts access to the class, method, or variable within the same class. It cannot be accessed from any other class.
3. Protected: The protected access modifier allows access to the class, method, or variable within the same package or subclasses. It is similar to the default (package-private) access, but with the additional ability to be accessed by subclasses outside the package.
4. Default (Package-Private): If no access modifier is specified, it is considered as the default access modifier. It allows access to the class, method, or variable within the same package but restricts access from outside the package.
Constructors, on the other hand, are special methods in a Java class that are used to initialize objects of that class. They have the same name as the class and do not have a return type.
Constructors are called automatically when an object is created using the "new" keyword. They are used to set initial values to the instance variables of an object and perform any necessary setup operations.
Constructors can be overloaded, meaning a class can have multiple constructors with different parameters. This allows for different ways of creating objects with different initializations.
Access modifiers and constructors are fundamental concepts in Java programming. Understanding and effectively using them is crucial for creating well-designed and secure programs.

Sure! Here's an example that demonstrates the use of access modifiers in Java:

```java
public class Car {
    // public access modifier
    public String brand;

    // private access modifier
    private int speed;

    // protected access modifier
    protected boolean engineStatus;

    // default access modifier
    int year;

    // Constructor
    public Car(String brand, int year) {
        this.brand = brand;
        this.year = year;
        this.speed = 0;
        this.engineStatus = false;
    }

    // Public method
    public void accelerate() {
        speed += 10;
        System.out.println("Accelerating to " + speed + " km/h");
    }

    // Private method
    private void startEngine() {
        engineStatus = true;
        System.out.println("Engine started");
    }

    // Protected method
    protected void stopEngine() {
        engineStatus = false;
        System.out.println("Engine stopped");
    }

    // Default method
    void displayYear() {
        System.out.println("Manufactured in " + year);
    }
}
```


In this example, we have a `Car` class with different access modifiers:

- The `brand` variable is declared with the public access modifier, which means it can be accessed from any other class.
- The `speed` variable is declared with the private access modifier, which means it can only be accessed within the same class.
- The `engineStatus` variable is declared with the protected access modifier, which means it can be accessed within the same package or subclasses.
- The `year` variable is declared without an access modifier, which means it has default (package-private) access and can be accessed within the same package.

The class also has a constructor with the public access modifier, which can be accessed from any other class to create objects of the `Car` class.

Additionally, there are different methods with different access modifiers:

- The `accelerate()` method has the public access modifier, so it can be accessed from any other class.
- The `startEngine()` method has the private access modifier, so it can only be accessed within the same class.
- The `stopEngine()` method has the protected access modifier, so it can be accessed within the same package or subclasses.
- The `displayYear()` method has the default access modifier, so it can be accessed within the same package.

These access modifiers control the visibility and accessibility of the class members, ensuring proper encapsulation and data hiding.
