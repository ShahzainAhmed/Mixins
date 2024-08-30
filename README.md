# Mixins

Dart mixins is a concept in the programming lanauage which helps you do the concept of reusability. It helps u to make the code reusable. 

Now you will think, code reusability can be done using Inheritance also right. 
Create one parent class, and just extend the parent class from a child class to get all the properties of the parent class.

Cons of Inheritance: 
You cannot inherit mulitple classes. 
Lets say u want the properties of this class also, that class also.

Mixins, you can get properties of two differnt mixins. It is nothing just consider it like a class, it helps you to do reusablity.

```
class Animal with Walk, Talk, Reproduce {
  int legs = 0;
  // Animal class now has walk, talk, reproduce methods, and legs property
}

class Human with Walk, Talk, Reproduce {
  // Human class now has walk, talk, reproduce methods
}

mixin Walk {
  void walk() {}
}

mixin Talk {
  void talk() {}
}

mixin Reproduce {
  void reproduce() {}
}
```

## Advantages of Mixins:

- ### Multiple Mixins:
  A class can use multiple mixins to combine different functionalities.

- ### Avoids Deep Inheritance Hierarchies:
  Mixins help avoid complex class hierarchies by allowing a class to include functionality from various sources.

### Summary 
Mixins are a powerful feature in Dart that enable code reuse by allowing you to mix in functionality from multiple sources into a single class. This approach simplifies code management and avoids the limitations and complexities of deep inheritance hierarchies.

## Inheritance 

```
// Base class with common methods
class LivingBeing {
  void walk() {}
  void talk() {}
  void reproduce() {}
}

// Animal class extending the base class
class Animal extends LivingBeing {
  int legs = 0;
  // Animal class now inherits walk, talk, reproduce methods and has legs property
}

// Human class extending the base class
class Human extends LivingBeing {
  // Human class now inherits walk, talk, reproduce methods
}
```
## Explanation:
### 1. Base Class (LivingBeing):
- Contains the methods walk(), talk(), and reproduce() that you want to reuse.

### 2. Derived Classes (Animal and Human):
- Extend the LivingBeing class to inherit its methods.
- Animal has an additional property legs specific to it.
- Human inherits all the methods but does not have additional properties in this example.


## Key Differences from Mixins:

- ### Inheritance Restriction: 
  You can only extend one base class at a time. If you need to combine functionality from multiple base classes, inheritance will not suffice.

- ### Flexibility: 
  Mixins offer more flexibility by allowing a class to include multiple sets of functionality from different sources without needing a complex hierarchy.

Using inheritance is straightforward for scenarios where you have a clear single hierarchy and need to share methods among classes. Mixins, on the other hand, are ideal for scenarios where you need to combine functionalities from multiple sources without deep inheritance hierarchies.
