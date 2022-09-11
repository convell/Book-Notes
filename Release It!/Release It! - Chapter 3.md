# Chapter 3 - Stabilize Your System
## Summary
The name of this chapter is "Stabilize Your System" so this covers a lot on the idea of [[Stability]] and instability.

## Takeaways
- There are obvious costs to instability but also marketing cost to acquire that customer, and reputation.
- Robust systems are typically what "stability" refers to - users, and transactions carry on while stresses, impulses, and component failures occur.
- Find longevity bugs by setting up dev envs and running traffic against it
- Creating crumple zones in cars allow us to design safe failure modes
	- Software should utilize safe failure modes to keep failures from core functionality. Think of timeouts 
- Less tightly coupled architectures act as shock absorbers, diminishing effects of upstream errors
- Chain of failures always look improbable due to chances of all the different aspects coming together, however consider one error greatly increases the chances of encountering other errors

## Terms
| Term            | Definition                                                                           |
| --------------- | ------------------------------------------------------------------------------------ |
| Transaction     | Abstract unit of work processed by a system                                          |
| Mixed Workloads | Combination of different transaction types                                           |
| System          | Complete set of hardware, apps, and services need to process transactions            |
| Impulse         | Quick shock to the system                                                            |
| Stress          | Force applied over time                                                              |
| Strain          | How a system changes under stress                                                    |
| Failure Modes   | Cracks in the system that when under stress spread to other parts of system to break |
| Fault           | A condition that creates incorrect internal state                                    |
| Error           | Visibly incorrect behavior                                                           |
| Failure         | An unresponsive system                                                               |
|                 |                                                                                      |

## Quote's
> Poor stability carries significant real costs.

>The amazing thing is that the highly stable design usually costs the same to implement as the unstable one

>If all else fails, production becomes your longevity testing environment by default. You’ll definitely find the bugs there, but it’s not a recipe for a happy lifestyle.

>Triggering a fault opens the crack. Faults become errors, and errors provoke
failures. That’s how the cracks propagate.