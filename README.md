# Class-D-amplifier : ProjectEGO

## The individual blocks — oscillator, comparator, MOSFET switching, and LC filter

### Oscillator:
Option 1 — 555 Timer
Pros:
Very easy
Cheap
Great for learning
Cons:
Frequency drifts a bit
Doesn't produce a very linear triangle wave

Option 2 — Op-amp relaxation oscillator
Pros:
Beautiful triangle wave
Stable
Exactly how many educational analog circuits are introduced
Cons:
Slightly more components

Option 3 — Crystal oscillator
Ridiculously accurate.
Not useful for learning Class D fundamentals.

Option 4 — Microcontroller PWM
Amazing later.

-----------------------------------------------------------------------------------

(Since i chose to build a Op-amp relaxation oscillator)

## What is a Relaxation Oscillator?
A relaxation oscillator is a periodic signal generator that produces non-sinusoidal waveforms, for example, a square wave, triangular wave, or rectangular wave, using passive energy storage elements (for example, capacitors/ inductors) and nonlinear elements such as op-amps or transistors.

### A relaxation oscillator satisfies all the conditions below:
It must provide a non-sinusoidal waveform (of either voltage or current parameter) at the output.
It must provide a periodic signal or repetitive signal like a Triangular, Square or Rectangular wave at the output.
The circuit of a relaxation oscillator must be a nonlinear one. That means the design of the circuit must involve semiconductor devices like a Transistor, MOSFET or OP-AMP.
The circuit design must also involve an energy-storing device like a Capacitor or Inductor, which charges and discharges continuously to produce a cycle. The frequency or period of oscillation for such an oscillator depends on the time constant of its respective capacitive or inductive circuit.

<img width="550" height="531" alt="Screenshot 2026-08-02 060935" src="https://github.com/user-attachments/assets/69ec2842-c4e8-490c-b5a8-85b0506e6128" />

## Relaxation Oscillator Frequency Formula and Calculations
The relaxation oscillator frequency formula determines the oscillation rate based on circuit component values. Obviously, the frequency of oscillation depends on the time constant of C1 and R3 in the circuit. Higher values of C1 and R3 will lead to longer charge and discharge rates, thus producing lower frequency oscillations. Similarly, smaller values will produce higher frequency oscillations.

Here, R1 and R2 also play a critical role in determining the frequency of the output waveform. This is because they control the voltage thresholds that the C1 needs to charge up to. For example, if the threshold is set to 5V, then C1 only needs to charge and discharge up to 5V and 5V, respectively. On the other hand, if the threshold is set to 10V, then C1 is needed to charge and discharge to 10V and -10V.

# f = 1 / 2 x R3 x C1 x ln (1 + k / 1 - k)
## Here, K = R2 / R1 + R2
