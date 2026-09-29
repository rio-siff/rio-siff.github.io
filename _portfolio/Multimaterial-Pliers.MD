---
title: "Multi-Material Pliers"
excerpt: "Multi-material needle nose pliers capable of picking up resistors."
header:
  image: /assets/img/Pliers_with_Resistor.JPG
  teaser: /assets/img/Pliers_with_Resistor.JPG
toc: true
toc_label: "Table of Contents"
toc_sticky: true
toc_icon: bars
---

Print-in-place parts are multiple-component prints that contain moving or interlocking parts. These designs can be used immediately after printing with no post-print assembly required. Print-in-place parts can be produced with one material through careful 3D design, consideration of clearances, and orientation on the print bed. Print-in-place parts can also be created using two materials with a multi-material printer. Elastic plastic is used to create a flexible joint between rigid plastic parts. Print-in-place parts are useful because they do not require assembly time or assembly materials such as bolts, screws, and glue. Examples of print-in-place applications include this [fun octopus toy](https://all3dp.com/2/coolest-print-in-place-3d-models/) and this [spring loaded box](https://www.instructables.com/Print-in-Place-Spring-Loaded-Box/).  

The goal of our project was to design and print needle nose pliers capable of picking up through-hole resistors. The pliers must be multi-material and contain a spring component made out of flexible material that returns the pliers to the open position when not in use. Since there was only one multi-material printer in the lab, we were allowed to print the parts on separate printers and then assemble the pliers by hand. 

## Design Decisions
Materials: The spring component of the pliers was printed with TPU. The handles, jaws, and pivot were printed with PLA.

Pivot: The pivot allows the handles to smoothly rotate the jaws. For clearance, I gave the top pivot ring an inner diameter of 10.2 mm and the bottom pivot pin a diameter of 10.0 mm.

Skinny jaws: After practicing with various pliers in the Digital Fabrication lab, I choose skinny jaws in the shape of a “V” for my plier model instead of larger claw jaws. I chose the “V” design because this shape allows the jaws to easily come together and pick up the resistor, while being simple to design and print.

Small size: I chose to make my pliers small so that they could easily fit in my hand. This allows me to easily hold and operate the pliers, while also saving material and print time.

Straight leaf spring: I chose the straight leaf spring design because of its design simplicity and effectiveness. Applying pressure on the handles causes the spring to bend, storing elastic energy. Releasing the pressure on the handles causes the spring to release the stored energy and return the pliers to the open position.

Dovetail joints: I chose dovetail joints to attach my spring to the handles as these joints securely held the spring in place, while still allowing easy attachment of the spring to the handles.

Spring placement: Placing the spring further from the pivot causes a stronger reopening force but requires more force to close the pivot. I wanted the pliers to spring open quickly when released, so placed the spring about three quarters the length of the handles from the pivot.

Two mirror components: The plier contains 3 components- the bottom component, the top component, and the spring component. The bottom part of the plier has one jaw, one handle, the pivot pin base, and the pivot pin. The top part of the plier has one jaw, one handle, and the pivot ring that secures the pivot pin. The bottom and top pivot sketches are mirrors of each other. To make the top part, I simply made a copy of the bottom part sketch, rotated by 180 degrees, and extruded in the appropriate directions.

Parameters: I parameterized the lengths of the dovetail joints and pin diameter across all three components to streamline design iterations.

## Iterations
From my first print, the pivot worked well and without the spring, compressing the handles easily closed the jaws. However, when the spring was placed in the handles, the pliers were difficult to compress, and the jaws could not close. At 4.0 mm, the spring was too stiff to easily close the handles. In addition, the sharp edges of the handles made the pliers uncomfortable to hold.

![first iteration](/assets/img/First_Print.JPG)

For the second print, I changed the spring thickness from 4.0 mm to 2.5 mm. At this thickness, the handles closed easily but still sprang open quickly. I added fillets to the handles to make the pliers comfortable to hold. I also lengthened the handles for an improved fit in my hand. The new adjustments made the pliers comfortable to hold and easy to work with. With this print, I was able to quickly pick up resistors, hold the resistors in the pliers, and return the resistors to the table. 

![second iteration](/assets/img/Second_Print.JPG)

## CAD Model
<iframe src="https://vanderbilt643.autodesk360.com/shares/public/SH90d2dQT28d5b602811e1f197d4b5897920?mode=embed" width="640" height="480" allowfullscreen="true" webkitallowfullscreen="true" mozallowfullscreen="true"  frameborder="0"></iframe>

## Plier Specifications

Part | Measurement (mm)
--- | ---
Jaw length | 34.0
Jaw capacity | 14.7
Center diameter | 20.0
Width of handles | 65.4
Length of pliers | 125.5
Thickness | 11.0

## Print Settings
I used the standard print settings and printed on a Voron printer.

Elastic 95A TPU - 0.6 mm nozzle

| Setting | Value |
|---|---|
| Perimeters – Contour | **2 minimum** |
| Wall Thickness | **0** |
| Spiral Vase | **Off** |
| Solid Layers – Top | **4** |
| Solid Layers – Bottom | **3** |
| Minimum Shell Thickness – Top | **0 mm** |
| Minimum Shell Thickness – Bottom | **0 mm** |
| Sparse Infill Pattern | **Gyroid** |
| Infill Density | **25%** |
| Top Infill Pattern | **Monotonic** |
| Supporting Dense Layer | **Off** |
| Only One Perimeter on Top Surfaces | **On** |
| Detect Overhangs | **On** |
| Seam Position | **Rear** |
| Fuzzy Skin | **None** |

Rigid PLA - 0.6 mm nozzle

| Setting | Value |
|---|---|
| Perimeters – Contour | **3 minimum** |
| Wall Thickness | **0** |
| Spiral Vase | **Off** |
| Solid Layers – Top | **3** |
| Solid Layers – Bottom | **3** |
| Minimum Shell Thickness – Top | **0.8 mm** |
| Minimum Shell Thickness – Bottom | **0.8 mm** |
| Sparse Infill Pattern | **Gyroid** |
| Infill Density | **15%** |
| Top Infill Pattern | **Monotonic** |
| Supporting Dense Layer | **Off** |
| Only One Perimeter on Top Surfaces | **On** |
| Detect Overhangs | **On** |
| Seam Position | **Rear** |
| Fuzzy Skin | **None** |

## Photos
![Pliers in Action](/assets/img/Plier_In_Action.gif)
![Pliers with Resistor](/assets/img/Pliers_with_Resistor.JPG)
![Pliers Closeup](/assets/img/Pliers_Closeup.JPG)






