# LightControlBox

# description of circuit...

components:

Arduino board (e.g. Arduino Uno)
12V to 5V Voltage Regulator (e.g. LM7805)
Capacitors (e.g. 10μF and 0.1μF for smoothing)
Relays (6, rated for 12V and current as per load requirement)
Diodes (6, for relay protection, e.g. 1N4007)
Resistors (e.g. 10kΩ resistors for pull-downs)
Momentary Push Buttons (6)
12V power source (motorcycle battery)
Jumper wires
Breadboard or a custom PCB to solder the components
Here is a rough outline for wiring up this circuit. Note that this is just a starting point, and you might need to adjust this for your specific needs.

Connect the 12V line from the motorcycle to the input pin of the 7805 voltage regulator.
Connect a 10μF capacitor between the input of the voltage regulator and ground. Connect a 0.1μF capacitor between the output of the voltage regulator and ground. This is for smoothing.
Connect the output pin of the 7805 voltage regulator to the 5V pin on the Arduino.
Connect the ground pin of the voltage regulator to the ground of Arduino and the motorcycle battery.
Now, for each light/component (6 in total - running light, brake light, headlight, hi/low beam, left/right indicators):

Connect the normally open (NO) terminal of the relay to the positive terminal of the 12V battery.
Connect the common (COM) terminal of the relay to the positive terminal of the light/component.
Connect the negative terminal of the light/component to the motorcycle battery ground.
Connect the relay coil terminal to the corresponding Arduino digital pin (via a suitable resistor if necessary).
Connect the other relay coil terminal to the 5V output of the 7805 regulator.
Connect a diode in parallel with the relay coil for protection. The cathode of the diode should be on the 5V side, and the anode should be on the Arduino pin side.
For each momentary button:

Connect one terminal of the momentary switch to the 5V output of the 7805 regulator.
Connect the other terminal to both an Arduino digital pin and to the ground through a 10kΩ resistor as a pull-down.
Please ensure you are comfortable working with electrical systems before attempting any wiring on a vehicle. Also, take the necessary safety precautions when working with automotive electrical systems and consider consulting a professional if you have any concerns or uncertainties.
