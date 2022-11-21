# blockBot

<a href="https://ibb.co/JymTJHW"><img src="https://i.ibb.co/WPGXJfN/2.png" alt="2" border="0"></a>

Per their official definition balena-blocks are “intelligent, drop-in chunks of functionality built to handle the basics, allowing you to focus on solving the hard problems”.

blockBot is an ongoing implementation of those values in hardware. The role of this project is to provide a playground for robotics prototyping that allows you to focus on developing and experimenting with your idea.

However, this is not a product, it’s more of a tamplate

blockBot doesn’t have a list of features, it has a list of values: 

**Affordable and accessible**

This is meant to be built with the simplest, most affordable and available parts and tools on the market. One should be able to build this just by ordering the components, 3D printing the needed parts, and with a minimal toolkit. A multimeter, screwdriver and soldering iron should be enough. 

**Modular to the bone**

One of the most annoying things about prototyping (at least in my experience) is having to move parts around, and redo steps you’ve already done, and modify core components just because you want to try another type of sensor for example. 

If you need to replace one component, the modifications to the other components should be minimal, even close to zero. You shouldn’t have to change the fusebox in your house, just because you got a new stereo. 

**A serious toy.** 

One thing that I absolutely love about ROS is it’s scalability. It simply grows with your solution. Let’s take the example of mapping. You can use gmapping inside a simulation on your workstation, or with a €100 sensor such as the [RPLidar A1](http://www.slamtec.com/en/lidar/a1), or with a €7K professional unit like [this one](https://www.robotshop.com/eu/en/m8-1-plus-lidar-sensor-sw-sdk.html). The software stack remains mainly unchanged, apart from some minor differences in  configuration.

Build your awesome software stack using this, and then move to a more professional hardware implementation as you grow. Balena is here to help you trough the whole journey, from early protoypes to mass deployment. 

**Open-source**

You added a LIDAR sensor to your robot? Great, publish your code together with the CAD files of the part needed to mount it to so that others can build on top of that. 

And this answers a question you probably have by now. Why build yet another maker robot platform ? Because nothing on the market comes close to offering this.

Ok, enough rambling, let’s get to the fun part, the implementation of these ideas. 

# The brick system


# Bill of Materials 
| Part 	| Seeed SKU 	| Units 	| Unit Price 	| Total Price 	|
|---	|---	|---	|---	|---	|
| [Mini Gear Motor](https://www.seeedstudio.com/Gear-reduction-motor-p12-6V-60RPM-p-236.html) 	| 08100005 	| 2 	| 9.00 	| 18.00 	|
| [Wheels](https://www.seeedstudio.com/Motor-Wheel-p-4121.html) 	| 114090042 	| 2 	| 2.00 	| 4.00 	|
| [Power Regulator](https://www.seeedstudio.com/Adjustable-Step-Down-DC-DC-Converter-0-8V-18V-3-p-1716.html) 	| 106990005 	| 1 	| 4.50 	| 4.50 	|
| [Battery Holder](https://www.seeedstudio.com/18650-Battery-Holder-Case-2-Slot-with-Switch-p-4160.html) 	| 114090053 	| 1 	| 1.49 	| 1.49 	|
| [Grove - I2C Motor Driver (TB6612FNG)](https://www.seeedstudio.com/Grove-I2C-Motor-Driver-TB6612FNG-p-3220.html) 	| 108020103 	| 1 	| 10.98 	| 10.98 	|
| [Grove - Base Hat for RPi](https://www.seeedstudio.com/Grove-Base-Hat-for-Raspberry-Pi.html?queryID=a34c5fca64bbabe1fc11727c46c018d9&objectID=31&indexName=bazaar_retailer_products) 	| 103030275 	| 1 	| 9.99 	| 9.99 	|
| [Grove - Ultrasonic Distance Sensor](https://www.seeedstudio.com/Grove-Ultrasonic-Distance-Sensor.html?queryID=e862ca0995704ebf10982cf813a90666&objectID=2281&indexName=bazaar_retailer_products) 	| 101020010 	| 3 	| 3.95 	| 11.85 	|
| [Grove IMU 9DOF v2.0 - MPU-9250](https://www.seeedstudio.com/Grove-IMU-9DOF-v2-0.html) 	| 101020080 	| 1 	| 14.20 	| 14.20 	|
| [Raspberry Pi Camera](https://www.seeedstudio.com/Raspberry-Pi-Camera-Module-V2.html) 	| 113990214 	| 1 	| 29.95 	| 29.95 	|
|  	|  	|  	|  	| 104.96 	|

# Electronics

