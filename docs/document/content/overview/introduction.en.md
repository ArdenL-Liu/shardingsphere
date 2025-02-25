+++
pre = "<b>1.1 </b>"
title = "What is ShardingSphere"
weight = 1
chapter = true
+++

## Definition

Apache ShardingSphere is an open source ecosystem of distributed databases, including two independent products: JDBC & Proxy.
It adopts a plugin-oriented (or plugabble) architecture and expands the original databases' features list thanks to components. 

ShardingSphere provides many enhanced features in the form of database protocol and SQL, including data sharding, access routing, data security, etc.
It supports MySQL, PostgreSQL, SQL Server, Oracle, and other data storage engines. 

The idea of the Apache ShardingSphere project is to provide an enhanced database computing service platform and then build an ecosystem around it.
The project makes full use of the computing and storage capabilities of existing databases and enhances their core capabilities thanks to plugins.
It can solve many digital transformation challenges faced by enterprises and empower them to accelerate digital applications.

ShardingSphere became an [Apache](https://apache.org/index.html#projects-list) Top-Level Project on April 16, 2020.
You are welcome to check out the mailing list and discuss via [mail](mailto:dev@shardingsphere.apache.org).

### ShardingSphere-JDBC

As the community's first product and the predecessor of Apache ShardingSphere, ShardingSphere-JDBC is a lightweight Java framework that provides additional services at Java's JDBC layer. With the client connecting directly to the database, it provides services in the form of jar and requires no extra deployment and dependence. It can be considered as an enhanced version of the JDBC driver, which is fully compatible with JDBC and all kinds of ORM frameworks.
- Applicable in any ORM framework based on JDBC, such as JPA, Hibernate, Mybatis, Spring JDBC Template, or direct use of JDBC;
- Support any third-party database connection pool, such as DBCP, C3P0, BoneCP, HikariCP;
- Support any kind of JDBC standard database: MySQL, PostgreSQL, Oracle, SQLServer and any JDBC adapted databases.

|                        | ShardingSphere-JDBC | ShardingSphere-Proxy |
| ---------------------- | ------------------- | -------------------- |
| Database               | `Any`               | MySQL/PostgreSQL     |
| Connections Count Cost | `More`              | Less                 |
| Heterogeneous language | `Java Only`         | Any                  |
| Performance            | `Low loss`          | Relatively High loss |
| Decentralization       | `Yes`               | No                   |
| Static entry           | `No`                | Yes                  |

ShardingSphere-JDBC is suitable for java applications.

### ShardingSphere-Proxy

ShardingSphere-Proxy is Apache ShardingSphere's second product.
It is a transparent database proxy, providing a database server that encapsulates database binary protocol to support heterogeneous languages. 

Currently, MySQL and PostgreSQL (compatible with PostgreSQL-based databases, such as openGauss) versions are provided.
It can use any kind of terminal (such as MySQL Command Client, MySQL Workbench, etc.) that is compatible with MySQL or PostgreSQL protocol to operate data, which is more friendly to DBAs.

- Transparent to applications, it can be used directly as MySQL/PostgreSQL;
- Applicable to any kind of client that is compatible with MySQL/PostgreSQL protocol.

|                        | ShardingSphere-JDBC | ShardingSphere-Proxy   |
| ---------------------- | ------------------- | ---------------------- |
| Database               | Any                 | `MySQL/PostgreSQL`     |
| Connections Count Cost | More                | `Less`                 |
| Heterogeneous language | Java Only           | `Any`                  |
| Performance            | Low loss            | `Relatively High loss` |
| Decentralization       | Yes                 | `No`                   |
| Static entry           | No                  | `Yes`                  |

The advantages of ShardingSphere-Proxy lie in supporting heterogeneous languages and providing operational entries for DBA.

## Positioning

- Build a standard layer & ecosystem above heterogeneous databases

Apache ShardingSphere is positioned as Database Plus and aims at building a standard layer and ecosystem above heterogeneous databases.
The project focuses on how to maximize the original database computing and storage capabilities - rather than creating a new database.
Placed above databases, ShardingSphere enhances database inter-compatibility and collaboration.

- Provide relational databases with expansions and enhancements

Apache ShardingSphere is designed to fully unlock relational databases compute and storage capabilities in distributed scenarios, instead of creating an entirely new relational database.
Relational databases still have a considerable market share today and are the cornerstone of the core system of enterprises.
It is for such reasons that we believe that we should focus on enhancing it rather than overturning it.

- Support multi access endpoint and unified management

Apache ShardingSphere is an ecosystem composed of multiple access ports.
By combining ShardingSphere-JDBC and ShardingSphere-Proxy, and using the same registry to configure sharding strategies, it can flexibly build application systems for various scenarios, enabling architects to adjust the system architecture for current businesses freely.

## Roadmap

![Roadmap](https://shardingsphere.apache.org/document/current/img/roadmap_v2.png)
