## linux下STM32开发环境
## 具体教程请见博客:

ubuntu linux下建立stm32开发环境: GCC安装以及工程Makefile建立:
http://www.embbnux.com/2014/02/01/linux_stm32_gcc_makefile/

ubuntu linux下建立stm32开发环境: 程序烧录 openocd+openjtag:
http://www.embbnux.com/2014/02/01/linux_stm32_use_openocd_openjtag/


# On Mac OS

You need some tools as follows:

* `stm32flash` </br>
Flash program for the STM32 ARM processors using the ST serial bootloader over UART or I2C
* `coreutils` </br>
Readlink
* `gcc-arm-none-eabi`

## stm32flash
install some tools that `make` need:

```
$ brew install autoconf
```

```
$ brew install automake
```

```
$ brew install pkg-config
```

Then install stm32flash:

```
$ git clone https://github.com/ARMinARM/stm32flash
$ cd stm32flash
$ make
```

## coreutils
```
$ brew install coreutils
```
## gcc-arm-none-eabi
```
$ brew install gcc-arm-none-eabi
```
## Edit file
```
$ cd stm32_development_on_linux
$ open Makefile.common
```

Change line 32:

```
TOP=$(shell greadlink -f "$(dir $(lastword $(MAKEFILE_LIST)))")

```


