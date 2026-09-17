# EXPT 1: Computation-of-DFT-using-direct-method

## AIM
To perform and verify DFT using direct method by SCILAB.
## APPARATUS REQUIRED
PC installed with SCILAB
## PROGRAM 
clear;
clc;
x = [1, 2, 3, 4];

n = 0:length(x)-1;

omega = linspace(-%pi, %pi, 500);

X_dtft = x * exp(-%i * n' * omega);

mag = abs(X_dtft);

phase = atan(imag(X_dtft), real(X_dtft));

scf(0); // Open new figure

subplot(2, 1, 1);

plot2d(omega, mag, style=2);

xtitle("Magnitude Spectrum", "Frequency (\omega)", "|X(\omega)|");

xgrid();

subplot(2, 1, 2);

plot2d(omega, phase, style=5);

xtitle("Phase Spectrum", "Frequency (\omega)", "Phase (radians)");

xgrid();




<br>
### CALCULATIONS:
<img width="899" height="1599" alt="WhatsApp Image 2026-09-15 at 08 47 45" src="https://github.com/user-attachments/assets/238d98d3-3d1f-4f14-a3a0-bc9043c1f7a8" />
<img width="899" height="1599" alt="WhatsApp Image 2026-09-15 at 08 47 57" src="https://github.com/user-attachments/assets/38b63742-92ca-49c4-a768-4d6701092fb9" />



### SAMPLE OUTPUT:
<img width="1600" height="898" alt="WhatsApp Image 2026-08-08 at 09 00 23" src="https://github.com/user-attachments/assets/628d531f-7d92-4110-82bf-75d124c511a9" />


## RESULT:
Thus,  DFT using direct method for two given sequences were performed and its result was verified.

