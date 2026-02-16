---
layout: post
title:  "Pico-11: Winter Woes No More"
date:   2025-12-21 22:00:00 +0000
categories: balloons
---

## Introduction

Pico-11 was launched on 19/12/2025 and used the same 60-inch 'cymylar' balloon that worked well on the last flight. It also used a new tracker design that makes significant changes to the previous design.

## New Design

We fixed all the issues we had with the previous design, while also making the board significantly smaller. We did this in part by moving the GPS module to the back of the PCB. We also moved the boost converter off the main PCB and replaced it with a simple 3.3 V LDO. This gives us much more flexibility when it comes to powering the tracker.

### Tracker
![3D render](3d.png)

![Schematic](SCH_Schematic1_1-P1_2025-12-21.png)

Aside from changing some of the pins, we also added an LED. This made both debugging and the launch itself much easier, as we could tell when the tracker was working correctly and at what point it started transmitting. We added a TP4056 LiPo charging module as we hope to experiment with overnight transmissions in the future. In order to help with high inrush current, we added MOSFET gate slew-rate control.

In order to save space and simplify routing, we simply exposed pads for debugging pins. This turned out to make life difficult, and more than a few problems were caused by dodgy connections. While it does work, I will be unlikely to do this again.

### Boost module
![3 panel boost module](SCH_Schematic3_1-P1_2025-12-21.png)

This module is designed to work with 3 individual panels which are mounted vertically. It uses ideal diodes in an OR-ing configuration.

We also designed a single PCB holder for a horizontal 4-panel configuration. This is only really useful in the summer and aims to keep the payload as light as possible.

![Solar PCB](solar_pcb.png)
![Scales](scales.jpg)

## Balloon details
We used a 3-panel vertical configuration, designed to work at solar angles as low as 0°. We mounted 4 × 0.5 V solar cells to styrofoam boards and glued them together to form a prism. We used Kapton tape to attach the panels, as we found that superglue seemed to damage the surface of the panels.

The payload ended up weighing 16.8 g and we used 5.1 g of free lift. We sealed the nozzle with superglue.

We decided to try the 17 m amateur band this time, as 20 m is relatively congested with balloons and we've had coverage issues with 10 m before.

## Launch Day
The sky was relatively clear with some small patches of cloud. There were periods of gusty wind, but otherwise it was reasonably calm. The tracker powered up quickly and the LED made it easy to see that it was working correctly.

![The payload before launch](payload.jpg)

The launch went smoothly and the balloon rose steadily. It carried on transmitting until the solar angle was 2° - a significant improvement. Unfortunately, this was before it reached float altitude.

![The balloon at launch](balloon.jpg)

The following day, the tracker started up with a 0° solar angle. The float altitude was 11.7 km. Unfortunately, it quickly became apparent that it was suffering from GPS spoofing over Russia, and we got very little data over the following hours.

The tracker has continued to operate reliably at low solar angles and has transmitted at latitudes that would not have been possible with the previous design.

Ironically, predictions show that the balloon will now drift south, where low solar angles are less of a problem.

## Update 03/01/26

After 14 days in the air, the balloon has completed it's first lap. It works consistently at low solar angles. Sometimes, at the start of the day, transmissions are intermittent. We believe this is due to poor GPS performance at low temperatures, similar to what happened in Pico-3.

## Update 16/02/26

After 57 days and almost 5 laps, Pico-11 seems to have gone down. It's unclear what the cause of failure was.

## Next steps

The current tracker seems to work well and no immediate changes are needed. The lack of data overnight makes it difficult to determine the cause of failure as this is when balloons are most likely to go down. Night time transmission would fix this issue, although it adds a whole other set of challenges.

We've almost used up our current supply of hydrogen, so we're now looking into hydrogen generation.