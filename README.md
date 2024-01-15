# esp32-wifi-template-std


## Install 



## Copy project

```sh
git clone https://github.com/nikoincc/esp32-wifi-template-std.git
cd <your-path-to-copyed-project>
```

## Build

```sh
cargo build
```

## Flash

In the root of the project:

```sh
cargo espflash flash --release --monitor
```

- Replace `dev/ttyUSB0` above with the USB port where you've connected the board. If you do not
specify any USB port, `espflash` will print a list of the recognized USB ports for you to select
the desired port.
- Replace `<your-project-name>` with the name of the generated project
- The `--monitor` argument for the `espflash` command to open a serial monitor after flashing the device.
- For more details on [`espflash` usage see the README](https://github.com/esp-rs/espflash/tree/main/espflash#usage)

## Monitor
```sh
espflash monitor /dev/ttyUSB0
```



