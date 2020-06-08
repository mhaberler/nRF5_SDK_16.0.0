# nRF5_SDK_16.0.0
Nordic nRF5 SDK with a board definition for the Sparkfun WRL-13390


branch master is a pristine checkin from nRF5_SDK_16.0.0_98a08e2.zip

branch wrl-13390 adds support for compiling on MacOS with armgcc, and flashing/debugging/erasing
with a https://github.com/blacksphere/blackmagic probe. The USB port should be automatically 
detected on MacOS - for other platforms, you might have to set BMP_PORT explicitly.

The MacOS GNU Arm Embedded Toolchain is the 9-2020-q2-update from
https://developer.arm.com/tools-and-software/open-source-software/developer-tools/gnu-toolchain/gnu-rm/downloads/9-2020-q2-update

To build and run, cd to one of the supported examples:

````
cd examples/peripheral/blinky/wrl13990/blank/armgcc
make
make erase
make gdbflash
````

````
# this example needs a soft device
cd examples/ble_peripheral/ble_app_blinky/wrl13990/s132/armgcc
make 
make erase
make gdbflash_softdevice
make gdbflash
````

to debug, run 'make gdb'.
