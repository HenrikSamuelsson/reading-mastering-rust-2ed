# Reading Wastering Rust Second Edition

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

Choosed 1 to proceed with the installation. There was some downloads and then a message that Rust was installed.

Closed the current installer console window and opened another console window. Checked the Rust version and got the answer 1.61.0:

```txt
H:\>rustc --version
rustc 1.61.0 (fe5b13d68 2022-05-18)
```

Noted that if want to uninstall in the future so is the command for this:

```txt
rustup self uninstall
```
