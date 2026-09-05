# Quantum Technology Lab

> _"Assumptions kill an investigation." - Reacher_

**EE 400, University of Washington Seattle.** Ten weeks, four quantum technology
experiments and one extension.

PHYS 225 gave me quantum mechanics as theory. I took this lab course to see how
Rabi frequency, quantum key distribution, and entanglement behave on a bench.
What I did not anticipate was how much of the real work goes into identifying
and quantifying uncertainty. That looks obvious in retrospect, but I only
learned it by measuring.

Each experiment below links to a retrospective write-up on my site, where I work
back through the analysis with more care than the lab period allowed.

| # | Experiment | Description | Note |
| --- | --- | --- | --- |
| 1 | [Quantum State Control](#quantum-state-control) | Find the qubit resonant frequency, drive Rabi oscillations, and analyze performance using the spin of a defect in diamond. Demonstrates basic single-qubit functionality. | Nitrogen Vacancy (NV) center qubit. |
| 2 | [Quantum Entanglement](#quantum-entanglement) | Violate Bell's inequalities using an entangled photon source based on parametric down-conversion. Proves that non-local correlations exist in quantum systems. | |
| 3 | [Quantum Key Distribution (BB84)](#quantum-key-distribution-bb84) | Implement BB84 and analyze its performance using a single-photon source based on parametric down-conversion. Demonstrates fundamentally secure cryptographic key distribution. |  |
| 4 | [Tomography and Teleportation](#tomography-and-teleportation) | Explore quantum state tomography and teleportation on cloud quantum hardware. | |
| 5 |[Quantum Magnetometry](#extension-quantum-magnetometry) | Extend the Quantum State Control setup beyond the standard procedure, using the diamond defect spin as a magnetic field sensor. |  Extension of Experiment 1|


## Quantum State Control 

The objectives were: 
1. Determine the qubit energy levels
2. Drive coherent rotations between two qubit levels and measure Rabi frequency and qubit decay time
3. Experimentally determine the relationship between Rabi frequency and applied MW power

I learned to drive a full ODMR measurement chain: a SpinCore PulseBlaster
sequencing TTL pulses to the laser, the MW switch, and the lock-in reference; a
Windfreak generator setting microwave frequency and power; and an Ametek lock-in
amplifier pulling the photoluminescence signal out of noise. Sweeping 2750 to
3000 MHz resolved the eight transitions predicted from the four NV orientations.
Pulsed-ODMR narrowed the resonance to 2788 MHz, and Rabi oscillations gave
2.22 MHz at -15 dBm and 2.86 MHz at -12 dBm. 

**Report:** [EE 400 Lab 1 (PDF)](./reports/lab1-qubit-control.pdf)
**Retrospective:** [full analysis on my site](https://eric-hur-21.github.io)

## Quantum Key Distribution (BB84) 

*Reference: [Quantum Computation and Quantum Information by Isaac Chuang and Michael Nielsen
](https://www.amazon.com/dp/1107002176?lv=shuf&channelId=500&plpRedirect=mhFallback) page 582* 



## Quantum Entanglement



## Tomography and Teleportation 


---

All the projects were completed in Spring 2025 Quarter. 
