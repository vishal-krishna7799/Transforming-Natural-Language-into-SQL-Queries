# 🧠 Transforming Natural Language into SQL Queries using MySQL

## Abstract

Efficient data retrieval from relational databases typically requires proficiency in SQL, which can act as a significant barrier for non-technical users. This project bridges that gap by translating **natural language queries into executable SQL commands**, enabling a more intuitive and accessible method of interacting with databases. By leveraging **state-of-the-art language models**, **natural language processing (NLP) frameworks**, and **vector embeddings**, we convert plain English queries into accurate SQL statements that are executed on a MySQL database.

Our system has been tested across a variety of query types—from simple SELECT statements to complex joins and aggregations—showing **high accuracy and efficiency**. This approach significantly enhances the usability of database systems for individuals without technical expertise and opens up new opportunities for user-friendly data access.

---

## 📘 Table of Contents

- [Introduction](#introduction)
- [Technologies Used](#technologies-used)
- [Methodology](#methodology)
  - [Architecture](#architecture)
- [Dataset](#dataset)
- [Experimental Results](#experimental-results)
- [Comparison with Alternatives](#comparison-with-alternative-solutions)
- [Conclusion](#conclusion)
- [Future Work](#future-work)
- [Project Images](#project-images)
- [How to Run the Project](#how-to-run-the-project)
- [License](#license)

---

## 📌 Introduction

This project aims to simplify database interactions for non-technical users by allowing them to use **natural language** instead of writing **structured SQL queries**. It is built on modern NLP and deep learning technologies to enable seamless, reliable, and scalable database querying through intuitive interfaces. 

This initiative is especially useful for:
- Business analysts who need data without writing SQL.
- Dashboard users who want insights using everyday language.
- Developers who want to embed natural-language query systems in applications.

---

## 🛠️ Technologies Used

| Technology | Description |
|------------|-------------|
| **Google PaLM** | A cutting-edge large language model used for natural language understanding and SQL generation. |
| **LangChain** | A framework for chaining language model calls, managing prompts, and executing dynamic SQL generation pipelines. |
| **MySQL** | The relational database system used for storing and querying data. |
| **Hugging Face Transformers** | Used for generating semantic embeddings of user queries. |
| **ChromaDB** | An open-source vector database for storing and retrieving query embeddings for similarity search. |

---

## 🔍 Methodology

### 1. **Natural Language Processing**
- The user provides a plain English query.
- **Google PaLM** interprets this using pre-trained language understanding.

### 2. **Translation into SQL**
- **LangChain** takes this interpretation and constructs an appropriate SQL query using templating and parsing rules.

### 3. **Embedding for Query Context**
- **Hugging Face models** convert both natural language and SQL templates into embedding vectors.
- These embeddings are stored and compared using **ChromaDB** to improve similarity detection and accuracy.

### 4. **Execution**
- The final SQL query is executed on a **MySQL** database (Classicmodels schema), and results are returned to the user.

---

## 🏗️ Architecture

The overall architecture integrates several components in a modular and scalable fashion:

### 🔧 System Flow:

1. User inputs a natural language query.
2. Google PaLM interprets and contextualizes the input.
3. LangChain uses predefined SQL templates and embeddings.
4. Hugging Face generates query embeddings for similarity matching.
5. ChromaDB stores/query these embeddings.
6. Final SQL is generated and executed on MySQL.

### 📷 Architecture Diagram:
![Architecture](https://github.com/vishal-krishna7799/Transforming-Natural-Language-into-SQL-Queries/blob/main/Picture1.png)

> _Figure 1: Self-developed system architecture illustrating the data flow and technology stack._

---

## 🧾 Dataset

The **Classicmodels** MySQL schema is used as the target dataset. It includes tables like:

- `customers`
- `orders`
- `orderdetails`
- `products`
- `employees`
- `offices`

These tables simulate a real-world business environment, making them ideal for testing natural language query translation.

---

## 📊 Experimental Results

The system was tested across various types of queries:
- Simple SELECT statements
- Aggregation functions (SUM, AVG)
- Multi-table JOINs
- Conditional filters (WHERE, LIKE)

It performed significantly better than traditional methods in terms of:
- **Query accuracy**
- **Result relevance**
- **Response time**
- **User satisfaction**

### 📷 Output Example:
![Experimental Result](https://github.com/vishal-krishna7799/Transforming-Natural-Language-into-SQL-Queries/blob/main/Picture2.png)

> _Figure 2: Output of natural language query execution showing seamless translation and data retrieval._

---

## ⚖️ Comparison with Alternative Solutions

| Feature | Manual SQL | Existing SQL Builders | Our System |
|--------|------------|-----------------------|------------|
| Requires SQL knowledge | ✅ | ⚠️ | ❌ |
| Supports Natural Language | ❌ | ⚠️ | ✅ |
| Embedding-based Matching | ❌ | ❌ | ✅ |
| User-friendly UI | ❌ | ⚠️ | ✅ (planned) |
| LLM-Driven Accuracy | ❌ | ⚠️ | ✅ |

This system **outperforms traditional tools** by offering intelligent query understanding and removing technical barriers for database access.

---

## ✅ Conclusion

This project presents a transformative approach to interacting with relational databases using natural language. By integrating **LLMs**, **NLP frameworks**, and **vector embeddings**, we deliver a tool that enables users to query databases intuitively—**without writing a single line of SQL**.

Key benefits:
- Democratized access to data
- Improved business decision-making speed
- Scalable integration with different database systems

---

## 🔭 Future Work

- 🔤 **Multi-language support**: Add support for global languages like Spanish, Hindi, Mandarin, etc.
- 🤖 **Advanced query understanding**: Enhance support for nested queries, subqueries, and updates.
- 🗃️ **Support for more databases**: PostgreSQL, Oracle, MongoDB, etc.
- 🖥️ **Web-based UI**: Build a drag-and-drop or chatbot interface.
- 📈 **Scalability & performance**: Optimize for high-frequency queries and large datasets.

---

