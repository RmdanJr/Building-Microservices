# Building Microservices

## CHAPTER 1: Microservices

### What Are Microservices?

Microservices are small, autonomous services that work together.

#### Small, and Focused on Doing One Thing Well

##### Small

A microservice is a piece of code that could be rewritten in two weeks and feels small enough to be managed by a small team. The smaller the service, the more you maximize both the benefits and downsides of microservice architecture.

##### Focused on One Thing

Microservices follow the single responsibility principle. All services are independent and focused on doing one specific functionality.

#### Autonomous

Microservice is a decoupled entity. It should be changed and deployed independently without affecting anything else. Services communicate via network calls to enforce separation and avoid tight coupling. Well-designed APIs are essential for decoupling, and they may be technology-agnostic.

 ### Benefits

#### Technology Heterogeneity

The microservices architecture provides the flexibility to choose the right technology for each job (i.e. service) rather than choosing a standard technology that fits all jobs in the monolithic architecture.



![Microservices can allow you to more easily embrace different technologies](https://www.oreilly.com/api/v2/epubs/9781491950340/files/assets/bdms_0101.png)



#### Resilience

In a microservices system, If one service of a system fails, you can isolate the problem and the rest of the system can carry on working while degrading functionality. Unlike a monolithic system, If the service fails, everything stops working.

#### Scaling

In microservices application, we can scale only services that need scaling. Unlike monolithic application, we have to scale everything together. This allows us to control our costs more effectively.

![1. Microservices - Building Microservices [Book]](https://www.oreilly.com/api/v2/epubs/9781491950340/files/assets/bdms_0102.png)

#### Ease of Deployment

With microservices, we can make a change to a single service and deploy it independently. This allows us to get our code deployed faster. If a problem does occur, it can be isolated quickly to an individual service, making fast rollback easy to achieve. Unlike a monolithic application, small change requires the whole application to be deployed. This makes deployments end up happening infrequently.

#### Organizational Alignment

Microservices help us minimize the number of people working on one codebase which improves productivity. As smaller teams working on smaller codebases is more productive.

#### Composability

With microservices, we allow for our functionality to be reused in different ways for different purposes. This can be especially important when we think about how our consumers use our software. 

#### Optimizing for Replaceability

With our individual services being small in size, the cost to replace them with a better implementation, or even delete them altogether, is much easier to manage. While it's a costly job to rewrite or delete a big service in a monolithic system.

### What About Service-Oriented Architecture?

Service-oriented architecture (SOA) is a design approach where multiple services collaborate to provide some end set of capabilities. A service here typically means a completely separate operating system process. Communication between these services occurs via calls across a network rather than method calls within a process boundary.

It aims to promote the reusability of software and make it easier to maintain or rewrite software. <ins>The microservices is a specific approach to do SOA well.</ins>

### Other Decompositional Techniques

#### Shared Libraries

A standard decompositional technique is breaking down a codebase into multiple libraries. Libraries give you a way to share functionality between teams and services.

But there are some drawbacks. You lose technology heterogeneity, the ease with scaling, and your ability to deploy changes in isolation.

#### Modules

Some languages provide their own modular decomposition techniques that go beyond simple libraries. They allow some lifecycle management of the modules, such that they can be deployed into a running process, allowing you to make changes
without taking the whole process down.

But within a process boundary, it is also much easier to fall into the trap of making modules overly coupled to each other. So we still have the same shortcomings as we do with normal shared libraries. 

### No Silver Bullet

Microservices are no silver bullet. They have all the associated complexities of distributed systems. Every system is different. A number of factors will play into whether or not microservices are right for you, and how aggressive you can be in adopting them.
