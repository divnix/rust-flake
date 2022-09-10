# Standard, and Nix and Rust, oh my!

This template uses Nix to to create a sane development shell for Rust
projects, Standard for keeping your Nix code well organized, Fenix for
pulling the latest rust binaries via Nix, and Crane for building Rust
project in Nix incrementally, making quite iteration a breeze.

Rust analyzer is wired up with the proper variables for immediate use
from a terminal based editor with language server support. Need a good
one for Nix and Rust? Try Helix! 

## Bootstrap

```bash
# make a new empty project dir
mkdir my-project
cd my-project

# grab the template
nix flake init -t github:divnix/rust-flake

# do some inititialization
git init
cargo init # pass --lib for library projects
cargo build # to generate Cargo.lock
git add .
g commit -m "init"

# enter the devshell
direnv allow || nix develop
``` 