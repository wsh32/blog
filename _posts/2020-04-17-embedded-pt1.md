---
layout: post
title: Embedded engineering, part 1
---

This begins my series of posts about embedded engineering, and now begins my summer of learning. This summer, I am focusing on improving my skills as an embedded engineer, both in hardware and in firmware.


My time on my school's Formula SAE team taught me lots of nuances that comes with PCB design. I did get the opportunity to design and work on the car's traction control system, which included the wheel speed sensor modules and the torque-limiting control system. I may go into more detail on this control system in another post, but to prepare myself for next year, I will be studying up on embedded hardware and firmware development.

### Learning goals

Wow, am I even an Olin student if I don't mention learning goals?

I'll do my best to track these learning goals throughout the summer. That being said, they are all flexible, and as I learn more, I expect to pick up new goals.

For now, here they are:

1. Understand AVR firmware. 
2. Understand Atmega16m1 and Atmega328p hardware design. We commonly use these two microcontrollers in Formula, so I want to build a more solid foundation. A couple of key questions I have revolves around pin allocation.
3. Understand STM32 firmware. I've had a couple of STM32 dev kits sitting on my desk for about a year without much work going into using them. 
4. Understand common serial communication protocols. I've used CAN, I2C, SPI, etc before, but I want to gain a much deeper understanding of how these work and best practices on how to design hardware around these.
5. Build up good engineering habits. Yeah.

### Project based learning

Wow, am I even an Olin student if I don't mention pRoJeCt bAsEd lEarNiNg?!?

I also have a couple of projects that I have in mind for this summer. Both of them have been on my mind for a while and went stale, but I want to bring them back with the sudden influx of free time.

![Online classes? No classes?](/images/2020-04-17/semester_over.jpg)

#### Custom Mechanical Keyboard

I've had this project on the backburner since last winter, but I've been meaning to design and build a custom modular mechanical keyboard for a while. I had some progress done last winter, but once all of the Chinese PCB manufacturers got shut down due to the COVID-19 pandemic, progress stopped. For that project, I found the STM32F042K6 chip, which had a USB peripheral. This allows it to emulate an HID device, to disguise as a keyboard and mouse. The game plan was to develop multiple parts of a keyboard that could be connected over the I2C bus, with one master node (the left half of the keyboard) connected to your computer over USB C. The modularity of the keyboard would also allow it to have addon modules-- things like a microphone addon to have noise-reactive backlighting, or a bluetooth and battery wireless addon. 

#### IoT RGB LED Controller

Next year, my roommate Jasper and I are planning ond decking out our room with RGB LED strips. One of the ways Olin is unique is with our "loft culture"-- some rooms on the fourth floor of West Hall have ceilings that are around 18 feet high. Because of this, the students who live in those rooms build lofts and make their room duplexes. One of the underrated advantages of this is that it gives you full control of the ceiling on th bottom floor, the "living room". One of the ideas I had was to cover the ceiling with RGB light panels. We also have plans to use LED strips to outline the structure of the loft, as well as backlighting furniture. Because of this, we need a way to connect the lights together to have a unified lighting experience.

The way that we are currently planning on doing this is designing a custom PCB that sits on top of a Raspberry Pi zero. The Pi zero GPIO exposes a power rail to power the Pi, as well as UART and SPI communication pins. This allows the wiring to be simplified down to one connector for power and one connector for the lighting strip. There is a considerable amount of software to write in conjunction to this, but the firmware and hardware are relatively simple and provide a good learning project.

---

I'm really looking forward to improving my skills this summer and for the next year. Both of the projects mentioned above have been on my mind for months now-- but I haven't had the time or the justification to put in the money to get them done before. Now, I do, and I'm so excited to get the ball rolling.
