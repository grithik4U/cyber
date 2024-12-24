# cyber
Hardware debug
Cyber Apocalypse 2024

Debug

Your team has recovered a satellite dish that was used for transmitting the location of the relic, but it seems to be malfunctioning. There seems to be some interference affecting its connection to the satellite system, but there are no indications of what it could be. Perhaps the debugging interface could provide some insight, but they are unable to decode the serial signal captured during the device's booting sequence. Can you help to decode the signal and find the source of the interference?

Author: Grithik

hw_debug.zip
Tags: hardware

Solution

In this solution im presented with a SALEAE file. I can open the file in Logic 2 and inspect whats going on. There is only one signal without much information.

![image001](https://github.com/user-attachments/assets/8e9a649d-2f6e-483a-8940-32dd1404f4d4)

So a bit more analysis is needed. Adding a async serial analyzer with 115200 bit rate (rest kept to standard) for the channel leads immediately some readable log of a boot sequence of some sort.


![image002](https://github.com/user-attachments/assets/0aeddc16-f22b-41e8-b14e-9e37ed2a1f53)


![image003](https://github.com/user-attachments/assets/2021edeb-8788-4472-b2f9-b16337a2b0e2)


Scrolling a bit further down we can see the flag distributed in the log.

![image004](https://github.com/user-attachments/assets/bf33361f-b2b2-4d73-942a-5fe76d8a8818)


Stitching it all together leads to the "flag HTB{547311173_n37w02k_c0mp20m153d}."
