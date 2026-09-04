//including libraries for code functionality
#include <AccelStepper.h>
#include <ezButton.h>
//pins are used to control the stepper motor with the AccelStepper library
AccelStepper stepper(AccelStepper::DRIVER, 3, 2);
//flowRate in mL/min to be set
double flowRate;
//Diameter of the pump to be given
double pumpDiam;
//steps per revolution of the motor is 200
int stepsPerRev = 200;
//8mm lead screw;
int screwLead = 8;
//variable to represent the constant ratio of 60 seconds per 1 minute
int secPerMin = 60;
//use area formula for a circle to calculate pi(r)^2 for cross sectional
area of syringe barrel with given pump diameter
//given pump diameter is adjusted to be 2mm less since diameter of inside
of syringe is less than syringe actual diameter
double barrelArea = M_PI * pow((pumpDiam - 2 ) / 2, 2);
//0.001 is for 1 mm^3 in 0.001 mL
double motorSpeed = (flowRate * stepsPerRev) / (0.001 * barrelArea *
secPerMin * screwLead);
//variables assigning each part of the LED wiring with its associated pin
number on the Arduino
int blue_LED = 9;
int green_LED = 10;
R & D Rascals, 13
 int red_LED = 11;
//variables for the button and switch with appropriate pin numbers
int currentButton;
int button = 7;
ezButton limitSwitch(6); //imported library allows for creation of the
limitSwitch object connected to pin 6.
void setup() {
  //speed for stepper motor
  stepper.setMaxSpeed(1000);
  stepper.setSpeed(motorSpeed);
  limitSwitch.setDebounceTime(100); //100 millisecond debounce time
  //used to set mode of each part of the LED wiring's associated pins,
  allowing for control of LED
  pinMode(red_LED, OUTPUT);
  pinMode(green_LED, OUTPUT);
  pinMode(blue_LED, OUTPUT);
  //sets the default pin value to HIGH meaning when pressed it switches to
  LOW
  pinMode(button, INPUT_PULLUP);
}
void loop() {
  //allows for the state of limitSwitch to be continuously updated.
  limitSwitch.loop();
  //variable to read if button is pressed or not
  currentButton = digitalRead(button);
  //checks if limit switch has been pressed or not
  int currentSwitch = limitSwitch.getState();
  //when the pump is running, and the limit switch has not been pressed
  yet, run the motor and turn the LED green.
  if (currentButton == LOW && currentSwitch == HIGH) {
    analogWrite(red_LED, (0));
    analogWrite(green_LED, (121));
R & D Rascals, 14

analogWrite(blue_LED, (0));
    stepper.runSpeed();
}
  //when the pump has been paused and the limit switch has not been
  pressed yet, LED turns yellow.
  if (currentButton == HIGH && currentSwitch == HIGH) {
    analogWrite(red_LED, (206));
    analogWrite(green_LED, (75));
    analogWrite(blue_LED, (0));
}
  //when the limit switch is in a low state (pressed), LED turns red.
  if (currentSwitch == LOW) {
   analogWrite(red_LED, (255));
   analogWrite(green_LED, (0));
   analogWrite(blue_LED, (0));
} }
