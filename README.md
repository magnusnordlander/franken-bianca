# Franken-Bianca

## Humble beginnings

Life for my Bianca started out simple. It's a Lelit Bianca V2, bought back in 2020. For a time, everything was normal, or at least mostly normal. I wasn't too keen on refilling the tank all the time, so I hooked up the Bianca to the water mains. Nothing too wild.

There was some tinkering; opening up the machine, [sniffing the bus between the LCC and the Gicar Control Board](https://github.com/magnusnordlander/lelit-bianca-protocol), but nothing too wild. The real modding started in mid-2021, when I designed a [replacement LCC PCB](https://github.com/magnusnordlander/smart-lcc), built around an Arduino RP2040 Connect. The goal was to be able to integrate the machine into my Smart Home.

For a time, that was it. There were a couple of hardware revisions of that, and I tinkered a lot with with the firmware.

I moved to a different apartment. Having gotten used to having the machine plumbed, and the new kitchen not allowing for direct plumbing, I decided to install a Flojet. 

After a few years, I also decided to redesign the LCC board, creating my own RP2040 based design.

## A descent into madness

The [Open LCC board](https://github.com/open-lcc/open-lcc-board) went through a couple of different revisions. The goals was to address some issues with the Arduino RP2040 Connect based boards. First of all, being all metal and grounded, Wi-fi reception inside the Bianca wasn't great. Secondly, the ESP32 on the Arduino RP2040 is kind of nerfed for anything but the WiFiNina firmware.

The new board still uses an RP2040, but it's now using an ESP32-S3 with an external antenna, and a lot more exposed IO and expandability. Oh, and a color LCD.

That expandability started a feature frenzy. Since it has Bluetooth, I integrated my Acaia Lunar. Using the QWIIC connector, I added additional temperature probes. When the group manometer broke, I bought a Pressensor, and integrated that. I also added taller feet, to be able to place the scale under the machine instead of on the drip tray.

All the while Lelit released a V3 of the Bianca. Most of the features were kind of boring (using a controllable power LED, e.g.), but the feature that caught my eye was the Low Flow mode, enabled by a Low Flow solenoid valve. Obviously I got one of those. The Bianca has a flow paddle, but a solenoid valve is programmable, so you know, gotta have that.

I also decided to switch the steam and water knobs for joysticks, because they're cooler.

## A brave new world

One might think that I should stop here, but obviously that would be no fun. Other machines have *programmable* pressure profiling. Having a manual flow control paddle was a great deciding factor __for__ the Bianca, but of course, using it is manual work. I want both. That's why I've bought a gear pump. The long term plan is to replace the rotary vane pump in the Bianca with a gear pump. I *could* do that with the standard Gicar control board and just the Open LCC, but I've also decided to create a replacement for the Gicar Control Board. In order to use the Gear Pump properly, I'll also add a pressure transducer.

Will that be it? We'll just have to see.
