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

CODE:

// Define LED pins
const int led1 = 2;
const int led2 = 3;
const int led3 = 4;
const int led4 = 5;
const int led5 = 6;

void setup() {
  // Set LED pins as OUTPUT
  pinMode(led1, OUTPUT);
  pinMode(led2, OUTPUT);
  pinMode(led3, OUTPUT);
  pinMode(led4, OUTPUT);
  pinMode(led5, OUTPUT);
}

void loop() {
  // 1. Chase Effect: LEDs turn on one by one
  for (int i = 2; i <= 6; i++) {
    digitalWrite(i, HIGH);
    delay(200);
    digitalWrite(i, LOW);
  }

  // 2. Alternating Blink: Odd LEDs ON, then Even LEDs ON
  digitalWrite(led1, HIGH);
  digitalWrite(led3, HIGH);
  digitalWrite(led5, HIGH);
  delay(500);
  digitalWrite(led1, LOW);
  digitalWrite(led3, LOW);
  digitalWrite(led5, LOW);

  digitalWrite(led2, HIGH);
  digitalWrite(led4, HIGH);
  delay(500);
  digitalWrite(led2, LOW);
  digitalWrite(led4, LOW);

  // 3. All LEDs Blink Together
  for (int i = 0; i < 3; i++) {  // Repeat 3 times
    digitalWrite(led1, HIGH);
    digitalWrite(led2, HIGH);
    digitalWrite(led3, HIGH);
    digitalWrite(led4, HIGH);
    digitalWrite(led5, HIGH);
    delay(300);
    digitalWrite(led1, LOW);
    digitalWrite(led2, LOW);
    digitalWrite(led3, LOW);
    digitalWrite(led4, LOW);
    digitalWrite(led5, LOW);
    delay(300);
  }
}
