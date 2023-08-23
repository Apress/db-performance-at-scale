# References and Additional Resources
This page provides quick access to the resources shared throughout the book, as well as additional articles, tech talks, etc. that are relevant to the topic of database performance at scale.

## Chapter 1 - A Taste of What You’re Up Against: Two Tales

## Chapter 2 - Your Project, Through the Lens of Database Performance

### Learn More
- [DynamoDB Transactions Performance Testing](https://www.alexdebrie.com/posts/dynamodb-transactions-performance/) - Alex Debrie (DeBrie Advisory) shares his assessment of how large of a performance cost is incurred with DynamoDB transactions


## Chapter 3 - Database Internals: Hardware and Operation System Interactions

### Learn More
 - [What We Need to Unlearn About Persistent Storage](https://www.p99conf.io/session/what-we-need-to-unlearn-about-persistent-storage/) - Pavel Emelyanov (ScyllaDB) talks about ways to measure the performance of modern hardware and what it all means for databases

- [Avoiding Data Hotspots at Scale](https://www.p99conf.io/session/avatar-image-avoiding-data-hotspots-at-scale/) - Konstantine Osipov (ScyllaDB) addresses the tradeoffs between hash and range-based sharding

## Chapter 4 - Database Internals: Algorithmic Optimizations

## Chapter 5 - Database Drivers

## Chapter 6 - Getting Data Closer

## Chapter 7 - Infrastructure & Deployment Models

## Chapter 8 - Topology Considerations 

### Learn More


## Chapter 9 - Benchmarking

## Chapter 10 - Monitoring

### Learn More
- [How to Monitor PostgreSQL](https://www.youtube.com/watch?v=JmKATEVYC8s) - Baron Schwartz (Percona) on how to monitor a database by understanding the difference between workload and resource monitoring—and the golden signals for each
## Chapter 11 - Admin

## Appendix A - A Brief Look at Fundamental Database Design Decisions

- [NoSQL Distilled: A Brief Guide to the Emerging World of Polyglot Persistence](https://martinfowler.com/books/nosql.html), a book by Pramod J. Sadalage and Martin Fowler
- [Designing Data-Intensive Applications](https://www.oreilly.com/library/view/designing-data-intensive-applications/9781491903063/), a book by Martin Kleppman
- [Database Internals](https://www.databass.dev/), a book by Alex Petrov 

### Learn More
- [Introduction to NoSQL](https://www.youtube.com/watch?v=qI_g07C_Q5I) - Martin Fowler's crash course on NoSQL foundations

- [Avoiding Data Hotspots at Scale](https://www.p99conf.io/session/avatar-image-avoiding-data-hotspots-at-scale/) - Konstantine Osipov (ScyllaDB) addresses the tradeoffs between hash and range-based sharding

 - [Building state-of-art LSM-tree compaction](https://www.scylladb.com/presentations/scaling-scylladb-storage-engine-with-state-of-art-compaction/) - Raphael Carvalho's (ScyllaDB) perspective on using RUM conjecture and controller theory to engineer state-of-art LSM-tree compaction

- [Scaling Raft](https://www.youtube.com/watch?v=TP17idY3VHI) - Konstantine Osipov (ScyllaDB) on the challenges of supporting hundreds of instances of the Raft protocol on a single node and how to significantly reduce the static burden on the network and disk each Raft group creates

- [Consistency Tradeoffs in Modern Distributed Database System Design](https://www.cs.umd.edu/~abadi/papers/abadi-pacelc.pdf) - Dr. Daniel Abadi (UMD) introduces the PACELC theorem: In case of network partitioning (P) in a distributed computer system, one has to choose between availability (A) and consistency (C) (as per the CAP theorem), but else (E), even when the system is running normally in the absence of partitions, one has to choose between latency (L) and consistency (C)
- [Leveraging Consistent Hashing in your Python Applications](https://www.youtube.com/watch?v=erINlrgygEk) - Alexys Jacob (Numberly) introduces consistent hashing, and the problems it solves, by walking through a practical use case in a Python application
- [You're Already Eventually Consistent](http://rustyrazorblade.com/post/2015/2015-06-02-youre-already-eventually-consistent/) - Jon Haddad (Rustyrazorblade) clears up some misconceptions about eventual consistency
- [Inconsistent Thoughts on Database Consistency](https://www.alexdebrie.com/posts/database-consistency/) - Alex Debrie (DeBrie Advisory) discusses the various definitions of the word "consistency" that are used in the distributed databases space then shares some of his issues with conversations about consistency
- [Understanding Eventual Consistency in DynamoDB](https://www.alexdebrie.com/posts/dynamodb-eventual-consistency/) - Alex Debrie (DeBrie Advisory) dispels some of the fear around eventual consistency in DynamoDB
  

## Data Modeling
Getting data modeling right is vital for database performance, but it's a massive topic that varies significantly across database models and types. We reference data modeling throughout the book, but did not feel that adding a dedicated chapter on data modeling would be feasible or adequate. Here are some recommended resources we recommend: 

- [NoSQL Distilled: A Brief Guide to the Emerging World of Polyglot Persistence](https://martinfowler.com/books/nosql.html) - A book by Pramod J. Sadalage and Martin Fowler

- [Data Modeling Concepts and Principles](https://www.youtube.com/watch?v=ukpr6VIJNxY) - Pascal Desmarets, (Hackolade) discusses the foundations of NoSQL data modeling

- [NoSQL Data Modeling 101](https://www.youtube.com/watch?v=v_Vhuovsejw) - Tzach Livatan (ScyllaDB) covers NoSQL vs SQL data modeling and how to get started with NoSQL (primary key selection, application query analysis, & more) 
 
- [Top NoSQL Data Modeling Mistakes for Performance](https://youtu.be/QIeT_LppzSg) - Felipe Cardeneti Mendes (ScyllaDB) on how to avoid the top data modeling mistakes that impact performance (access the demonstrated "bad practices" in this [GitHub repo](https://github.com/fee-mendes/masterclass-datamodeling))
- [Indexes, Filters, and Other Animals](https://www.scylladb.com/tech-talk/indexes-filters-and-other-animals/) - Piotr Sarna (Turso) on the performance impacts of global/local secondary indexes and filtering 

- [The Myth of Schema-less](http://rustyrazorblade.com/post/2014/2014-07-09-the-myth-of-schemaless/) - Jon Haddad (Rustyrazorblade) debunking the myth of schemaless databases

- [Everything you need to know about DynamoDB Partitions](https://www.alexdebrie.com/posts/dynamodb-partitions/) - Alex Debrie (DeBrie Advisory) takes a deep look at DynamoDB partitions -- what they are, why they matter, and how they should affect your data modeling
- [The What, Why, and When of Single-Table Design with DynamoDB](https://www.alexdebrie.com/posts/dynamodb-single-table/) - Alex Debrie (DeBrie Advisory) provides a deep dive on the concepts behind DynamoDB's single-table design




