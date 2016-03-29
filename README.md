# u-boot-ocean

u-boot compiler for Ocean devices, forked off u-boot-sunxi (https://github.com/linux-sunxi/u-boot-sunxi)

## How to Compile

To compile, generate the `config.h` and then `make` the `.bin` file.

_Note_: The `config.h` file has already been created. Unless you know what you are doing, please skip this step.

To generate `config.h`, run

	# <BOARD_CONFIG> is the name of the board you are compiling u-boot
	# BlueOcean is a fork of Cubietruck, so in this case, this would be 'Cubietruck_config'
    make CROSS_COMPILE=arm-linux-gnueabihf- <BOARD_NAME>_config

This generates `include\config.h` and includes all the necessary header files.

To generate `.bin` image, run

	make CROSS_COMPILE=arm-linux-gnueabihf- -j4
