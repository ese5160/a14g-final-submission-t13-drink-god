[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-24ddc0f5d75046c5622901739e7c5dd533143b0c8e959d652212380cedb1ea36.svg)](https://classroom.github.com/a/kzkUPShx)
# a14g-final-submission

    * Team Number: 13
    * Team Name: Drink God
    * Team Members: 
    * Github Repository URL: https://github.com/ese5160/a14g-final-submission-t13-drink-god.git
    * Description of test hardware: (development boards, sensors, actuators, laptop + OS, etc) 

## 1. Video Presentation
### Video Link:  

## 2. Project Summary
### Device Description  
Our project is an IOT automatic beverage machine called Drink God. The device is based on the SAMD25 microcontroller and the WINC1500 Wi-Fi Chip. The device can be selected on the mobile device to get the desired drink. The Drink God contains distance sensors to ensure that the drink poured into the glass does not overflow. In addition, Drink God also contains temperature sensors to detect the current temperature of the environment to determine whether you need to add ice to your drink to ensure that you enjoy your drink at the most suitable temperature. At the same time, Node-red Interactive Interface will show the name of the beverage you are currently drinking and the number of times you have drunk various beverages in a short period of time. The device could make it easier for people to choose what they want to drink. The use of Internet connection in this device can make this product more intelligent. After using the Internet connection, people can observe their drinking habits on the mobile device, so people can combine the recorded data to improve their drinking habits and make their life more healthy.  
### Inspiration  
In daily life, people need to drink water or beverages every day. Motivated by the idea of wanting to realize a more convenient way to get drinks while keeping track of one's drinking habits, this project was started.  
### Device Functionality   
The Drink God project is an advanced IoT automatic beverage machine, which utilizes a complex array of sensors and actuators integrated with the SAMD25 microcontroller serving as the brain of the device. It features an ultrasonic distance sensor HC-SR04 to monitor the drink level and prevent spillage, and a temperature sensor MCP 9080 to ensure drinks are served at the optimal temperature by adding ice if necessary. The device operates pumps via relays to transfer beverages and controls servo motors to show the working state. Connectivity is managed by the WINC1500 Wi-Fi Chip, handling network interactions including connection, authentication, and communication with a mobile app. This allows users to select their preferred beverages seamlessly through a user-friendly interface. The device is designed to prevent overfills and adjust drink temperature automatically, enhancing user convenience. Drink choices and consumption statistics are displayed on the NODE-RED UI interface, making it easy for users to track and manage their consumption. The project leverages essential electronics concepts such as timers, interrupts, analog-to-digital conversion (ADC), and I2C communication, ensuring a sophisticated and efficient operation.  
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

### Project Links  


## 3. Hardware & Software Requirements

## 4. Project Photos & Screenshots
