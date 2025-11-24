# EXP 2 : Linear and Circular Convolution

## AIM: 

 To perform Linear and Circular Convolution for two given sequence using SCILAB. 

## APPARATUS REQUIRED: 
PC installed with SCILAB. 

## PROGRAM (Linear Convolution & Circular Convulation): 
clc;
clear;
close;

x = [1 2 3 4];
h = [1 1 1];

y_lin = conv(x, h);

N = max(length(x), length(h));
X = fft([x zeros(1, N-length(x))]);
H = fft([h zeros(1, N-length(h))]);
Y = X .* H;
y_circ = real(ifft(Y));

figure(1);
subplot(3,1,1);
plot(0:length(x)-1, x);
title("Input x(n)");

subplot(3,1,2);
plot(0:length(h)-1, h);
title("Input h(n)");

subplot(3,1,3);
plot(0:length(y_lin)-1, y_lin);
title("Linear Convolution");

figure(2);
plot(0:length(y_circ)-1, y_circ);
title("Circular Convolution");



## OUTPUT (Linear Convolution): 

<img width="1600" height="900" alt="image" src="https://github.com/user-attachments/assets/ba190233-1c03-433e-a795-6ccb3d3b1432" />


## OUTPUT (Circular Convolution): 

<img width="1600" height="900" alt="image" src="https://github.com/user-attachments/assets/584eca52-0905-4e53-8989-9d41a4eed52b" />


## RESULT: 

Thus, the linear and circular convulation is performed for two different sequences and output is verified. 
