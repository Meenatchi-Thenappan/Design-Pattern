# Design-Pattern
# Patterns
Patterns capture experienced in software development that have been proven to work again and again,and thus provide a solution to specific problems

# Categories by Abstraction Level
* Idioms
* Architectural Patterns
* Design Patterns

## Examples of Python idioms
* Chained comparison operators:
  *Don't do this*
    ```python
    if 0<x and x<10:
        print('x is greater than 0 but less than 10')
    ```
    *Instead, do this*
    ```python
    if 0<x<10:
        print('x is greater than 0 but less than 10')
    ```
* Top-level script environment:
  *Execute only if runs as a script and not as a module*
   ```python
   if __name__=='__main__':
       print('Hello from Script!')

* Conditional expressions:
  *This statement*
    ```python
    if x<5:
        return 10
    else:
        return 20
  *can be reduced to this one*
    return 10 if x<5 else 20

* Indexing during iteration:
  *Don't do this*
   ```python
   index=0
   for value in collection:
       print(index,value)
       index += 1
    ```
  *Nor this*
  ```python
  for index in range(len(collection)):
      value = collection[index]
      print(index,value)
  ```
  *Definetely not this*
  ```python
  index=0
  while index<len(collection):
      value=collection[index]
      print(index,value)
      index += 1
  ```
  *Instead do this*
  ```python
  for index,value in enumerate(collection):
      print(index,value)

# Design Principles

 Markup :1. Seperate out the things that change from those that stay the same
         2. Program to an interface not an implementation
         3. Prefer composition over inheritance
         4. Delegation
# Design Patterns

Markup :1.Singleton Pattern
        2.Template Method Pattern
        3.Adapter Pattern
        4.Observer Pattern

## Singleton Pattern

![Image of ClassDiagram of singleton pattern](https://media.geeksforgeeks.org/wp-content/uploads/20200122161234/singleton-class-diagram.png)

This pattern restricts the instantiation of a class to one object. It is a type of creational pattern and involves only one class to create methods and specified objects.It provides a global point of access to the instance created.

## Template Method Pattern

![Image of ClassDiagram of Template Method Pattern](https://media.geeksforgeeks.org/wp-content/uploads/claasDia.jpg)

Template method design pattern is to define an algorithm as a skeleton of operations and leave the details to be implemented by the child classes. The overall structure and sequence of the algorithm are preserved by the parent class.

## Adapter Pattern

![Image of ClassDiagram of Adapter Pattern](https://media.geeksforgeeks.org/wp-content/uploads/classDiagram.jpg)

Adapter pattern works as a bridge between two incompatible interfaces. This type of design pattern comes under structural pattern as this pattern combines the capability of two independent interfaces.This pattern involves a single class which is responsible to join functionalities of independent or incompatible interfaces. A real life example could be a case of card reader which acts as an adapter between memory card and a laptop.

## Observer Pattern

![Image of ClassDiagram of Observer Pattern](https://upload.wikimedia.org/wikipedia/commons/thumb/a/a8/Observer_w_update.svg/500px-Observer_w_update.svg.png)

In this pattern, objects are represented as observers that wait for an event to trigger. An observer attaches to the subject once the specified event occurs. As the event occurs, the subject tells the observers that it has occurred.
