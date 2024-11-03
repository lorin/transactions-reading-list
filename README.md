# Transactions reading list

A reading list of interesting papers related to database transactions

### Principles of Transaction-Oriented Databse Recovery
Theo Haerder, Andreas Reuter, Computing Surveys, Vol. 15, No. 4, December 1983.

Introduced the concept of ACID transactions.

### A Critique of ANSI SQL Isolation Levels
Hal Berenson, Phil Bernstein, Jim Gray, Jim Melton, Elizabeth O'Neil, Patrick O'Neil, Microsoft Research Technical Report MSR-TR-95-51, June 1995.

This paper pointed out problems in the ANSI SQL definition of isolation levels. Introduces the concept of *snapshot isolation*. 

### Weak Consistency: A Generalized Theory and Optimistic Implementations for Distributed Transactions
Atul Adya, PhD dissertation, Massachusetts Institute of Technology, March 1999. 
<https://hdl.handle.net/1721.1/149899>

Builds on the Berenson et al. paper to formalize isolation levels (see Generalized Isolation Level Definitions below).

### Generalized Isolation Level Definitions
Atul Adya, Barbara Liskov, Patrick O'Neil. Proceedings of the IEEE International Conference on Data Engineering, March 2000.

This is a publication out of Adya's PhD dissertation work. It describes phenomena in terms of dependency cycles and defines the following isolation levels.

* PL-1
* PL-2
* PL-2.99
* PL-3

### Making Snapshot Isolation Serializable
Alan Fekete, Dimitrios Liarokapis, Elizabeth O'Neil, Patrick O'Neil, Dennis Shasha, ACM Transactions on Database Systems, Vol. 30, No. 2, June 2005.

Describes in detail the conditions in which a snapshot isolation execution history can be non-serializable. 

### Serializable Isolation for Snapshot Databases
Michael J. Cahill, Uwe Röhm, Alan D. Fekete, SIGMOD '08, June 2008.

Builds on the *Making Snapshot Isolation Serializable* paper to describe an algorithm for extending snapshot isolation to achieve serializability.


### Highly Available Transactions: Virtues and Limitations
Peter Bailis, Aaron Davidson, Alan Fekete, Ali Ghodsi, Joseph M. Hellerstein, Ion Stoica, Proceedings of the VLDB Endowment, Vol. 7, No. 3. 2013

One of the contributions of this paper is to provide a hierarchy of isolation levels, which is the source of the left-hand side of the diagram at <https://jepsen.io/consistency>.

### Seeing is Believing: A Client-Centric Specification of Database Isolation
Natacha Crooks, Youer Pu, Lorenzo Alvisi, Allen Clement, Proceedings of PODC '17, July 2017.
<https://dl.acm.org/doi/10.1145/3087801.3087802>

Provides an alterative formalism to transaction isolation levels, based on state.
