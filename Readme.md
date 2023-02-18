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
```

## digitalWrite

// digitalWrite(pin, value)
// Writes a HIGH or LOW value to the specified digital pin.
```arduino
int edPin = 13;

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

// Table of Contents:
// [digitalRead()](#digitalread)
// [digitalWrite()](#digitalwrite)
// [analogRead()](#analogread)
// [analogWrite()](#analogwrite)
// [delay()](#delay)
// [Serial.println()](#serialprintln)
// [if...else statement](#ifelse-statement)
// [millis()](#millis)
// [constrain()](#constrain)
// [map()](#map)
// [array](#array)
// [for loop](#for-loop)
// [max()](#max)
// [min()](#min)
// [2D arrays](#2d-arrays)
// [nested for loops](#nested-for-loops)
// [user-defined functions](#user-defined-functions)
// [abs()](#abs)
// [switch...case statement](#switchcase-statement)
// [logical AND operator](#logical-and-operator)
// [+= and -= operators](#-and--operators)

// digitalRead()
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

// digitalWrite()
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

// analogRead()
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

// analogWrite()
// Writes an analog value (PWM wave) to the specified pin.
int ledPin = 9;
int brightness = 0;

void setup() {
  pinMode(ledPin, OUTPUT);
}

void loop() {
  analogWrite(ledPin, brightness);
  brightness = brightness + 5;
  if (brightness > 255) {
    brightness = 0;
  }
  delay(50);
}

// delay()
// Pauses the program for the specified number of milliseconds.
void setup() {
  Serial.begin(9600);
}

void loop() {
  Serial.println("Hello, world!");
  delay(1000);
}

// Serial.println()
// Prints the data to the serial port as human-readable ASCII text followed by a newline character.
int sensorValue = 0;

void setup() {
  Serial.begin(9600);
}

void loop() {
  sensorValue = analogRead(A0);
  Serial.println(sensorValue);
  delay(100);
}

// if...else statement
// Executes a block of code if a specified condition is true, and another block of code if it is false.
int sensorValue = 0;

void setup() {
  Serial.begin(9600);
}

void loop() {
  sensorValue = analogRead(A0);
  if (sensorValue > 500) {
    digitalWrite(ledPin, HIGH);
  } else {
    digitalWrite(ledPin, LOW);
  }
  delay(100);
}

// millis()
// Returns the number
