# blockBot

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

# Parts

[Untitled](https://www.notion.so/629ecc59edc243d6a4b02ef3d0db4501)

# Electronics

### Power Delivery

- **TP4056** Battery charger
- **U3V70F5** 5V Step-Up Power Regulator

### Motor Control

- **Arduino Pro Mini 8Mhz**
- **TB6612FNG** Motor Driver

# BYOB

Additionally, for a fully functional robot, you will need a SBC and a rechargeable battery.

## SBC

## Batteries

block-robot is designed to use a single 3.7V Li-Po/Li-Ion cell (or multiple balanced cells in parallel). That gives us a few different options:

### 18650 Cells

These are kind of a larger version of the AA batteries, that are rated for 3.7V. They range from 2000mAH to 3500mAh, and you can connect them in parallel as long as all batteries have been fully charged.

These batteries are often used for vapes and e-cigarettes, so if you cannot find them at a local electronics store, you might be able to find them at vape shops.

You can also find them in packs like

[these](https://shop.pimoroni.com/products/lithium-ion-battery-pack?variant=23417820487)

### LiPo Packs

**Pro tip:** USB Powerbanks tend be way cheaper than any of the options above. Plus, you can find them everywhere. Inside every power-bank there is a Li-Po cell waiting for a new life, you just need to crack that case open.