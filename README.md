# ccprog

This project is based on https://github.com/ps2/ccprog.

TI CC1110 GPIO-based (bitbang) programmer

Used to program cc1110 devices over GPIO lines on Raspberry Pi.

## Building

`make`

## Usage

```
Usage: ./ccprog command

 Commands supported: erase reset write read

 Command line options:
   -p DC,DD,RESET              specify wiringPi pins for debugging cc chip:
```

## Example

`./ccprog write program.hex`
`./ccprog read dump.bin`

### Wiring for Raspberry Pi

Just remember it uses wiringPi numbering, so don't enter BCM numbering here.

## What has changed

Compares to the original project, this project:

1. Adds proper delay to IO operations, so it would function correctly even on Raspberry Pi 4.
2. Use wiringPi instead of mraa.
3. Adds read out option.

## License

The original author didn't specify any license. My changes are released under either MIT or GPL, whichever applicable/ compatible with original license. Please consult original author for confirmation.