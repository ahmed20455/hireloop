# ADR-001: : Database Choice – PostgreSQL (Neon) over MongoDB/Firebase

**Status:** Accepted
**Date:** 2026-07-26

## Context
The project requires storing users, products, conversations, and other related information. As the application grows, the data will have relationships between different tables, and efficient querying will become important. I also wanted to choose a database that aligns with what is commonly used in enterprise software and provides skills that transfer well to future backend roles.

## Decision
I chose PostgreSQL hosted on Neon as the primary database.

## Alternatives considered
MongoDB

MongoDB offers flexible schemas and is easy to start with. However, this project has structured and related data where relational modeling is a better fit. Handling relationships and complex queries is generally simpler and more reliable in PostgreSQL.

Firebase Firestore

Firestore provides real-time synchronization and is quick for prototypes. However, it is more tightly coupled to the Firebase ecosystem, and performing complex relational queries is less straightforward than with PostgreSQL

## Consequences
# Benefits
- Strong support for relational data using tables, foreign keys, and joins.
- Excellent query performance with indexes.
- Advanced features such as full-text search and JSONB for semi-structured data.
- Experience with PostgreSQL is highly transferable to enterprise software development and many production systems.

# Trade-offs
- Requires designing the database schema before development.
- Relational databases generally involve more planning than document databases.
- More concepts to learn initially, such as normalization and indexing.

Overall, PostgreSQL provides a strong long-term foundation for both this project and my backend engineering skills.
