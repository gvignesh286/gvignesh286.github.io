#  Rust Language Tutorial

Welcome to this Rust tutorial! This guide walks you through the core components of the Rust programming language — perfect for beginners or those coming from other languages.

---

## Table of Contents
1. [Entry Point](#entry-point)
2. [Data Types & Operations](#data-types--operations)
3. [Control Structures](#control-structures)
4. [Functions & Closures](#functions--closures)
5. [Standard Data Structures](#standard-data-structures)
6. [Custom Data Types](#custom-data-types)
7. [Unique Language Features](#unique-language-features)
8. [Memory Management](#memory-management)
9. [Conclusion & Resources](#conclusion--resources)


---

## Entry Point

Rust programs start execution at the `main()` function:

```rust
fn main() {
    println!("Hello, Rust!");
}
```
#    Data Types & Operations
## Scalar Types
```rust
let x: i32 = 42;
let y: f64 = 3.14;
let z: bool = true;
let c: char = 'R';
```
## Compound Types
```rust
let tuple: (i32, f64, u8) = (500, 6.4, 1);
let array: [i32; 3] = [1, 2, 3];
```
## Operations
```rust
let sum = 5 + 10;
let is_equal = 10 == 10;
let not = !true;
```

#   Control Structures
## Conditionals
```rust
let number = 7;

if number < 5 {
    println!("Less than five!");
} else {
    println!("Five or more!");
}
```

