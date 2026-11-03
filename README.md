# Inverter-using-SPWM-DC-to-AC-
Maded the custom circuit in LTspice as well as in real hardware to convert DC into AC using SPWM scheme 
SPWM-Based DC to AC Inverter Using Arduino UNO

Project Overview

This project focuses on designing and implementing a DC-to-AC inverter using the Sinusoidal Pulse Width Modulation (SPWM) technique.

The project is divided into two major parts:

Part 1 – Software Simulation: Designing and simulating the inverter circuit in LTspice to analyse its switching behaviour and output waveform.

Part 2 – Hardware Implementation: Building the actual inverter circuit on a breadboard using Arduino UNO, N-channel MOSFETs, and passive components, followed by practical testing using an oscilloscope.

The objective is to understand the working principle of SPWM-based power conversion and compare theoretical simulation results with practical hardware performance.

PART 1 – SOFTWARE SIMULATION (LTspice)

Circuit Design and Simulation

The inverter circuit was designed and simulated using LTspice before proceeding with hardware implementation.

The simulation includes the power switching stage, SPWM switching behaviour, and LC output filter.

Simulation Circuit


<img width="1917" height="881" alt="Screenshot 2026-10-31 203745" src="https://github.com/user-attachments/assets/100c3dfe-02a3-4082-9416-ae08760ce8fb" />


Simulation Waveforms

The simulated waveforms were analysed to understand the switching operation and the effect of the LC filter on the inverter output.

Before LC filter output.

<img width="1917" height="1078" alt="Screenshot 2026-11-03 231627" src="https://github.com/user-attachments/assets/0e0cde88-f5f5-4ff9-96ef-9de507f2e0ea" />

After LC Filter output. 

<img width="1917" height="1078" alt="Screenshot 2026-11-03 222530" src="https://github.com/user-attachments/assets/da07b5b9-7573-42cc-92b2-df75d5bc63d5" />


Simulation Objectives

Analyse the H-bridge switching configuration.

Study SPWM-based DC-to-AC conversion.

Observe the output before and after LC filtering.

Understand high-frequency switching components.

Verify the expected output waveform.

PART 2 – HARDWARE IMPLEMENTATION

Practical Circuit Development

After completing the LTspice simulation, the inverter was physically implemented on a breadboard using the required electronic components.

The hardware consists of an Arduino UNO for SPWM signal generation, four N-channel MOSFETs arranged in an H-bridge configuration, and an LC filter for smoothing the output waveform.

Components Used

Component-[4 N channel MOSFETS , 2 MOSFET driver IC (each drives 2 MOSFETS) , one microcontroller board(I Used Arduino UNO) , 1uF capacitors(2) , 6 fast recovery diodes , Breadboard ,  For Filter (2X10 mH inductors , 2 x 2.2uF Capacitors) 



Hardware Setup

<img width="4080" height="1840" alt="IMG_20261101_194030" src="https://github.com/user-attachments/assets/dab6b8e0-3875-4785-ac56-9bfc69c9a837" />

<img width="8160" height="6144" alt="IMG_20261103_232000" src="https://github.com/user-attachments/assets/2a3fe20b-ddb8-40ba-9fa7-966474341d63" />

<img width="4080" height="1840" alt="IMG_20261103_232705" src="https://github.com/user-attachments/assets/be516801-64bf-4e7f-a738-7881a3712a1b" />


Oscilloscope Output

The hardware output was observed using an oscilloscope to examine the generated waveforms.

The oscilloscope measurements help demonstrate the actual switching behaviour and the effect of the LC filter on the output waveform.

 Filtered AC Output


<img width="4080" height="1840" alt="IMG_20261029_165955" src="https://github.com/user-attachments/assets/fc21c683-c01d-4474-ac9a-5284ca68acd6" />
<img width="3374" height="1840" alt="IMG_20261101_182824" src="https://github.com/user-attachments/assets/0ae169ba-14fd-486b-89c6-f6c1c899c0eb" />
<img width="4080" height="1840" alt="IMG_20261031_125743" src="https://github.com/user-attachments/assets/6047a423-6f2c-4f8d-92ca-f2e45e4b6a23" />
<img width="4080" height="1840" alt="IMG_20261029_153250" src="https://github.com/user-attachments/assets/5082c4fc-338e-4582-a4a7-911bae326aab" />




Working Principle

Arduino UNO generates SPWM signals using a sinusoidal reference.

The generated signals goes in MOSFET Driver ICs.

The ICs modulate the signal and increase the voltages of the SPWM signal.

The H-bridge produces a modulated output from the DC input.

The LC low-pass filter attenuates high-frequency switching components.

The filtered output approaches a sinusoidal AC waveform.

Tools and Technologies

Arduino UNO

LTspice

Arduino IDE

N-channel MOSFETs

H-Bridge Topology

Sinusoidal Pulse Width Modulation (SPWM)

LC Low-Pass Filter

Digital Oscilloscope

Key Learning Outcomes

Understanding SPWM generation.

Practical implementation of an H-bridge inverter.

MOSFET switching and power electronics.

LC filter design and waveform smoothing.

Circuit simulation using LTspice.

Hardware testing and waveform analysis using an oscilloscope.

Understanding the differences between simulated and practical circuit behaviour.

Future Improvements

Closed-loop output voltage regulation.

Improved MOSFET gate driving and protection.

Dead-time implementation.

Output voltage and current monitoring.

Improved PCB-based hardware implementation.

Project Status

Completed – LTspice Simulation and Breadboard Hardware Implementation.
