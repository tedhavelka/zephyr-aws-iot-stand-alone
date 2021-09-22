# zephyr-aws-iot-stand-alone
Work to extend Nordic Semiconductor nrf-sdk sample app named aws_iot.


### Requirements On Build Host ###
*  about 2.5GB disk space
*  Zephyr RTOS toolchain and Nordic Semi nrf-sdk version 1.6.1
*  one of development boards **thingy91_nrf9160** or **sparkfun_thing_plus_nrf9160**


### Getting Started ###

Developers ideally clone this project into a directory dedicated to it and free of other projects and files.  Because this application is Zephyr RTOS based a couple of steps following `git clone` are needed to make ready the cloned project for further development.  The following brief download and preparation steps assume that end developer has already installed and configured [west, Nordic sdk and Nordic Semi toolchain](https://developer.nordicsemi.com/nRF_Connect_SDK/doc/latest/nrf/gs_installing.html).  With these tools and utilities in place, carry out the following steps to reach a "build ready" project point:

+  mkdir -pv ./dedicated-workspace/zz-aws-iot-stand-alone
+  cd ./dedicated-workspace/zz-aws-iot-stand-alone
+  git clone git@github.com:tedhavelka/zephyr-aws-iot-stand-alone.git .
+  west init
+  west update


### Building via west ###

To build this Zephyr based application for the development board thingy91_nrf9160 invoke `west` this way . . . note that the dollar sign is a bash or other Unix shell command prompt:

$ west build -b thingy91_nrf9160ns

To switch to an alternate board or targeted hardware and rebuild, call `west` with the new board name and `-p` to perform a *pristine build*, in other words a complete rebuild.  An example pristine build invocation of west:

$ west build -b sparkfun_thing_plus_nrf9160 -p


### Supported Boards ###

*  thingy91_nrf9160
*  sparkfun_thing_plus_nrf9160


2021-09-21 - trivial change to test 'dot ssh config' file with two github accounts - TMH


### EOF ###
