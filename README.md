High Voltage Amplifier
======================

A high-voltage amplifier takes a lower voltage input signal -- e.g. from a 
function generator of some sort -- and amplifies it to a high voltage. In this
case, the output range is -200V to +200V. High voltage amplifiers can be used
for a variety of applications, such as driving piezos, or digital microfluidics
electrodes. 

This board was created in KiCad 6.0.4. 

![HV Amplifier](/docs/HVAmplifier_topoff.jpg?raw=true "HV Amplifier")

## A WARNING

This project can be dangerous. 200V is sufficient to kill you under
the right conditions. Even under the best conditions, it can give you a 
painful shock. You should not build this unless you know what you're doing.
If you do build this, you should handle it with caution. Be very careful about
what you touch when it is energized. Don't touch it with both hands
simultaneously. If you don't have to have it exposed, enclose it. Insulate
any wiring connected to the HV output.

## Description

This design uses the Apex PA88 high-voltage op-amp. These are fairly expensive
(~$250) at mouser, but I was able to find one for much cheaper on Ebay when I
built this. It also has a switching power supply which generates the positive
and negative high voltage rails from a 9V input. 

It can be operated at 100V, or 200V, based on whether the jumper JP1 is shorted.

The gain (Output voltage / control voltage) is adjustable from 15.9x to 60.2x,
using the potentiometer. At maximum gain, an input of 3.3V will provide an
output of 199V. 

When idle, it draws about 40mA when operating at 100V, and about 80mA at 200V. It
should be able to source about 4mA, although I have not tested under this kind
of load. For my application the current draw is much less. At some point I may
stress test it, but I am putting it off in case this test proves to be destructive!

## Enclosure 

I have provided some mesh files for a 3D printable enclosure. It requires some
M3 heat inserts (like [these](https://www.amazon.com/initeq-M3-0-5-Threaded-Inserts-Printing/dp/B073W2898C/))
and M3 screws to assemble. The STLs can be found in the [enclosure](enclosure/) 
directory.

![HV Amplifier](/docs/HVAmplifier.jpg?raw=true "HV Amplifier")


