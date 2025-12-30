---
layout: post
title:  "Pico-8: Circumnavigation"
date:   2025-10-31 14:00:00 +0000
categories: balloons
---

## Introduction
Pico-8 was the first payload to use the new solar system on the new tracker, which uses only 4 cells compared to the 6 we normally use. In the new design, the PCB "arms" that hold the panels are soldered directly to the tracker board. This can be seen in the photo for Pico-6.

The total payload mass ended up being 8.67g, which is the lightest so far.

We used the PartyWoo 50" again as it had promising results in the Pico-7 flight.

![The payload](pico-8-scales.jpg)

## Launch day
Pico-8 was launched on 22/08/2025. While the sky was initially clear, a few clouds started to appear as we prepared the balloon. We inflated it with around 2g free lift.

The launch and ascent went smoothly and there were no issues with the cloud.

![The balloon at launch](balloon-in-flight.jpg)

## Post-Launch
The following day, the tracker did not wake up despite a high solar angle of 45°. It was unclear at first whether this was an issue with the balloon or the tracker. There were two main differences between this payload and the payload from Pico-7:
 - Only 4 solar panels compared to 6 on Pico-7
 - The reset IC (MAX809STRG) was wired to monitor VCC and reset the MCU, as opposed to monitoring VIN and resetting the boost converter on Pico-7

We could quickly eliminate the first difference as the cause since we knew the panels could provide enough power for the tracker to operate. This left the second option. Due to the lower solar voltage, we were unable to rewire the reset IC on the boards as the threshold voltage was too high, and it would have just held the boost converter permanently off. Ideally, we would have ordered a part with a lower threshold voltage.

Luckily, three days later, as we prepared to launch another balloon, we noticed that the tracker had woken up and was floating over Kyrgyzstan. It's unclear why it worked some days and not others, but if it did manage to start up, it continued to operate throughout the day.

After reaching an initial float altitude of around 11,900m, the balloon slowly stretched and reached a peak altitude of 12,840 a week into the flight. The altitude then slowly dropped until it reached around 12,000m. It's still unclear to use how the loss of altitude occurs: 
- loss of helium should slightly increase altitude until it has negative free lift, at which point the balloon descends
- vertical motion in the atmosphere and variations in pressure seem unlikely to produce these long term trends

A plausible explanation is that the balloon gains mass, either to the tracker or diffusion of atmospheric air into the balloon, although it's unclear how this would happen.

## Circumnavigation and new records
On 03/09/2025, the balloon completed its first lap of the world. Unfortunately, it didn't start up that day, or the next. Or the day after that. It wasn't until 6 days later that we were able to confirm the circumnavigation. The balloon continued to float for a total of 24 days and 45049km before disappearing off the Russian-Pacific coast.

## New tracking website
Around this time, we also starting using our own tracking website, based on the work by the developer at [wsprtv.com](https://wsprtv.com). This allowed us to process the data before displaying it, meaning we can make better use of the extended telemetry data.

[New website](https://adamlawson.uk/balloons)
