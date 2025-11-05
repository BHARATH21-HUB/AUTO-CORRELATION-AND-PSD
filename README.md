# AUTO-CORRELATION-AND-PSD

## AIM
Write a program for Autocorrelation and Power Spectral Density (PSD) of signals in Scilab and verify the Wiener–Khinchin relation.

## EQUIPMENT NEEDED
Computer with Intel i3 processor (or higher)
Scilab software

## THEORY

The Wiener-Khinchin theorem states that the power spectral density of a wide sense stationary random process is the Fourier transform of the corresponding autocorrelation function.

<img width="719" height="146" alt="image" src="https://github.com/user-attachments/assets/69b34db8-277d-4ad1-950c-ec5edb0dd185" />

This relationship bridges the time-domain correlation and frequency-domain power representations of a signal.

## ALGORITHM

1. Load or Define the Signal: Input your time-domain signal.
2. Compute Autocorrelation: Calculate the autocorrelation function of the signal.
3. Compute Power Spectral Density (PSD):
4. Estimate the PSD using either:
5. Fourier Transform of the autocorrelation function, or
6. Methods like Welch’s periodogram.
7. Plot Results: Visualize both the autocorrelation function and PSD.

## PROCEDURE

1. Refer Algorithms and write code for the experiment.
2. Open SCILAB in System
3. Type your code in New Editor
4. Save the file
5. Execute the code
6. If any Error, correct it in code and execute again
7. Verify the generated waveform using Tabulation and Model Waveform

## PROGRAME
```
t=0:0.01:2*%pi;
x=5*sin(8*t);
subplot(3,2,1);
plot(x);
au=xcorr(x,x);
subplot(3,2,2);
plot(au);
v=fft(au);
subplot(3,2,3);
plot(abs(v));
fw=fft(x);
subplot(3,2,4);
plot(fw);
fw2=(abs(fw)).^2;
subplot(3,2,5);
plot(fw2);
```

## OUTPUT

<img width="819" height="610" alt="Screenshot 2025-11-05 094104" src="https://github.com/user-attachments/assets/6e59ae2f-c3fd-4c01-8b03-9400f2e914fa" />

## RESULT

Thus the Autocorrelation and PSD are executed in Scilab and output is verified.
