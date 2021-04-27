# Project OizysAMP

**Designer**: Maxim Vovenko

## Warning:
This was designed in High School for a club called AVBotz, this work predates my studies of EE at San Jose State University. Reuse Design at your own peral, Im not responsible for anything that happens or gurentee this works. This is only stored for historical record.

## Description:
This is the Hydrophone Amplifier Code name "Oizys". The code name reflects the absord amount of time 
figuring out how to make the amplifier and the amount of rivisions that have been trashed. This is the 
First version of the amplifer wich has been designed based on reasearch and simulations run in LTSpice
by Analog Devices. Oziys board is a three stage amplifier and filter combo witch has been tunned to
filter out signals below 20khz and above 55khz. The recommended sample rate is above 200khz. The board
Consists of three stages each one is powered by an ad8676 dual channel opamp. Dual channel opamps were
selected due to the relative little cross talk they have and there ability to process two signals at a
time. Stage one is a preamp/decoupling stage witch is required due to the use of piezoelectric 
Hydrophones. A 1 giga ohm resistor is used to stabalize and prevent saturation of the piezoelectric 
element. Stage two is an amp stage with the ability to be set to static out-put or variable output by 
selecting weather you use resistors R2A/R2B or trimpots vr1/vr2 respectively. Stage 3 is an anti-aliasing 
filter prioritizing speed over atenuation. There is a final passive stage wich offsets the signal by 1.64v 
using a high pass filter with ground replaced by 1.64v. The amp is to be tuned to function within 0-3.3v.
Resources used to build this design are included and so is a BOM.

While the material distrubuted with the mit license I can not and do not take credit for any work done except
for the following files: HydrophoneAmpliferCircuit.sch, HydrophoneAmpliferCircuit.brd, README.md, BOM.ods,AmpV0.asc
the files listed above are as a result of my work and are as a result covered under MIT License.

## Software Used: 
Eagle, LTSPICEXVII

## Known Issues:
-Design is suboptimal, the stages for amplification and signal conditioning should be reversed to prevent clipping
-Power Supply instantly fails under _any_ transient voltage spikes.
-Improper Crimping may result in damage to power supply due to no reverse polarity protection being present and software engineers not being able to decode wire coloring.
-The reference voltage is coupled to the signal producing artifacts in the signal, this needs to be decoupled.
-Gain calculations may be off by factor of 10, recalculation required (Symptoms: Signal observed to be in 10mv range instead of 1v).


## Revision History:
V1.2
-Updated License
-OpenSourced with MIT License
-Updated Silkscreens to reflect new state of the project.

V1.1
-Miscillaneous changes
-Moved around silkscreen for ease of assembly
-DRC Check Cleared
-Added OshaPark DRC

V1.0
-Finalized Schematic
-Created and finalized board layout and traces.
-Created Silk Screens.

V0.3
-Finalized Schematic
-Updated Library With Necessary Componets
-Organized BRD slightly before building final board

V0.2
-Semi-final design
-LTspiceXVII Simulation Files Added
-1.6V Rail Created 
-1.6v Filtering added using 1uf
-Identified resistor to replace with pot
TODO:
-Calculate Amplifier Circuit to add calibration ability
-Add C Filtering to 24v rail
-Add C Filter 12v
-Add C Filter -12v 

V0.1.1
-Renamed to  "Project OizysAMP"
-Updated Capcitors In Filtering circuit to accuratly reflect components being installed
-Lost hope in humanity
-Wished that power supply filtering was as easy as it is to say power supply filtering

V0.1
Initial Incomplete design
-Missing Power supply filtering
-missing connectors
-Missing Board Design
-missing design constraints
-Completed amplyfiying circuit
-Missing trim pot for tuning amp circuit
-Testpoints were added to faciilitate diagnostics.

**Copyright (c) 2020 Maxim Vovenko**

Software is hereby defined to be any and all digital files needed to produce a 
physical copy of the design as described by these digital files as well as any
physical designs produced utilizing the original files.

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
