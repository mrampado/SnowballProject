# Arduino Learning Platform (ALP)
Arduino Learning Platform was first designed as a simple way to teach my cousin Arduino in Nov 2021 without the frustration of breadboards, wiring, or polarity of LEDs. For many users wanting to start with Arduino, the hardware can be difficult to set up, troubleshoot, and is often not something that many want to deal with. This often leads to frustration in not knowing if the problem is software or hardware related, and the learning experience suffers.

Arduino Learning Platform was designed to maximize the setup of an Arduino, but in an all-in-one setup that requires no experience in hardware. Most importantly, it just works. 


## Initial Prototype

The initial prototype was designed over a weekend in November 2021, and subsequently manufactured by JLCPCB in time for me to deliver as Christmas gifts.  

![Gen1BoardView](InitialPrototype(Gen1)/BoardPhotos/IMG_3308.JPEG)

### Hardware Overview

The initial prototype of the ALP system uses a mounted Arduino Nano onto a custom PCB, with all through hole components so it can easily be soldered by hand. The board had the following inputs and outputs
3 pushbuttons
3 rotational potentiometers
1 temperature sensor
1 light sensor
1 buzzer
6 5mm LEDs
10 WS2812b LEDs (similar to neopixels)
1 power LED

From this hardware, over 15 projects were ideated from the most basic of flashing an LED, to more complex utilizing the sensors to sound the buzzer or LEDs. All projects could be completed with the board, and only the board. This leads to ease of use in learning how to program Arduino without extra components to deal with. 

### Software Overview

A number of projects were developed as a way to test the board such as flashing the WS2812b LEDs:

https://user-images.githubusercontent.com/31992845/184553061-3517018b-8d40-42bd-8cc7-a411898c9277.MP4



Or a Star Wars theme [credit to original developer here](https://github.com/NassimBouyacoub/Star-Wars-theme-Song-Arduino-)

https://user-images.githubusercontent.com/31992845/184553076-f6d57d24-914b-4a0a-8b67-bb8ad6814c24.MP4



And many other projects that successfully allowed both myself, and those that I helped to learn Arduino to successfully start programming with little other work. Unfortunately, the software will not be released as it is being changed for the released version below that uses a new chip. 

However, for those that choose to build this initial prototype, the schematic can be used to reference pinout diagrams allowing you to use any other Arduino tutorial online to get started with programming. 



### Feedback on the Prototype

The feedback I received from both my cousin as well as others I gave the board to was awesome, however, with all projects there is always room for improvement. 

The buttons are too small to easily press. As a manufacturing note, they also do not fit well into the board with glue being required at times to ensure real durability. 
The rotational potentiometers are large, bulky, and easy to break off. 
The temperature and light sensors are not attached to the board itself, and instead string off. This can lead to them being damaged in a backpack if not cared for properly.
For my feedback, using an off the shelf component (specifically the Nano) at the time made sense, but long term is not practical as it adds both manufacturing complexity and reliance on other vendors. I plan to embed the Arduino into the board which will allow the prototyping lab (in my case JLCPCB) to fully assemble the test boards for me. Others can then also place an order for the same configuration without a need to source other components. 



## Released Version

The released version has not been fully designed, but is currently being worked on to mitigate many of the issues I have listed for the initial prototype. 

I am documenting the process in the format of the _Engineering Design Process_ and this will be released with the project, either here or on my website. The goal of this release is to not only provide the open source hardware, but also to explain the process of how to approach a problem, ideate potential solutions, and work towards developing a solution. 

As no software was released for the prototype project, I plan to release all code I have to work with the new board design as it fixes a few issues. The new hardware will use the ATMEGA32u4, which has built in USB. This will simplify the driver issues known around the legacy Arduinos (see FT232 known issues with Windows 11).

I expect this to be released by Christmas 2022.


## License

This hardware is covered under the CERN-OHL-S-V2 open source hardware license. Details on this license can also be found [at this link](https://choosealicense.com/licenses/cern-ohl-s-2.0/). 

Software for this project is covered under GNU Public License v3.0. Details on this license can be found [at this link](https://choosealicense.com/licenses/gpl-3.0/)

As per the details in each of the licenses, replication is accepted under the provision that all commercial and individual replications must also follow the same license as in this project, and **remain fully open source**. 

While not required, please contact me before starting any commercialization efforts. At the current moment, I am unable to commercialize this project thus unable to sell finished boards. I am happy to (in a limited capacity) support anyone / business that wants to utilize my efforts with ALP to use as a basis for teaching anyone and everyone Arduino. 

It is my personal belief that this project shall remain open source for the entire community, with all schematics, gerber files, and code available to all. I have benefited greatly from the open source community and this project will hopefully help others learn and get started too! 

