# Rust Undefined Behavior Example: Raw Pointer Vector Modification

This repository demonstrates a common error in Rust involving the use of raw pointers to manipulate vectors. Modifying a vector's contents through a raw pointer after potential reallocation leads to undefined behavior.

## The Problem
The `bug.rs` file contains code that attempts to directly modify a vector's elements using a raw pointer.  This is dangerous because vector reallocation can invalidate the pointer, causing a crash or unpredictable results.

## The Solution
The `bugSolution.rs` file presents a safer approach, avoiding raw pointers and leveraging Rust's safe memory management features.

## How to run
1. Clone the repo: `git clone <repo_url>`
2. Navigate to the directory: `cd <repo_name>`
3. Compile and run the buggy code: `rustc bug.rs && ./bug`
4. Compile and run the fixed code: `rustc bugSolution.rs && ./bugSolution`

Observe the difference in behavior and the importance of using safe Rust idioms when working with vectors and memory management.