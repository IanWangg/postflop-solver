# Trainer solver baseline

Based on upstream b-inary/postflop-solver commit
`9d1509fe5077d019825f833eed04b16d342dfda1`.

The solver source matches the version used by RangeLab: three explicit
borrows in `src/action_tree.rs` permit compilation on Rust 1.90 without
changing the algorithm. The standalone manifest pins bincode and
bincode_derive to 2.0.0-rc.3, matching the trainer dependency versions.
Cargo.lock records the standalone baseline dependencies.

Profile incentives have not been implemented. The upstream commit
history, attribution, and AGPL-3.0-or-later license are preserved.

Validation command: `cargo test --locked --release --features zstd`.
