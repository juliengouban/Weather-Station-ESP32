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

The DHT11 is a popular digital temperature and humidity sensor. It measures temperature from 0 to 50°C with ±2°C accuracy and humidity from 20 to 80% with ±5% accuracy. The sensor communicates via a single data pin, making it easy to integrate into projects like weather stations and environmental monitoring systems. It offers a good balance of cost and functionality for basic temperature and humidity measurements:
![Alt text](image/6.png?raw=true "PCB in 3D view")

Finally we have added a photoresistor, which is a type of resistor whose resistance changes based on the amount of light it receives. In the presence of light, its resistance decreases, allowing more current to flow, while in darkness, its resistance increases, limiting the current:
![Alt text](image/7.png?raw=true "PCB in 3D view")


<h1>PCB Design</h1>


The board is a 2-layer design. On the top you can see the 3.3V regulator and the Micro-USB type B connector.
In the middle of the board you'll find the ESP32 microcontroller and its wifi antenna.
At the right side of the board you will find the DHT11 sensor at the top, DS1307 module at the middle and at the bottom a MicroSD card.
A ground plane has been created on the TOP layer to connect all the GNDs together with a ground plane. This ground plane is around the wifi antenna but not to close to it.

Here are the 3d and top layer views of the PCB:

![Alt text](image/8.png?raw=true "PCB in 3D view")

Here is a 3d view of the PCB:

![Alt text](image/9.png?raw=true "PCB in 3D view")


