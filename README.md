# Java Abstract Shapes

A Java console application developed for a Programming II coursework assignment at Colorado State University Global. The project demonstrates object-oriented programming concepts through geometric surface area and volume calculations.

The application uses an abstract base class and three subclasses to demonstrate abstraction, inheritance, polymorphism, and method overriding.

## Project Overview

This application calculates the surface area and volume of three geometric shapes:

- Sphere
- Cylinder
- Cone

Each shape is represented by its own Java class, which inherits from the abstract `Shape` class.

The application creates an instance of each shape, stores the objects in a shared `Shape` array, and displays their calculated properties using overridden `toString()` methods.

The project demonstrates how different objects can share a common structure while implementing their own mathematical formulas.

## Features

- Abstract `Shape` class defining required methods
- Three subclasses representing geometric shapes
- Surface area and volume calculations
- Parameterized constructors for shape dimensions
- Method overriding using `@Override`
- Polymorphic storage using a `Shape` array
- Enhanced `for` loop to process different shape objects
- Formatted numerical output to two decimal places
- UML diagram documenting the class relationships
- Screenshots demonstrating program execution and testing

## Technologies Used

- **Java** — Application logic and mathematical calculations
- **Java Math Library** — Mathematical constants and square root calculations
- **Object-Oriented Programming** — Abstraction, inheritance, polymorphism, and encapsulation
- **UML** — Visual representation of class relationships
- **Command Line** — Compiling and executing the application

## Object-Oriented Programming Concepts

### Abstraction

The `Shape` class is declared as abstract and defines two methods:

```java
public abstract double surface_area();
public abstract double volume();
```

These methods establish a common structure for all shapes without providing specific calculations.

Each subclass must implement its own surface area and volume formulas.

### Inheritance

The `Sphere`, `Cylinder`, and `Cone` classes extend the abstract `Shape` class.

For example:

```java
public class Sphere extends Shape
```

This establishes a parent-child relationship between the general `Shape` class and the individual geometric shapes.

### Polymorphism

The application stores different shape objects in a single array:

```java
Shape[] shapeArray =
{
    sphere,
    cylinder,
    cone
};
```

Although the objects represent different geometric shapes, they can all be referenced through the shared `Shape` type.

An enhanced `for` loop processes each object:

```java
for (Shape shape : shapeArray)
{
    System.out.println(shape);
    System.out.println("---------------------------");
}
```

Java automatically calls the appropriate overridden `toString()` method for each object.

### Encapsulation

Each shape stores its dimensions in private instance variables.

For example:

```java
private double radius;
private double height;
```

The values are initialized through parameterized constructors.

This demonstrates how object data can be maintained within individual classes.

### Method Overriding

Each subclass implements the abstract methods inherited from `Shape`.

The subclasses also override `toString()` to provide readable output containing their dimensions, surface area, and volume.

The `@Override` annotation identifies methods that implement or replace methods declared in a parent class.

## Geometric Calculations

The application uses standard mathematical formulas to calculate surface area and volume.

### Sphere

A sphere is defined by its radius.

**Surface Area:**

\[
A = 4\pi r^2
\]

**Volume:**

\[
V = \frac{4}{3}\pi r^3
\]

Where:

- `r` = radius

### Cylinder

A cylinder is defined by its radius and height.

**Surface Area:**

\[
A = 2\pi r^2 + 2\pi rh
\]

**Volume:**

\[
V = \pi r^2h
\]

Where:

- `r` = radius
- `h` = height

### Cone

A cone is defined by its radius and height.

**Surface Area:**

\[
A = \pi r(r + \sqrt{r^2 + h^2})
\]

**Volume:**

\[
V = \frac{1}{3}\pi r^2h
\]

Where:

- `r` = radius
- `h` = height

The cone's surface area calculation includes the slant height, calculated using the Pythagorean theorem.

## Project Structure

```text
java-abstract-shapes/
├── src/
│   ├── Shape.java
│   ├── Sphere.java
│   ├── Cylinder.java
│   ├── Cone.java
│   └── ShapeArray.java
├── screenshots/
│   └── Program development and testing screenshots
├── uml/
│   └── Miro UML Screenshot.pdf
├── .gitignore
├── LICENSE
└── README.md
```

### Source Files

| File | Purpose |
|------|---------|
| `Shape.java` | Abstract parent class defining surface area and volume methods |
| `Sphere.java` | Implements sphere calculations |
| `Cylinder.java` | Implements cylinder calculations |
| `Cone.java` | Implements cone calculations |
| `ShapeArray.java` | Creates the objects, stores them in an array, and displays the results |

## How to Run

### Requirements

- Java Development Kit (JDK)
- Terminal or command prompt

No external libraries are required.

### Instructions

1. Clone or download the repository.

2. Open a terminal in the repository's root directory.

3. Compile the Java source files:

   ```bash
   javac src/*.java
   ```

4. Run the application:

   ```bash
   java -cp src ShapeArray
   ```

5. The console displays the surface area and volume of each shape.

The application uses predefined dimensions, so no keyboard input is required.

## Example Output

The application creates the following objects:

- Sphere with radius `5.0`
- Cylinder with radius `4.0` and height `10.0`
- Cone with radius `3.0` and height `7.0`

Example console output:

```text
Sphere
Radius: 5.0
Surface Area: 314.16
Volume: 523.60
---------------------------
Cylinder
Radius: 4.0
Height: 10.0
Surface Area: 351.86
Volume: 502.65
---------------------------
Cone
Radius: 3.0
Height: 7.0
Surface Area: 100.10
Volume: 65.97
---------------------------
```

The numerical results are formatted to two decimal places.

## UML Class Diagram

The UML diagram illustrates the inheritance relationships between the abstract `Shape` class and its three subclasses.

It documents the shared abstract methods and the individual classes responsible for implementing the calculations.

[View the UML Class Diagram](uml/Miro%20UML%20Screenshot.pdf)

## Development and Testing Screenshots

The `screenshots/` directory contains images documenting the original development and testing process.

These include:

- Java source code in the IDE
- Initial program execution
- Changes to geometric dimensions
- Console output after modifying shape values
- Additional testing of the shape calculations
- Original GitHub repository documentation

[View the Screenshots Directory](screenshots/)

The screenshots demonstrate how the application was tested using different values for the shapes.

## Current Limitations

This project was developed as an introductory object-oriented programming assignment.

Its current limitations include:

- Shape dimensions are predefined in `ShapeArray.java`.
- Users cannot enter dimensions interactively.
- The application does not validate negative or zero dimensions.
- Output is displayed in the console rather than a graphical interface.
- The application supports only three geometric shapes.
- Calculations are displayed but are not saved to an external file.

These limitations reflect the educational scope of the original assignment.

## Educational Context

This project was developed for a Programming II course at Colorado State University Global.

The assignment provided practical experience with:

- Creating abstract classes
- Extending classes through inheritance
- Implementing abstract methods
- Applying method overriding
- Using private instance variables and constructors
- Demonstrating polymorphism through arrays
- Working with geometric formulas in Java
- Formatting numerical output
- Creating UML class diagrams
- Testing calculations using different input values

The original coursework structure, pseudocode, and implementation have been preserved to demonstrate progression in Java programming and object-oriented design.

## License

This project is licensed under the MIT License. See [LICENSE](LICENSE) for details.
