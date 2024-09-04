# Design-and-Develop-a-System-to-Tighten-Access-to-Sensitive-Information
Designing a system that simulates limiting the number of roles a user has at a given point in time.
### Imortance / Need Of the System (Background):
Let’s take a step back and discuss some important concepts behind access control.

Users with more roles increase risk to the organization. If that user’s account was compromised, the attacker would have a significant head start, so to speak. For that reason, administrators would like automation solutions to enforce the least privilege, giving users the minimal set of roles required and removing extraneous roles.

### Purpose:
The goal of this code is to design a system that limits the number of active roles that any given person has. A role gives the user access to some thing, whether it be a piece of data or an internal system. The system achieves this requirement by keeping track of the last k roles that a person has used. If a new role is used, the oldest role is removed if there are already k active roles for that person. Each role has a name and a message which contains details about its use by the person. We only need to store the last message for a role invocation.

### Runtime Complexities
We have used Big O notation, i.e. O(1), O(N), etc, to fillout the runtime complexity for the get, set and overall space used. For a refresher on Big O notation, please review [Big-O Notation Explained](https://danielmiessler.com/study/big-o-notation/)

### Note:
Each instance of the RolesCache corresponds to a single person.
