# Logic-Trainer
Digital Logic Trainer for Electronics Lab Experiments

Finished: Atmega328 programming (handles LED matrixing over SERIAL, data taken in from I2C)

In progress: ESP32 programming. Handles the following:

1. Scans inputs for changes. FUNCTIONAL
   a. Will tie to interrupt to only handle when an input change is detected.
2. Scans buttons for changes. FUNCTIONAL
   a. Will tie to interrupt to only handle when an input change is detected.
3. Handles changing and tracking of button output modes. PARTIALLY FUNCTIONAL - Toggle and Momentary
   a. If ENTER is held, pressing the button for an output will change it between Toggle, Momentary, Pulse, and Clock
   b. Pulse and Clock are handled using the millis() timer for changing without user intervention.
   c. Will tie to interrupt (internal) for clock sync, such as counting in binary.
4. Updating Outputs over i2c. FUNCTIONAL
5. Updating LEDs over i2c, communicating with Atmega328. FUNCTIONAL


Desired Features:

OTA Updates - Partially Functional
The desired outcome is for the ESP32 to connect to wifi, access a github or cloud drive, check for a more recent file than its own and update if there is. Right now I only have OTA updates via a web interface. I would also like if the esp32 could update the ATMega328's files over i2c after updating its own. 

Web Interface for management - changing features, settings via a web interface

Web Interface for digital logic table creation - live graphs showing logic states. 

Web Interface for "Project Completed!" - testing if labs were successfully completed. 
