# Arduino Function Reference

This is a reference guide to common Arduino functions, expressions, and logic. Each item includes a brief explanation, syntax, an example code snippet, and some additional notes where necessary.

## Table of Contents

- [digitalRead](#digitalread)
- [digitalWrite](#digitalwrite)
- [analogRead](#analogread)
- [analogWrite](#analogwrite)
- [delay](#delay)
- [Serial.println](#serialprintln)
- [if..then..else](#ifthenelse)
- [millis](#millis)
- [constrain](#constrain)
- [=!](#not-equal)
- [map](#map)
- [array](#array)
- [for..loop](#forloop)
- [max](#max)
- [min](#min)
- [2D arrays](#2d-arrays)
- [nested for loops](#nested-for-loops)
- [user-defined functions](#user-defined-functions)
- [abs](#abs)
- [switch..case](#switchcase)
- [&&](#and)
- [+=, -=](#increment-and-decrement)

## digitalRead

**Explanation:** Reads the value from a specified digital pin, either HIGH or LOW.

**Syntax:** `digitalRead(pin)`

**Example:**

```arduino
int buttonPin = 2; // declare button pin
int buttonState; // variable to hold button state

void setup() {
  pinMode(buttonPin, INPUT_PULLUP); // set button pin as input
  Serial.begin(9600); // initialize serial communication
}

void loop() {
  buttonState = digitalRead(buttonPin); // read button state
  Serial.println(buttonState); // print button state to serial monitor
  delay(100); // wait for 100ms
}

// digitalRead(pin)
// Returns HIGH or LOW depending on the voltage level at the specified digital pin.
int buttonPin = 2;
int buttonState;

void setup() {
  pinMode(buttonPin, INPUT_PULLUP);
  Serial.begin(9600);
}

void loop() {
  buttonState = digitalRead(buttonPin);
  Serial.println(buttonState);
}
'''
## digitalWrite

// digitalWrite(pin, value)
// Writes a HIGH or LOW value to the specified digital pin.
int ledPin = 13;

void setup() {
  pinMode(ledPin, OUTPUT);
}

void loop() {
  digitalWrite(ledPin, HIGH);
  delay(1000);
  digitalWrite(ledPin, LOW);
  delay(1000);
}

// analogRead(pin)
// Returns a value between 0 and 1023 representing the voltage level at the specified analog pin.
int analogPin = A0;
int sensorValue;

void setup() {
  Serial.begin(9600);
}

void loop() {
  sensorValue = analogRead(analogPin);
  Serial.println(sensorValue);
  delay(1000);
}

// analogWrite(pin, value)
// Writes an analog value (PWM wave) to the specified pin.
int ledPin = 9;
int brightness =
