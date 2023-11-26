### Dependencies

```
sudo apt install cmake gcc-arm-none-eabi libnewlib-arm-none-eabi libstdc++-arm-none-eabi-newlib
```

### Building

```
git clone https://github.com/EiNSTeiN-/roadrunner-filament-sensor.git
cd roadrunner-filament-sensor
git submodule update --init --recursive
cd rp2040
mkdir build
cd build
cmake ..
make
```

Find the `.uf2` file in the `roadrunner-filament-sensor/rp2040/build` directory

### Flashing

1. Connect RP2040-Zero to computer via USB
2. Press `BOOT` and `RESET` at the same time
3. Release `RESET` and 1 second later release `BOOT`
4. A drive named `RPI-RP2` will appear
5. Copy newly built `.uf2` file to the drive to flash the new firmware.