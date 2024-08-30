# Mixins

Dart mixins is a concept in the programming lanauage which helps you do the concept of reusability. It helps u to make the code reusable. 

Now you will think, code reusability can be done using Inheritance also right. 
Create one parent class, and just extend the parent class from a child class to get all the properties of the parent class.

### Cons of Inheritance: 
You cannot inherit mulitple classes. 
Lets say u want the properties of this class also, that class also.

Mixins, you can get properties of two differnt mixins. It is nothing just consider it like a class, it helps you to do reusablity.

## What Are Mixins? 
Mixins in Dart are a way to achieve code reusability by allowing you to reuse a set of properties and methods across multiple classes. They offer a solution to some of the limitations of traditional inheritance.

## Why Use Mixins? 
While inheritance allows a class to inherit from a single parent class, mixins provide a way to share code among multiple classes without the constraints of single inheritance. With mixins, you can include functionality from multiple sources in a class

## Limitations of Inheritance:

- ### Single Inheritance Limitation:
  In Dart, a class can only extend one parent class. This can be restrictive if you need features from multiple classes.

- ### Code Duplication:
  Using inheritance to achieve code reuse can lead to deep and complex class hierarchies, making the code harder to manage.

## Mixins vs. Inheritance: 
Mixins allow you to inject methods and properties from multiple sources into a class, while inheritance involves extending a single base class.

## Example:

### 1. Traditional Approach Using Inheritance:

- Create a base class that contains common functionality.
- Subclasses inherit from this base class.
```
class Animal {
  void walk() {}
  void talk() {}
  void reproduce() {}
  int legs = 0;
}

class Human extends Animal {
  // Human inherits walk, talk, reproduce, and legs from Animal
}
```

### 2. Using Mixins:

- Define mixins with common functionality.
- Apply mixins to classes using the with keyword.

```
mixin Walk {
  void walk() {}
}

mixin Talk {
  void talk() {}
}

mixin Reproduce {
  void reproduce() {}
}

class Animal with Walk, Talk, Reproduce {
  int legs = 0;
  // Animal class now has walk, talk, reproduce methods, and legs property
}

class Human with Walk, Talk, Reproduce {
  // Human class now has walk, talk, reproduce methods
}
```

## Advantages of Mixins:

- ### Multiple Mixins:
  A class can use multiple mixins to combine different functionalities.

- ### Avoids Deep Inheritance Hierarchies:
  Mixins help avoid complex class hierarchies by allowing a class to include functionality from various sources.

### Summary 
Mixins are a powerful feature in Dart that enable code reuse by allowing you to mix in functionality from multiple sources into a single class. This approach simplifies code management and avoids the limitations and complexities of deep inheritance hierarchies.

## Key Differences of Inheritance from Mixins:

- ### Inheritance Restriction: 
  You can only extend one base class at a time. If you need to combine functionality from multiple base classes, inheritance will not suffice.

- ### Flexibility: 
  Mixins offer more flexibility by allowing a class to include multiple sets of functionality from different sources without needing a complex hierarchy.

Using inheritance is straightforward for scenarios where you have a clear single hierarchy and need to share methods among classes. Mixins, on the other hand, are ideal for scenarios where you need to combine functionalities from multiple sources without deep inheritance hierarchies.
