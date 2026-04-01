# Enums and pattern matching

Enums pair naturally with `match`.

```rust
enum Message {
    Quit,
    Write(String),
}

fn describe(message: Message) -> &'static str {
    match message {
        Message::Quit => "quit",
        Message::Write(_) => "write",
    }
}
```
