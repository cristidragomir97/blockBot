# blockBot

<img src="https://raw.githubusercontent.com/cristidragomir97/blockBot/main/images/assambled/2.png" alt="2" border="0">

Per their official definition balena-blocks are “intelligent, drop-in chunks of functionality built to handle the basics, allowing you to focus on solving the hard problems”.

blockBot is an ongoing implementation of those values in hardware. The role of this project is to provide a playground for robotics prototyping that allows you to focus on developing and experimenting with your idea.

**Affordable and accessible**

This is meant to be built with the simplest, most affordable and available parts and tools on the market. One should be able to build this just by ordering the components, 3D printing the needed parts, and with a minimal toolkit. A multimeter, screwdriver and soldering iron should be enough. 

**Modular to the bone**

One of the most annoying things about prototyping (at least in my experience) is having to move parts around, and redo steps you’ve already done, and modify core components just because you want to try another type of sensor for example. 

If you need to replace one component, the modifications to the other components should be minimal, even close to zero. You shouldn’t have to change the fusebox in your house, just because you got a new stereo. 

**A serious toy** 

One thing that I absolutely love about ROS is it’s scalability. It simply grows with your solution. Let’s take the example of mapping. You can use gmapping inside a simulation on your workstation, or with a €100 sensor such as the [RPLidar A1](http://www.slamtec.com/en/lidar/a1), or with a €7K professional unit like [this one](https://www.robotshop.com/eu/en/m8-1-plus-lidar-sensor-sw-sdk.html). The software stack remains mainly unchanged, apart from some minor differences in configuration.

Build your awesome software stack using this, and then move to a more professional hardware implementation as you grow. Balena is here to help you trough the whole journey, from early protoypes to mass deployment. 

**Open-source**

You added a LIDAR sensor to your robot? Great, publish your code together with the CAD files of the part needed to mount it to so that others can build on top of that. 

And this answers a question you probably have by now. Why build yet another maker robot platform ? Because nothing on the market comes close to offering this.

Ok, enough rambling, let’s get to the fun part, the implementation of these ideas. 

# The brick system

## Description

## Structural Bricks 

## Adapter Bricks 
| Pic 	| Name 	|
|---	|---	|
| <img src="https://raw.githubusercontent.com/cristidragomir97/blockBot/main/images/parts/electronics_rpi_mount.png" width=320> 	| Adapter for Raspberry Pi SBC 	|
| <img src="https://raw.githubusercontent.com/cristidragomir97/blockBot/main/images/parts/electronics_dual_18650_mount.png"  width=320> 	| Adapter for Dual 18650 Battery Holder 	|
| <img src="https://raw.githubusercontent.com/cristidragomir97/blockBot/main/images/parts/electronics_dual_18650_mount_with_switch.png"  width=320> 	| Adapter for Dual 18650 Battery Holder with Switch 	|
| <img src="https://raw.githubusercontent.com/cristidragomir97/blockBot/main/images/parts/electronics_breadboard_mount.png"  width=320> 	| Adapter for Half-Size Breadboard 	|
| <img src="https://raw.githubusercontent.com/cristidragomir97/blockBot/main/images/parts/electronics_i2c_motor_driver.png"  width=320> 	| Adapter for [Grove I2C Motor Driver](https://www.seeedstudio.com/Grove-I2C-Motor-Driver-TB6612FNG-p-3220.html) 	|
| <img src="https://raw.githubusercontent.com/cristidragomir97/blockBot/main/images/parts/electronics_MP1584EN_regulator_mount.png"  width=320> 	| Adapter for [Seeed Power Regulator](https://www.seeedstudio.com/Adjustable-Step-Down-DC-DC-Converter-0-8V-18V-3-p-1716.html) 	|
| <img src="https://raw.githubusercontent.com/cristidragomir97/blockBot/main/images/parts/electronics_sparkfun_scmd_dual_regulator.png"  width=320> 	| Adapter for  [Seeed Power Regulator](https://www.seeedstudio.com/Adjustable-Step-Down-DC-DC-Converter-0-8V-18V-3-p-1716.html) and [Sparkfun SCMD Motor Driver](https://www.sparkfun.com/products/15451) 	|
| <img src="https://raw.githubusercontent.com/cristidragomir97/blockBot/main/images/parts/sensors_raspicam.png"  width=320> 	| Adapter for [Raspberry Pi Camera](https://www.seeedstudio.com/Raspberry-Pi-Camera-Module-V2.html) 	|
| <img src="https://raw.githubusercontent.com/cristidragomir97/blockBot/main/images/parts/sensors_triple_ultrasound.png" width=320> 	| Adapter for Triple [Grove - Ultrasonic Distance Sensor](https://www.seeedstudio.com/Grove-Ultrasonic-Distance-Sensor.html?queryID=e862ca0995704ebf10982cf813a90666&objectID=2281&indexName=bazaar_retailer_products) 	|

## Core Bricks
| Pic 	| Name 	|
|---	|---	|
| <img src="https://raw.githubusercontent.com/cristidragomir97/blockBot/main/images/parts/block_1x1_large.png" width=240> 	| 1x1 Large Brick 	|
| <img src="https://raw.githubusercontent.com/cristidragomir97/blockBot/main/images/parts/block_1x2_large.png"  width=240> 	| 1x2 Large Brick 	|
| <img src="https://raw.githubusercontent.com/cristidragomir97/blockBot/main/images/parts/block_1x3_large.png"  width=240> 	| 1x3 Large Brick 	|
| <img src="https://raw.githubusercontent.com/cristidragomir97/blockBot/main/images/parts/block_1x4_large.png"  width=240> 	| 1x4 Large Brick 	|
| <img src="https://raw.githubusercontent.com/cristidragomir97/blockBot/main/images/parts/block_1x1_small.png" width=240> 	| 1x1 Small Brick 	|
| <img src="https://raw.githubusercontent.com/cristidragomir97/blockBot/main/images/parts/block_1x2_small.png"  width=240> 	| 1x2 Small Brick 	|
| <img src="https://raw.githubusercontent.com/cristidragomir97/blockBot/main/images/parts/block_1x3_small.png"  width=240> 	| 1x3 Small Brick 	|
| <img src="https://raw.githubusercontent.com/cristidragomir97/blockBot/main/images/parts/block_1x4_small.png"  width=240> 	| 1x4 Small Brick 	|
| <img src="https://raw.githubusercontent.com/cristidragomir97/blockBot/main/images/parts/block_2x2_large.png"  width=240> 	| 2x2 Large Brick 	|
| <img src="https://raw.githubusercontent.com/cristidragomir97/blockBot/main/images/parts/block_2x3_large.png"  width=240> 	| 2x3 Large Brick 	|
| <img src="https://raw.githubusercontent.com/cristidragomir97/blockBot/main/images/parts/block_2x4_large.png"  width=240> 	| 2x4 Large Brick 	|
| <img src="https://raw.githubusercontent.com/cristidragomir97/blockBot/main/images/parts/block_2x2_small.png"  width=240> 	| 2x2 Small Brick 	|
| <img src="https://raw.githubusercontent.com/cristidragomir97/blockBot/main/images/parts/block_2x3_small.png"  width=240> 	| 2x3 Small Brick 	|
| <img src="https://raw.githubusercontent.com/cristidragomir97/blockBot/main/images/parts/block_2x4_small.png"  width=240> 	| 2x4 Small Brick 	|

You can find the dwg files 

# Bill of Materials 
|  	| Part 	| Vendor 	| SKU 	| Units 	| Unit Price 	| Total Price 	|
|---	|---	|---	|---	|---	|---	|---	|
| <img src="https://raw.githubusercontent.com/cristidragomir97/blockBot/main/images/components/motor.png"  height=120> 	| [Mini Gear Motor](https://www.seeedstudio.com/Gear-reduction-motor-p12-6V-60RPM-p-236.html) 	| Seeed 	| 08100005 	| 2 	| 9.00 	| 18.00 	|
| <img src="https://raw.githubusercontent.com/cristidragomir97/blockBot/main/images/components/roata.png" height=120> 	| [Wheels](https://www.seeedstudio.com/Motor-Wheel-p-4121.html) 	| Seeed 	| 114090042 	| 2 	| 2.00 	| 4.00 	|
| <img src="https://raw.githubusercontent.com/cristidragomir97/blockBot/main/images/components/motor_driver.png" height=120> 	| [Grove - I2C Motor Driver (TB6612FNG)](https://www.seeedstudio.com/Grove-I2C-Motor-Driver-TB6612FNG-p-3220.html) 	| Seeed 	| 108020103 	| 1 	| 10.98 	| 10.98 	|
| <img src="https://raw.githubusercontent.com/cristidragomir97/blockBot/main/images/components/pihat.png" height=120> 	| [Grove - Base Hat for RPi](https://www.seeedstudio.com/Grove-Base-Hat-for-Raspberry-Pi.html?queryID=a34c5fca64bbabe1fc11727c46c018d9&objectID=31&indexName=bazaar_retailer_products) 	| Seeed 	| 103030275 	| 1 	| 9.99 	| 9.99 	|
| <img src="https://raw.githubusercontent.com/cristidragomir97/blockBot/main/images/components/regulator.png" height=120> 	| [Power Regulator](https://www.seeedstudio.com/Adjustable-Step-Down-DC-DC-Converter-0-8V-18V-3-p-1716.html) 	| Seeed 	| 106990005 	| 1 	| 4.50 	| 4.50 	|
| <img src="https://raw.githubusercontent.com/cristidragomir97/blockBot/main/images/components/battery_holder.png" height=120> 	| [Battery Holder](https://www.seeedstudio.com/18650-Battery-Holder-Case-2-Slot-with-Switch-p-4160.html) 	| Seeed 	| 114090053 	| 1 	| 1.49 	| 1.49 	|
| <img src="https://raw.githubusercontent.com/cristidragomir97/blockBot/main/images/components/ultrasound.png" height=120> 	| [Grove - Ultrasonic Distance Sensor](https://www.seeedstudio.com/Grove-Ultrasonic-Distance-Sensor.html?queryID=e862ca0995704ebf10982cf813a90666&objectID=2281&indexName=bazaar_retailer_products) 	| Seeed 	| 101020010 	| 3 	| 3.95 	| 11.85 	|
| <img src="https://raw.githubusercontent.com/cristidragomir97/blockBot/main/images/components/imu.png" height=120> 	| [IMU 9DOF v2.0 - MPU-9250](https://www.seeedstudio.com/Grove-IMU-9DOF-v2-0.html) 	| Seeed 	| 101020080 	| 1 	| 14.20 	| 14.20 	|
| <img src="https://raw.githubusercontent.com/cristidragomir97/blockBot/main/images/components/rpicam.png" height=120> 	| [Raspberry Pi Camera](https://www.seeedstudio.com/Raspberry-Pi-Camera-Module-V2.html) 	| Seeed 	| 113990214 	| 1 	| 29.95 	| 29.95 	|
| <img src="https://raw.githubusercontent.com/cristidragomir97/blockBot/main/images/components/caster.png" width=120 height=120> 	| [Ball Caster with 3/8″ Metal Ball](https://www.pololu.com/product/951) 	| Pololu 	| 951 	| 1 	| 2.49 	| 2.49 	|
|  	|  	|  	|  	|  	|  	| 107.45 	|

# Electronics

