CMP 129 – Computer Science II
Week 10 – Lab 2: Abstract Animal Class
Learning Objectives

After completing this lab, students should be able to:

Define an abstract class.
Declare and implement an abstract method.
Extend an abstract superclass.
Call a superclass constructor using super().
Inherit a concrete method from a superclass.
Instantiate subclasses directly without using polymorphism.
Assignment: Animal Abstract Class

Create a Java program containing these four classes:

Animal
Dog
Cat
AnimalTest

Do not create an object directly from the abstract Animal class. Do not use polymorphic references in this assignment.

Part 1: Animal Abstract Class

Create:

Animal.java

Declare Animal as an abstract class:

public abstract class Animal

Include these private attributes:

private String name;
private int age;
private String species;
Constructor

Create a constructor that initializes all attributes:

public Animal(String name, int age, String species)

Use the this keyword when assigning the values.

Getter and Setter Methods

Create getters and setters for all three attributes:

getName()
setName()
getAge()
setAge()
getSpecies()
setSpecies()
Concrete Method

Create:

public void displayInfo()

This concrete method must display the animal’s name, age, and species clearly.

Abstract Method

Declare:

public abstract void makeSound();

Do not provide a method body. Each subclass must implement this method.

Part 2: Dog Class

Create:

Dog.java

The class must extend Animal:

public class Dog extends Animal
Constructor

Create:

public Dog(String name, int age, String species)

Use super() to call the Animal constructor:

super(name, age, species);
Required Methods

Implement the inherited abstract method:

@Override
public void makeSound()

It must print:

Woof!

Also create:

public void displayType()

It must print:

Animal type: Dog
Part 3: Cat Class

Create:

Cat.java

The class must extend Animal:

public class Cat extends Animal
Constructor

Create:

public Cat(String name, int age, String species)

Use super() to call the Animal constructor.

Required Methods

Implement:

@Override
public void makeSound()

It must print:

Meow!

Also create:

public void displayType()

It must print:

Animal type: Cat
Part 4: AnimalTest Class

Create:

AnimalTest.java

Place the main() method in this class.

The program must:

Create at least two Dog objects.
Create at least two Cat objects.
Call displayInfo() for every animal.
Call makeSound() for every animal.
Call displayType() for every animal.
Use at least one getter method.
Use at least one setter method.
Display the updated animal information.

Declare objects using their subclass types:

Dog dog1 = new Dog("Buddy", 3, "Golden Retriever");
Cat cat1 = new Cat("Luna", 2, "Siamese");

Do not use:

Animal animal = new Dog(...);
Example Output
Animal Information
------------------
Name: Buddy
Age: 3
Species: Golden Retriever
Animal type: Dog
Sound: Woof!

Animal Information
------------------
Name: Luna
Age: 2
Species: Siamese
Animal type: Cat
Sound: Meow!

Students may use different animal information.

Restrictions

Do not:

Attempt to instantiate the abstract class:
Animal animal = new Animal(...);
Use polymorphic references:
Animal animal = new Dog(...);
Create an array or collection of Animal references.
Place main() inside Animal, Dog, or Cat.
Remove the abstract keyword from Animal or makeSound().
General Requirements
Declare Animal as an abstract class.
Keep all attributes private.
Use extends to create the subclasses.
Use super() in each subclass constructor.
Use @Override when implementing makeSound().
Place each public class in a separate Java file.
Follow standard Java naming and formatting conventions.
Include comments explaining abstract classes, inheritance, and abstract methods.
Test all required methods.
Ensure the program compiles and runs without errors.
Follow the course AI-use policy.
Record any AI assistance in AI-Use-Report.md.
Required Organization

Keep these files directly in the repository root:

- `CMP129-Week-10-Lab-02.md`
- `AI-Use-Report.md`
- `Animal.java`
- `Dog.java`
- `Cat.java`
- `AnimalTest.java`

Do not create or use a `src` folder.


Submission

Students must push:

Animal.java
Dog.java
Cat.java
AnimalTest.java
Lab-02/AI-Use-Report.md

Suggested commit messages:

Create abstract Animal class
Implement Dog and Cat subclasses
Complete animal class testing
