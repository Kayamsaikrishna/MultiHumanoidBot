# MultiHumanoidBot
A MULTI FUNCTIONAL HUMANOID ROBOT FOR INTERACTIVE AUTOMATION


This circuit appears to be a complex system incorporating an ESP32 microcontroller, various sensors (ultrasonic, line tracking, temperature), actuators (servos, DC motors), power management modules (buck converters), and output devices (loudspeakers, NeoPixel rings, fan). The ESP32 serves as the central processing unit, interfacing with sensors to receive environmental data, controlling actuators based on programmed logic, and managing outputs like sound and light. Power is supplied by a 12V battery [bonka lipo battery 35c] . The L298N motor driver controls the DC motors, and the PAM8403 module drives the loudspeakers. The servos are likely used for precise movement or positioning. The NeoPixel rings provide visual feedback or decoration.
Component List

Microcontroller
  ESP32 38 PIN: A microcontroller with a variety of GPIO pins for interfacing with sensors, actuators, and other peripherals.
                
Sensors
  HC-SR04 Ultrasonic Sensor: Measures distance by emitting ultrasonic waves and measuring the time taken for the echo to return.
  KY-033 Line Tracking Sensor: Detects lines or contrast on surfaces, commonly used in robotics for path following.
  Temperature Sensor (LM35): Measures ambient temperature with an analog voltage output proportional to the temperature.
                             Actuators
  Servo: A rotary actuator that allows for precise control of angular position.
  Hobby Gearmotor with 48:1 gearbox: A DC motor with a gearbox for increased torque, used for driving wheels or other mechanical parts.
  Fan: Provides airflow, possibly for cooling electronic components or for a specific application requirement.
       Power Management
  XL4015 5A DC Buck Step-down: A voltage regulator that steps down the input voltage to a lower output voltage. [convert to 4.50 - 5 v]
  L298N DC motor driver: An H-bridge motor driver that allows for control of the speed and direction of two DC motors.
  12V Battery: The main power source for the circuit. [bonka lipo battery]
  200W 20A DC-DC Buck Converter Step Down Module Constant Current LED Driver Module: converts a higher DC input voltage to a lower DC output voltage with constant current capability. It's commonly used for                                                                                      applications such as powering LED drivers, battery charging, and other electronic devices requiring stable voltage                                                                                            regulation.

Output Devices
  PAM8403: An audio amplifier module for driving loudspeakers.
  Loudspeaker: Converts electrical signals into sound.
  Adafruit 12 NeoPixel Ring: An LED ring with individually addressable RGB LEDs.

Miscellaneous
  Terminal PCB 2 Pin: A simple two-pin terminal block for making secure electrical connections.

Wiring Details
ESP32 38 PIN
  Connected to various components for control and data acquisition.
  Interfaces with sensors like the HC-SR04, KY-033, and LM35.
  Drives servos, NeoPixel rings, and controls the L298N motor driver.
  Manages power distribution from the XL4015 modules.
  HC-SR04 Ultrasonic Sensor
  VCC connected to 5V power supply.
  TRIG connected to ESP32 for triggering distance measurement.
  ECHO connected to ESP32 for receiving distance information.
  GND connected to ground.
  KY-033 Line Tracking Sensor
  VCC connected to 5V power supply.
  D0 connected to ESP32 for digital line detection output.
  GND connected to ground.
  Temperature Sensor (LM35)
  +Vs connected to 5V power supply.
  Vout connected to ESP32 for analog temperature reading.
  GND connected to ground.

Servos
  VCC connected to a regulated power supply from the XL4015 module.
  GND connected to ground.
  Pulse connected to various GPIO pins on the ESP32 for control signals.
  Hobby Gearmotor with 48:1 gearbox
  Connected to the L298N motor driver for control over motor speed and direction.
  PAM8403
  SPKR+ and SPKR- connected to loudspeakers for audio output.
  VCC connected to 5V power supply.
  GND connected to ground.

Loudspeakers
  Connected to the PAM8403 audio amplifier module.
  XL4015 5A DC Buck Step-down
  Input + connected to the 12V battery.
  Input - connected to ground.
  Output + connected to 5V power rails for components requiring 5V.
  Output - connected to ground.

L298N DC motor driver
  12V connected to the 12V battery for motor power.
  GND connected to ground.
  5V connected to 5V power supply (if jumper is in place, otherwise external 5V required).
  ENA, ENB connected to ESP32 for enabling motor outputs.
  IN1, IN2, IN3, IN4 connected to ESP32 for motor direction control.
  OUT1, OUT2, OUT3, OUT4 connected to gearmotors.

Adafruit 12 NeoPixel Ring
  VDD connected to a regulated 5V power supply.
  GND connected to ground.
  IN connected to ESP32 for data input (first ring).
  OUT connected to the IN pin of the next ring in series.
  Fan
  5V connected to 5V power supply.
  GND connected to ground.

