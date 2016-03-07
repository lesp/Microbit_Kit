# micro:bit breadboarding kit

## Parts list

* M4 Countersunk Machine Screw 12MM (FNCP4M12) X 5  
* Nylon M4 Nut (FN00710) X 5  
* M4 Nylon Washers (FN00702) X 5  
* Solid core hookup wire X 5 <<PART NUMBER\>\>
* Breadboard (PC01771) X 1
* Red LED (SC11575) X 3
* Yellow LED (SC08040) X 3
* Green LED (SC11573) X 3
* Buzzer (LS03776) X 1
* 330 Ohm Resistors (RE03797) X 10 
*   
<<Diagram of the micro:bit\>\>

## Assembly Instructions  

### IMPORTANT: Machine screws must be finger tight and not tightened using any tools or machinery. Doing so may cause damage to your micro:bit.  

* Insert M4 Countersunk machine screw into the socket marked "0", the screw head should be rest in the socket and face upwards, with the screw thread residing under the micro:bit board.  
* Flip the micro:bit over while holding the machine screw in place.  
* Take 1 nylon M4 washer and slip it over the screw thread.  
* Take 1 nylon M4 nut and loosely attach it to the machine screw thread, leave a gap of around 5mm.  
* Take 1 length of pre-cut wire. Wrap one end of exposed wire around the machine screw. Ensure that the wire is touching the machine screw and is secure.  
* Secure the nut to the machine screw so that the wire is held securely in place between the washer and the nut.  
* Repeat this process for the 4 remaining sockets.  
You should now have all 5 wires secured to each of the GPIO sockets. At the end of each wire there will be an exposed portion of the wire. This end can be inserted into the breadboard.  

## Simple Test of the components  
To test that our kit is working we need to use the following components

A breadboard

Red LED X 1

  
An LED has two "legs".

The longest leg is called the Anode and in a circuit current flows into the LED via this leg.

The shortest leg is called the Cathode and this is connected to Ground, often referred to as GND.

  
We shall be using a breadboard which enables projects to be prototyped and tested by pushing components into the breadboard. 

How a breadboard works is by thin strips of metal stretch horizontally across the board, known as rows, latching on to the components as they are pushed into the hole. Components in the same row are electrically connected, but to build a circuit we will also work vertically, known as columns. In the centre of the board there is a channel that serves as a divider, there is no connection between the two sides of the board, unless we use a component to bridge the divide.

For our first circuit we shall use the wires connected to 3V and GND. Insert the LED as per the illustration, with the long leg of the LED on the left of the board, the short leg of the LED should be inserted on the other side of the board.

Now take the wire from 3V and connect it *in-line *with the long leg of our LED. Now take the wire from GND and connect it*in-line* with the short leg of our LED.

![alt](https://github.com/lesp/Microbit_Kit/blob/master/Hardware_Test.png) 

The LED will now light up, confirming that our code is correct.

## Project 1 - Flash an LED  

With this test complete, remove the 3V wire from the breadboard. In its place add the wire from "0" instead.

You may have noticed that when we added the "0" wire to our circuit that nothing happened. This is because we haven't programmed it to do anything.

To program the micro:bit to flash an LED we shall use the Microsoft Blocks editor which can be found at [https://www.microbit.co.uk/create-code](https://www.microbit.co.uk/create-code) 

Click on "New Project" and the page will change to an editing window. This new window is blank but has a series of menus to the left.

Look for the menu labelled "Loops", left click on the menu and a series of blocks will appear. Using the left mouse button, click and drag "while true" from the menu and drop it into the main window. This loop will run any code inside of it forever.

Look back at the menu, find the Pins menu, left click on it and choose "digital write (0,1) 1 to pin P0". Drag this block and drop it inside of the loop. By default this block is set to turn on Pin 0\. In coding 1 is equal to on and 0 to off.

Now look for the Basic menu, left click on it and choose the "pause (ms) 100" block, drag it and place it under the previous block but inside of the loop.  Milliseconds is abbreviated to ms and 100 is equal to a tenth of a second. To change the pause to 1 second, left click on the value and type in the 1000\.

From the Pins menu grab another "digital write (0,1) 1 to pin P0" and place it under the pause block. This time change the value of "1" to "0" indicating that we wish to turn the pin off.

Finally add another "pause (ms) 100" block under the previous block but still inside the loop.