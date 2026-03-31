# Short Response: SQL Basics

Answer each question below. Write in complete sentences (3–5 per answer).

---

## Question 1

What is a database? Why do we use one instead of storing data in a JavaScript array on your server?

**Your answer:**

A database is a collection of data organized in a way that is easy to retrieve. Before we used to store data in a Javascript array, however changes made to those arrays were erased once the server stopped. With a database, data is stored reliably, on either a disk or hard drive.  So if a server shut downs, crashes, or restarts, the data won’t be lost/disrupted.

## Question 2

What is a primary key? Why does every table need one?

**Your answer:**

A primary key uniquely identifies each row in a table. Every table needs a primary key so that the database knows which row you are referring to. Also, foreign keys point to primary keys, which is how relationships between tables are made. For instance, a books table can reference a specific borrower by using the borrower's primary key as a foreign key.

## Question 3

In one sentence, describe what this query does in plain English:

```sql
SELECT * FROM books WHERE genre = 'fiction' ORDER BY year DESC LIMIT 5;
```

Aim for something like: *"It returns the 5 most recently published fiction books."*

**Your answer:**

It returns the 5 most recently published fiction books.

`SELECT * FROM books`: Get all the data from books table
`WHERE genre = 'fiction'`: Get all fiction books\
`ORDER BY year DESC LIMIT 5;`: Return 5 fiction books ordered from newest to oldest


## Question 4

Why is it dangerous to run `DELETE FROM books` without a `WHERE` clause? What does it actually do?

**Your answer:**

It is dangerous to run `DELETE FROM books` because `DELETE` without a `WHERE` clause deletes every row in a table. The `WHERE` clause specifies which rows you want to delete from a table.

## Question 5

What is the difference between `ORDER BY` and `LIMIT`? Could you use one without the other? Give an example to support your answer.

**Your answer:**
`ORDER BY` sorts results by columns in either an **ascending(default)** or **descending** order, while `LIMIT` returns a specified number of rows, without sorting. You can use one without the other. For instance, `SELECT * FROM books ORDER BY year DESC` returns all books sorted from newest to oldest with no row limit.  On the other hand  
`SELECT * FROM books LIMIT 5` return the first 5 rows of books in whatever order the database uses.