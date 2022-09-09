# VextraVisualTools
Various essential tools and techniques I collected and created for making music visuals.

# Quantizer

Add a BP_QuantManager to your map and set your preferred bpm in the details panel. 
Any actors inheriting the BPI_QuantizationEvents can listen to events that get fired every bar, half bar, quarter, etc etc.
The QuantManager uses Quartz and its clock will start right at play. You can disable auto-activation in the details panel, you will have to start the clock using a 
reference to the QuantManager. You can start the clock this way using the StartClock event, this event can also be fired to change the BPM.

# EffectController
Add a BP_EffectController to your map to activate various post-process effects. These effects are fully controllable in real-time and can be controlled using the sequencer,
though they do only work during PIE or builds due to the use of timelines. These effects are mainly copied from other plugins and assets, it is basically a wrapped-up
collection of stuff I like and use often.

They currently include:
Anamorphic lens flares
Normal Distortion
Cyber Scan

# Impact Generator
The EffectController can easily generate "impacts" to be used in the QuantManager or straight up in your sequencer. Options for an impact are set within a struct per-hit
so every impact can be totally different. These impacts are configured and fired using the "Play Impact Hit" event.
Current options include: chromatic aberration, camera shake, bloom and radial blur. The details panel of the EffectController contains a debug button together
with a debug struct for you to test out your impacts; though as mentioned above they only work during play.

# Extras
The materials folder includes a master decal material to use on meshes as well as a master caustics light function. The Epic Games folder contains local mist and
light beams made by the epic team.


 
