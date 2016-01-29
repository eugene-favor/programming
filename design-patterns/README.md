**Template method** - http://reefpoints.dockyard.com/ruby/2013/07/10/design-patterns-template-pattern.html

Template Method pattern is not difficult at all. 
We first defined a base class, within which we defined necessaryhook methods to be overridden by our subclasses.

Hook Methods serve two purposes:

Override the skeletal implementation and define something new
Or, accept the default implementation

**Strategy** - http://reefpoints.dockyard.com/2013/07/25/design-patterns-strategy-pattern.html

The Strategy pattern is a delagation-based design pattern, and shares some similarities with the Template Method pattern. 
However, instead of depending so heavily on inheiritance between a superclass and subclasses to use our target algorithm, 
we take our algorithm and consider it as a separate object. 
As long as we remember the relationship between the strategies and the context, we earn real advantages over the Template Method

The Strategy pattern employs strategies, objects of which possess identical behavior. 

Context class, the operator of the strategies

Resolves problems:

Subclasses are tightly bound to a superclass or baseclass
Runtime flexibility is hindered
Only a portion of the desired alogrithm is varied

**Adapter** - 

An Adapter is used when you want to provide a unified interface to a number of different objects that implement similar functionality. 
This pattern is easy to spot in the wild for a Ruby developer, as most of us have to use ActiveRecord in our day to day work. 
Under the hood, ActiveRecord talks to a large amount of different databases, 
but wraps them up in a common interface its implementation code can avoid worrying about their individual differences. This is exactly the sort of thing the Adapter pattern is useful for.

Increasingly, Rubyists are finding this pattern to be useful in other settings as well. 
In particular, things like Intridea’s multi_json gem allow libraries and applications to be built against an abstract interface rather than requiring some particular JSON library that might conflict with other dependencies. Inspired by the ideas behind multi_json, a Mendicant University student (Mitko Kostov) built a similar adapter library for Markdown processors called Marky. The base implementation is very simple, and gives us a good opportunity to look at one way to implement an Adapter in Ruby from the ground up.

**Decorator** -

**Factory method** -

The Factory Method pattern is used for putting a layer of abstraction on top of object creation 
so that directly working with its constructor is no longer necessary. 
This process can lead to more expressive ways of building new objects, and can also allow for the creation of new objects without explicitly referencing their class.

**Abstract factory** - http://www.devinterface.com/blog/en/2010/06/design-patterns-in-ruby-abstract-factory/

An abstract Factory provides a common interface for creating families of related objects together.
The client object does not bother to build objects directly, but it calls the methods provided by this common interface.
Can use Singleton in their implementations

**Iterator** - 

**Observer** - 

http://reefpoints.dockyard.com/2013/08/20/design-patterns-observer-pattern.html
http://addyosmani.com/resources/essentialjsdesignpatterns/book/#observerpatternjavascript
               
There are a few similarities between the Observer and Strategypatterns. 
Both patterns employ an object (the Observer's subject and the Strategy's context) 
that makes calls to another object (the Observer's observer or Strategy's strategy). 
The difference between the two patterns is the purpose and use case. 
The Strategy pattern relies on the strategy to do the work, 
while the Observer pattern informs theobservers of what is going on with the subject.

**Singleton** - 

The concept of the Singleton pattern is fairly straightforward: only a single instance of a class can exist.

**State** -

**Builder** - 

Builder focuses on constructing a complex object step by step.  
Builder often builds a Composite.Sometimes creational patterns are complementary: 
Builder can use one of the other patterns to implement which components get built. 
Can use Singleton in their implementations

**Chain of responosbility** - 

**Command** - 

http://reefpoints.dockyard.com/2013/11/05/design-patterns-command-pattern.html

The Command design pattern intends to separate and decouple an object of invocation from the object that receives the message of invocation. 
We will encapsulate all pertinent information of a method and execute the method at a later time. 
Essentially, the Command pattern gives us the ability to queue a series of operations for a later time.

**Mediator** - 

Object that handles the workflow between many other objects, aggregating the responsibility of that workflow knowledge into a single object.
 
**Proxy** - 

A Proxy is any object that acts as a drop-in replacement object that does a bit of work and then delegates to some other underlying object.

**Facade** - 

The Facade pattern simplifies how users interact with a codebase by implementing an interface that hides many implementation
 details for the most common behaviors needed by consumers.
 
**Prototype** - http://devblog.avdi.org/2012/12/11/modeling-the-world-with-prototypes/  

The prototype pattern is a creational design pattern in software development. 
It is used when the type of objects to create is determined by a prototypical instance, which is cloned to produce new objects. 

This pattern is used to:

avoid subclasses of an object creator in the client application, like the abstract factory pattern does.
avoid the inherent cost of creating a new object in the standard way (e.g., using the 'new' keyword) when it is prohibitively expensive for a given application.

**Flyweight** -

flyweight pattern - is pattern for sharing objects, where each state does not contain its own state, but stores its externally, 
this allows efficient tsharing of objects to save space when there are many instances but only a few different types
