🐍 Python OOP: Abstract Class & Method Example
🎯 AIM
To create an abstract class named Shape with an abstract method calculate_area, and implement this method in two subclasses: Rectangle and Circle.

🧠 ALGORITHM
Import ABC module:

Use from abc import ABC, abstractmethod to define abstract classes and methods.
Create Abstract Class Shape:

Define an abstract method calculate_area() with @abstractmethod.
Create Subclass Rectangle:

Set default values for length and breadth.
Override calculate_area() to compute the rectangle area.
Create Subclass Circle:

Set default value for radius.
Override calculate_area() to compute the circle area.
Create Objects & Call Methods:

Instantiate Rectangle and Circle.
Call their calculate_area() methods.
💻 Program
from abc import ABC, abstractmethod

class Shape(ABC):
    @abstractmethod
    def calculate_area(self):
        pass

class Rectangle(Shape):
    def __init__(self, length, breadth):
        self.length = length
        self.breadth = breadth

    def calculate_area(self):
        return self.length * self.breadth

class Circle(Shape):
    def __init__(self, radius):
        self.radius = radius

    def calculate_area(self):
        return 3.14 * self.radius * self.radius

rect = Rectangle(10, 5)
circle = Circle(7)

print("Area of Rectangle:", rect.calculate_area())
print("Area of Circle:", circle.calculate_area())
Output
image

Result
The program successfully demonstrates the concept of abstract classes and methods in Python by implementing calculate_area() in both Rectangle and Circle subclasses.
