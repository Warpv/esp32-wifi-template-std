# esp32-wifi-template-std


## Installation

Linux/Mac users: Make sure you have the dependencies installed,that are mentiond in the [esp-idf install guide](https://docs.espressif.com/projects/esp-idf/en/latest/esp32/get-started/linux-macos-setup.html#step-1-install-prerequisites). You **dont** need to manually install esp-idf, just its dependencies.

For detailed instructions see [Setting Up a Development Environment](https://esp-rs.github.io/book/installation/index.html) chapter of The Rust on ESP Book.

### Install Rust (with `rustup`)

If you don't have `rustup` installed yet, follow the instructions on the [rustup.rs site](https://rustup.rs)

### Install Cargo Sub-Commands

```sh
cargo install cargo-generate
cargo install ldproxy
cargo install espup
cargo install espflash
cargo install cargo-espflash # Optional
```
> **Note**
>
> If you are running macOS or Linux then `libuv` must also be installed for `espflash` and `cargo-espflash`; this is available via most popular package managers. If you are running Windows you can ignore this step.
> ```
> # macOS
> brew install libuv
> # Debian/Ubuntu/etc.
> apt-get install libuv-dev
> # Fedora
> dnf install systemd-devel
> ```
> Also, the `espflash` and `cargo-espflash` commands shown below, assume that version `2.0` or
> greater.


## Copy project

```sh
git clone https://github.com/nikoincc/esp32-wifi-template-std.git
cd <your-path-to-copyed-project>
```

## SSID setup

> **Note**
>
>in main you need to change 
>SSID and PASS to acsess
>esp32 board operates at a frequency of 2.4 GHz, so we connect to the 2.4 GHz network accordingly
>

So in "src/main.rs" change:

```rust
ssid: "YOUR_SSID"
password: "YOUR_PASS"
```

## Build

```sh
cargo build
```

## Flash

connect to your esp32

In the root of the project:

```sh
cargo espflash flash --release --monitor
```
- The `--monitor` argument for the `espflash` command to open a serial monitor after flashing the device.
- For more details on [`espflash` usage see the README](https://github.com/esp-rs/espflash/tree/main/espflash#usage)


## Additional information

For more information, check out:
* The [Rust on ESP Book](https://esp-rs.github.io/book/)
* The [ESP STD Embedded Training](https://github.com/esp-rs/std-training)
* The [esp-idf-hal](https://github.com/esp-rs/esp-idf-hal) project
* The [embedded-hal](https://github.com/rust-embedded/embedded-hal) project
* The [esp-idf-svc](https://github.com/esp-rs/esp-idf-svc) project
* The [embedded-svc](https://github.com/esp-rs/embedded-svc) project
* The [esp-idf-sys](https://github.com/esp-rs/esp-idf-sys) project
* The [Rust for Xtensa toolchain](https://github.com/esp-rs/rust-build)
* The [Rust-with-STD demo](https://github.com/ivmarkov/rust-esp32-std-demo) project




