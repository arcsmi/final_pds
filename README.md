# newvisuals.pd

Currently, newvisuals.pd is the only patch in this collection. It uses two MIDI inputs, *notein 1* and *notein 2*. When MIDI is received by these, visuals (objects) in the gem window are affected. Parameters that control these objects can be edited to the user's preference.

### Sphere object

- *notein 2* causes the sphere to collapse down to a small size and then grow.
- *notein 2* causes the number of sections in the sphere's wire frame to be randomised.

### Circle object

- *notein 1* causes a circle to fade in at the centre of the window.
- *notein 2* causes the circle to disappear as the sphere "collapses".

### Curve3d objects

- *notein 1* causes a random transform animation on each curve.

### Particles (triangle and circle)

- *notein 1* increases the speed of the particles.
- *notein 2* decreases the speed of the particles.

## Usage

To run this patch you will need [plugdata](https://plugdata.org/download.html) and the Gem external which can be installed in plugdata.

You will also need [loopMIDI](https://www.tobias-erichsen.de/software/loopmidi.html) so your DAW can communicate with plugdata and detect incoming MIDI (enable loopMIDI Port in plugdata settings -> MIDI -> MIDI Inputs).

To ensure MIDI data is being sent and recieved, keep loopMIDI running. In your DAW, send pure MIDI to the loopMIDI Port and select a channel e.g. *notein 1* detects input from channel 1. *Note: in Ableton you cannot send MIDI if there is an instrument on your track. To send MIDI from existing tracks you will need to duplicate them and remove the instrument, so you are left with one audio track and one track that sends pure MIDI.*