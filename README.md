# rs-hello
Demo Rust hello server from Rust [`book`](https://doc.rust-lang.org/book/ch20-00-final-project-a-web-server.html).
Contains collection of Rust design patterns:
 - create OS native threads with `std::thread`;
 - thread communication with `std::sync::mpsc channel`;
 - use `Arc<Mutex<...>>` for safe share receiver end between threads (use channel as shared queue);
 - passing job closure to worker theads (use trait object type `Box<dyn FnOnce() + Send + 'static>` for it);
 - simple use Tcp Listener;
 - use `Option<...>` enum to `take()` some value from mut self reference (move `JoinHandler` value from self to `join()`);
 - use type asias;
 - impl `Drop` trait for gracefull shutdown.
