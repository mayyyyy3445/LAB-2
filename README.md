# LAB-2

This is a Tinkercad simulation of an Arduino Uno connected to a breadboard with five LEDs and current-limiting resistors.

Breakdown of the Circuit:
	1.	Arduino Uno:
	•	The microcontroller that controls the LEDs.
	•	It is powered via a USB cable.
	2.	Breadboard:
	•	Used to easily connect and arrange components.
	•	The LEDs are placed in a row.
	3.	LEDs:
	•	Five LEDs (blue, yellow, red, brown, and green) are connected to the Arduino.
	•	Each LED has its anode (+) connected to a digital output pin.
	•	Each LED’s cathode (-) is connected to the ground (GND) via a resistor.
	4.	Resistors:
	•	These resistors (likely 220Ω - 1kΩ) limit the current to protect the LEDs.
	5.	Wiring:
	•	LEDs’ anodes are connected to Arduino digital pins (possibly 2 to 6).
	•	Cathodes are connected to GND through resistors.
	•	The black wire connects the breadboard’s ground rail to the Arduino’s GND pin.

Functionality:
	•	The Arduino can be programmed to turn the LEDs on and off in a sequence.
	•	The sequence can be controlled via code (similar to the one I provided earlier).
	•	The LEDs can blink in patterns like:
	•	Sequential (one after another)
	•	Alternating (odd-even LEDs)
	•	All on, all off
	•	Random blinking

