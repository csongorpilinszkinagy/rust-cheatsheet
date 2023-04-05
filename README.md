# Rust cheatsheet

## How to learn Rust

**GitHub Repo of the YouTube channel No Boilerplate**

https://github.com/0atman/noboilerplate

**Rust website**

https://rustup.rs

**Rustlings GitHub repo**

https://github.com/rust-lang/rustlings

**Install Rustlings on Mac**

```zsh
curl -L https://raw.githubusercontent.com/rust-lang/rustlings/main/install.sh | bash
```

**Start Rustlings excersises**

```zsh
cd rustlings
rustlings
rusltings watch
```

## Main differences coming from Python

1. [Example code](#example-code)
1. [Performance](#performance)
1. [Memory Safety](#memory-safety)
1. [Concurrency](#concurrency)
1. [Interoperability](#interoperability)
1. [Ecosystem](#ecosystem)
1. [Community](#community)

### Example code

Fibonacci example in Python

```python
def fibonacci(n: int) -> int:
    if n <= 1:
        return n
    return fibonacci(n - 1) + fibonacci(n - 2)
```

Fibonacci example in Rust

```rust
fn fibonacci(n: u32) -> u32 {
    match n {
        0 => 0,
        1 => 1,
        _ => fibonacci(n - 1) + fibonacci(n - 2),
    }
}
```

### Performance

Rust is a compiled language, which means it generally offers better performance than interpreted languages like Python. The Rust compiler optimizes your code, making it run faster and use less memory. This is particularly useful for CPU-bound tasks and projects that require high-performance computing. Python runs at almost 80x slower than C while Rust maintains speed by running only 10% slower. It sometimes compiles to the same as C would. All while still being a high level language.

### Memory safety

Rust's memory safety guarantees are one of its most significant advantages over Python. By design, Rust eliminates many common programming errors like null pointer dereferences, buffer overflows, and data races. This makes your code more secure and reliable.

### Concurrency

Concurrency is another area where Rust shines. Rust's ownership system and borrowing rules allow you to write concurrent code without the need for a garbage collector, resulting in efficient and safe multithreading. The borrowing system may be the most difficult to get used to coming from Python. In comparison, Python's Global Interpreter Lock (GIL) often becomes a bottleneck for concurrent tasks.

### Interoperability

Rust has excellent support for C-compatible FFI (Foreign Function Interface), making it easy to integrate with existing C and C++ codebases. This feature also allows you to write performance-critical parts of your Python applications in Rust, leveraging its speed and safety benefits.

### Ecosystem

The Rust ecosystem is growing rapidly, with an extensive collection of libraries and packages available through the Cargo package manager. While Python's ecosystem is still more extensive, Rust's is quickly catching up, and the quality of the available libraries is impressive.

### Community

The Rust community is welcoming and supportive, making it easy to learn the language and get help when needed. The Rust programming language's official documentation is comprehensive and easy to follow, and there are numerous tutorials, articles, and forums to assist you throughout your journey.

## Insights from the Rust book

### Introduction

Contermporary development tools:
* Cargo: the included dependency manager and build tool
* Rustfmt: formatting tool
* Rust Language Server: IDE integration for code completion and inline error messages

### Getting started

#### Installation

Install Rust on Mac
```zsh
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
```

Check installation
```zsh
rustc --version
```

Updating Rust on Mac
```zsh
rustup update
```
