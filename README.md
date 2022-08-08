# What is Caching?
In computing, a cache is a high-speed data storage layer which stores a subset of data, typically transient in nature, so that future requests for that data are served up faster than is possible by accessing the data’s primary storage location. Caching allows you to efficiently reuse previously retrieved or computed data.

# How does Caching work?
The data in a cache is generally stored in fast access hardware such as RAM (Random-access memory) and may also be used in correlation with a software component. A cache's primary purpose is to increase data retrieval performance by reducing the need to access the underlying slower storage layer.

Trading off capacity for speed, a cache typically stores a subset of data transiently, in contrast to databases whose data is usually complete and durable.

# Caching Overview
### RAM and In-Memory Engines:
Due to the high request rates or IOPS (Input/Output operations per second) supported by RAM and In-Memory engines, caching results in improved data retrieval performance and reduces cost at scale. To support the same scale with traditional databases and disk-based hardware, additional resources would be required. These additional resources drive up cost and still fail to achieve the low latency performance provided by an In-Memory cache.

### Applications: 
Caches can be applied and leveraged throughout various layers of technology including Operating Systems, Networking layers including Content Delivery Networks (CDN) and DNS, web applications, and Databases. You can use caching to significantly reduce latency and improve IOPS for many read-heavy application workloads, such as Q&A portals, gaming, media sharing, and social networking. Cached information can include the results of database queries, computationally intensive calculations, API requests/responses and web artifacts such as HTML, JavaScript, and image files. Compute-intensive workloads that manipulate data sets, such as recommendation engines and high-performance computing simulations also benefit from an In-Memory data layer acting as a cache. In these applications, very large data sets must be accessed in real-time across clusters of machines that can span hundreds of nodes. Due to the speed of the underlying hardware, manipulating this data in a disk-based store is a significant bottleneck for these applications.

### Design Patterns:
In a distributed computing environment, a dedicated caching layer enables systems and applications to run independently from the cache with their own lifecycles without the risk of affecting the cache. The cache serves as a central layer that can be accessed from disparate systems with its own lifecycle and architectural topology. This is especially relevant in a system where application nodes can be dynamically scaled in and out. If the cache is resident on the same node as the application or systems utilizing it, scaling may affect the integrity of the cache. In addition, when local caches are used, they only benefit the local application consuming the data. In a distributed caching environment, the data can span multiple cache servers and be stored in a central location for the benefit of all the consumers of that data.

### Caching Best Practices: 
When implementing a cache layer, it’s important to understand the validity of the data being cached. A successful cache results in a high hit rate which means the data was present when fetched. A cache miss occurs when the data fetched was not present in the cache. Controls such as TTLs (Time to live) can be applied to expire the data accordingly. Another consideration may be whether or not the cache environment needs to be Highly Available, which can be satisfied by In-Memory engines such as Redis. In some cases, an In-Memory layer can be used as a standalone data storage layer in contrast to caching data from a primary location. In this scenario, it’s important to define an appropriate RTO (Recovery Time Objective--the time it takes to recover from an outage) and RPO (Recovery Point Objective--the last point or transaction captured in the recovery) on the data resident in the In-Memory engine to determine whether or not this is suitable. Design strategies and characteristics of different In-Memory engines can be applied to meet most RTO and RPO requirements.

## Advantages of Cache Memory
Some of the advantages of cache memory are as follows −

Cache memory is faster than main memory as it is located on the processor chip itself. Its speed is comparable to the processor registers and so frequently required data is stored in the cache memory.
The memory access time is considerably less for cache memory as it is quite fast. This leads to faster execution of any process.
The cache memory can store data temporarily as long as it is frequently required. After the use of any data has ended, it can be removed from the cache and replaced by new data from the main memory.

## Disadvantages of Cache Memory
Some of the disadvantages of cache memory are as follows −

Since the cache memory is quite fast, it is extremely useful in any computer system. However, it is also quite expensive and so is used judiciously.
The cache is memory expensive as observed from the previous point. Also, it is located directly on the processor chip. Because of these reasons, it has a limited capacity and is much smaller than main memory.



![image](https://user-images.githubusercontent.com/110393859/183361288-6328ad0b-5338-4a30-aaa4-9fbae025f8c3.png)

### Reference
https://aws.amazon.com/caching/

https://www.tutorialspoint.com/What-is-caching
