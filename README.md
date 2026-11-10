# EXPT 1b: Computation-of-DFT-using-FFT-ALGORITHM

## AIM
To perform and verify DFT using FFT-ALGORITHM by SCILAB.
## APPARATUS REQUIRED
PC installed with SCILAB
## PROGRAM 
### DFT FFT-ALGORITHM
```scilab
clc;
clear;
clf;

xn = [1,2,3,4,4,3,2,1];
N = length(xn);
n = 0:N-1;

Xk = fft(xn);

disp("FFT output:");
disp(Xk);

K = 0:N-1;
magnitude = abs(Xk);
phase = atan(imag(Xk), real(Xk));

y = ifft(Xk);

subplot(2,2,1);
plot2d3(n, xn);
xtitle("Input Sequence", "n", "x(n)");

subplot(2,2,2);
plot2d3(K, magnitude);
xtitle("Magnitude Spectrum", "k", "|X(k)|");

subplot(2,2,3);
plot2d3(K, phase);
xtitle("Phase Spectrum", "k", "Phase (radians)");

subplot(2,2,4);
plot2d3(n, real(y));
xtitle("Inverse FFT Output", "n", "x(n)");
### CALCULATIONS:
<img width="1575" height="1600" alt="image" src="https://github.com/user-attachments/assets/d474feaa-9d4c-4d01-a4e8-028ee38ae33f" />
<img width="1000" height="1600" alt="image" src="https://github.com/user-attachments/assets/95dbbc89-1219-4af5-a2d3-d36af8f22b71" />
<img width="1013" height="1600" alt="image" src="https://github.com/user-attachments/assets/0252b76f-80ea-4c26-89a7-eaa1dd857d42" />
<img width="899" height="1599" alt="image" src="https://github.com/user-attachments/assets/879b64c5-9ffa-4bd9-a23c-64eb03a8b2bd" />

### SAMPLE OUTPUT:
<br>
<img width="1080" height="1378" alt="image" src="https://github.com/user-attachments/assets/148530c8-09c9-4da4-87f0-72f4f4c1cf65" />

<br>



## RESULT:
Thus,  DFT using FFT-ALGORITHM for two given sequences were performed and its result was verified.

