![](Pasted%20image%2020250707115647.png)
![](Pasted%20image%2020250707130821.png)
# Working principle
This 3-stage ring oscillator works by taking advantage of the second Barkhausen's criterion - making the phase around the loop 360°.
The amplifier stage is a MOSFET in a common source configuration. This offers a 180° phase shift. Then the RC circuit in combination provides a certain phase shift that after 3 stages of 180° inversions, offers a total 180° phase shift so that the total phase shift becomes 360°.
Thus we see that the phase shift offered by each RC circuit must be 60°. This implies that the operating frequency will be $\sqrt{3}$ times the pole frequency.
At a frequency $\sqrt{3}$ times the pole frequency, the signal will experience a diminishing of 50%.
Thus we require the minimum gain of each MOSFET CS amplifier to be 2 so as to satisfy the first Barkhausen's criterion.
# Frequency
We can do an FFT on the waveform output to see how close to a pure sinusiodal wave the output is (what the amount of phase noise is):
![](Pasted%20image%2020250707134923.png)
# Power Supply Sensitivity
Since changing the supply voltage will change the operating point of the MOSFET, and thus its gain, it will also change the amplitude and frequency of the wave. 
Here is a plot of the outputs with different supply voltages:
![](Pasted%20image%2020250707135901.png)
![](Pasted%20image%2020250707135930.png)
This can enable it to be used as a VCO in a radio frequency modulator, but the variance in frequency is not linear with the change in supply voltage.
