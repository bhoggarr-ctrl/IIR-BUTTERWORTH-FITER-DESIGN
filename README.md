# EXP 3 : IIR-BUTTERWORTH-FITER-DESIGN

## AIM: 

 To design an IIR Butterworth filter  using SCILAB. 

## APPARATUS REQUIRED: 
PC installed with SCILAB. 

## PROGRAM (LPF): 
```clc;
clear;


Fs = 5000;


fc = 1500;
Wn = 2 * fc / Fs;


b = [0.2452  0.4904  0.2452];
a = [1.0000  -0.8683  0.2569];


N = 512;
[H, f_norm] = frmag(b, a, N);


f = f_norm * Fs;


clf();
plot(f, 20 * log10(H + %eps));
xlabel("Frequency (Hz)");
ylabel("Magnitude (dB)");
title("Butterworth Low Pass Filter (Order 2) — fc = 1500 Hz");
xgrid();
```

## PROGRAM (HPF): 
```clc;
clear;

Fs = 8000;

fc = 2000;

b = [0.6389 -1.2777 0.6389];
a = [1.0000 -0.5095 0.1825];
N = 512;
[H, f_norm] = frmag(b, a, N);

f = f_norm * Fs;

clf();
plot(f, 20 * log10(H), 'LineWidth', 2);
xlabel("Frequency (Hz)");
ylabel("Magnitude (dB)");
title("Butterworth High Pass Filter (Order 2) Frequency Response");
xgrid();


xset("color", 2);
plot([fc fc], [-80 5], '--');
xset("color", 1);
```



## OUTPUT (LPF) : 
<img width="1380" height="704" alt="image" src="https://github.com/user-attachments/assets/22d8556a-5fcf-4886-ab15-0d206638ef04" />


## OUTPUT (HPF) : 
<img width="1375" height="721" alt="Screenshot 2025-09-22 032916" src="https://github.com/user-attachments/assets/d8ca19ea-ff7f-4d1a-a537-06c0e27792e4" />


## RESULT: 
design of an IIR Butterworth filter  is simulated using scilab
