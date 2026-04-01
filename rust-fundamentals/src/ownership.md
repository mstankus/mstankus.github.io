# Ownership and borrowing

Rust manages memory with ownership rules enforced at compile time.

```rust
fn main() {
    let s = String::from("hello");
    takes_ref(&s);
    println!("{s}");
}

fn takes_ref(s: &str) {
    println!("{s}");
}
```

Key points:

- values have owners
- moves transfer ownership
- borrowing avoids moves when shared access is enough
