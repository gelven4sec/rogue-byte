# Rogue byte

Demonstration of an anti-disassembly technique, weaponized to be used in Rust.

Details in my post : [here](https://gelven4sec.github.io/posts/rogue_byte/)

## Usage

```bash
cargo run               # Check that it runs
cargo build --release
```
Then observe the mess:
```bash
objdump -D -M intel target/release/rogue-byte | less
```

## Detection

I wrote a Yara rule to detect the usage of this technique:
```bash
boreal detection/rogue_byte.yar target/release/rogue-byte
```
