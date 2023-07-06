# Vehicle Theft Detection System

This GitHub repository contains the code and documentation for a Vehicle Theft Detection System. The system is a combination of a locking system and a tracking system, aimed at ensuring the correct accessibility of a vehicle and tracking it in case of theft.

## Hardware Components

The following hardware components are used in this project:

- Arduino Mega 2560: The Arduino Mega 2560 board is utilized because it provides 4 serial ports, which are required for the GPS and GSM modules.
- GPS Module (NEO 6M): The NEO 6M GPS module is used for tracking the vehicle's location.
- GSM Module (SIMCOM 900A): The SIMCOM 900A GSM module is used for sending SMS alerts to the vehicle owner and tracking the vehicle.
- 5V Relay Module: The 5V relay module is used to control the vehicle's starter motor and lock the engine.
- LED: An LED is used to simulate the starter motor.
- Switch: A switch is used to simulate the ignition key.

## Testing and Simulation

The individual components of the system were tested as follows:

- GPS and GSM: Online code samples available on the Arduino forum were used to test the GPS and GSM modules.
- Other Components: Unit testing was performed for the other components.

Simulation of the GPS and GSM functionality was done using PROTEUS, a software tool for simulating electronic circuits. However, please note that the circuit shown in the image within this repository is a dummy circuit and does not represent the actual connections used in the project. Due to limitations of the software used to design the circuit, it was not possible to create an accurate representation of the actual circuit.

## Functionality

The Vehicle Theft Detection System operates as follows:

1. The LED, acting as the starter motor, will start only if the correct password is entered through the switch, simulating the ignition key.
2. If an incorrect password is entered, the GPS and GSM modules interfaced with Arduino will track the vehicle's location and send an SMS to the owner containing the coordinates.
3. The vehicle will remain locked, as the relay will interrupt the flow of current and prevent the LED (starter motor) from engaging and unlocking the engine.
4. The system will continue to lock the vehicle until the correct password is entered.
5. When the system is active, the GSM module will send a message to the owner if the vehicle is in unauthorized hands. The SMS will also include a Google Map link to the vehicle's location.
6. In case of an incorrect password, the starter motor circuit (LED) will remain open even after the switch (ignition key) is engaged.

## Code and Operation

The code in this repository is developed to achieve the desired functionality described above. When the correct password is entered through the switch, an SMS will be sent, and the LED (starter motor) will be allowed to run. However, if an incorrect password is entered, an alert SMS with a Google Map link will be sent, and the relay will interrupt the flow of current, effectively locking the vehicle.
