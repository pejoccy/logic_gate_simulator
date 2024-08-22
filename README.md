[![Build Status](https://travis-ci.org/pejoccy/logic_gate_simulator.svg?branch=master)](https://travis-ci.org/pejoccy/logic_gate_simulator)

# logic_gates

This is a logic gates simulation crate built to demonstrate writing unit tests and integration tests


## Examples

```rust
fn and(a: u8, b: u8) -> u8 {
  match (a, b) {
    (1, 1) => 1,
    _ => 0
  }
}

assert_eq!(1, and(1, 1));
assert_eq!(0, and(1, 0));
assert_eq!(0, and(0, 1));
assert_eq!(0, and(0, 0));


fn xor(a: u8, b: u8) -> u8 {
  match (a, b) {
    (1, 0) | (0, 1) => 1,
    _ => 0
  }
}

assert_eq!(0, xor(1, 1));
assert_eq!(1, xor(1, 0));
assert_eq!(1, xor(0, 1));
assert_eq!(0, xor(0, 0));
```

