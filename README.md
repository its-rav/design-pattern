# Design Pattern

## Intro
This repository contains code samples for learning design patterns in C#, Golang, and Python. It provides helpful resources for understanding the concepts and working through various examples to better acquaint oneself with designing applications with design patterns in the various languages.

> Hey I'm a total noob myself, so don't blame me for any mistake I make during making this repo. - said me

So, what exactly are design patterns?
### Wat da hell is it?
> In software engineering, a software design pattern is a general, reusable solution to a commonly occurring problem within a given context in software design. It is not a finished design that can be transformed directly into source or machine code. Rather, it is a description or template for how to solve a problem that can be used in many different situations. Design patterns are formalized best practices that the programmer can use to solve common problems when designing an application or system. - [Wikipedia](https://en.wikipedia.org/wiki/Software_design_pattern)

> Design patterns are typical solutions to common problems
in software design. Each pattern is like a blueprint
that you can customize to solve a particular
design problem in your code. - [Refactoring Guru](https://refactoring.guru/design-patterns)

### Why?

Hey, trust me bro, you might manage to do just fine as a software engineer without knowing any of this. Going through some of them, you will figure out you might have been implementing it unwittingly. But yea below is why you need them:

- **Tested, proven development paradigms** - everyone has used it for a while, "for a while" I mean who know how long, it just very very long time ago. *Hey! Trust the elders!*
- **Godspeed development process** - imagine facing a problem and you just know right away how to solve it *Oh shit I recognize this, we can just use Observer*
- Use it instead of coming up with a more shitty solution!

_________________
## Types of design patterns
These are categorized by the *intent*, or *purpose*

### [Creational](https://github.com/its-rav/design-pattern/blob/master/creational)
Creational patterns are focused towards how to instantiate an object or group of related objects that increase flexibility and reuse of existing code
#### Factory Method
Factory Method provides an interface for creating objects in a superclass, but allows subclasses to alter the type of objects that will be created. 
> Creating objects by calling a (factory) method — either specified in an interface and implemented by child classes, or implemented in a base class and optionally overridden by derived classes—rather than by calling a constructor.

#### Abstract Factory
The abstract factory pattern provides a way to encapsulate a group of individual factories that have a common theme without specifying their concrete classes
> Basically, it is a list of "standards" for factories creating objects that have a common theme, so that the products are compatible with each others
#### Builder
A creational design pattern that lets you construct complex objects step by step. The pattern allows you to produce different types and representations of an object using the same construction code.
> Imagine you have to make a BobaMilkshake with various toppings and ingredients. Constructors are not suitable for this task, since there are numerous steps required to assemble the drink and countless possible combinations that need to be taken into consideration. The builder pattern can help you out with this issue by extracting the object-building code out of its own class and moving into a Builder class, such as BobaMilkshakeBuilder, which would have functions like putMilk(), putWater(), putTopping(toppingType, amount), etc
#### Prototype
 A creational design pattern that lets you copy existing objects without making your code dependent on their classes.
 > In plain words, creating object based on an existing object through cloning.
#### Singleton
This one restricts the instantiation of a class to one object. This is useful when exactly one object is needed to coordinate actions across the system.
> The infamous singleton. Just like the name, "ton" is much very single, he likes and is meant to be the one and only.
### [Structural](https://github.com/its-rav/design-pattern/tree/master/structural)
Structural patterns are focused towards how to assemble objects and classes into larger structures.  Or yet another explanation would be, they help in answering "How to build a software component?"
#### Adapter
a structural design pattern that allows objects with incompatible interfaces to collaborate.
> it allows the interface of an existing class to be used as another interface. It is often used to make existing classes work with others without modifying their source code. For instance, if an application primarily interacts with XML and the newly integrated service is JSON based, an adapter can be utilized.
#### Bridge
A structural design pattern that lets you split a large class or a set of closely related classes into two separate hierarchies—abstraction and implementation—which can be developed independently of each other.
> "Decouple an abstraction from its implementation so that the two can vary independently". To be specific, instead of having BlueCircle, RedCircle, YellowSquare, WhiteSquare derived from Shape, utilizing Bridge pattern, you can make Circle, Square derived from Shape that has a type Color attribute. Doing this will allow for Shape and color to be abstracted from each other, and have far more expansions of the derivatives.
#### Composite
A structural design pattern that lets you compose objects into tree structures and then work with these structures as if they were individual objects.
> The Composite pattern provides you with two basic element types that share a common interface: simple leaves and complex containers. A container can be composed of both leaves and other containers. This lets you construct a nested recursive object structure that resembles a tree.
#### Decorator
 A structural design pattern that lets you attach new behaviors to objects by placing these objects inside special wrapper objects that contain the behaviors.
 > Basically, a wrapper that wrap around an object that you want to change its behavior
#### Facade
Facade provides a simplified interface to a library, a framework, or any other complex set of classes.
> a simple interface to the complex subsystem is a facade.
#### Flyweight
Flyweight lets you fit more objects into the available amount of RAM by sharing common parts of state between multiple objects instead of keeping all of the data in each object.
> It is used to minimize memory usage or computational expenses by sharing as much as possible with similar objects. For instance, you are making a 2D shooting game where a large number of Bullet objects are involved. While it is common sense that your Bullet will have coord, color, image, vector, speed attributes, you risk overwhelming the RAM capacity of your system if your game has 1 billion or more bullets. Rather, the Flyweight design pattern can be employed to create FlyweightBullet objects that store the shared, common image attribute values across the whole application.
#### Proxy
Using the proxy pattern, a class represents the functionality of another class.
> Decorator and Proxy have similar structures, but very different intents. Both patterns are built on the composition principle, where one object is supposed to delegate some of the work to another. The difference is that a Proxy usually manages the life cycle or the security of its service object on its own, whereas Decorators is used to add responsibilities to an object(without using inheritance).
### [Behavioral](https://github.com/its-rav/design-pattern/blob/master/behavioral)
Behavioral designs are capable of identifying common communication patterns between objects and realize these patterns, or, you can just say, they take care of effective communication and the assignment of responsibilities between objects.

#### Chain of responsibility
#### Command
#### Iterator
#### Mediator
#### Memento
#### Observer
#### State
#### Strategy
#### Template method
#### Visitor

## Warning
- 
> Design patterns differ by their complexity, level of detail and scale of applicability to the entire system being designed. I like the analogy to road construction: you can make an intersection safer by either installing some traffic lights or building an entire multi-level interchange with underground passages for pedestrians.
- Kludges for a weak programming language 
    - Developers tend to use design patterns as a workaround or "kludge" to get around the limitations of the language. Design patterns are often used to make up for the shortcomings of a "weak" programming language, allowing the developer to still create a program even if the language doesn't have the necessary tools.
    > This practice is not only common, but institutionalized. For example, in the OO world you hear a good deal about "patterns". I wonder if these patterns are not sometimes evidence of case (c), the human compiler, at work. 
    > When I see patterns in my programs, I consider it a sign of trouble. The shape of a program should reflect only the problem it needs to solve. Any other regularity in the code is a sign, to me at least, that I'm using abstractions that aren't powerful enough - often that I'm generating by hand the expansions of some macro that I need to write. 
    > -- <cite> PaulGraham, which leads to the question "Are Patterns a LanguageSmell?"</cite>
    - http://www.paulgraham.com/icad.html
    - http://wiki.c2.com/?AreDesignPatternsMissingLanguageFeatures
- Inefficient solutions
    - Patterns should be applied with the context of the problem you are trying to solve, not "to the letter" => which leads to inefficient
    - Design patterns are not a magic wand to all of your problems, do not try to force them
## De end
> k bye