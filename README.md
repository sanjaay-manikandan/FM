# FM

EXP NO: 4	GENERATION AND DETECTION OF FM


AIM:
To write a program for Frequency Modulation and Demodulation using SCILAB and to observe and measure the frequency deviation and the modulation index of FM.


EQUIPMENTS REQUIRED

•	Computer with i3 Processor
•	SCI LAB

THEORY:

Frequency modulation is a type of modulation in which the frequency of the high frequency (carrier) is varied in accordance with the instantaneous value of the modulating signal.
FREQUENCY DEVIATION f and MODULATION INDEX m f :
The frequency deviation f represents the maximum shift between the  modulatedsignal
frequency, over and under the frequency of the carrier.

We define modulation index m f the ratio between f and the modulating frequency
m= f / fm


FREQUENCY MODULATION GENERATION:
The circuits used to generate a frequency modulation must vary the frequency of a high frequency signal (carrier) as function of the amplitude of a low frequency signal (modulating signal). In practice there are two main methods used to generate FM.
Algorithm
1.	Define Parameters:
•	Fs: Sampling frequency.
•	T: Duration of the signal.
•	Fc: Carrier frequency.
•	Fm: Frequency of the modulating signal.
•	Beta: Modulation index, which controls the extent of frequency deviation.
2.	Generate Signals:
•	Modulating signal: Sinusoidal signal used for modulation.
•	Carrier signal: The high-frequency carrier signal.
•	Modulated signal: FM modulated signal calculated by varying the carrier frequency according to the modulating signal.
3.	FM Modulation:
•	Modulated signal is obtained by modulating the carrier signal with the modulating signal.
 
4.	FM Demodulation:
•	Differentiation: Computes the derivative of the modulated signal to extract frequency variations.
•	Envelope Detection: Takes the absolute value to retrieve the envelope of the signal.
•	Low-pass Filtering: Applies a Butterworth low-pass filter to smooth the envelope and recover the original modulating signal.
5.	Visualization:
•	Plots the modulating signal, carrier signal, FM modulated signal, and demodulated signal for analysis.



PROCEDURE


•	Refer Algorithms and write code for the experiment.
•	Open SCILAB in System
•	Type your code in New Editor
•	Save the file
•	Execute the code
•	If any Error, correct it in code and execute again
Verify the generated waveform using Tabulation and Model Waveform

MODEL GRAPH:

<img width="512" height="365" alt="image" src="https://github.com/user-attachments/assets/acd787bd-5281-4f1b-802f-1aa39fac9189" />


Program
```
Am=7.3;
Ac=14.6;
fm=577;
fc=5770;
fs=57700;
b=6.25;
t=0:1/fs:2/fm;
wm=2*3.14*fm;
wc=2*3.14*fc;
m=Am*cos(wm*t);
subplot(3,1,1);
plot(t,m);
c=Ac*cos(wc*t);
subplot(3,1,2);
plot(t,c);
efm=Ac*cos((wc*t)+(b*sin(wm*t)));
subplot(3,1,3);
plot(t,efm);
```

Output Waveform

<img width="1565" height="954" alt="FM Output waveform" src="https://github.com/user-attachments/assets/1269e57f-9b8e-4c00-ae41-2f429657353a" />


Tabulation

![FM Tabulation](https://github.com/user-attachments/assets/4d0697f9-3e9a-4570-bf9a-93c13e2746a8)


Calculation

![FM Calculation](https://github.com/user-attachments/assets/b1308491-f2fd-4008-9aaf-397d143e24db)


Frequency Deviation Practical = 4117.65

Modulation Index Practical	= 7.205

Modulation Index Theoretical	= 6.25


RESULT:

Thus, the frequency modulation and demodulation is successfully done and the output is experimentally verified.


