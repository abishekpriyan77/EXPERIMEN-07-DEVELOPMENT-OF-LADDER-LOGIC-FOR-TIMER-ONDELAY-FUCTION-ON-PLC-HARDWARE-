### EXPERIMENT-07-DEVELOPMENT-OF-LADDER-LOGIC-FOR-TIMER-ONDELAY-FUCTION-ON-PLC-HARDWARE-

### AIM 
To develop and execute a ladder logic program using an ON-Delay Timer (TON) in Delta SV2 PLC, and observe its behavior on PLC hardware.
### Hardware & Software Required:
Component	Specification
PLC	Delta SV2 Series (e.g., DVP-SV2)
Programming Cable	USB to RS232/RS485
PLC Software	WPLSoft (for programming Delta PLCs)
Input Devices	Push Button (NO)
Output Devices	LED Indicator / Lamp
Power Supply	24V DC for I/O, 230V AC for PLC (as per specs)
### Theory:
An ON-Delay Timer (TON) starts counting after the input condition is TRUE. The output turns ON after the preset time elapses.

## TON Instruction Format in Delta PLC:
T0 K500  // T0 = timer number, K500 = 500 x 10ms = 5 sec delay
Wiring Diagram (Example):
PLC Input	Description
X0	Push Button (NO)
Y0	Output Indicator (e.g., lamp)
## Ladder Logic Diagram:


|-----[ X0 ]------------[TON T0 K50]------------------|
|                                               |
|-----[ T0 ]------------------------------------[ Y0 ]|

X0: Start push button
T0: Timer 0
K50: Time delay (K50 = 50 × 10ms = 0.5 sec)
Y0: Output coil (Lamp or LED)
## Steps to Program in WPLSoft:
1.	Open WPLSoft and create a new project.
2.	Select PLC Model: DVP-SV2.
3.	In the ladder editor: Add a normally open contact X0.
4.	Add a TON instruction for T0 with preset K50.
5.	Add a normally open contact T0 connected to coil Y0.
6.	Compile the ladder logic.
7.	Connect PLC via USB and download the program.
8.	Set PLC to RUN mode.
Procedure:
•	Wire the push button to X0 and lamp to Y0.
•	Power ON the PLC and load the program.
•	Press X0; the timer starts.
•	After 0.5 sec, Y0 turns ON.
•	Release X0; the timer resets.
### Observation Table:
S.No	Input (X0)	Time Delay (sec)	Output (Y0)
1	Pressed	0.5	ON
2	Not Pressed	0	OFF







### LADDER LOGIC
<img width="634" height="186" alt="560716680-5afe19af-04a0-470b-acf0-7c4d5db349b2" src="https://github.com/user-attachments/assets/4091a8bf-920d-4a16-8fdf-40983819d6f5" />
<img width="640" height="144" alt="560716698-79b74443-448b-40ba-8734-30e3fb636ddd" src="https://github.com/user-attachments/assets/71dd5336-504b-4155-8db4-56b1c7a3ee71" />

## MONITOR TABLE
<img width="1353" height="181" alt="560715254-6cc665a8-a14d-4a42-90ef-f86adc21dea6" src="https://github.com/user-attachments/assets/0de9946f-12c7-4dd8-a71f-5155cb6e0f62" />

###  HARDWARE SETUP 
![560720441-f1d6a94f-20a3-401f-83b8-1a0b88df7e9f](https://github.com/user-attachments/assets/65569da5-d816-4c44-8c3e-fb63bfcc7f7a)

### Conclusion:
The ON-Delay timer function was successfully implemented using Delta SV2 PLC. The output activated after a 0.5-second delay once the input was turned ON.
