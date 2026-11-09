# EE186_Lab4_final

Part 2.

STM32L4R5 datasheet (DS12023 Rev 5), Section 6.3.21, Table 81 “ADC characteristics,” p. 214: Resolution,	Fast channels,	Slow channels
12-bit	5.33 Msps	4.21 Msps
10-bit	6.15 Msps	4.71 Msps
8-bit	7.27 Msps	5.33 Msps
6-bit	8.88 Msps	6.15 Msps

If we had no divider, the photo diode would simply pull the pin up to the supply voltage. We use a divider so that we can turn the variable resistance based on light into a voltage reading that can be processed at the pin.

Part 3.

Vout = B/2^n (Vref) = 9/2^12 (Vref) = 0.0022Vref.

The sampling rate determines how long a voltages is held before switching to a new value. Higher sampling rate makes the audio smoother and avoids aliasing.

Sine: Pure tone with no harmonics. Smooth and consistant. Square: Adding odd harmonics, sounds buzzy and contains more total power than sine wave. Sawtooth: Adds all harmonics. Tends to sounds aggressive or harsh.

The capacitor is meant to DC coupling the audio signal. There is no DC component of sound, so it would be a waste of power to drive the constant offset portion of the output into the actual load.
