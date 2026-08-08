# EXPT 1: Computation-of-DFT-using-direct-method

## AIM
To perform and verify DFT using direct method by SCILAB.
## APPARATUS REQUIRED
PC installed with SCILAB
## PROGRAM 
### DFT DIRECT METHOD
```
clear;
clc;

x = [1, 2, 3, 4, 4, 3, 2, 1];
N = length(x);
n = 0:(N-1);
k = 0:(N-1);

// Compute DFT using fast vectorized matrix multiplication
Xk = x * exp(-%i * 2 * %pi * n' * k / N);

mag = abs(Xk);
phase = atan(imag(Xk), real(Xk));

disp("Computed DFT values X(k):");
disp(Xk);

figure(1);
clf();

// Define a soft background grid color
bg_grid = color("lightgrey");

// 1. Input Sequence
subplot(3, 1, 1);
plot2d3(n, x, style=2); // style=2 makes the stem line Blue
plot(n, x, 'ro', "MarkerFaceColor", "red", "MarkerSize", 6); // Large filled red circles
xtitle('Input Sequence', 'Time (n)', 'Amplitude x(n)');
xgrid(bg_grid);

// 2. Magnitude Spectrum
subplot(3, 1, 2);
plot2d3(k, mag, style=2);
plot(k, mag, 'ro', "MarkerFaceColor", "red", "MarkerSize", 6);
xtitle('Magnitude Spectrum', 'Frequency Index (k)', 'Magnitude |X(k)|');
xgrid(bg_grid);

// 3. Phase Spectrum
subplot(3, 1, 3);
plot2d3(k, phase, style=2);
plot(k, phase, 'ro', "MarkerFaceColor", "red", "MarkerSize", 6);
xtitle('Phase Spectrum', 'Frequency Index (k)', 'Phase (radians)');
xgrid(bg_grid);
```
### CALCULATIONS:

<img width="984" height="1600" alt="image" src="https://github.com/user-attachments/assets/c8bc23d6-6c3b-4cb3-8757-631d66525094" />
<img width="1002" height="1600" alt="image" src="https://github.com/user-attachments/assets/e81a28fa-fad3-46da-8003-6c49aeb7d9d8" />

### SAMPLE OUTPUT:

<img width="1536" height="704" alt="image" src="https://github.com/user-attachments/assets/1fc01b91-391a-40f7-8c57-db95a1ddcba3" />

## RESULT:
Thus,  DFT using direct method for two given sequences were performed and its result was verified.

