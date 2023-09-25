# MAJOR-PROJECT
The main aim of this work is to develop a fully automated IoT based sub-station by which associated equipment can be protected, monitored and controlled from any place in the world only by the authorized personnel at a very low cost.

# SUBSTATION MONITORING AND CONTROLLING USIN ARDUINO NANO

# TEAM MEMBERS
1. B. Poojitha
2. B. Sandhya
3. B. Rakesh
4. N. Prashanth Reddy

# OBJECTIVE OF THE PROJECT
Present days in a substation there is at least one operator for measuring parameter like voltage, current level and temperature etc. Belonging to Transformer and other equipment’s. These can affect the Transformer and parallax error too. So by using this project we can minimize error. In this project sensor are used to change the parameter of Transformer like level and temperature, then this data is sent to arduino and it is sent to web server through communicating device
Ethernet. Through the interface of the webpage user and control the device attached to the arduino . Additionally an LCD is also interfaced with the microcontroller to provide interface through theuse of our keys. The main outcome of this project is to minimize work related to the maintenance substation. Valuable data is provided of every auxiliary (transformer) of substation to analysis the value of various parameters in auxiliary (transformer) to monitor this working in day and night and for analysis in future.

# INTRODUCTION

The purpose of this project is to acquire the remote electrical parameters like voltage, current, frequency and send these real time values over network along with temperature at power station. This project is also designed to protect the electrical circuitry by operating a relay. This relay gets activated whenever the electrical parameters exceeds the predefined values and This system can be designed to send alerts whenever the relay trips or whenever the voltage or current exceeds the predefined limits. The Arduino controller can efficiently communicate with the different sensors being used When we give supply to our prototype all the sensors start sensing the electrical parameters and update all the real time values to the server as well as shows on the display. It compares all the real time values with the pre-defined values, if any of the values exceeds pre-defined values it sends a fault alert to the relay and buzzer as well as update it on the display. If the fault exists for the pre-set time then relay isolates the load from the rest of the system. In the meantime, comparison goes on as before, if the fault gets cleared relays reconnect the load with the rest of
the system.

# BLOCK DIAGRAM DESCRIPTION:

1) ARDUINO CIRCUIT:
Arduino will give signal to the relay to cut off the particular area electricity where fault has been occurred. For open circuit, if current is less than the minimum value current, then the relay of that particular area will be off. For very high voltage, if voltage is greater than the cut off voltage, then the relay of that particular area will be off Buzzer and indicator of the panel will become ON to alarm the people in the Substation. Although Arduino will automatically cut off the power supply of the particular area. Then, also a cut OFF and ON which has been provided in the panel to manually cut OFF and ON the particular area Distribution line.

2) POWER SUPPLY:
The project required +5 volt and +12 volt power supplies. +5 volts is given to the microcontroller board and LCD display. +12 Volts are used for Relay and All Other Driver.

3) 16 X 2 LCD DISPLAY:
It consists a user program area of RAM that can be programmed to generate any character that can be showed using a dot matrix. To controlling, the hexadecimal command byte 80H is used to indicate that the display RAM address 00H is selected. The display takes high time to performing its function. LCD bit 7 is monitored at logic high. Hence the display is not overwritten.

4) GSM MODEM:
The wireless modem works like a dial-up modem. The difference between is that dial-up modems send and receive data over fixed telephone lines, and wireless modems send and receive data over radio waves. In GSM mobile phones, a SIM card from the mobile phone provider is required for operating the GSM modem. The GSM modem is an external unit or a PCMCIA card (known as a PC card). External GSM modems connect to your PC via a serial cable, USB cable, Bluetooth, or infrared.

5) RELAY DRIVER:
We are using node MCU ESP8266 to control the relay and therefore electricity to Distribution area Through internet. The microcontroller output is not enough to drive the relay directly. Hence to drive a relay, use a relay driver uses a transistor as a switch.

# WORKING:

1) At First we have to insert our sim card in GSM . Then user start the circuit by connecting it to power supply and by switching on.
2) By Default it shows substation on the LCD display after switching on the circuit because we set substation string displayed on LCD in the code which is simulated by arduino nano.
3) Then the code initializes GSM module, collects a mobile number from the user through serial input and display the message “send msg store” on LCD Display.
4) The user have to send SMS of his mobile number with * to the circuit in which Sim card is inserted in the GSM like *9989113710. After sending sms to the circuit, the mobile number will get registered to the circuit.
5) After registering the mobile number, the circuit starts monitoring the electrical parameters like voltage, current, frequency, temperature.
6) The code is dumped into the Arduino nano and the minimum and maximum values of all electrical parameters are defined in the code.
7) The circuit monitors the values according to the predefined values mentioned in the code.
8) If the monitoring values exceeds the predefined range (or) minimum (or) maximum values of all electrical parameters, then buzzer produce a beep sound and GSM sends messages to the registered mobile number of the user about the status of the circuit like over current: 30, under voltage: 170 etc..
9) Then the user send SMS command to get the load on so that values can be controlled using potentiometers by the people who are near to the circuit and the SMS command to get the load on is *1#.
10) The surrounding area of the circuit is warned by the buzzer sound, then people near the circuit can control the voltage, current, frequency and temperature by using potentiometers.
11) While people controlling the circuit with potentiometers, then every controlled value is sent to the user mobile until the values come to predefined range.
12) If the values are controlled (or) came to the predefined range, then the user will not get alert messages.
13) If the user conformed about values are at predefined values, then user will off the load by sending another SMS command i.e; *2#.
14)  So, that load will be getting off and montoring of the values will be started and the process continues.

# ADVANTAGES

1) The immediate attention can take place if a variation happens in the sub- station parameters.
2) IOT based control is easy to identify the fault in any variant.
3) The various parameters can be modified and analyzed continuously through a network.

# APPLICATIONS

1) Sub-station
2) Power generation
3) Distribution area
