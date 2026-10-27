---
title: "radxaRGBdx"
github: "https://github.com/opilitethesmartdev/radxargbdx"
description: "WS2812B array HAT, compatible with raspberry pi zero / radxa boards (zero form factor), (maybe?) with an built-in gyroscope"
created_at: "2026-10-26"
total_time: "3h 36m"
---

# October 27, 2026: Preliminary routing
<!-- fabricate:entry 1332 -->

I decided to first do this HAT before i do the power HAB and other hats, just so i get experience and a *cool* hat.
I first started with the wiring (and a *TON* of LEDs).
![](https://fabricate.hackclub-assets.com/8bf61df01e858499c11d8d74b8ecdbaf8717b54f3bfa94e9fed4361aedf8aa0c/image-png/image.png)
I still have to put the microcontroller and some sensors on it, so it's not done.
This is the layout:
![](https://fabricate.hackclub-assets.com/79269d7db85490b67c1f5eed9ce544a467e806e05e650a2c5d36eb79eb5b7e8f/image-png/image.png)
This looks pretty fine, and i seem to have enough room for the other stuff (let's see how the routing will go though).

Timelapse: https://lapse.hackclub.com/timelapse/EpcuFMJYnD2x

**Total time spent: 1h 6m**

# October 27, 2026 (entry 2): Routing work
<!-- fabricate:entry 1348 -->

So uh, i did a lot of work. I first properly routed the RGBs. I'm trying to keep the board down at 2 layers, so it's a bit finnicky. this is how it looked like:
![](https://fabricate.hackclub-assets.com/e7cda17fa845bb3ed303dfd8b9c5c284e59ecdb7322f4a62c4de31d6ad1ae791/image-png/image.png)
I then started adding some stuff:
- An ATtiny1614 for i2c->ws stuff conversion:
![](https://fabricate.hackclub-assets.com/bcb264dc8438b8abb0049340f805b7e67d942e116b73ad94f47c95a9f8434cf1/image-png/image.png)
Two converters, because it seems that neither raspberry pis nor radxas like 5v IOs:
![](https://fabricate.hackclub-assets.com/8fa684dc5d6618520ab9d3a326f8d2ebedb91e5531fec6033f7c17192c23e151/image-png/image.png)
And finally, the LGA Inertial Measurement Unit (BNO055, which i have NO clue if i can solder 🥀✌️): 
![](https://fabricate.hackclub-assets.com/742fff0adb97bafeae20c8bf6301b8524572c664cb6434b8d2d75e41eab9c4e3/image-png/image.png)
(No, it's not done, but it's late).
The routing did require some clever workarounds, because two layers really is NOT enough, but i *somehow* managed it:
![](https://fabricate.hackclub-assets.com/800c3decf9dc1e8ac99907d2c0aa6efb523f16a5a204ba70d6f12e0542cf1cee/image-png/image.png)
![](https://fabricate.hackclub-assets.com/8b5a12ad9d002975e4a0a498fc6d0eb7e1586ede06ebbd6875bb72ee3a3ac918/image-png/image.png)
(Note that i have absolutely *NO* idea how to bring those two pins over 💀😭).
anyways, i think i'll have to figure out the BNO, but then i should be fine (and somehow have to make firmware for stuff i haven't touched once in my life 💀🥀✌️)

Timelapse: https://lapse.hackclub.com/timelapse/sfsbPlbpYoME

**Total time spent: 2h 30m**
