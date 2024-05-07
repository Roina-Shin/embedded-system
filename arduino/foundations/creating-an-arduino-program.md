## Creating an Arduino program

- Here, we will take a tour of the Arduino IDE software. The Arduino IDE uses what we call a graphical text editor for writing code with all the word processing features like copy, cut, and paste.


- You notice that when you open the software, it comes in with a default starting code.


![arduino-ide](/pictures/arduino/arduino-ide/arduino-ide.PNG "arduino ide")


- Programs written using the Arduino IDE are called sketches. Go to the File in the menu bar and click Examples. You will different types of Examples there. Click Basics > Blink.


![file-examples](/pictures/arduino/arduino-ide/file-examples.png "file examples")


![blink-example-code](/pictures/arduino/arduino-ide/blink-example-code.PNG "blink example code")


- As mentioned, when you open the software, it comes in with a default code. And the code contains 2 functions:

  - **Setup** function

  - **Loop** function


- The Arduino program calls the setup function as the first thing when the Arduino unit powers up.


- So, any code you place in the Setup function in your sketch runs first, and it only runs one time.


- The Setup function is a great place to initialize input and output pins so they are ready to be used. 


- Then, the program moves to the loop function code. The program calls the code inside the loop function repeatedly until the Arduino board is powered off.


- Most of the time, we place the main code inside the loop function section. It is the heart of most sketches.


- This is where we tell the Arduino what to do in the sketch. Each time the sketch reaches the end of the loop function, it returns to the beginning of the loop. 


- For your program to run, you need to include both functions, setup and loop, in your sketch. 


## pinMode()

- Let's understand some of the main commands used with an Arduino IDE.


![digital-pins](/pictures/arduino/arduino-ide/digital-pins.PNG "digital pins")


- You can use each digital interface on the Arduino as either an input or an output, but not both at the same time. 


- Now, in order to tell the Arduino which mode your sketch uses for the specific digital or analog interface, we need to use **pinMode()** function.


- In pinMode() function, we basically configure at the specific pin in Arduino to behave either as an input or an output. 


```
pinMode(pin, mode)
```

- This is the way the function is written. The pinMode() function requires 2 parameters. The **pin** parameter determines the pin member to configure. The **mode** parameter determines whether the pin operates as an input or an output. 


There are 3 values you can use for the interface mode setting:


  - INPUT: normal input mode to receive a voltage.

  - INPUT_PULLUP: input mode that utilizes the Arduino's internal pullup resistor.

  - OUTPUT: normal output mode to send a voltage.


- We usually add the pinMode() function the Setup function.


![add-pinMode-function](/pictures/arduino/arduino-ide/add-pinMode-function.PNG "add pinMode function")



## digitalWrite()

- We use digitalWrite() function to output a value to a pin that has been configured as an output. The digitalWrite() function outputs a value on that specific pin.


```
digitalWrite(pin, value)
```


- The pin is for the configured pin that we want to specify, and the value is high or low.


```
digitalWrite(2, HIGH)
```


- If we want to turn on the LED, we send **HIGH** value. So, digitalWrite() on pin 2 and then HIGH.


- Now, if we want to turn it off, we send a **LOW** value. 


- We use the digitalWrite() function inside the void loop() function.


- Now, let's write our first sketch.


- We will define a varible called LED at the beginning and use it in our functions. Also, we will use **delay** to wait for a specific number of milliseconds before continuing on to the next line. If I write 2000 then I tell the machine to wait for 2 seconds before moving on.


![first-sketch](/pictures/arduino/arduino-ide/first-sketch.PNG "first sketch")


- After completing the code, make sure you select the right board and then go on to verify the code.


![select-the-right-board](/pictures/arduino/arduino-ide/select-the-right-board.png "select the right board")

