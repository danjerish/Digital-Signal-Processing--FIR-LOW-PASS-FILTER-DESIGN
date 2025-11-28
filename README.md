# Digital-Signal-Processing--FIR-LOW-PASS-FILTER-DESIGN
## AIM:
To generate design of low pass FIR digital filter using Window.
## Software Required:
MAT LAB R2012.
## Algorithm:
Step 1: Open MATLAB and Write the program.

Step 2: Read the values of cut off frequency wc.

Step 2: Read the values of Order of the filter N.

Step 3: Find out the desired impulse response of the Low Pass filter Coefficient.

Step 4: Find out the windowing sequence.

Step 5: Plot the magnitude spectrum with x-label and y-label with suitable title.

Step 6: Terminate the program.

## PROGRAM: 
```

clc; % clear screen
clear all; % clear screen
close all; % close all figure windows
wc=input('enter the value of cut off frequency');
N=input('enter the value of filter');
alpha=(N-1)/2;
eps=0.001;
%Low Pass Filter Coefficient 
n=0:1:N-1;  
hd=(sin((n-alpha+eps)*wc))./(pi*(n-alpha+eps)) 
%Hanning Window Sequence
n=0:1:N-1;
wh=0.5-0.5*cos((2*pi*n)/(N-1))
hn=hd.*wh
% Plot the Low Pass Filter with Bartlett Window Technique
w=0:0.01:pi;
h=freqz(hn,1,w);
plot(w/pi,abs(h),'blue');
```

## OUTPUT:
<img width="1621" height="831" alt="dspexp3" src="https://github.com/user-attachments/assets/1326ffe3-fe49-4680-a561-42e4650fa4f3" />

## RESULT:
![EXP3](https://github.com/user-attachments/assets/fa8692f2-1809-4e7d-94dd-cabb02c16e35)
