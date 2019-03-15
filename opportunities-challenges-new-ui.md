# Opportunities and Challenges of New User Interfaces



Gregory Bowe



University of Maryland University College


> The following is my final paper for Computer Systems Architecture


---
---



## <a id="top"></a>Table of Contents

- [Introducton](#intro)
- [Section 1: Types of User Interfaces](#sec1)
  - [Touch Screen UI](#touch)
  - [Interactive Voice UI](#voice)
  - [Gesture UI](#gesture)
- [Section 2: Multimodal Interfaces](#sec2)
  - [Assistive Robotic Manipulators](#robot)
  - [Senior Living](#senior)
  - [System Example and Requirements](#example)
- [Conclusion](#end)
- [References](#source)

---
## Abstract

New user interfaces are creating opportunities and challenges for enterprise IT departments who want to increase user engagement and reduce costs, especially for users with physical or cognitive challenges. These user interfaces move beyond traditional I/O devices such as keyboards, keypads, and mice, to more modern interfaces such as touchscreens, voice, motion, and even predictive UI&#39;s. These interfaces can be particularly useful to people using assistive technologies with visual, motor skill, or cognitive impairments. Architecting systems that incorporate these devices is largely dependent upon network system requirements. However, physical requirements are inexpensive and simple, requiring only basic local processor and memory usage. Challenges present themselves in the back-end systems designed to classify and identify user inputs in an accurate way, especially for auditory and visual inputs.



## <a id="intro"></a>Human Computer Interaction - An Introduction

The way people interact with computers has changed little since the first computers went online in the 1950&#39;s. Although punch cards are no longer used, I/O devices such as  the keyboard/mouse combination has been standard since the 1980&#39;s. Graphical user interfaces (GUI&#39;s) were introduced into mainstream PCs with the Apple Lisa in 1983 and became standard with the Apple Macintosh and Microsoft Windows shortly after. A decade later, processors became small enough for mobile technology to blossom and grow into its own category.

These technologies began maturing at the same time that a major demographic shift began. The global population is aging to the point that the US Census Bureau estimates that by the year 2050, 1.6 billion people will be age 65 or older (He, W et al, 2016).  As people age, sight and hearing tend to decline, as well as cognition, especially when trying to use new and unfamiliar technology. Because of this, a great opportunity exists to create new, intuitive, user interfaces that move beyond traditional keyboard or button-based inputs.

[^ Back to Top](#top)

## <a id="sec1"></a>Section 1: Types of User Interfaces

### <a id="touch"></a>Touch Screen UI

One type of user interface that can be optimized, although not new, is touchscreen technology. Touchscreens have been in use since the 1970&#39;s. The first touchscreen was created by two CERN engineers in the early 1970&#39;s. This early version of resistive touch recognized the input from a heavy object pressing on its surface (Erickson, C. 2012).

Touch UI&#39;s are used in many settings, from ATM machines to Point of Sale cash registers, medical monitors, game consoles, phones, vehicle consoles, and mobile devices. Their use in assistive technologies has grown as well, as engineers develop software that can recognize simple touch gestures and use them to control robotic devices that assist in daily activities such as picking up objects, opening and closing doors, controlling lights, climate control systems, and basic appliances. As the hardware becomes cheaper and more advanced, these systems can and should become available to more people. A downside of touch UI, especially when used on mobile devices, is that they are small, fragile, and difficult to handle.

One of the primary ways to implement touch screens is through resistive touch. This analog method consists of using two layers to create a small electrical current that can be interpreted as a user input. The glass display layer, such as an LCD screen, is the lower layer while the top layer is often made of transparent plastic. Between these layers is a thin transparent layer of a conductive material such as indium tin oxide. When the screen is pressed, contact is made between the two grid layers resulting in an electrical connection. The touch point is calculated on the x and y-axis. The signal is converted from analog to digital and used as an input signal from the user to the processor in order to execute a command. (Poor 2012)

[^ Back to Top](#top)

### <a id="voice"></a>Interactive Voice UI

Talking to a machine and having a response has been a dream of computer scientists from the start of the computer age. Voice interfaces offer a powerful and intuitive way for a user to interact with various devices, objects, or even people. New systems such as Amazon&#39;s Alexa offer developers a framework to create unique and specialized applications that can run on minimal and inexpensive hardware such as the $35 Raspberry Pi.

Voice UIs can be implemented in multiple ways. Most of these involve a local device with input from a microphone, a local vocabulary stored in the device&#39;s memory, a transmitter and receiver from the audio I/O register to the CPU through a direct audio bus or a WiFi or Bluetooth wireless connection. Uninterpreted input is the initial user input, which is often in a binary form of audio (Dahl, D. A. 2017). If the commands are not recognized, the modules typically sent an HTTP request to a database server or application to determine the command and return a response.

With Amazon&#39;s Alexa service, specific &quot;skills&quot; can be created and accessed through an HTTP/2 request, which eventually returns a response. (A more detailed explanation can be found in their documentation).

[^ Back to Top](#top)

### <a id="gesture"></a>Gesture UI

Gesture user interfaces are perhaps the most complex and potentially the most useful. This interface requires the use of one or more camera systems, an application to recognize specific gestures as inputs, and a PC or computer that can receive real time inputs and issue appropriate commands.

One device that can identify gestures is a Kinetic sensor used to detect hand gestures, such as &quot;move&quot;, &quot;grab&quot;, and &quot;release&quot;. (Hsiao, S., 2017) In a recent study, the Kinetic sensor was programmed to recognize specific movements used to control a television entertainment system. This sensor includes a digital camera to track movements and accesses the OpenNI API to classify these movements. (Hsiao, S., 2017)

The primary challenge in this system is two-fold. 1) The device must be connected to a network that can quickly and seamlessly process HTTP requests and 2) The device must have enough local memory, whether in the I/O registers or processor, to send and receive these requests.

[^ Back to Top](#top)

## <a id="sec2"></a>Section 2: Multimodal Interfaces

A system that combines multiple inputs in known as a multimodal system. These systems can incorporate voice, gesture, keyboard, touchscreen, sensor, visual, or other inputs to control almost anything, from devices and entertainment systems, to complete environments. To put it another way, &quot;A multimodal system supports more than one sensory and response modality such as tactile, visual, auditory, verbal and manual activity, among others&quot; (Alor-Hernández, G, 2012).

### <a id="robot"></a>Multimodel For Assistive Robotic Manipulators

An application for integrating a multimodal UI is in the design of assistive robotic technology for people with serious spinal cord injuries. &quot;In the United States, about 19.9 million people have difficulties with physical tasks relating to upper extremity functioning, including lifting, grasping, pushing/pulling, reaching, dressing, and eating.&quot;  (Chung, C., 2017) This population has difficulty performing activities of daily living (ADL).  Assistive robotic manipulators (ARMs) can help. They are essentially robotic arms that can be attached to a motorized wheelchair and used to turn switches on or off, pick-up various items, turn door-knobs and water faucets, open containers, and more.

In the study by Chung, the ARM controller tested received input from a 4 x 4 keypad and 3-axis joystick controller. This devices operates the Cartesian joint that provides movement on the x, y, and z-axis, and finger movements to grab, hold, and twist. The joystick provides for the horizontal and twisting movements. However, as pointed out in their study, Chung found the users had such a difficult time with the twisting motion, that this feature was rarely (and sometimes never) used. (Chung, C. 2017)

An alternative user interfaces was created using a mobile touchscreen that recognized two kinds of user input - tapping and one-finger swiping. This enabled users to control the device without needed the dexterity required to operate the twist-movement of the joystick. The UI system requires a three-component set, a mobile touchscreen, control program, and the robotic arm.

The first component is a mobile touchscreen device with the user interface application. A device with a 1.4 GHz quad-core processor, 5-inch touchscreen LCD display, Bluetooth, and Wi-Fi, which now represents a basic smartphone, is more than adequate.

The mobile device connects to a PC, via Bluetooth or WiFi, that has the control program for the ARM. Even the latest JACO robotic arm requires relatively little computing power and can connect to a PC through a USB or wirelessly.

The final component is the robotic arm itself. In the Chung example, a JACO robotic manipulator was used. The ARM itself has a built-in 360 Mhz processor and multiple I/O ports. (Kinova, 2017)

The mobile touchscreen UI enabled users to learn how to operate the ARM quicker than the joystick, and these users were able to take full advantage of the features, including the ability to twist a doorknob, thanks to the UI.(Chung, C. 2017)

In an application such as this one, the advantages of using a touchscreen outweigh the disadvantages. This UI requires little additional hardware and is simple to implement, despite barriers with mobile devices.  One of the barriers to adopting mobile devices has been the reduced processing power, storage space, communication capabilities and interaction quality (Alor-Hernández, G, 2012). However, as these devices become more powerful and efficient, this barrier becomes smaller.

[^ Back to Top](#top)

### <a id="senior"></a>Multimodel For Senior Living

Recent trends in user interfaces include &#39;smart technology&#39;, which is another way of saying integrated systems. These trends include networking appliances, lighting, HVAC, and other systems within a home allowing users to control these systems remotely. For consumers, this represents the convenience of operating everything from entertainment systems to lighting remotely, through voice control, pre-programmed times, or even using gesture UI&#39;s. One of the great opportunities of these systems involves integrating them into the living spaces of senior adults and others with visual, auditory, cognitive, or other impairments.

With nearly 17% of the adult population predicted to be age 65 or older by 2050, the development of these technologies is even more important.

In the following example designed by Yu-Liang, H et al, (2017), a multimodel approach was used to monitor the smoke detectors, appliances, TV, lights, and HVAC system in the home through a combination of wearable sensors, integrated smoke detectors, and temperature sensors. The wearable sensors tracked a user&#39;s movement through the home and were programmed to recognize six specific gestures that control devices. The smoke detectors were designed to recognize and warn of any fire while the temperature sensors were designed to want and turn off appliances if they were left on or notify emergency personnel in case of a fire.

[^ Back to Top](#top)

### <a id="example"></a>System Example and Requirements

One of the requirements of this system was cost-effectiveness, as reflected in the components used to build it. These components were segmented into different modules: wearable inertial sensing modules, information processing module, air sensor modules, decision module, intelligent monitoring interface and the household appliance plant.

#### Wearable Inertial Sensing Module

This module used two sensors, one for the hand and one attached to the foot. These sensors used a triaxial accelerometer and triaxial gyroscope to measure movement and acceleration on the x, y, and z-axis. Digital signals were transmitted to the Information Processing Module using a Radio Frequency wireless transmitter. A module similar to the one used in this study could be built using an MPU- 6050 chip to process the data, a converter and communications chip to transmit the data in a 16 bit IIC format. The 16 bit format limits signed integers to a range of -32768 to 32767, which is acceptable in this case. This chip requires a small 3 to 5-volt power supply.

#### Information Processing Module

The information processing module was built using an Arduino Mega microcontroller board. This board includes 54 digital I/O pins which are used as inputs by the hand and foot sensors and temperature sensor, and outputs for the TV, AC, kitchen exhaust fans, and lights. Analog pins are used as inputs for the CO sensor. The module connects to the decision-making module (the PC) via USB. Onboard flash memory is able to cache data, which enables fast data transmission rates.

This module sends and receives data from the PC and sends data to the appliance module.

#### Sensor Modules

The sensor modules include both smoke/carbon dioxide detectors and temperature-detector. The CO sensor sends analog data to the information processing module and while the temperature sensor sends a digital signal.

#### Decision Module

The decision Module is a PC that receives data from the information processing module and runs various functions, depending on what information is received. For example, in this use case, a gesture UI was created to recognize the arm movements of the user. In order to do this, the information received from the wearable arm sensor needs to be compared to specific classes. These classes are pre-trained and tested to recognize the gestures. There is also a separate confusion-set classification to recognize movements that indicate distress. Additional classes include those for recognizing if an appliance was left on through an increase in temperature. If the data received falls into one of the classifications, the appropriate action is taken. (Yu-Liang, H, 2017)

Various algorithms can be used to recognize the gestures, and in this example, there models are pre-trained and tested outside of this architecture. For example, a 3D gesture recognition algorithm is used to determine if a particular movement is a command gesture. These algorithms are trained and tested with large amounts of data so their accuracy can be as high as possible. Another important algorithm is the probabilistic neural network-based (PNN) classification. This determines the likelihood or probability that a certain input is actually a command from the instruction set or confusion set.  (Yu-Liang, H, 2017)

#### UI Commands

Example of commands include the following:

    a) Gesture 1: Turns TV on.
    b) Gesture 2: Turns TV off.
    c) Gesture 3: Next TV channel
    d) Gesture 4: Previous channel
    e) Gesture 5: Turn AC on
    f) Gesture 6: Turn AC off
    g) PNN Classification: 1 is safe, no action
    h) PNN Classification 2: warning
    i) PNN Classification 3: danger

This module requires a CPU architecture that can quickly receive, process, and send information to and from the I/O devices. This data is primarily in a 16 bit format, making the PC needs basic.

#### Intelligent Monitoring Interface

The user accesses the information through the intelligent monitoring interface. This interface is displayed on a monitor and can be used to pre-program the timing and execution of certain commands such as adjusting the lights when a user walks into a room and allows the user to monitor the system. (Yu-Liang, H, 2017)

#### Household Appliance Plant

This module receives and executes commands from the information processing module, such as turning an appliance on or off, changing a channel on the TV, turning lights on or off, or turning exhaust fans on/off. (Yu-Liang, H, 2017)

### Device Variations

One advantage of creating multimodal UI&#39;s is the flexibility available when designing these systems. 
        
For example, in the smart-home, a simple voice UI could be added using Amazon&#39;s Alexa platform. With this platform, using a voice controller or creating an app for a different device is as simple as creating custom commands (referred to as skills), testing these skills and implementing them. 

The primary system constraint is having a fast WiFi or wired network suitable for the volume of HTTP requests and responses. Like other voice UI&#39;s (Dahl, D. A. 2017), Amazon processes the voice request on its cloud servers. If an enterprise wanted to implement more than a basic voice interface without using a service such as Amazon, using servers that can process data quickly would be one of the key requirements. (Goruck, 2017)

[^ Back to Top](#top)

## <a id="end"></a>Conclusion

Using new user interfaces in multi modal can be an effective means to engage users in a way that us natural, easy to learn, and beneficial. Systems designed for these interfaces don&#39;t require enormous amounts of costly hardware. However, they do require processors that can send and receive digital and analog data, have enough onboard memory to transfer this data in real time, and include decision machines, such as a local PC, that is able to communicate quickly with these devices. Accessing memory, especially when using machine learning classifiers, becomes one of the most important features. Programs using standards such as SCXML markup can implement voice-UI on small devices in ANSI C, even with very limited processing capabilities and even integrated circuits (Dahl, D. A. 2017). However, this dictates the use of network connections that are fast and reliable. Because this network plays such an important role, it becomes a risk to systems designed for medical and other life-saving needs. The central challenge becomes creating user interface systems that don&#39;t rely so heavily on making API calls through a network interface.

[^ Back to Top](#top)


## References:

Alor-Hernández, G., Sánchez-Cervantes, J. L., Juárez-Martínez, U., Posada-Gómez, R., Cortes-Robles, G., &amp; Aguilar-Laserre, A. A. (2011). _ITOHealth: a multimodal middleware-oriented integrated architecture for discovering medical entities._ Informatics for Health and Social Care, _37_(2), 74-91. doi:10.3109/17538157.2011.613552

Chung, C., Ka, H. W., Wang, H., Ding, D., Kelleher, A., &amp; Cooper, R. A. (2017). _Performance Evaluation of a Mobile Touchscreen Interface for Assistive Robotic Manipulators: A Pilot Study._ Topics in Spinal Cord Injury Rehabilitation, 23(2), 131-139. doi:10.1310/sci2302-131

Dahl, D. A. (2017). _Multimodal interaction with W3C standards: toward natural user interfaces to everything_. Cham: Springer.

Erickson, C. (2012, November 09). _The Touching History of Touchscreen Tech_. Retrieved November 26, 2017, from [http://mashable.com/2012/11/09/touchscreen-history/#d0lIW.Ss9sqY](http://mashable.com/2012/11/09/touchscreen-history/#d0lIW.Ss9sqY)

Goruck (2017, March 31). _Alexa Lambda Linux (ALL) Reference Design._ Retrieved November 26, 2017, from [https://github.com/goruck/all](https://github.com/goruck/all)

He, W., Goodkind, D., &amp; Kowa, P. (2016, March). _An Aging World: 2015 International Population Reports_(Rep.). Retrieved https://www.census.gov/content/dam/Census/library/publications/2016/demo/p95-16-1.pdf

Hsiao, S., Lee, C., Yang, M., &amp; Chen, R. (2017). _User interface based on natural interaction design for seniors._ Computers in Human Behavior, _75_, 147-159. doi:10.1016/j.chb.2017.05.011

Orphanides, A. K., &amp; Nam, C. S. (2017). _Touchscreen interfaces in context: A systematic review of research into touchscreens across settings, populations, and implementations._ Applied Ergonomics, _61_, 116-143. doi:10.1016/j.apergo.2017.01.013

Poor, A. (2012, October 17). _How it works: The technology of touch screens._ Retrieved November 26, 2017, from [https://www.computerworld.com/article/2491831/computer-hardware/computer-hardware-how-it-works-the-technology-of-touch-screens.html](https://www.computerworld.com/article/2491831/computer-hardware/computer-hardware-how-it-works-the-technology-of-touch-screens.html)

_Robot arms_. (n.d.). Retrieved November 26, 2017, from [http://www.kinovarobotics.com/innovation-robotics/products/robot-arms/](http://www.kinovarobotics.com/innovation-robotics/products/robot-arms/)

Yu-Liang, H., Po-Huan, C., Hsing-Cheng, C., Shyan-Lung, L., Shih-Chin, Y., Heng-Yi, S., &amp; ... Yu-Chen, K. (2017). _Design and Implementation of a Smart Home System Using Multisensor Data Fusion Technology_. Sensors (14248220), 17(7), 1-21. doi:10.3390/s17071631

[^ Back to Top](#top)