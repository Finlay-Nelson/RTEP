# RTEP

"EMG as user input to a gaming environment using a Raspberry Pi”

**PROJECT AIMS**

As part of the Real Time Embedded Programming course offered by the Engineering Department at the University of Glasgow, the remit of this project is the development, design, construction and promotion of a product requiring realtime operation. To this end, we aim to develop a system which uses electromyography (EMG) to read signals from select muscles, and use them to control the movement of an object in a video game. This system has two primary proposed uses:

1) A greater level of submersion of the user in the gaming environment, adding an extra dimension to the experience.
2) With development, the system could be used to encourage persistence with otherwise unpleasant rehabilitative exercise programs.

The system will turn the gamer into their own controller, and therefore, a less complicated game with fewer potential inputs is easier to both produce and play. We aim to first achieve this in a simple system, using only 2 inputs (left/right) to a rudimentary game such as the retro classic "Pong", validating the concept. Further work would then look to add a greater range of control options (up/down/jump etc) to more complex games, by incorporating the EMG signals from more muscles. 

**METHDOLOGY**

Two standard Ag/AgCl electrodes should be placed approximately 20cm apart on the muscle.
The signal from these electrodes is sent through a two stage amplifer, the first stage being the differential stage, 
the second being a gain stage. 
The output from the amplifiers is sent to an Analogue/Digital Converter (ADC) and then passed to a Raspberry Pi via the I2C bus protocol for post-processing and game connection. 

**PROGRESS** 

We have produced a working board with the AD7705 that reads a stream of data to plot, while we fabricate and test the EMG board. A successful QT program for realtime plotting has been produced, the basis of which is presented using "window.cpp". 
=======================================================================================
The chosen ADC has been changed from the AD7705 to the ADS1115, and can now read real time data using I2C. A version of Pong now runs based on input to the ADC, and displays on Android devices, transferring data via the User Datagram Protocol (UDP)

Only thing left to do is get some muscle signals!
