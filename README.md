# Reading Mastering Rust Second Edition

Notes and code related to reading the book Mastering Rust, second edition, written by Rahul Sharma and Vesa Kaihlavirta.

## Daily Log

### 2022-06-03

Downloaded rust installation file for windows. Exact file was called RUSTUP-INIT.EXE (64-BIT) from [rust-lang.org](www.rust-lang.org/tools/install).

Ran the downloaded installer. Got the below message.

```txt
The Cargo home directory located at:

  C:\Users\XXX\.cargo

This can be modified with the CARGO_HOME environment variable.

The cargo, rustc, rustup and other commands will be added to
Cargo's bin directory, located at:

  C:\Users\XXX\.cargo\bin

This path will then be added to your PATH environment variable by
modifying the HKEY_CURRENT_USER/Environment/PATH registry key.

You can uninstall at any time with rustup self uninstall and
these changes will be reverted.

Current installation options:


   default host triple: x86_64-pc-windows-msvc
     default toolchain: stable (default)
               profile: default
  modify PATH variable: yes

1) Proceed with installation (default)
2) Customize installation
3) Cancel installation
```

Chose 1 to proceed with the installation. There was some downloads and then a message that Rust was installed.

Closed the current installer console window and opened another console window. Checked the Rust version and got the answer 1.61.0:

```txt
$ H:\>rustc --version
rustc 1.61.0 (fe5b13d68 2022-05-18)
```

Noted that if want to uninstall in the future so is the command for this:

```txt
rustup self uninstall
```

Tested a command to run a script that updates Rust, there were no updates available at this point in time:

```txt
rustup update
```

### 2022-06-04

Tested to create a project with Cargo, which is Rust's build system.

First checked the Cargo installation by reading out the version:

```txt
$ cargo --version
cargo 1.61.0 (a028ae42f 2022-04-29)
```

Created a new project using Cargo:

```txt
$ cargo new hello_cargo
(no output but sub-folders and code was created)
```

Built the project using Cargo:

```txt
$ cargo build
   Compiling hello_cargo v0.1.0 (C:\git_repos\reading-mastering-rust-2ed\projects\hello_cargo)
    Finished dev [unoptimized + debuginfo] target(s) in 1.23s
```

Run the created executable:

```txt
$ .\target\debug\hello_cargo.exe
Hello, world!
```

Tested secondary way to run the executable:

```txt
$ cargo run
    Finished dev [unoptimized + debuginfo] target(s) in 0.02s
     Running `target\debug\hello_cargo.exe`
Hello, world!
```

### 2022-06-05

Created a new project for the exercise from chapter 1:

```txt
cargo new word_counter   
     Created binary (application) `word_counter` package
```

### 2022-06-06

The code snippet taken from the book have errors, the goal of the word_counter exercise is to fix these errors.

First error:

```txt
failed to resolve: use of undeclared type `HashMap`
```

Imported HashMap to fix this error:

```rust
use std::collections::HashMap;
```

Added a self parameter to the increment function.

Fixed the spelling error of the variable filename.

Got some more errors and fixed these by following the instructions from the compiler.

Created a file called word_file.txt at the root of the project with the intention to run this file. Provided the argument like this:

```txt
$ cargo run word_file.txt
Finished dev [unoptimized + debuginfo] target(s) in 0.01s
     Running `target\debug\word_counter.exe word_file.txt`
Processing file: word_file.txt
counts: 1
file: 1
program: 1
counter: 1
a: 1
input: 1
to: 1
word: 2
that: 1
```

Program seems to count the words in the file correctly.
