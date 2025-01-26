# Unsafe Rust Pointer Manipulation Example

This repository demonstrates a potential issue with unsafe Rust code involving direct pointer manipulation of a vector.  Incorrectly handling raw pointers can lead to memory corruption and undefined behavior. The example showcases the problem and provides a safer alternative.

## Bug Description

The `bug.rs` file contains code that modifies a vector's data directly using a raw pointer obtained via `as_mut_ptr()`. While this works in this simple example, it's inherently unsafe and prone to errors if not handled meticulously.  The primary danger is that it bypasses Rust's memory safety guarantees. 

## Solution

The `bugSolution.rs` demonstrates a safer approach to manipulating vector elements, using standard Rust methods instead of direct pointer manipulation.  This ensures memory safety and avoids potential data corruption.
