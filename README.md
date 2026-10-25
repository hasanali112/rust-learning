# 🦀 Rust Learning Flow

My personal roadmap for learning Rust, following [The Rust Programming Language](https://doc.rust-lang.org/book/) ("The Book").

## 📍 Progress

| # | Chapter | Folder | Status |
|---|---------|--------|--------|
| 1 | Getting Started (install, Hello World, Cargo) | `../hello_world` | ✅ Done |
| 2 | Programming a Guessing Game | `../guessing_game` | ✅ Done |
| 3 | Common Programming Concepts | `chapter-03` (this) | 🚧 In progress |
| 4 | Understanding Ownership | — | ⬜ Todo |
| 5 | Structs | — | ⬜ Todo |
| 6 | Enums and Pattern Matching | — | ⬜ Todo |
| 7 | Packages, Crates, and Modules | — | ⬜ Todo |
| 8 | Common Collections | — | ⬜ Todo |
| 9 | Error Handling | — | ⬜ Todo |
| 10 | Generics, Traits, and Lifetimes | — | ⬜ Todo |
| 11 | Writing Automated Tests | — | ⬜ Todo |
| 12 | I/O Project: Command Line Program (`minigrep`) | — | ⬜ Todo |
| 13 | Iterators and Closures | — | ⬜ Todo |
| 14 | More About Cargo and Crates.io | — | ⬜ Todo |
| 15 | Smart Pointers | — | ⬜ Todo |
| 16 | Fearless Concurrency | — | ⬜ Todo |
| 17 | Async and Await | — | ⬜ Todo |
| 18 | Object-Oriented Programming Features | — | ⬜ Todo |
| 19 | Patterns and Matching | — | ⬜ Todo |
| 20 | Advanced Features (unsafe, macros, advanced traits) | — | ⬜ Todo |
| 21 | Final Project: Multithreaded Web Server | — | ⬜ Todo |

---

## 🗺️ Learning Flow

```
Stage 1: Basics          Stage 2: Core Rust        Stage 3: Real Programs
──────────────────       ──────────────────        ──────────────────────
Ch 1  Setup & Cargo  ─►  Ch 4  Ownership      ─►   Ch 9  Error Handling
Ch 2  Guessing Game      Ch 5  Structs              Ch 10 Generics/Traits/Lifetimes
Ch 3  Concepts           Ch 6  Enums & match        Ch 11 Testing
                         Ch 7  Modules              Ch 12 minigrep project
                         Ch 8  Collections

Stage 4: Idiomatic Rust  Stage 5: Advanced
──────────────────────   ─────────────────
Ch 13 Iterators/Closures Ch 17 Async/Await
Ch 14 Cargo & crates.io  Ch 18 OOP in Rust
Ch 15 Smart Pointers     Ch 19 Patterns
Ch 16 Concurrency        Ch 20 Advanced Features
                         Ch 21 Web Server project
```

**Tip:** Ownership (Ch 4) is the most important topic. Take your time there before moving on.

---

## 📘 Chapter 3: Common Programming Concepts

### 3.1 Variables and Mutability
- Variables are **immutable** by default.
- Use `mut` to make a variable mutable.
- `const` must have a type and is always immutable.
- **Shadowing**: declare a new variable with the same name using `let`.

```rust
let x = 5;
let x = x + 1;          // shadowing
let mut y = 10;
y += 1;                 // mutation
const MAX_POINTS: u32 = 100_000;
```

### 3.2 Data Types
- **Scalar**: integers (`i8`..`i128`, `u8`..`u128`, `isize`, `usize`), floats (`f32`, `f64`), `bool`, `char`.
- **Compound**: tuples and arrays.

```rust
let tup: (i32, f64, u8) = (500, 6.4, 1);
let (a, b, c) = tup;    // destructuring
let first = tup.0;      // index access

let arr = [1, 2, 3, 4, 5];
let zeros = [0; 5];     // [0, 0, 0, 0, 0]
```

### 3.3 Functions
- Use `snake_case` for names.
- Parameters must have types.
- The last expression (no `;`) is the return value.

```rust
fn add(a: i32, b: i32) -> i32 {
    a + b
}
```

### 3.4 Comments
```rust
// line comment
/* block comment */
/// doc comment (for docs)
```

### 3.5 Control Flow
```rust
// if is an expression
let number = if condition { 5 } else { 6 };

// loop, with a return value
let result = loop {
    counter += 1;
    if counter == 10 { break counter * 2; }
};

// while
while n != 0 { n -= 1; }

// for over a range or collection
for i in (1..4).rev() { println!("{i}"); }
```

### ✏️ Practice Exercises
- [ ] Convert temperatures between Fahrenheit and Celsius
- [ ] Generate the nth Fibonacci number
- [ ] Print the lyrics to "The Twelve Days of Christmas" using loops

---

## 🛠️ Useful Commands

```bash
cargo new <project>     # create a new project
cargo build             # compile
cargo run               # compile and run
cargo check             # fast check, no binary
cargo test              # run tests
cargo fmt               # format code
cargo clippy            # lint
rustup update           # update Rust
rustup doc --book       # open The Book offline
```

---

## 📚 Resources

- [The Rust Book](https://doc.rust-lang.org/book/)
- [Rust by Example](https://doc.rust-lang.org/rust-by-example/)
- [Rustlings](https://github.com/rust-lang/rustlings) — small exercises
- [Standard Library Docs](https://doc.rust-lang.org/std/)
- [Exercism Rust Track](https://exercism.org/tracks/rust)
