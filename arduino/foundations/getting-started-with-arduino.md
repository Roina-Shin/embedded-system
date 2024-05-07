## Getting started with Arduino


### What you need to program Arduino

1. Hardware

A circuit board, containing a programmable microcontroller with input and output pins.


2. Software

An IDE, or integrated development environment, is used to write and upload the code to the Arduino.


### Microcontroller

- A computer chip with minimal processing power

- Typically designed for automatic control of external devices


### Arduino Uno

- The Arduino Uno is one of the most commonly used units for prototypes that require a simple microcontroller.


![arduino-board](/pictures/arduino/foundations/arduino-board.PNG "arduino board")


1. USB Port

- There's a standard USB port for connecting the unit to the computer. It's also used for powering Arduino Uno board, uploading the program sketches into the Arduino, and for communication.


2. 3. Power Connector / Voltage Regulator

- Power Connector is used to provide power to the Arduino board when it's not plugged into the USB port. It accepts voltage between 9 and 15 volt, depending on the board. You can also see the voltage regulator beside it.


4. Power Pins

- These provide 5 volt, 3.3 volt, and ground connections to power your circuit.


5. Reset Button

- The reset button is used to reset the Arduino board back to its default state and for debugging purposes.


6. Digital I/O Pins

- The Arduino Uno has 14 digital input and output interfaces. There are 6 digital interfaces for pulse width modulation. They are marked in Arduino using tilde (~) before the digital pin number. (3, 5, 6, 9, 10, 11)


7. Analog Pins

- On the other side, there are 6 analog interfaces. You notice that analog pins have an A beside the pin number. 


8. Onboard LEDs

- The Arduino Uno also has a three built in LEDs. The first one, which is a **green LED** that's marked **ON**, is used to indicate that the Arduino is receiving power. It's useful for debugging.


- We have **two yellow LEDs marked TX and RX** that indicate when receiving or sending data between the Arduino and a computer. They flicker rapidly during the sketch upload as well as during the CRL communication.


- And the last one, a yellow LED, marked L, is connected to the digital output pin number 13. You can use it for a simple program for debugging if needed. 


9. Microcontroller

- The ATmega328 Microcontroller is the brain of the Arduino. This is the chip that runs the programs you create in the Arduino IDE software. 


- The ATmega AVR microcontroller chip is a complete microcontroller system built into a single chip. 



## Digital interfaces / Digital Pins


- Let's take a look at digital pins.


![digital-pins](/pictures/arduino/foundations/digital-pins.PNG "digital pins")


- Digital values are signals that simply mean 0 or 1. So, it's either **ON** or **OFF**.


- The example is an LED. The light is either ON or OFF. 


![communication-pins](/pictures/arduino/foundations/communication-pins.PNG "communication pins")


- The pins in the Arduino are for sending or receving digital values. Some of the digital pins can be used for other secondary purposes. Depending on the program inside the microcontroller, pin 0 and pin 1 are communication pins. Pin 0 is a receiving pin and Pin 1 is a transmitter. (0-RX, 1-TX)


![pulse-width-modulation-pins](/pictures/arduino/foundations/pulse-width-modulation-pins.PNG "pulse width modulation pins")


- Pulse Width Modulation Pins are used for applications like running a motor. So, in Arduino Uno, there are 6 pins for **pulse width modulation**. You notice that the tilde symbol beside the number.


- Each of the digital interfaces on the Arduino can be used as either an input or an output. 



## Analog interfaces / Analog Pins


- Analog signals are simply signals that have a continuous range of values. In other words, they are not ON or OFF, but they are rather values in between. 


![analog-signal](/pictures/arduino/foundations/analog-signal.PNG "analog signal")


- For example, a temperature sensor, where you have a range of temperatures. A light sensor, the light intensity changes. Motor, different speeds for the motor. 


![example-analog-inputs](/pictures/arduino/foundations/example-analog-inputs.PNG "example analog inputs")


- In the Arduino board, the pins that are for the analog inputs are identified with a letter A. Labels range from A0 to A5 for Arduino Uno. For Arduino Uno, those are the only analog pins available. 


![analog-pins](/pictures/arduino/foundations/analog-pins.PNG "analog pins")


- In Arduino Mega, it has 16 analog pins. When working with analog signals, the Arduino board uses **Analog to Digital Converter, ADC**. This converts analog signals that are coming from the external devices through one of the Arduino pins into digital values that the Microcontroller can understand and work with. 


- Then, the program, the Arduino software, reads the digital values produced by the ADC to determine the original vale of the analog signal. 


- For most of the Arduino models, Analog to Digital converter is a **10-bit resolution**. This returns integer values between 0 and 1023. 


![analog-to-digital-converter](/pictures/arduino/foundations/analog-to-digital-converter.PNG "analog to digital converter")


- DAC, Digital to Analog Converter, translates a digital value into an analog signal that can be used to provide power to analog circuits.


- The DAC receives a value from the microcontroller and converts it to an analog voltage that can be used to provide signals to an analog device or a circuit.


![analog-pins](/pictures/arduino/foundations/analog-pins.PNG "analog pins")


- While the main function of the analog pins for most of the Arduino boards is to read and write an analog signal. The analog pins may be configured and used in exactly the same manner as digital pins of 0 to 13.



## Power Pins


![power-pins](/pictures/arduino/foundations/power-pins.PNG "power pins")


- Power pins are usually located on the left side of the Arduino board. The first one is a **VIN (Voltage In)**, labeled Vin or 9V. It is used when powering Arduino via external power adapter (as opposed to 5V USB).


- An example is when providing a voltage from external source, like a solar panel. Note that different boards accept different input voltages. 


- The **5 Volts** pin outputs regulated 5 volts from the regulator on the board to provide a voltage to your circuit.


- The **3.3V** provides an ouput of 3.3 volts. 


- And finally, the **GND (Ground) pins**. When we build circuits, it's important to have a common ground with Arduino, these are where we connect it.


