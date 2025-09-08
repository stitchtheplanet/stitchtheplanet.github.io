---
layout: default
title: StitchReg - Stitch Regulator for Juki TL Machines
---
# Stitch Regulator for Juki TL Machines

This is a stitch regulator that can be used with Juki TL machines. Commercial versions of these are very expensive ($700 - $1,000 USD), but the way they work is fairly simple. You can build a DIY version using an Arduino microcontroller, an old PS/2 optical mouse, and a handful of inexpensive electronic components.

## Table of Contents
- [How It Works](#how)
- [Building One](#build)
  - [What You Need](#bom)
  - [Schematics](#schematic)
  - [Instructions](#instructions)
- [Frequently Asked Questions](./questions.html)

## How It Works <a name="how"></a>

StitchReg works by using the optical sensor from a mouse to calculate the speed of the machine/fabric and control the speed of the machine by acting as the foot pedal with a digital potentiometer.

The Juki foot pedal is basically a resistor and there are 3 states we need to care about:

- **idle** - when the foot pedal is not depressed forward or backward it sits around 140k ohms
- **thread cutter** - to trigger the thread cutter the pedal drops to around 44k ohms
- **sewing** - sewing happens, slow to fast, from around 20k ohms to around 500 ohms

## Building One For Yourself <a name="build"></a>

### What You Need <a name="bom"></a>

Currently this is just breadboarded with an Arduino Uno Rev 3. Once the design is final I'll create a PCB and enclosure.

- [PS/2 Optical Mouse](https://www.amazon.com/dp/B0DH58555P)
- [Arduino kit](https://www.amazon.com/dp/B01D8KOZF4)
- [MCP4131-104E/P](https://www.mouser.com/ProductDetail/Microchip-Technology/MCP4131-103E-P)
- [Momentary switch](https://www.amazon.com/dp/B0BR41KCDP)

The parts below are in the linked arduino kit, but I'll find better options.

- Relay (in the above arduino kit)
- 10k ohm resistor (2) (in the above arduino kit)
- 100k ohm resistor (in the above arduino kit)
- Buzzer (in the above arduino kit)
- Barrel Jack (cut the one off the battery connector in the arduino kit)

### Schematic <a name="schematic"></a>

![Schematic](./schematic.png)

### Instructions <a name="instructions"></a>

