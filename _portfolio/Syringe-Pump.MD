---
title: "Cyber Scooter"
excerpt: "This custom electric vehicle can reach speeds of up 30 MPH and has a range of over 50 miles!"
header:
  image: /assets/img/Syringe_Pump_Portrait_Website.jpg
  teaser: /assets/img/Syringe_Pump_Portrait_Website.jpg
---

This automated syringe pump dispenses liquid at a custom flow rate (mL/min). This device ensures that fluids are delivered accurately at a steady rate. In a hospital setting, this can give healthcare workers peace of mind and save them time. The project utilizes 3D designed parts, electronics, and coding. The pump is driven by a stepper motor coupled to a lead screw. The screw turns at a set rate, pushing a carriage against the plunger to dispense liquid. This syringe pump features an LED light that turns green when running, yellow when paused, and red when out of liquid. It has a latching button to start and pause the motion of the pump. A switch is built in to stop the motion of the pump when the plunger has reached its limit. It is compatible with 10 mL and 20 mL syringes.

## Off-the-shelf Parts

Part | Quantity
--- | ---
250 mm lead screw with 2 mm pitch and 2 mm lead | 1
250 mm lead screw with 2 mm pitch and 8 mm lead | 1
1/4" x 8mm Flexible Coupling | 1
200 mm linear rod with 8 mm diameter | 2
LM8UU Linear bearing for 8 mm diameter rod | 2
2040 Aluminum Extrusion 1' Length | 1
Nema 17 Stepper Motor | 1
MEAN WELL RQ-65D AC-DC Power Supply Quad Output 5V 12V 24V 12V 4 Amp | 1
Arduino Uno | 1
A4988 Stepper Driver | 1
Small Breadboard | 1
Panel Mount Latching Push Buttons | 1
Limit Switch | 1
RGB Common Cathode LED | 1

## 3D Printed Parts

Part | Quantity
--- | ---
electronics box | 1
electronics box lid | 1
motor mounting plate | 1
lead screw support | 1
carriage | 1
back barrel stabilizer | 1
front barrel stabilizer | 1

## Arduino Code

This [Arduino code] sets the flow rate of the syringe pump. Enter the desired flow rate and syringe pump diameter.

## CAD Model
<iframe src="https://vanderbilt643.autodesk360.com/shares/public/SH90d2dQT28d5b6028111d35c611cb0d02c3?mode=embed" width="640" height="480" allowfullscreen="true" webkitallowfullscreen="true" mozallowfullscreen="true"  frameborder="0"></iframe>

## How to Operate
Define the flow rate and syringe pump diameter variables in the Arduino code. Upload the code to Arduino. Prepare the syringe with the desired fluid. Securely place the syringe between the front and back barrel stabilizers. The tip of 10 mL syringe goes in the lower hole on the front barrel stabilizer, with the flange of the 10 mL syringe going in the lower slot on the back barrel stabilizer. The tip of 20 mL syringe goes in the higher hole on the front barrel stabilizer, with the flange of the 20 mL syringe going in the higher slot on the back barrel stabilizer. Press the latching button to start the syringe pump, and press again to pause.

