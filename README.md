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

The objectives: 
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


**Retrospective:** [full analysis on my site](https://eric-hur-21.github.io)

## Quantum Entanglement (CHSH Bell Test)

The objective:
1. Empirically quantify and demonstrate CHSH Bell Test

I learned to operate a quED SPDC source: a half-wave plate setting the pump to
45°, two Type-I crystals producing polarization-entangled pairs, motorized
polarizers, and fiber-coupled APDs feeding a coincidence counter. Polarization
carried the correlation. Fitting the coincidence curves in Python separated the
two signatures: the unentangled state factorizes as cos²α·cos²β, while the
entangled state depends only on the angle difference, ½cos²(β−α). CHSH gave
S = 2.241 ± 0.040 entangled and S = 1.404 ± 0.043 with the half-wave plate
removed, straddling the classical bound of 2. Uncertainties came from Poisson
counting statistics propagated through the S calculation.

**Retrospective:** [full analysis on my site](https://eric-hur-21.github.io)

## Quantum Key Distribution (BB84) 

*Reference: [Quantum Computation and Quantum Information by Isaac Chuang and Michael Nielsen
](https://www.amazon.com/dp/1107002176?lv=shuf&channelId=500&plpRedirect=mhFallback) page 582* 

The objective:
1. Demonstrate BB88 Quantum key distribution protocol 

I learned to run BB84 end to end on a quED system: a fiber beamsplitter and
three APDs generating quantum random bits, motorized half-wave plates and
polarizers encoding them, and quApp's BB84 mode transmitting and measuring.
Python handled the rest, sifting matched-basis detections into a 1024-bit key
and XORing it against a 32×32 image. Comparing Alice's and Bob's keys gave a bit
error rate of 4.30%, 44 mismatched bits, which appear directly as 44 flipped
pixels in the decrypted image. The key rate came to 23.51% against an ideal 25%.
The RNG showed a 41.7% bias toward zeros.

**Report:** [EE 400 Lab 3 (PDF)](./reports/lab3-bb84.pdf)
**Retrospective:** [full analysis on my site](https://eric-hur-21.github.io)

<img width="582" height="245" alt="image" src="https://github.com/user-attachments/assets/9fbd5cd1-9602-4a84-bf06-f973dd455192" />




## Tomography and Teleportation 


---

All the projects were completed in Spring 2025 Quarter. 
