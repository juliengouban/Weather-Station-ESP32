# Weather-Station-ESP32
In this board, I have designed a weather station based on the ESP32 with sensor of temperature, humidity and photoresistor


<h1> Electronic diagram</h1>
We'll now take a closer look at how our electronic board works: 

![Alt text](image/schema.png?raw=true "PCB in 3D view")

For powering the circuit, we've used a Micro USB type B connector to supply our board with 5V. As the RP2040 uses 3.3V, we've fitted a regulator to convert 5V to +3.3V: 

![Alt text](image/2.png?raw=true "PCB in 3D view")

This is where you'll find the 128-megabit flash memory to store the program. The 2-pin connector allows you to force USB boot:

![Alt text](image/3.png?raw=true "PCB in 3D view")

The 12Mhz crystal provides the clock for our RP2040 microcontroller:

![Alt text](image/4.png?raw=true "PCB in 3D view")


We have added a LED to be programmed on GPIO18 to check that our card is working properly: 
![Alt text](image/5.png?raw=true "PCB in 3D view")

Finally, we have the RP2040 microncontroller. It is supplied with 3.3V with decoupling capacitors:
![Alt text](image/6.png?raw=true "PCB in 3D view")

![Alt text](image/7.png?raw=true "PCB in 3D view")


<h1>PCB Design</h1>


The board is a 2-layer design. On the top you can see the 3.3V regulator and the Micro-USB type B connector.
In the middle of the board you'll find the flash memory and the RP2040 microcontroller.
At the bottom of the board you'll find the 2-pin USB boot connector and the 12Mhz quartz crystal.
A ground plane has been created on the TOP layer to connect all the GNDs together.

Here are the 3d and top layer views of the PCB:

![Alt text](image/8.png?raw=true "PCB in 3D view")

Here is a 3d view of the PCB:

![Alt text](image/9.png?raw=true "PCB in 3D view")


