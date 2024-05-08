[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-24ddc0f5d75046c5622901739e7c5dd533143b0c8e959d652212380cedb1ea36.svg)](https://classroom.github.com/a/kzkUPShx)
# a14g-final-submission

    * Team Number: 13
    * Team Name: Drink God
    * Team Members: Haige Xu & Xinyuan Jin
    * Github Repository URL: https://github.com/ese5160/a14g-final-submission-t13-drink-god.git
    * Description of test hardware: (development boards, sensors, actuators, laptop + OS, etc) 

## 1. Video Presentation
### Video Link: https://drive.google.com/file/d/1ydrR2BuqvclqR9ZWK_gxwQd7aG0sl-bE/view?usp=drive_link  

## 2. Project Summary
### Device Description  
Our project is an IOT automatic beverage machine called Drink God. The device is based on the SAMD25 microcontroller and the WINC1500 Wi-Fi Chip. The device can be selected on the mobile device to get the desired drink. The Drink God contains distance sensors to ensure that the drink poured into the glass does not overflow. In addition, Drink God also contains temperature sensors to detect the current temperature of the environment to determine whether you need to add ice to your drink to ensure that you enjoy your drink at the most suitable temperature. At the same time, Node-red Interactive Interface will show the name of the beverage you are currently drinking and the number of times you have drunk various beverages in a short period of time. The device could make it easier for people to choose what they want to drink. The use of Internet connection in this device can make this product more intelligent. After using the Internet connection, people can observe their drinking habits on the mobile device, so people can combine the recorded data to improve their drinking habits and make their life more healthy.  
### Inspiration  
In daily life, people need to drink water or beverages every day. Motivated by the idea of wanting to realize a more convenient way to get drinks while keeping track of one's drinking habits, this project was started.  
### Device Functionality   
The Drink God project is an advanced IoT automatic beverage machine, which utilizes a complex array of sensors and actuators integrated with the SAMD25 microcontroller serving as the brain of the device. It features an ultrasonic distance sensor HC-SR04 to monitor the drink level and prevent spillage, and a temperature sensor MCP 9808 to ensure drinks are served at the optimal temperature by adding ice if necessary. The device operates pumps via relays to transfer beverages and controls servo motors to show the working state. Connectivity is managed by the WINC1500 Wi-Fi Chip, handling network interactions including connection, authentication, and communication with a mobile app. This allows users to select their preferred beverages seamlessly through a user-friendly interface. The device is designed to prevent overfills and adjust drink temperature automatically, enhancing user convenience. Drink choices and consumption statistics are displayed on the NODE-RED UI interface, making it easy for users to track and manage their consumption. The project leverages essential electronics concepts such as timers, interrupts, analog-to-digital conversion (ADC), and I2C communication, ensuring a sophisticated and efficient operation.  
### Challenges  
The biggest challenge we encountered in this project was to write drivers for each sensor, because we couldn't use the written libraries directly, we needed to make these sensors work in our own freertos environment, so we needed to refine the .c and .h files for these sensors ourselves.  
In order to overcome this problem, we carefully read the datasheet of every sensor we used and also scrutinized the structure of our freertos, and with perseverance, made every sensor work properly.  
### Prototype Learnings  
I learned how to draw and fabricate PCBAs, I learned how to write drivers for sensors, and I learned how to use Node-Red for wireless control.  
In the design of the PCBA, it will make the output pin port allocation more reasonable, make the whole PCB layout more beautiful, and also can redesign the appearance of the PCB.  
### Next Steps  
Further enhancements can be realized in several ways:  
1. Advanced User Interface and Experience
Enhanced Mobile App Features: Develop additional features in your app, such as personalized drink recommendations, the ability to save favorite mixes, or schedule drink preparations in advance.
Interactive Feedback System: Implement a feature where users can rate drinks or provide feedback directly through the mobile app or Node-Red interface, which could help in improving drink recipes and user satisfaction.
2. Environmental and Health Features
Eco-Friendly Modes: Introduce more energy-efficient operating modes to minimize the environmental impact.
Health-Conscious Options: Offer settings that adjust recipes according to dietary restrictions or nutritional goals, such as low-sugar or low-calorie options.
3. Market Expansion and Customization
Customizable Skins and Accessories: Offer customizable options for the machine’s exterior design to cater to different aesthetic preferences or kitchen decors.
Expanded Beverage Options: Continuously expand the range of beverage options available, potentially collaborating with beverage companies to offer branded and specialty drinks.  
### Takeaways from ESE5160  
Through the course ESE5160, we learned how to design custom PCB, how to use freertos, how to use CLI commands, and how to write driver to sensors.  
### Project Links  
Link to final code: https://github.com/ese5160/a12g-firmware-drivers-t13-drink-god/blob/8808a773dc6873d1049dcacce21018b73d383078/ESE516Final.zip  
Link to Node-RED dashboard code(The latest version of node-red could not be exported due to the VM being shut down, as we have successfully demonstrated on DEMO day.): https://github.com/ese5160/a10g-cloud-t13-drink-god/blob/c9f9968850e1ba79861dadd41687125dc3a1c840/DrinkGod.json  
Link to final PCBA on Altium 365: https://upenn-eselabs.365.altium.com/designs/A984600D-580C-470D-BB41-1C56840180C3#design  


## 3. Hardware & Software Requirements
### Planned hardware features:  
HRS 01 – Project shall be based on SAMD21 microcontroller and WINC1500 Wi-Fi Chip.  
HRS 02 – Ultrasonic distance sensor HC-SR04 shall be used to measure distance. In this project the sensor was used to measure the height of the beverage surface.  
HRS 03 – The temperature sensor MCP9808 shall be used to measure the temperature of the beverage. In this project, the value recorded by the temperature sensor is used to determine whether the beverage needs to be iced.  
HRS 04 – SSD1306 OLED display shall be used for user interface.  
HRS 05 – The relay module receives control signals from the MCU to control the operation of the water pump, which is used to add drinks.  
HRS 06 – The servo motor SG90 in this device can be used to control whether or not to add ice to the drink.  
HRS 07 – The motor driver DRV2605LDGSR shall be used to control motor operation.  
### Function implementation:  
HRS 01: The project was successfully carried out based on the SAMD21 microcontroller and WINC1500 Wi-Fi Chip, and realized the control of the actuator through the return value of the sensor.  
HRS 02: The HCSR04 distance sensor can be successfully used to read the distance value and provide real-time feedback on the liquid level.  
HRS 03: The MCP9808 temperature sensor can be successfully used to read the temperature value, and because the MCP9808 is finally placed on the PCB, its function is modified to provide real-time feedback on the ambient temperature.  
HRS 04: Due to a problem in distributing the PCB output pins, the function of OLED was not realized. We output the feedback data through the Node-red UI interface.  
HRS 05: According to the feedback value of the distance sensor, the pump can be successfully controlled by controlling the relay module by enabling the PIN.  
HRS 06: The SG90 servo motor can also be successfully controlled by enabling the output pin.  
HRS 07: In this project, it was ultimately not used.  
### Planned software features:  
SRS 01 - The SAMD21 microcontroller shall transmit sensor data to WINC1500 Wi-Fi Chip via SPI at predefined intervals.  
SRS 02 - WINC1500 Wi-Fi Chip shall send the sensor data to the mobile app for real-time display on the user’s device.  
SRS 03 - The system shall monitor temperature with the MCP9808 sensor, reading data everysecond and outputting it through I2C.  
SRS 04 - The system shall monitor the distance between the users and Drink God via ultrasonic distance sensor HC-SR04, and communicating SAMD21 with UART. When the distance is less than a threshold, Drink God will provide drinks.  
SRS 05 - The system shall display sensor readings on an OLED, updated periodically.  
SRS 06 - The user shall be able to select the kind of drinks through a mobile app.  
SRS 07 - The SAMD21 microcontroller control DRV2605LDGSR motor driver by I2C in order to provide drinks.  
SRS 08 - All the sensors and other modules are controlled by the program in the SAMD21 microcontroller.  
### Function implementation:  
SRS 01: The project was successfully carried out based on the SAMD21 microcontroller and WINC1500 Wi-Fi Chip, and realized the control of the actuator through the return value of the sensor.  
SRS 02: By using the WINC1500 Wi-Fi module, you can successfully control the device from the mobile device and return the value to the mobile device.  
SRS 03: Through I2C transmission protocol, the measured value of MCP9808 can be obtained successfully.  
SRS 04: The measurement of HCSR04 can be obtained successfully through the UART transport protocol.  
SRS 05: The use of OLeds is not implemented.  
SRS 06: By using node-red, it is possible to use mobile devices to make different pumps work and thus obtain different drinks.  
SRS 07: The pump is not controlled by controlling the motor driver, but by enabling the relay module to control the work of the pump.  
SRS 08: All sensors and actuators can be successfully controlled through the MCU.  
## 4. Project Photos & Screenshots
### 3D prints
This is one from 3D print: ![9ccd1d24831b740c21efea24f2f21f1](https://github.com/ese5160/a14g-final-submission-t13-drink-god/assets/87221660/d387b932-6357-42d8-8b44-d175feac22c3)  
However, it is found that the size is so small that we can not put our sensors and PCB board in it. So we made one by our hand. (It can be used normally and it worked well in demo day): ![28dd267305136ff7801cf340596eace](https://github.com/ese5160/a14g-final-submission-t13-drink-god/assets/87221660/2bd30891-dd92-432f-9c63-796257cff672)

The standalone PCBA, top: ![2](https://github.com/ese5160/a14g-final-submission-t13-drink-god/assets/87221660/ee38c55c-a045-42d6-9c70-ac1e3901e006)  

The standalone PCBA, bottom: ![1](https://github.com/ese5160/a14g-final-submission-t13-drink-god/assets/87221660/1e1538c5-bde8-4595-9a48-b4603ff17359)

Thermal camera images while the board is running under load:   
![image](https://github.com/ese5160/a14g-final-submission-t13-drink-god/assets/87221660/7fc56b88-e064-444c-9b6c-1345b74811b3)  

The Altium Board design in 2D view (screenshot): ![c19f04b18d9bd787d1646373804a0d0](https://github.com/ese5160/a14g-final-submission-t13-drink-god/assets/87221660/e4f4df49-5b53-4743-98f6-de88816764f0)  

The Altium Board design in 3D view (screenshot): ![c9cf192f6b7dea9cc085652bd31a1fd](https://github.com/ese5160/a14g-final-submission-t13-drink-god/assets/87221660/98bfecc1-45b1-433c-be48-bf664ff5ef7e)  
![b783e3d7b9fcdffbf450ec02abfa270](https://github.com/ese5160/a14g-final-submission-t13-drink-god/assets/87221660/0d7ba6c7-35fb-4d1e-9196-d54e856f49bc)  

Node-RED dashboard: ![31819be3702f628342f79018ecb5124](https://github.com/ese5160/a14g-final-submission-t13-drink-god/assets/87221660/e4e25002-dfae-4206-b71d-ee10b711d922)

Node-RED backend: ![15e6b8908dc7e137688def7b70055a3](https://github.com/ese5160/a14g-final-submission-t13-drink-god/assets/87221660/29b97a10-72eb-4c2e-9680-ede1c34e485c)

Block diagram of your system: ![A14G](https://github.com/ese5160/a14g-final-submission-t13-drink-god/assets/87221660/a616a942-644c-430d-906f-3dac7ce283ff)  

## 5. A12G Codebase
All the codes are shown in (It is the same as before): https://github.com/ese5160/a12g-firmware-drivers-t13-drink-god/blob/8808a773dc6873d1049dcacce21018b73d383078/ESE516Final.zip 
