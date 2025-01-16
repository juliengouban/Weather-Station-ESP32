# Weather-Station-ESP32
In this board, I have designed a weather station based on the ESP32 with sensor of temperature, humidity and photoresistor. 
The ESP32 is a highly versatile and cost-effective microcontroller, ideal for PCB design due to its powerful dual-core processor, built-in Wi-Fi and Bluetooth, and low power consumption. Its wide range of I/O options and support for various communication protocols make it suitable for many applications, especially in IoT projects. The compact form factor and extensive development support further simplify the design process, allowing for efficient and flexible PCB layouts.

Our board is a two layers designed with Altium Designer.

<h1> Electronic diagram</h1>
We'll now take a closer look at how our electronic board works: 

![Alt text](image/schema.png?raw=true "PCB in 3D view")

For powering the circuit, we've used a Micro USB type B connector to supply our board with 5V. As the ESP32 uses 3.3V, we've fitted a regulator to convert 5V to +3.3V: 

![Alt text](image/2.png?raw=true "PCB in 3D view")

We have added a clock module that allows for an accurate time even when our board is powered off. This module is powered by +5V and uses a coin cell battery when the board is off: 

![Alt text](image/3.png?raw=true "PCB in 3D view")

We use a MicroSD card module to store temperature measurements along with a date and time, allowing us to generate graphs on our web server:

![Alt text](image/4.png?raw=true "PCB in 3D view")


For the ESP32, we have chosen th ESP32-S3 Mini 1-N8. This is a compact and powerful microcontroller board designed by Espressif. It features the ESP32-S3 chip, which integrates a dual-core processor, Wi-Fi, and Bluetooth capabilities, making it ideal for a wide range of IoT applications. With 8MB of flash memory, this board offers ample storage for firmware and data. The ESP32-S3 Mini 1-N8 is known for its low power consumption, high performance, and rich set of peripherals, including SPI, I2C, UART, and GPIOs, making it a versatile solution for embedded systems and smart device development:
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


