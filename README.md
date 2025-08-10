# VacuumCleaner
Lames

Vacuum cleaner robot with room mapping using mpu6050 and distance measuring sensors.
 <img width="452" height="458" alt="image" src="https://github.com/user-attachments/assets/36464427-6b92-4dfa-bff2-73d7dd23bfe8" />

The robot used a vacuum chamber to make a pressure difference thus making a vacuum effect that sucks air in at inlet.
![WhatsApp Image 2025-08-10 at 18 42 26_bb0a317a](https://github.com/user-attachments/assets/8084d072-f165-416c-be88-4d1f22aa11a2)

The chamber consisted of a high rpm brusless motor and a propeller.
![WhatsApp Image 2025-08-10 at 18 42 28_1f977b98](https://github.com/user-attachments/assets/973ccec5-55b6-43d8-97d2-dcd20521899f)

Assembly of the chamber and main body.
![WhatsApp Image 2025-08-10 at 18 42 22_3c0a6f0d](https://github.com/user-attachments/assets/82ccb641-5e6b-4a69-878e-33034b301e98)

The chamber motor was controlled by a relay connected to the MCU along with other sensors and encodersa as follows/
<img width="1497" height="736" alt="image" src="https://github.com/user-attachments/assets/ed89ebfa-7f0b-45a8-bcb6-30ea88cdbc96" />


Main PCB board was made to work with:
    -Esp32
    -L298n motor driver
    -Rotary encoders
    -Ulrasonic distance sensor
    -MPU 6050
    -Relay module
		-Servo

It also included Voltage dividers for 5v sensors to make them applicable to 3.3v logic level for esp32.
With indicating LED ,filter and decoupling capacitors and terminals for ease of wiring with other components.

Final PCB looks
<img width="930" height="720" alt="image" src="https://github.com/user-attachments/assets/b99d156c-6e45-4f41-a003-32b2167680dd" />


**Logic wise**
The robot would start from any location in the room preferably a corner and register the distance measured until the ultrasonic pick anything infront of it within a range of 30cm, it register that, and the robot truns until the ultrasonic sweep find a clear path infront of it again, then repeat the cycle again with all the data registered being saved in 2d array containg the data (turn angles, turn measured and converted to distance by the encoders and obstacles or walls detected by the ultrasonic)

With the ability to manually control the robot movement and vacuum ability utilizing the wifi capabilities of the esp32
![WhatsApp Image 2025-08-10 at 18 42 29_65807fcf](https://github.com/user-attachments/assets/8eff5842-6703-48b0-824a-ee4715485408)
