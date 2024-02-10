# References and Additional Resources
This page provides quick access to the resources shared throughout the book, as well as additional articles, tech talks, etc. that are relevant to the topic of database performance at scale.

## Chapter 1 - A Taste of What You’re Up Against: Two Tales
- [Wireshark](https://www.wireshark.org/)
- [Cassandra hashing quirk](https://github.com/apache/cassandra/blob/56ea39ec704a94b5d23cbe530548745ab2420cee/src/java/org/apache/cassandra/utils/MurmurHash.java#L31-L32)
- [Rubber duck debugging](https://rubberduckdebugging.com)
- [OpenTelemetry](https://opentelemetry.io/)
- [mdBook](https://rust-lang.github.io/mdBook/)
- [Jepsen page on Linearizability](https://jepsen.io/consistency/models/linearizable) 

## Chapter 2 - Your Project, Through the Lens of Database Performance
- [Cassandra Anti-Patterns: Queues and Queue-like Datasets](https://www.datastax.com/blog/cassandra-anti-patterns-queues-and-queue-datasets)
- [Tencent Games’ Real-Time Event-Driven Analytics System Built with ScyllaDB + Pulsar](https://www.scylladb.com/2023/05/15/tencent-games-real-time-event-driven-analytics-system-built-with-scylladb-pulsar/)
- [Using ScyllaDB for Distribution of Game Assets in Unreal Engine](https://www.youtube.com/watch?v=aEgP9YhAb08)
- [If You Care About Performance, Employ User Defined Types](https://www.scylladb.com/2017/12/07/performance-udt/)
- [How NOT to Measure Latency](https://www.youtube.com/watch?v=lJ8ydIuPFeU)
- [Misery Metrics and Consequences](https://www.p99conf.io/session/misery-metrics-consequences)
- [Performance Under Load](https://netflixtechblog.medium.com/performance-under-load-3e6fa9a60581)
- [Understanding the Scaling Behaviour of DynamoDB OnDemand Tables](https://theburningmonk.com/2019/03/understanding-the-scaling-behaviour-of-dynamodb-ondemand-tables/)
- [DynamoDB Autoscaling Dissected: When a Calculator Beats a Robot](https://www.scylladb.com/2021/07/08/dynamodb-autoscaling-dissected-when-a-calculator-beats-a-robot/)
- [Getting the Most Out of Lightweight Transactions in ScyllaDB](https://www.scylladb.com/2020/07/15/getting-the-most-out-of-lightweight-transactions-in-scylla/)
- [Amazon DynamoDB Transactions: How it Works](https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/transaction-apis.html)

### Learn More
- [DynamoDB Transactions Performance Testing](https://www.alexdebrie.com/posts/dynamodb-transactions-performance/) - Alex Debrie (DeBrie Advisory) shares his assessment of how large of a performance cost is incurred with DynamoDB transactions

## Chapter 3 - Database Internals: Hardware and Operation System Interactions
- [Exploring Phantom Traffic Jams in Your Data Flows (video)](https://www.youtube.com/watch?v=IXS_Afb6Y4o)
- [Exploring Phantom Traffic Jams in Your Data Flows (blog)](https://www.scylladb.com/2022/04/19/exploring-phantom-jams-in-your-data-flow/)
- [Diskplorer](https://github.com/scylladb/diskplorer)
- [Understanding Storage I/O Under Load](https://www.youtube.com/watch?v=Am-nXO6KK58)
- [The CPU Cost of Networking on a Host](https://people.kernel.org/dsahern/the-cpu-cost-of-networking-on-a-host)
- [DPDK (Data Plane Developers Kit)](https://www.dpdk.org/)
  
### Learn More
 - [Building Efficient I/O Intensive Applications with Seastar](https://www.youtube.com/watch?v=p8d28t4qCTY) - Avi Kivity (ScyllaDB) on the theory behind Seastar, how it is used in practice, and the advanced C++ techniques used.
 - [Different I/O Access Methods for Linux, What We Chose for ScyllaDB, and Why](https://www.youtube.com/watch?v=27Xz21RJoUA) - Avi Kivity (ScyllaDB) shares why ScyllaDB chose asynchronous direct I/O (AIO/DIO) and explains how that decision has impacted engineering efforts as well as product performance
 - [A discussion on readahead [LWN.net]](https://lwn.net/Articles/897786/) - Jake Edge's thoughts on Linux readahead prefetching from a performance standpoint 
 - [What We Need to Unlearn About Persistent Storage](https://www.p99conf.io/session/what-we-need-to-unlearn-about-persistent-storage/) - Pavel Emelyanov (ScyllaDB) talks about ways to measure the performance of modern hardware and what it all means for databases
- [How io_uring and eBPF Will Revolutionize Programming in Linux](https://www.scylladb.com/2020/05/05/how-io_uring-and-ebpf-will-revolutionize-programming-in-linux/) - Glauber Costa (Turso) shares his take on why io_uring and eBPF will completely change the way applications work with, and think about, the Linux Kernel
- [Linux Kernel vs DPDK: HTTP Performance Showdown](https://talawah.io/blog/linux-kernel-vs-dpdk-http-performance-showdown/) - Marc Richards (AWS) uses an HTTP benchmark to compare the performance of the Linux kernel networking stack with userspace networking doing kernel bypass via DPDK
- [How Application-Level Priority Management Keeps Latency Low and Throughput High](https://www.linuxfoundation.org/webinars/how-application-level-priority-management-keeps-latency-low-and-throughput-high) - Avi Kivity (ScyllaDB) on how high throughput and low latency can both be achieved in a single application by using application-level priority scheduling
- [Inside ScyllaDB’s Internal Cache](https://www.scylladb.com/2024/01/08/inside-scylladbs-internal-cache/) - Tomasz Grabiec (ScyllaDB) on why it makes sense to completely bypasses the Linux cache during reads and use a specialized ,highly efficient row-based cache instead

## Chapter 4 - Database Internals: Algorithmic Optimizations
- [Branch predictor: How many "if"s are too many? Including x86 and M1 benchmarks!](  https://blog.cloudflare.com/branch-predictor/)
- [Eytzinger Binary Search](https://algorithmica.org/en/eytzinger)
- [ScyllaDB GitHub repo](https://github.com/scylladb/scylladb)
- [Tarantool GitHub repo](https://github.com/tarantool/tarantool)

## Chapter 5 - Database Drivers
 - [PostgreSQL Frontend/Backend Protocol](https://www.postgresql.org/docs/7.3/protocol-protocol.html)
 - [DynamoDB Developer Guide on the DynamoDB API](https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/HowItWorks.API.html)
 - [gRPC](https://grpc.io)
 - [Apache Spark]( https://spark.apache.org/)
 - [Wrong data returned due to reusing stream ids of requests that timed out on the client side](https://datastax-oss.atlassian.net/browse/PYTHON-1286)
 - [ResponseFuture: do not return the stream ID on client timeout](https://github.com/scylladb/python-driver/pull/106)
 - [Stop reusing stream ids of requests that have timed out due to client-side timeout](https://github.com/datastax/python-driver/pull/1114)
 - [ScyllaDB Gossip documentation](https://docs.scylladb.com/stable/kb/gossip.html)
 -  [A Universally Unique IDentifier (UUID) URN Namespace](https://www.ietf.org/rfc/rfc4122.txt)
 -  [DataStax Murmur3Partitioner documentation](https://docs.datastax.com/en/cassandra-oss/3.x/cassandra/architecture/archPartitionerM3P.html)
 -  [Logical Clocks](https://homes.cs.washington.edu/~arvind/cs425/lectureNotes/clocks-2.pdf)
 -  [Efficient IO with io_uring](https://kernel.dk/io_uring.pdf)
 -  [Seastar documentation on Futures and Promises](https://seastar.io/futures-promises/)
 -  [PostgreSQL Drivers documentation](https://wiki.postgresql.org/wiki/List_of_drivers)

### Learn More
 - [We’re Porting Our Database Drivers to Async Rust](https://www.scylladb.com/2022/02/22/were-porting-our-database-drivers-to-async-rust/) - Piotr Sarna (ScyllaDB) explains the design decisions taken in implementing a Rust driver and unifying  unify all other ScyllaDB drivers to use Rust underneath
- [Optimizing Performance in Rust for Low-Latency Database Drivers](https://www.linuxfoundation.org/webinars/optimizing-performance-in-rust-for-low-latency-database-drivers?hsLang=en) Piotr Grabowski (ScyllaDB) on the performance gains achieved by using the Tokio framework as the backbone of a new, high-performance driver and optimizing various driver components

## Chapter 6 - Getting Data Closer
- [CVE-2021-44521](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2021-44521)
- [CVE-2021-44521: Exploiting Apache Cassandra User-Defined Functions for Remote Code Execution](https://jfrog.com/blog/cve-2021-44521-exploiting-apache-cassandra-user-defined-functions-for-remote-code-execution/)
- [Microsoft Azure documentation on the Noisy Neighbor antipattern](https://learn.microsoft.com/en-us/azure/architecture/antipatterns/noisy-neighbor/noisy-neighbor)
- [Bytecode Alliance documentation](https://wasmtime.dev)
- [Wasmtime documentation](https://docs.wasmtime.dev/api/wasmtime/struct.Store.html#method.fuel_consumed)
- [ScyllaDB documentation on ScyllaDB CQL Extensions](https://github.com/scylladb/scylladb/blob/master/docs/cql/cql-extensions.md#reducefunc-for-uda)
- [PostgreSQL documentation on User-Defined Aggregates](https://www.postgresql.org/docs/current/xaggr.html#XAGGR-MOVING-AGGREGATES)
- [Wasmtime](https://wasmtime.dev/)
- [Wasmer.io](https://wasmer.io/)
- [WasmEdge](https://wasmedge.org/)
- [V8](https://v8.dev/)
- [wapm]( https://wapm.io/)
- [WebAssembly: The Definitive Guide](https://www.oreilly.com/library/view/webassembly-the-definitive/9781492089834/)
- [Programming WebAssembly with Rust](https://pragprog.com/titles/khrust/programming-webassembly-with-rust/)
- [ScyllaDB’s Take on WebAssembly for User-Defined Functions](https://thenewstack.io/scylladbs-take-on-webassembly-for-user-defined-functions/) 

### Learn More
- [The Whole WebAssembly Enchilada](https://www.youtube.com/watch?v=J3hK7O5Oc2Y) - Brian Sletten (author of "WebAssembly: The Definitive Guide") highlights major trends and offers some suggestions about where WebAssembly is going and why now is the time to start paying attention
- [What the Heck is the Edge Anyway?](https://blog.turso.tech/what-the-heck-is-the-edge-anyway-a159a12f2412) - Glauber Costa (Turso) on why bringing compute to the edge only solves half the problem, especially if you’re making calls to a centralized database somewhere in a far away cluster
- [WebAssembly Functions for your SQLite-Compatible Database](https://blog.turso.tech/webassembly-functions-for-your-sqlite-compatible-database-7e1ad95a2aa7) - Piotr Sarna (Turso) on creating WebAssembly user-defined functions for libSQL, an open source, open contribution fork of SQLite
- [How WebAssembly is Eating the Database, One UDF At a Time](https://dylibso.com/blog/wasm-udf/) - Dominique Saulet and Steve Manuel (dylibso) on what’s driving the new wave of UDF implementations, along with some thoughts and considerations for the future
  

## Chapter 7 - Infrastructure & Deployment Models
- [How Discord Supercharges Network Disks for Extreme Low Latency](https://discord.com/blog/how-discord-supercharges-network-disks-for-extreme-low-latency)
- [Diskplorer results](https://github.com/scylladb/diskplorer#sample-results)
-  [Detecting CPU Steal Time in Guest Virtual Machines](https://opensource.com/article/20/1/cpu-steal-time)
-  [The Cost of Containerization for Your ScyllaDB Deployment](https://www.scylladb.com/2018/08/09/cost-containerization-scylla/)
- [Create a Pod that Gets Assigned a QoS Class of Guaranteed](https://kubernetes.io/docs/tasks/configure-pod-container/quality-service-pod/#create-a-pod-that-gets-assigned-a-qos-class-of-guaranteed)
- [Operator Pattern in the Kubernetes docs](https://kubernetes.io/docs/concepts/extend-kubernetes/operator/)

### Learn More
- [Top Mistakes with ScyllaDB: Intro & Infrastructure](https://www.scylladb.com/2023/04/27/top-mistakes-infrastructure/)  - Felipe Mendes applying the lessons of this chapter to a specific database, ScyllaDB.
- [Top Mistakes with ScyllaDB: Storage](https://www.scylladb.com/2023/07/17/top-mistakes-with-scylladb-storage/) - Felipe Mendes applying the storage-focused lessons of this chapter to a specific database, ScyllaDB. 

## Chapter 8 - Topology Considerations 
-  [Cassandra Production Guidelines](https://cassandra.apache.org/doc/latest/cassandra/getting_started/production.html)
-  [Heat Weighted Load Balancing](https://www.scylladb.com/2017/09/21/scylla-heat-weighted-load-balancing/)
 - [How Discord Migrated Trillions of Messages from Cassandra to ScyllaDB](https://www.youtube.com/watch?v=S2xmFOAUhsk)
 - [ShareChat’s Path to High-Performance NoSQL with ScyllaDB](https://www.youtube.com/watch?v=Y2yHv8iqigA)
- [Load Balancing in ScyllaDB’s DynamoDB-Compatible API, Alternator](https://www.scylladb.com/2021/04/13/load-balancing-in-scylla-alternator/)

## Chapter 9 - Benchmarking
- [How Optimizely (Safely) Maximizes Database Concurrency](https://www.youtube.com/watch?v=cSiVoX_nq1s)
- [YCSB](https://github.com/brianfrankcooper/YCSB)
- [TPC-C](http://tpc.org/tpcc/default5.asp)
- [NdBench](https://github.com/Netflix/ndbench)
- [Nosqlbench](https://github.com/nosqlbench/nosqlbench)
- [pgbench](https://www.postgresql.org/docs/current/pgbench.html)
- [TLP-stress](https://github.com/thelastpickle/tlp-stress)
- [Cassandra-stress](https://github.com/scylladb/scylla-tools-java/tree/master/tools/stress)
- [How NOT to Measure Latency](https://www.youtube.com/watch?v=lJ8ydIuPFeU)
- [On Coordinated Omission](https://www.scylladb.com/2021/04/22/on-coordinated-omission/)

### Learn More
- [How to Measure Latency](https://www.p99conf.io/session/how-to-measure-latency/) - Heinrich Hartmann (Zalando) shares strategies for avoiding pitfalls with collecting, aggregating and analyzing latency data for monitoring and benchmarking.
- [Solving the Issue of Mysterious Database Benchmarking Results](https://www.youtube.com/watch?v=x4ySN6L9LOQ) - Daniel Seybold (benchANT) on the unique challenges of running database benchmarks in the cloud
- [The Do's and Don'ts of Database Benchmarking](https://www.youtube.com/watch?v=HS97mZDOdsM) - Glauber Costa (ScyllaDB) outlines a  set of best practices to improve the quality of your benchmarks
- [Database Benchmarking Efficiency with OtterTune’s Andy Pavlo](https://www.youtube.com/watch?v=i-m9_JuUJ44) - Andy Pavlo (Ottertune) on  “databaseology” and optimizing databases for efficient testing
- [How to Benchmark Redis](https://www.youtube.com/watch?v=d6KPJ6aKRJI) Filipe Oliveira and
Or Shwartz (Redis) present several benchmark tools that you can use to understand how Redis (and other databases) performs in an independent, stable, and easily reproducible manner 
- [Demystifying Benchmarks: How to Use Them To Better Evaluate Databases](https://www.youtube.com/watch?v=RFKNDQa29qA) - Peter Friedenbach (Clustrix) covers different benchmarks measures, why they matter, and which ones best apply to your particular use case

  
## Chapter 10 - Monitoring
- [perf Heat Maps](https://www.brendangregg.com/blog/2014-07-01/perf-heat-maps.html)

### Learn More
- [How to Monitor PostgreSQL](https://www.youtube.com/watch?v=JmKATEVYC8s) - Baron Schwartz (Percona) on how to monitor a database by understanding the difference between workload and resource monitoring—and the golden signals for each
- [Observability Best Practices in Distributed Databases](https://youtu.be/cRf20DUDpSE) - Felipe Cardeneti Mendes (ScyllaDB) on distributed database observability, showing several real-world situations that may affect workload performance and how to diagnose them
- [Top DynamoDB Performance Metrics](https://www.datadoghq.com/blog/top-dynamodb-performance-metrics/) - Jean-Mathieu Saponaro (Datadog) on key performance metrics across requests and throttling, errors, and Global Secondary Index creation
- [Top Cassandra Performance Metrics](https://www.datadoghq.com/blog/how-to-monitor-cassandra-performance-metrics/) - John Matso (Datadog) on key performance metrics across throughput, latency, disk usage, GC, and more
  
## Chapter 11 - Admin
-  [How a Database Looks from a Disk’s Perspective](https://www.p99conf.io/session/how-a-database-looks-from-a-disks-perspective/) 

## Appendix A - A Brief Look at Fundamental Database Design Decisions

- [NoSQL Distilled: A Brief Guide to the Emerging World of Polyglot Persistence](https://martinfowler.com/books/nosql.html), a book by Pramod J. Sadalage and Martin Fowler
- [Designing Data-Intensive Applications](https://www.oreilly.com/library/view/designing-data-intensive-applications/9781491903063/), a book by Martin Kleppman
- [Database Internals](https://www.databass.dev/), a book by Alex Petrov 

### Learn More
- [Introduction to NoSQL](https://www.youtube.com/watch?v=qI_g07C_Q5I) - Martin Fowler's crash course on NoSQL foundations
- [CMU Database Group's YouTube Channel](https://www.youtube.com/@CMUDatabaseGroup) - Andy Pavlo offers free online access to his much-talked-about CMU courses, which range from intro to advanced topics
- [Avoiding Data Hotspots at Scale](https://www.p99conf.io/session/avatar-image-avoiding-data-hotspots-at-scale/) - Konstantine Osipov (ScyllaDB) addresses the tradeoffs between hash and range-based sharding

 - [Building State-of-the-Art LSM-tree compaction](https://www.scylladb.com/presentations/scaling-scylladb-storage-engine-with-state-of-art-compaction/) - Raphael Carvalho (ScyllaDB) on using RUM conjecture and controller theory to engineer state-of-art LSM-tree compaction

- [Scaling Raft](https://www.youtube.com/watch?v=TP17idY3VHI) - Konstantine Osipov (ScyllaDB) on the challenges of supporting hundreds of instances of the Raft protocol on a single node and how to significantly reduce the static burden on the network and disk each Raft group creates

- [Consistency Tradeoffs in Modern Distributed Database System Design](https://www.cs.umd.edu/~abadi/papers/abadi-pacelc.pdf) - Dr. Daniel Abadi (UMD) introduces the PACELC theorem: In case of network partitioning (P) in a distributed computer system, one has to choose between availability (A) and consistency (C) (as per the CAP theorem), but else (E), even when the system is running normally in the absence of partitions, one has to choose between latency (L) and consistency (C)
- [Leveraging Consistent Hashing in your Python Applications](https://www.youtube.com/watch?v=erINlrgygEk) - Alexys Jacob (Numberly) introduces consistent hashing, and the problems it solves, by walking through a practical use case in a Python application
- [You're Already Eventually Consistent](http://rustyrazorblade.com/post/2015/2015-06-02-youre-already-eventually-consistent/) - Jon Haddad (Rustyrazorblade) clears up some misconceptions about eventual consistency
- [Inconsistent Thoughts on Database Consistency](https://www.alexdebrie.com/posts/database-consistency/) - Alex Debrie (DeBrie Advisory) discusses the various definitions of the word "consistency" that are used in the distributed databases space then shares some of his issues with conversations about consistency
- [Understanding Eventual Consistency in DynamoDB](https://www.alexdebrie.com/posts/dynamodb-eventual-consistency/) - Alex Debrie (DeBrie Advisory) dispels some of the fear around eventual consistency in DynamoDB
  

## Data Modeling
Getting data modeling right is vital for database performance, but it's a massive topic that varies significantly across database models and types. We reference data modeling throughout the book, but did not feel that adding a dedicated chapter on data modeling would be feasible or adequate. Here are some resources that focus on the topic: 

- [NoSQL Distilled: A Brief Guide to the Emerging World of Polyglot Persistence](https://martinfowler.com/books/nosql.html) - A book by Pramod J. Sadalage and Martin Fowler

- [Data Modeling Concepts and Principles](https://www.youtube.com/watch?v=ukpr6VIJNxY) - Pascal Desmarets (Hackolade) discusses the foundations of NoSQL data modeling

- [NoSQL Data Modeling 101](https://www.youtube.com/watch?v=v_Vhuovsejw) - Tzach Livatan (ScyllaDB) covers NoSQL vs SQL data modeling and how to get started with NoSQL (primary key selection, application query analysis, & more) 
 
- [Top NoSQL Data Modeling Mistakes for Performance](https://youtu.be/QIeT_LppzSg) - Felipe Cardeneti Mendes (ScyllaDB) on how to avoid the top data modeling mistakes that impact performance (access the demonstrated "bad practices" in this [GitHub repo](https://github.com/fee-mendes/masterclass-datamodeling))
- [Indexes, Filters, and Other Animals](https://www.scylladb.com/tech-talk/indexes-filters-and-other-animals/) - Piotr Sarna (Turso) on the performance impacts of global/local secondary indexes and filtering 
- [NoSQL Data Modeling Mistakes that Ruin Performance](https://thenewstack.io/nosql-data-modeling-mistakes-that-ruin-performance/) - Felipe Cardeneti Mendes explores three of the most common ways to ruin your NoSQL database performance, along with tips on how to avoid or resolve them
- [The Myth of Schema-less](http://rustyrazorblade.com/post/2014/2014-07-09-the-myth-of-schemaless/) - Jon Haddad (Rustyrazorblade) debunking the myth of schemaless databases

- [Everything You Need to Know about DynamoDB Partitions](https://www.alexdebrie.com/posts/dynamodb-partitions/) - Alex Debrie (DeBrie Advisory) takes a deep look at DynamoDB partitions -- what they are, why they matter, and how they should affect your data modeling
- [The What, Why, and When of Single-Table Design with DynamoDB](https://www.alexdebrie.com/posts/dynamodb-single-table/) - Alex Debrie (DeBrie Advisory) provides a deep dive on the concepts behind DynamoDB's single-table design




