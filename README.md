# CS580 Project: Query Processing on Database Systems

## Description
This project involves implementing and evaluating various algorithms for query processing on database systems. The tasks include performing joins using hashing and Yannakakis algorithms, evaluating line join queries, and comparing results and performance with MySQL.

## Introduction
This project report covers various query processing tasks for the CS580 course at the University of Illinois Chicago. It includes implementing algorithms for join operations, evaluating their correctness and performance, and comparing them with MySQL execution.

## Problem 1: Hash-Based Join
### Task
Implement an algorithm to evaluate the join query q(A, B, C) : −R1(A, B), R2(B, C) using hashing.

### Implementation
- Define relations R1 and R2.
- Create a hashmap for R2 indexed by attribute B.
- Join R1 and R2 using the hashmap for efficient lookup.

## Problem 2: Yannakakis Algorithm
### Task
Implement the Yannakakis algorithm for evaluating line join queries efficiently.

### Implementation
- Apply a full reducer to obtain a consistent instance.
- Construct a join tree and perform post-order traversal.
- Apply bottom-up and top-down semi-join reductions.

## Problem 3: Sequential Join
### Task
Implement a simpler sequential algorithm for evaluating line join queries.

### Implementation
- Define a hash join function.
- Perform sequential joins using the hash join function.

## Problem 4: 3-Line Join Dataset and Evaluation
### Task
Create a random dataset for a 3-line join and evaluate using both the Yannakakis and sequential algorithms.

### Implementation
- Generate datasets for relations R1, R2, and R3.
- Run both algorithms and compare their performance.

## Problem 5: Large Dataset Evaluation
### Task
Evaluate the performance of the algorithms on a larger dataset.

### Implementation
- Generate a larger dataset with specified characteristics.
- Compare the execution times of both algorithms.

## Problem 6: MySQL Comparison
### Task
Run the 3-line join using MySQL and compare the results and performance with the implemented algorithms.

### SQL Query
Use the following SQL query to perform the join in MySQL:
```sql
SELECT R1.A, R1.B, R2.C, R3.D
FROM R1
JOIN R2 ON R1.B = R2.B
JOIN R3 ON R2.C = R3.C;
```
