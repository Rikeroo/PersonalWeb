---
title: "Habit Reminder"
draft: false
---
# Introduction
PCB design has been something I’ve wanted to learn for a while now, and instead of reading extensively into the topic, I thought the best way to learn was to dive into a simple project and get my hands dirty. I thought up a fairly simple concept for a ‘habit reminder' with a configurable screen to display tasks and completion status as well as satisfying tactile buttons for when the task is completed. I hoped this would provide a more constant visual reminder of tasks I wanted to complete daily, as well as the tactile buttons giving my monkey brain a sense of gratification with each task completed. Due to working with the ESP32 for various home automation and IoT related projects, I knew its capabilities with respects to WiFi and bluetooth, as well as i2c support to drive displays, so I decided to go with it.

# Breadboard Prototyping
First, to understand which GPIO pins were available for peripherals, deduce power requirements and mockup basic firmware, a basic bread-board circuit was designed, with 3 tactile buttons, a strip of NeoPixel LED modules and an OLED display hooked up via i2c. Once I had proved everything was compatible and the project was possible, I started writing some initial code for a simple UI and began work on the PCB.

# Design of PCB for use with ESP32 DevKit
I decided that to learn the KiCad design process effectively, I would first design a PCB which uses the ESP32 DevKit itself to drive the display, LEDs and take button inputs. This would mean I wouldn't have to interface with individual ICs and their required peripherals (yet) and would mean I could learn to solve common problems before attempting a more complicated PCB with the bare ESP32 S3 Module. This proved to be the right move, as once I received and populated the board, seeing all the LEDs light up and buttons move me through the menu gave me the confidence to build a more compact and complex board.

# Compact ESP32 Module Board Design
After watching some tutorials and meditating on the lessons taught a long long time ago, in a galaxy far away in my Electrical Engineering modules in years 1 and 2 of university, I built a basic schematic, with the required peripherals for the module (mostly de-coupling capacitors). After this, I decided that I didn't want to deal with turning very small buttons on and off at very precise times, so I opted for the inclusion of a USB to UART chip for easier programming and debugging. This proved more difficult than the ESP32 itself, however once the transistors controlling the reset and programming pins on the ESP32 were all wired up it made a lot more sense. 

Transferring the schematic to a PCB layout wasn't as easy as with the DevKit board, as component placement had to much more considered, with decoupling capacitors placed near relevant ICs and layout balanced between ease of routing and ergonomic design. Eventually though, I decided on a layout I was happy with, and finished the real most important part: making the silkscreen look pretty.
