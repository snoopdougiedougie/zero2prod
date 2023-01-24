# Zero to production

This project is based on the book
**Zero to Production in Rust**.

## Configuration

The blurb about using **lld** didn't work for me.
I ended up finding 
[Build Windows EXEs from Linux](https://bevy-cheatbook.github.io/setup/cross/linux-windows.html),
which seems to work
(task: find out which loader is used).

## Command line

To run **cargo** with **clippy** (the Rust lint tool), 
**fmt** (formats the Rust code), **test**, and **run** options
whenever anything changes:

```shell
cargo watch -x clippy -x fmt -x test -x run
```

To check code coverage, without running the unit tests:

```shell
cargo tarpaulin --ignore-tests
```

To check for security vulnerabilities:

```shell
cargo audit
```
