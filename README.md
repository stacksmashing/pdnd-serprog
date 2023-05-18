# pdnd-serprog

This is a very basic flashrom/serprog compatible SPI flash reader/writer for the
Pico Debug'n'Dump.

It does not require a custom version of flashrom, just drag the compiled uf2 onto your Pico and you're ready to go.

## Build Instructions

```
export  PICO_SDK_PATH=...
mkdir build
cd build
cmake
make
```

## Usage

Dump a flashchip:

```
flashrom -p serprog:dev=/dev/ttyACM0:115200 -r foo.bin
```

## License

The project is based on the spi_flash example by Raspberry Pi (Trading) Ltd. which is licensed under BSD-3-Clause.

As a lot of the code itself was heavily inspired/influenced by `stm32-vserprog` this code is licensed under GPLv3.
