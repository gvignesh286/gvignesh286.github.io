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

## Pattern Matching
```rust
let number = 3;

match number {
    1 => println!("One!"),
    2 | 3 => println!("Two or three!"),
    _ => println!("Something else!"),
}

```

## Loops
```rust
// Infinite loop
loop {
    break;
}

// While loop
let mut x = 5;
while x > 0 {
    println!("{x}");
    x -= 1;
}

// For loop
for num in 1..4 {
    println!("{num}");
}
```

# Functions & Closures 
## Functions 
```rust
fn add(a: i32, b: i32) -> i32 {
    a + b
}

```

## Closures 
```rust
let multiply = |a: i32, b: i32| a * b;
println!("{}", multiply(3, 4));
```

## Scope and Shadowing
```rust
fn main() {
    let x = 5;
    {
        let x = x + 1;
        println!("Inner x: {x}");
    }
    println!("Outer x: {x}");
}
```

# Standard Data Structures 
## Vectors
```rust
let mut v = vec![1, 2, 3];
v.push(4);
println!("{:?}", v);
```

## HashMap
```rust
use std::collections::HashMap;

let mut map = HashMap::new();
map.insert("Rust", 2015);
map.insert("C++", 1985);

```
## Strings + Splicing
```rust
let s = String::from("hello");
let greeting = &s[0..4]; // slicing
```

## Option & Result
```rust
fn divide(x: i32, y: i32) -> Option<i32> {
    if y == 0 { None } else { Some(x / y) }
}

fn get_file() -> Result<(), std::io::Error> {
    std::fs::File::open("file.txt")?;
    Ok(())
}
```

##Custom Data Types

# Structs
```rust
struct User {
    username: String,
    age: u32,
}

let user1 = User {
    username: String::from("Alice"),
    age: 30,
};
```

##Enums
```rust
enum Direction {
    Up,
    Down,
    Left,
    Right,
}

let move_dir = Direction::Left;
```

## Methods with impl
``` rust
impl User {
    fn greet(&self) {
        println!("Hello, {}!", self.username);
    }
}
```

##Language Features
# Ownership and Borrowing
``` rust
fn main() {
    let s = String::from("hello");
    takes_ownership(s);
    // println!("{}", s); // Error: value moved
}

fn takes_ownership(some_string: String) {
    println!("{}", some_string);
}
```

#References
``` rust
fn main() {
    let s1 = String::from("hello");
    let len = calculate_length(&s1);
    println!("Length: {len}");
}

fn calculate_length(s: &String) -> usize {
    s.len()
}
```

# Memory Managemen
``` rust
let b = Box::new(5);
println!("b = {}", b);
``` 







