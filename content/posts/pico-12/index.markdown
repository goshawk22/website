---
layout: post
title:  "Pico-12: Superpressure"
date:   2026-04-30 12:00:00 +0100
categories: balloons
---

## Introduction

Pico-12 was launched on 25/03/2026 and used the same 60-inch 'cymylar' balloon and tracker that we used on Pico-11. The aim of this flight was to measure the internal temperature and pressure of the balloon, and to see whether the superpressure behaviour we expected would show up in flight.

## Balloon details
We used a single horizontal 4-cell panel and a boost converter. The LPS22 pressure sensor was soldered directly to the tracker and a BMP280 module was connected using four 32AWG wires. The sensor assembly was then inserted up the neck of the balloon so that it could measure the internal conditions.

Both pressure sensors were covered with foam to stop direct sunlight from affecting the readings.

We used the 10m band to reduce the antenna size and, as a result, keep the I2C wiring as short as possible.

## Launch Day
The launch itself was uneventful and the balloon appeared to rise normally. Unfortunately, the tracker never started transmitting, so we did not receive any data back from the flight.

## Conclusion
It is still unclear why the tracker failed, although a bad connection somewhere seems likely. We will need to revisit this design and see whether the issue can be isolated on the bench before trying it again in the air.