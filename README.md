# ADSR exponential envelope generator with range switch (4HP)

An updated version of the ADSR module - functionally the same as its predecessor, albeit with a couple of changes. The range switch is now broken out to the faceplate for easy access, and the mainboard is parallel to the faceplate, rather than perpendicular to it - hence it's a lot shallower.

This is an updated envelope generator which uses a 555 timer configured as a Schmitt trigger (see: https://www.nutsvolts.com/magazine/article/555-monostable-circuits - figure 15 in particular) from which the envelope is generated. The net result is something that not only triggers at around 1V but also has far fewer parts.

I'm going to call that a win, and it isn't dissimilar to the design that Doepfer use in their EG modules, albeit without the bells and whistles.

In addition, I've 'borrowed' a couple of features from a Rene Schmitz design, specifically: the resistor R13 is optional, but adding it will give the input a bit of hysteresis (the degree of which is governed by the values of R13 - 1MΩ is what I use) which is handy if you're using a slowly changing waveform as a trigger.

Secondly, there's a buffer between the sustain and decay pots which removes any interdependence between the two. It also uses up an otherwise uncommitted op-amp.
