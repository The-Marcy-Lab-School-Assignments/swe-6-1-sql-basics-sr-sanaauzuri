# Short Response: SQL Basics

Answer each question below. Write in complete sentences (3–5 per answer).

---

## Question 1

What is a database? Why do we use one instead of storing data in a JavaScript array on your server?

**Your answer:**

---

## Question 2

What is a primary key? Why does every table need one?

**Your answer:**

---

## Question 3

In one sentence, describe what this query does in plain English:

```sql
SELECT * FROM books WHERE genre = 'fiction' ORDER BY year DESC LIMIT 5;
```

Aim for something like: *"It returns the 5 most recently published fiction books."*

**Your answer:**

---

## Question 4

Why is it dangerous to run `DELETE FROM books` without a `WHERE` clause? What does it actually do?

**Your answer:**

---

## Question 5

What is the difference between `ORDER BY` and `LIMIT`? Could you use one without the other? Give an example to support your answer.

**Your answer:**
`ORDER BY` sorts results by columns in either an **ascending(default)** or **descending** order, while `LIMIT` returns a specified number of rows, without sorting. You can use one without the other. For instance, `SELECT * FROM books ORDER BY year DESC` returns all books sorted from oldest to newest with no row limit.  On the other hand  
`SELECT * FROM books LIMIT 5` return the first 5 rows of books in whatever order the database uses.