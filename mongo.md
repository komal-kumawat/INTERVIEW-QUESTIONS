Q.1  what is mongodb and how it is different from sql databases ?
Ans . 
### What is MongoDB?

**MongoDB** is a **NoSQL (non-relational) database**.
It stores data in a **document format** (called **BSON**, similar to JSON) instead of tables and rows.

Example MongoDB document:

```json
{
  "name": "Komal",
  "age": 22,
  "skills": ["JavaScript", "MongoDB", "React"]
}
```

So instead of rows and columns, MongoDB works with:

* **Database**
* **Collection** (like a table)
* **Document** (like a row)

---

### How MongoDB is different from SQL Databases

| Feature            | MongoDB (NoSQL)                         | SQL Databases (MySQL, PostgreSQL, Oracle) |
| ------------------ | --------------------------------------- | ----------------------------------------- |
| **Data structure** | Documents (JSON-like)                   | Tables (rows & columns)                   |
| **Schema**         | **Schema-less** (flexible)              | **Fixed schema**                          |
| **Relationships**  | References or embedded documents        | Foreign keys & joins                      |
| **Query language** | MongoDB Query Language (MQL)            | SQL                                       |
| **Scalability**    | Easy horizontal scaling                 | Mostly vertical scaling                   |
| **Transactions**   | Limited (now supported but less common) | Strong ACID transactions                  |
| **Best for**       | Big data, real-time apps                | Complex queries & relations               |

---

### Example Comparison

#### SQL (Table structure)

**Users table**

| id | name  | age |
| -- | ----- | --- |
| 1  | Komal | 22  |

#### MongoDB (Document)

```json
{
  "_id": 1,
  "name": "Komal",
  "age": 22
}
```

---

### Key Differences Explained Simply

#### 1️⃣ Schema

* **SQL**: You must define columns before inserting data
* **MongoDB**: Each document can have different fields

```json
// MongoDB allows this
{ "name": "Komal" }
{ "name": "Amit", "age": 24 }
```

---

#### 2️⃣ Relationships

* **SQL** uses **JOINs**
* **MongoDB** uses:

  * **Embedded documents** (data inside data)
  * **References** (store another document’s ID)

---

#### 3️⃣ Performance

* **MongoDB** is faster for:

  * Large data
  * Real-time apps
  * Rapid development
* **SQL** is better for:

  * Complex queries
  * Financial systems
  * Strong consistency

---

### When to Use MongoDB?

✅ Use MongoDB if:

* Data structure changes often
* You build **web apps, mobile apps**
* You need **high scalability**
* You work with **JSON data**

### When to Use SQL?

✅ Use SQL if:

* Data is highly structured
* You need **joins & transactions**
* You build **banking or enterprise apps**

---

### One-line Summary

> **MongoDB is a flexible, document-based NoSQL database, while SQL databases are structured, table-based relational systems.**


Q.2 explain the structure of mongodb document

Q.3 What is BSON ? Why is it used in mongodb document ?

Q.4 Differentiate between mongoDB and MySQL
Q.5 Explain mongoDB's replication and its importance
Q.6 What is indexing in mongoDB?
Q.7 How does sharding work in mongodb?
Q.8 Discuss the types of NoSQL databases
Q.9 what is GridFS in MongoDB?
Q.10 How does MongoDB ensure high availability?

