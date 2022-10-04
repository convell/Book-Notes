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
* Tight coupling can lead to one system failing to cause stress on other systems leading to a total system fail.
* Every integration point (DB, hosted SaaS integration, other microservices) has a high likelihood of failure. Unhandled, these integration failures can propograte to system failures.

## Quote's
>These hidden linkages often appear obvious during the post-
mortem analysis, but are in fact devilishly difficult to anticipate.

>(We do data collection when we can, but not at the risk of
breaking an SLA.)

>In the innocent days of DARPAnet and EDUnet, that all worked beautifully
well. Pretty soon after AOL connected to the Internet, though, we discovered
the need for firewalls.