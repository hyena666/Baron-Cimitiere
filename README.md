# Baron Cimitière
Baron Cimitière is a digital drums multiplatform application.
# ER-301 Custom Unit version:
It spawned as an ER-301 Custom Unit. ER-301 Sound Computer is an eurorack module manufactured by Orthogonal Devices. It allows the user to build powerful audio and control tools patching mid level objects via a very smart GUI. The units are in fact blocks of dsp made in C++ and glued together in LUA. The Lua environment (called "middle layer")is now open so that a user can patch the existing dsp blocks via coding. In the future the C++ layer will be exposed too for total freedom.

Baron Cimitière is patched in the GUI as i have no LUA skills.

Baron Cimitière is a sine-based digital percussion unit.

send it some gates, cvs, stepped or fluctuating randoms and hear it spit out sharp beats.

![ScreenShot](https://forum.orthogonaldevices.com/uploads/default/original/2X/5/55f72c2036bae2a67e3b0815273e8bff3219eaac.png)

controls are:

    - Gate - trigger it manually or send it whatever you want
    
    - A decay - decay\release control for amplitude
    
    - FB - amount of sine self modulation
    
    - Pitch - the Baron is tuned to C by default but you can mess with it here
    
    - P decay - decay\release control for pitch (useful to create the transient part)
    
    - P env amt - pitch envelope amount (tip: short p decay : high amt, long p decay : low amount)
    
    - Int PM - phase modulation index (more internal phase modulation = more harmonics)
    - PM pitch - tuning for the internal sine modulator
    
    - Dist - amount of distortion
    
    - P curve - positive values for log pitch decays, negative values for expo pitch decays
    


# Max\Msp version

I then ported the custom unit in Max 8. I'm learning Max in the very moment of patching this app so you'll see some probably unelegant and unefficient solutions but i managed to do it!

Actual 0.5.0 version sports internal sequencer and monome grid 128 varibright support for hands on experience!

![ScreenShot](https://forum.orthogonaldevices.com/uploads/default/original/2X/a/a2d64d8b5992d661c97335218ae0d4e897779149.png)

In the max version i added an internal sequencer made of three rows:

    - main sequencer: where you trigger the envelopes controlling amplitude and pitch
    
    - pm sequencer: where you trigger the envelope controlling phase modulation
    
    - dist sequencer: where you trigger the envelope controlling tanh~ distortion
    
You can then independently randomize the position of the playhead on all three sequencers, you can randomize the phase modulation oscillator frequency to main oscillator frequency ratio and the amount of distortion.    

You can now horizontally zoom in and out on all 4 envelopes for precise and intricate modulations on the micro-scale.

Two versions are available: 8 steps and 16 steps. The GUI's are different too.

I'm working on a proper max for live device.

The presets folder is an ongoing repo for the max/msp version presets. load them up with the "read" button. write your own collectin (and contribute here) with the "write" button after having stored your 6 presets.


some demos:

https://soundcloud.com/hyena/hyena-baron-cimitiere-tablas-er-301-version

https://soundcloud.com/hyena/hyena-baron-cimitiere-02-maxmsp-version-test

https://soundcloud.com/hyena/hyena-baron-cimitiere-test




