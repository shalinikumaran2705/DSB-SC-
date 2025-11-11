# DSBSC


EX NO: 2	DSB-SC-AM MODULATOR AND DEMODULATOR

AIM:

To write a program to perform DSBSC modulation and demodulation using SCI LAB and study its spectral characteristics

EQUIPMENTS REQUIRED

•	Computer with i3 Processor
•	SCI LAB

Note: Keep all the switch faults in off position

Algorithm:

1.	Define Parameters:
•	Fs: Sampling frequency.
•	T: Duration of the signal.
•	Fc: Carrier frequency.
•	Fm: Frequency of the message signal.
•	Amplitude: Maximum amplitude of the message signal.
2.	Generate Signals:
•	Message Signal: A sinusoidal signal that will be modulated.
•	Carrier Signal: A high-frequency sinusoidal signal used for modulation.
3.	DSBSC Modulation:
•	Modulated Signal: Multiply the message signal by the carrier signal to produce the DSBSC signal.
4.	DSBSC Demodulation:
•	Multiplication: Multiply the modulated signal by the carrier signal to get the product of the message signal with itself (i.e., the original message signal plus high-frequency components).
•	Low-pass Filtering: Apply a Butterworth low-pass filter to remove the high- frequency components and recover the original message signal.
5.	Visualization:
Plot the message signal, carrier signal, DSBSC modulated signal, and the recovered signal after demodulation.
PROCEDURE

•	Refer Algorithms and write code for the experiment.
•	Open SCILAB in System
•	Type your code in New Editor
•	Save the file
 
•	Execute the code
•	If any Error, correct it in code and execute again
•	Verify the generated waveform using Tabulation and Model Waveform

Model Waveform

<img width="703" height="679" alt="image" src="https://github.com/user-attachments/assets/e7c7c7f8-ccf2-41ac-b1f3-325989941a6f" />

Program
```
Am=11.5;
Fm=720;
Ac=23;
Fc=7200;
Fs=94000;
t=0:1/Fs:2/Fm;
em = Am*sin(2*3.14*Fm*t);
subplot(3,1,1);
plot(t,em);
xgrid;
ec = Ac*sin(2*3.14*Fc*t);
subplot(3,1,2);
plot(t,ec);
xgrid;
edsbsc = ((Am/2).*cos((2*3.14*Fc*t)-(2*3.14*Fm*t)))-((Am/2).*cos((2*3.14*Fc*t)+(2*3.14*Fm*t)));
subplot(3,1,3);
plot(t,edsbsc);
xgrid;
```

Output Graph

<img width="765" height="726" alt="image" src="https://github.com/user-attachments/assets/c52e6ea0-3e84-4d6f-87d7-c7ee5064ef02" />

Tablular Column

<img width="856" height="598" alt="image" src="https://github.com/user-attachments/assets/db6e366c-ab77-454a-b9ff-5d0a73f173c1" />

Result


Thus the DSB-SC-AM Modulation and Demodulation is generated.

