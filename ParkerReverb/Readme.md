VST3 and standalone Windows x64 application for Julian Parker's Faust reverb "JPverbRaw" as found here:

https://github.com/supercollider/sc3-plugins/tree/main/source/DEINDUGens/faust_src

To install the VST3 file, copy it to your VST3 plugins folder, e.g. 

C:\Program Files\Common Files\VST3

You can make folders under this one and (perhaps depending on your DAW settings) they will be found.  Using Ableton Live, I have to close the program before copying the VST3 file to this location.

https://github.com/HolyCityAudio/Plugins/blob/main/ParkerReverb/jpreverb.jpg

The cpp and jucer file were created from the DSP file using faust2juce.
There are some hand edits to the cpp file to change the default background color and the dialog name.

Use the cpp and jucer file with JUCE compiled by Visual Studio 2019.

* Early diff - early diffusion.  Below 0.707, noticeably rough attack.
* Size - "size" of the simulated space.  Adjusting in real time gives a slight pitch bend.
* t60 - reverb time.  Can get really long but one of the bands in the EQ section also has to be turned closer to 1.0.
* damp - damping.  Turn to 0 for longest reverbs, up to dampen reflections.
* wet - wet/dry mix
* lowX, midX, highX - equalizer to set balance of reverberated sound.  Controls reverb time per band.
* Xover - lowBand sets the crossover from lowX to midX.  highBand sets the crossover from midX to highX.
* Mod - modulation
* mDepth - depth
* mFreq - frequency

To be honest I cannot hear any impact of changing the Modulation settings.  I'm not convinced it's working properly.

![alt text](https://github.com/HolyCityAudio/Plugins/blob/main/ParkerReverb/jpreverb.jpg?raw=true)
