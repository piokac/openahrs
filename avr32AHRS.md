The avr32 AHRS is based on the [ATNGW100 reference design board](http://www.avrfreaks.net/wiki/index.php/Documentation:NGW).
The ATNGW100 runs Linux 2.6.x and provides expansion ports used to connect to the SPI A/D converters and the accelerometer.

In the current implementation AHRS output data (roll, pitch and yaw) is sent to a host computer through a ethernet network interface by UDP packets. A serial output is also possible.

There are some pictures of the v2 prototype here: http://openahrs.wordpress.com/2009/07/16/new-boards/

# Schematics #

Schematics are uploaded through GIT. Latest version can be downloaded in PDF format [at github](http://github.com/cbecker/openahrs/raw/e1deb416d77d9c3cb12a0c027c23bc80172cf455/AHRSs/avr32/hardware/openAHRSv2.pdf).


# Sensors #

## Gyros ##

A single axis gyro LISY300AL and a IDG-500 dual-axis gyro are used to measure angular rate on each body axis. Rate output is digitalized through a MCP3208 chip (SPI 12-bit A/D converter).


## Accelerometers ##

A LIS3LV02DQ 3-axis accelerometer is used to measure acceleration. The SPI interface is used to read acceleration data.

## Magnetic sensors ##

HMC1052 and HMC1051Z are used to measure magnetic field. The respective signals are digitalized through a ADS1256 A/D converter.