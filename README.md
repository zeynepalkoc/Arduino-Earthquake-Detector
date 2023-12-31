
# Arduino-Earthquake-Detector

# What I did use?
Arduino Nano (Personalized and Redesigned) and Arduino UNO
ADXL335 3 Axis Accelerometer
2x16 LCD Display
Led (Red and Green)
Resistors
Buzzer
Jumper Cables
Arduino IDE
Altium Designer
Processing 3
Tinkercad

# Tinkercad Connection Diagram
![enter image description here](https://camo.githubusercontent.com/7b78440662433823bd73caaef752d635df8223baa5cbe7299fa73dd1af6556b6/68747470733a2f2f692e68697a6c69726573696d2e636f6d2f6430337a3179302e4a5047)

    The sensitivity was very low when it was first turned on. In order to increase its sensitivity, 
    the AREF pin is connected to the 3V3 pin and the analogue inputs are set to 3.3V instead of 5V. 
    This made the ADXL335 work more smoothly.

# Conclusion and Discussion
I had the opportunity to test the project with artificial vibrations and real earthquakes and the expected results were obtained. Thanks to its small design, it adapts well to the place where it is intended to be mounted. The fact that this place is the columns of the building will enable the sensor to work more accurately. In addition, with Arduino, we can adjust how natural gas, water or other smart home systems of important systems should behave in case of an earthquake. Vibration waves can be watched and recorded live on Processing with the help of a computer. I designed an additional circuit to further increase its sensitivity.

    The main logic of this circuit was this: to amplify only the useful part of the signal without amplifying harmful noise.

> To do this, the instrumental operational amplifier i.e. OPAMP, connected in differential mode, OP07 IC can be used as an example. It can be used in any OPAMP IC. Using the potentiometer, we must set the voltage V2 to be slightly lower than V1 and set the utility signal with a second potentiometer. The formula for the amplification coefficient is

*Vout = (V1-V2) * K
K = 1 + 100 / P2 (kOhm)*

> This amplified signal must be connected to the analogue input of an Arduino microcontroller via a 1k resistor. To amplify the ADXL335's three outputs, we will need to use three identical amplifiers for each axis (x, y and z) separately.
