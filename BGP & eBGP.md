BGP is a type of [[Exterior Gateway Protocol (EGP)]], a routing protocol used to exchange routing information **between many [[Autonomous Systems]]**. BGP is a **path vector** or an **advanced distance vector** routing protocol.

---
#### **When to use BGP and when not to use BGP**

**Use BGP** if one or more of the following conditions are present:

- **The AS allows packets to travel through it** in order to reach another AS.
- **The AS has multiple connections** to other multiple other AS's.
- **The flow of traffic entering an AS must be manipulated**. This is done based on attributes ([[Metrics]]).

**Do not use BGP** if you have one or more conditions:

- **A single connection to the internet** or another AS.
- **No concern for routing policy** or routing selection.
- **A lack of memory on your routers OR lack of processing power** for routers to handle constant BGP updates.
- **A limited understanding of route filtering** and the BGP path selection process.
- **Low Bandwidth between AS's**.

---
##### BGP Message Types
There are 4 main types of BGP Messages. These are the following:

Type 1: OPEN

This message is **used to establish a connection with peers**. **Each neighbour uses this message to identify itself** and to specify its parameters:

- **BGP Version Number:** (defaults to version 4)
- **AS Number:** **AS number of the original router**, this **determines if BGP session is EBGP or IBGP**.
- **BGP Identifier:** IP address that **identifies the neighbour using the same method as OSPF Router ID**.
- **Optional Parameter:** authentication, etc.


Type 2: KEEPALIVE

**This message is sent periodically to maintain connections with peers and verify paths held by the router**. If the router accepts the parameters specified in its neighbours open message, **it responds with a keepalive**. **Messages are sent every 60 seconds** (If the periodic timer is set to 0, no keepalive messages are sent).

Type 3: UPDATE

The UPDATE messages are in charge of **advertising feasible routes, withdrawn routes, or both**. These message **contain all the required information for BGP to construct a loop-free path through the network**.

Type 4: NOTIFICATION

---





