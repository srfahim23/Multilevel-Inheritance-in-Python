# Multilevel-Inheritance-in-Python

Multilevel inheritance is a type of inheritance in object-oriented programming where a derived class inherits another derived class. This type of inheritance allows you to built a hierarchy of classes where one class builds upon another, leading to a more specialized class.

In Python, multilevel inheritance is archived by using the class hierarchy. The syntax for multilevel inheritance is quite simple and follows the same syntax as single inheritance.

# Syntax
    class Baseclass:
        # Base class code

    class DerivedClass1(BaseClass):
        # Derived class 1 code

    class DerivedClass2(DerivedClass1):
         Derived class 2 code

In the above example, we have three classes: BaseClass, DerivedClass1, and DerivedClass2. The DerivedClass1 class inherits fromt the BaseClass, and the DerivedClass 2 class inherits from the DerivedClass1 class. This create a hierarchy where DerivedClass2 has access to all the attributes and methods of both DerivedClass and BaseClass.

# Example
Let's take a look at an example to understand how multilevel inheritance works in Python. Consider the following classes:

    class Animal:
        def __init__(self, name, species):
            self.name = name
            self.species = species

        def show_details(self):
            print(f"Name: {self.name}")    
            print(f"Species: {self.species}")

    class Dog(Animal):
        def __init__(self, name, breed):
            Animal.__init__(self, name, species="Dog")        
            self.breed = breed

        def show_details(self):
            Animal.show_details(self)    
            print(f"Breed: {self.breed}")

    class GoldenRetriver(Dog):
        def __init__(self, name , color):
            Dog.__init__(self, name, breed="Golden Retriver")        
            self.color = color


        def show_details(self):
            Dog.show_details(self)          
            print(f"color: {self.color}")