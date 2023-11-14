# Bridge

_**Bridge** divides business logic or huge type into separate type hierarchies that can be developed independently_

Shows separation between the types of **remotes** and **devices** they control.

Remotes act as abstractions, and devices are their implementations, Thanks to common interfaces, the same remotes can work with different devices and vice versa.

The Bridge pattern allows changing or even creating new classes without touching the code of the opposite hierarchy.

## How to Run

```bash
cargo run --bin bridge
```

```
Tests with basic remote.
Remote power toggle
--------------------------------
| I'm a TV set.
| I'm enabled
| Current volume is 30%
| Current channel is 1
--------------------------------

Tests with advanced remote.
Remote: power toggle
Remote: mute
--------------------------------
| I'm a TV set.
| I'm enabled
| Current volume is 0%
| Current channel is 1
--------------------------------

Tests with basic remote.
Remote: power toggle
--------------------------------
| I'm a radio.
| I'm enabled
| Current volume is 30%
| Current channel is 1
--------------------------------

Tests with advanced remote.
Remote: power toggle
Remote: mute
--------------------------------
| I'm a radio.
| I'm enabled
| Current volume is 0%
| Current channel is 1
--------------------------------
```