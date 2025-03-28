---
title: "Mu Draconis"
description: "A polar 3d printer with modern hardware, but still not the most practical"
project_name: "Mu Draconis"
repository: "https://raw.githubusercontent.com/WilliamPrime/Mu-Draconis/refs/heads/main/design.md"
---
# mu draconis
Made by : William
respository link: https://github.com/WilliamPrime/Mu-Draconis

i have a 3d printer :D




pitch, make a polar 3d printer, not because its practical, but because its something different :D


i would be taking inspiration from this, but making it more functional
https://www.reddit.com/r/3Dprinting/comments/16dsugh/received_a_ton_of_constructive_criticism_on_my/

i want this to look very clean, probably be control only via klipper, no phyiscal controls

im still deciding if i want to have a heated bed or not, or if i want it to be a "fast" polar printer and use a nema 34 on the bed or something like that

the gantry should also be fairly easy to remove for shipping, so xt-60 connectors and other jst things will be needed to make sure that all the cables are easily detachable

also had the idea of having suction cup style things on the base so it sticks down to a table, its just a funny idea

**so far i have some parts ive found and extracted out of dead 3d printers:**
- ras pi 4 8gb
- big tree tech skr mini E3 (the mosfets for heaters and fans are dead, but stepper drivers still work)
- voron klipper expansion board
- hardmount v6 style hotend
- 70w 24v heater cartridge
- 40w 24v heater cartridge

im hopeing i can use them without them counting towards the cost of the BOM

#
# **first two days of planning, around 4hours into it**:
ive decided quite a bit about my printer
i want to use a 250mm round heated bed
i want to use a slip ring so i can get power to the bed and have a heated bed on this printer
i plan to use linear rods and linear bearing for both the x and z
the x will 100% be belted
im still deciding if the z should be belted or use a lead screw
i also started to model out some of the components i plan to use in fusion 360, such as the bed as a starting point
however it appears the technical drawing from the manufacturer REALLY isnt accurate

current rough BOM

| Part name                      | price         | notes                                                                                            |
|--------------------------------|---------------|--------------------------------------------------------------------------------------------------|
| 250mm dia hotbed               | £13.89        |                                                                                                  |
| ras pi 4 8GB                   | already owned |                                                                                                  |
| semi broken btt skr mini e3    | already owned | dead mosfets, but stepper drivers still good                                                     |
| klipper expansion board        | already owned | to compensate for the dead mosfets on the mainboard                                              |
| nema 17 motor with leadscrew   | £13.49        | 320mm leadscrew might trim down to 200mm                                                         |
| thermal fuse                   | £1.85         | 100c thermal fuse to prevent run away on the bed                                                 |
| nema 23, 76 mm motor for bed   | £18.69        | overkill, will prob change to help budget                                                        |
| slip ring                      | £13.02        | 3 channel, 30A per channel 22mm dia                                                              |
| bicycle bearing                | £1.46         | cheapest way to get a large bearing for bed (41mm id)                                            |
| C14 S8B3 power panel           | £1.36         |                                                                                                  |
| mellow sherpa mini kit         | £30.39        | good, light extruder                                                                             |
| gates 2GT 6mm belt 1m          | £4.79         |                                                                                                  |
| 20t pulley x2                  | £3.30         |                                                                                                  |
| 20t idler x2                   | £3.10         |                                                                                                  |
| LDO-42STH48-2804AH-R           | £26.09        | the goat of stepper motors, could use a cheaper 42STH48 2804AC-R instead for more torque i think |
| Meanwell LRS350                | £23.59        |                                                                                                  |
| pt1000 thermistor              | £4.53         | overkill but i maybe want high temp, no clue                                                     |
| 250mm bed surface+magnet+sheet | £15.39        |                                                                                                  |
| end stops x3                   | £3.20         |                                                                                                  |
| mosfet for bed/heater x2       | £3.28         |                                                                                                  |
| 200mm 8mm dia linear rod x2    | £5.76         |                                                                                                  |
| 330mm 8mm dia linear rod x2    | £6.32         |                                                                                                  |
| Fushi LM8-UU/2pcs              | £9.79         |                                                                                                  |
| Fushi LM8-LUU/2pcs             | £12.29        |                                                                                                  |



## 08/02/2025  (arround 5 total hours)
put another 2 or 3 hours into sketching out how im going to get this to work
finally managed to start getting stuff modelled in fusion 360

<img src="https://cloud-jr0f3cjmn-hack-club-bot.vercel.app/0image.png"
     alt="image of printer"
     style="float: left; margin-right: 10px;" />

the belting seems daunting but i recon its going to be nice

ive struggled to try and model the bed as almost all of the technical drawing on the aliexpress listings are horrible 

## 15/02/2025 (arround 13 total hours)
made alot more progress
ive been modelling the respective components im going to need for my build
ive also started to model the assemblies so i can start combining them

ive decided to start with the bed because i think the bed will be the biggest challenge to make
the bed is probably my biggest challenge because i need to deal with belts to rotate the bed, and also belt tensioning for that, but i also need to deal with getting power to the bed as i would like to have a powered bed, for that i also need to deal with the slip ring
the solution i think i have come up with is 3d printing a custom hollow pulley/sprocket that will attach to the bed, that way the slipring can be on the inside of it and still deliver power

here are some images of the CAD that ive started to hobble together


<img src="https://cdn.hackclubber.dev/slackcdn/2249a46613cd168fe8c47ccac4479448.png"
     alt="image of printer"
     style="float: left; margin-right: 10px;" />
<img src="https://cdn.hackclubber.dev/slackcdn/4487a36952424e21c55a8125484ab075.png"
     alt="image of printer"
     style="float: left; margin-right: 10px;" />
     <img src="https://cdn.hackclubber.dev/slackcdn/87fea6e6c3f6143f4372952cadccecca.png"
     alt="image of printer"
     style="float: left; margin-right: 10px;" />
     <img src="https://cdn.hackclubber.dev/slackcdn/797f056c130ea83b47509f0e03efe3a4.png"
     alt="image of printer"
     style="float: left; margin-right: 10px;" />
     <img src="https://cdn.hack.pet/slackcdn/1a2a60ba4b11c61f53306f0c2183026c.png"
     alt="image of printer"
     style="float: left; margin-right: 10px;" />
     <img src="https://cdn.hack.pet/slackcdn/7bbc1aec7b0fca603a153226776a2e31.png"
     alt="image of printer"
     style="float: left; margin-right: 10px;" />


## 18/02/2025 (arround 18 total hours)
started working on belt tensioners
     <img src="https://cdn.hackclubber.dev/slackcdn/db28638079230db44cd8334a3dad00f4.png"
     alt="image of printer"
     style="float: left; margin-right: 10px;" />
they were surprisingly tricky to design 
but im hoping maybe if i go all belts then i can reuse the belt tensioners across the printer

<img src="https://cdn.hack.pet/slackcdn/cbf5c1866e8a1887e0b50253c39c2e33.png"
     alt="image of printer"
     style="float: left; margin-right: 10px;" />

it feels quite voron 0 inspired, but that was what i was inspired by :D 

