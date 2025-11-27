# Dsbsc-using-Phyton

AIM:

To write a program to perform DSBSC modulation and demodulation using COLAB and study its spectral characteristics.

EQUIPMENTS REQUIRED

• Computer with i3 Processor • CO LAB.

Note: Keep all the switch faults in off position

Algorithm:

Define Parameters: • Fs: Sampling frequency. • T: Duration of the signal. • Fc: Carrier frequency. • Fm: Frequency of the message signal. • Amplitude: Maximum amplitude of the message signal.
Generate Signals: • Message Signal: A sinusoidal signal that will be modulated. • Carrier Signal: A high-frequency sinusoidal signal used for modulation.
DSBSC Modulation: • Modulated Signal: Multiply the message signal by the carrier signal to produce the DSBSC signal.
DSBSC Demodulation: • Multiplication: Multiply the modulated signal by the carrier signal to get the product of the message signal with itself (i.e., the original message signal plus high-frequency components). • Low-pass Filtering: Apply a Butterworth low-pass filter to remove the high- frequency components and recover the original message signal.
Visualization: Plot the message signal, carrier signal, DSBSC modulated signal, and the recovered signal after demodulation. PROCEDURE
• Refer Algorithms and write code for the experiment. • Open SCILAB in System • Type your code in New Editor • Save the file

• Execute the code • If any Error, correct it in code and execute again • Verify the generated waveform using Tabulation and Model Waveform

Model Waveform:

<img width="703" height="679" alt="503281973-bd22ca1a-4545-48f3-9e72-7a9a05b3809b" src="https://github.com/user-attachments/assets/71557e18-68cb-4e49-8b78-188d2add43e7" />

# Program
```asm
import numpy as np
import matplotlib.pyplot as plt
Am = 5.1     
Ac = 10.2   
fm = 437   
fc = 4370    
fs = 43700   
t = np.arange(0, 2/fm, 1/fs)
m = Am * np.cos(2 * np.pi * fm * t)
plt.subplot(3, 1, 1)
plt.plot(t, m)
c = Ac * np.cos(2 * np.pi * fc * t)
plt.subplot(3, 1, 2)
plt.plot(t, c)
s1 = (Ac + m) * np.cos(2 * np.pi * fc * t)
s2 = (Ac - m) * np.cos(2 * np.pi * fc * t)
s = s1 - s2
plt.subplot(3, 1, 3)
plt.plot(t, s)
```

# Output

<img width="706" height="530" alt="Screenshot 2025-11-27 113617" src="https://github.com/user-attachments/assets/5e12a812-84ee-400c-89ab-bd2a01c4a874" />

# Calculations:



# Result:

Thus the DSB-SC-AM Modulation and Demodulation using python is generated.


