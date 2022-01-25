# m10 mini dc control

This control board designed to precisely control the 9161C geared M10 mini motor with extended
shaft.

# Usage

In general you just need to connect the board to your I2C bus and power it with 5V of power (in
theory voltage regulator allows 2.5-5.5V so the motor can work on lower voltages with slower speed).

You will need to modify the `I2C_SLAVE_ADDRESS` in firmware, compile it (or use the predefined one)
and flash to the MK. After that you will be able to use as many motors as you want.

## Firmware

TODO

# Components

* 3V Micro Planetary Reducer Motor (9161C) - target motor with plastic reduction gearbox
* ATTiny 13A MMFR (DFN-10 3x3mm) - microcontroller to interface I2C and control the driver
* DRV8837C DSGR (WSON) - H-bridge driver for the motor
* MIC5365-3.3YMT-TZ (Thin MLF (MT)) - 5V to 3.3V voltage regulator to power the MK and driver logic
* QRE1113GR (100CY) - reflective object sensor to detect the motor rotation
* Various 0201 and 0402 resistors, caps and a LED

* (optional) Electrolitic capacitor to store the rest power from the motor (check driver DS)

## [3V Micro Planetary Reducer Motor (9161C)](https://www.amazon.com/dp/B07N7PY71F)

Price: $1.8 ($9 for 5pc)

### Motor specifications:

* Reduction ratio: 1:171
* Rated torque: 9.8 mN.m
* Maximum torque: 37.2 mN.m

* Rated voltage: 2.5V DC
* No-load current: 40mA
* No-load speed: 92 RPM

* Dimensions: 8x10x12mm (M10 motor)
* Planetary gearbox outer diameter: 9.9mm
* Weight: 4 grams
* Geared motor height: 19.5mm (motor + gear box)
* Output shaft: Gear with an outer diameter of 5.35mm (11 teeth)

### The following measures the motor speed under other voltages:

* Voltage: 3V
  * Current: 42mA
  * Speed: 110 RPM
* Voltage: 3.7V
  * Current: 48mA
  * Speed: 135 RPM
* Voltage: 4.2V
  * Current: 52mA
  * Speed: 154 RPM
* Voltage: 5V
  * Current: 58mA
  * Speed: 180 RPM

# How to order

Just go to your favorite PCB manufacturer and order as many boards as you want.

* [PCBWay](doc/pcbway_order.png)
