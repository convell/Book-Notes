# Chapter 4 - Stability Antipatterns
## Summary
This chapter goes over different antipatterns that are known to lead to faults in software. This chapter is a deep dive into all the way things can go wrong.

## Terms
| Term            | Definition                                                      |
| --------------- | --------------------------------------------------------------- |
| Software Crisis | Demand of new software outpacing capacity of software engineers |
|                 |                                                                 |

## Takeaways
* High interactive complexity is when systems have a lot of moving parts and internal dependencies that most operators mental models are incomplete or wrong. This causes operators with the best of intentions to take actions that are ineffective or harmful. 
* Tight coupling can lead to one system failing to cause stress on other systems, leading to a total system fail.

**Integration Points
* Every integration point (DB, hosted SaaS integration, other microservices) has a high likelihood of failure. Unhandled, these integration failures can propagate to system failures.
* HTTP can be hard to enumerate all the possibilities that can be sent back to your server from other servers or even a client.
* Vendor API Libraries can be a source of issues due to having little control over the source.
* Effective counters to integration points is using a circuit breaker or making sure to functional test the system.

**Chain Reactions
* In horizontally scaled systems, each failure of a node can actually cause a chain reaction due to the increased load on the other nodes making up for the failed node.
* A cascading failure in a layer can cause a cacascading failure in the calling layer.

## Quote's
>These hidden linkages often appear obvious during the post-
mortem analysis, but are in fact devilishly difficult to anticipate.

>(We do data collection when we can, but not at the risk of
breaking an SLA.)

>In the innocent days of DARPAnet and EDUnet, that all worked beautifully
well. Pretty soon after AOL connected to the Internet, though, we discovered
the need for firewalls.