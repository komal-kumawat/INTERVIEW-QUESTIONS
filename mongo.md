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
ans 

A **MongoDB document** is a **JSON-like data structure** stored internally in **BSON (Binary JSON)** format.
It consists of **key–value pairs** and represents a single record in a collection.

Every document contains a mandatory **`_id` field**, which uniquely identifies it.

MongoDB documents support:

* **Primitive fields** (string, number, boolean)
* **Arrays**
* **Embedded (nested) documents**
* **Different data types**

Example:

```json
{
  "_id": ObjectId("507f1f77bcf86cd799439011"),
  "name": "Komal",
  "age": 22,
  "skills": ["React", "MongoDB"],
  "address": {
    "city": "Jaipur",
    "pincode": 302001
  }
}
```

Key characteristics:

* **Schema-less**: documents in the same collection can have different fields
* **Hierarchical structure**: supports nesting and arrays
* **Flexible and scalable**: avoids complex joins

---

### **One-Line Version (If Interviewer Interrupts)**

> A MongoDB document is a BSON-based, JSON-like structure made of key-value pairs, with a unique `_id`, supporting arrays, nested documents, and flexible schemas.

---


Q.3 What is BSON ? Why is it used in mongodb document ?

Q.4 Differentiate between mongoDB and MySQL
Q.5 Explain mongoDB's replication and its importance
Q.6 What is indexing in mongoDB?
Q.7 How does sharding work in mongodb?
Q.8 Discuss the types of NoSQL databases
Q.9 what is GridFS in MongoDB?
Q.10 How does MongoDB ensure high availability?

📌 Schema Design & Relationships

Q.11 What is embedding vs referencing? When to use each?

Q.12 How do you model one-to-many relationships in MongoDB?

Q.13 How do you avoid data duplication in MongoDB?

📌 Indexing & Performance

Q.14 Types of indexes in MongoDB (single, compound, multikey, text, hashed)

Q.15 What is a compound index and when should you use it?

Q.16 How can indexes slow down performance?

Q.17 What is the explain() method?

📌 Aggregation Framework

Q.18 What is aggregation in MongoDB?

Q.19 Difference between find() and aggregate()

Q.20 Explain $match, $group, $project, $lookup

📌 Mongoose (Very Important for MERN)

Q.21 What is Mongoose?

Q.22 Difference between MongoDB and Mongoose

Q.23 What are schemas and models in Mongoose?

Q.24 What are middleware (pre & post hooks)?

Q.25 What is population in Mongoose?

📌 Transactions & Consistency

Q.26 Does MongoDB support transactions?

Q.27 What are ACID properties in MongoDB?

Q.28 What is write concern and read concern?

📌 Security & Backup

Q.29 How do you secure a MongoDB database?

Q.30 What is authentication and authorization in MongoDB?

Q.31 How do you take backup and restore in MongoDB?

🧠 Interviewer’s Favorite Scenario Questions

These are 🔥 gold questions:

Q.32 When should MongoDB NOT be used?

Q.33 How would you design a chat application schema?

Q.34 How do you handle millions of users in MongoDB?

Q.35 What happens if the primary node goes down?