EXPT 2a: LINEAR CONVOLUTION-USING-DFT
AIM
To perform and verify linear convolution operation of two given sequences using SCILAB.

APPARATUS REQUIRED
PC installed with SCILAB

PROGRAM:
LINEAR CONVOLUTION
~~~
clc;
clear;
x = [1 1 1 0];
h = [1 0 1 0];
m = length(x);
n = length(h);
a=0:1:m-1;
b=0:1:n-1;
subplot(3,1,1);
plot2d3(a,x);
xlabel('Time');
ylabel('Amplitude');
title('Graphical Representation of Input Signal X');
subplot(3,1,2);
plot2d3(b,h);
xlabel('Time');
ylabel('Amplitude');
title('Graphical Representation of Impulse Signal h');
for i = 1: n+m-1
conv_sum = 0;
for j = 1:i
if (((i-j+1) <= n)&(j <=m))
conv_sum = conv_sum + x(j)*h(i-j+1);
end;
y(i) = conv_sum;
end;
end;
disp(y,'Convolution Sum using Direct Formula Method = ')
subplot(3,1,3);
plot2d3(y)
title('Graphical Representation of output Signal y');
~~~






### CALCULATIONS:
<img width="899" height="1599" alt="image" src="https://github.com/user-attachments/assets/15634468-bca4-430d-94ae-4f03b4f2db02" />
<img width="899" height="1599" alt="image" src="https://github.com/user-attachments/assets/663722c9-d5d9-4a88-8cd2-6a7a79cf9f00" />
<img width="899" height="1599" alt="image" src="https://github.com/user-attachments/assets/46d5e58b-c7f7-4347-8792-9505f34791de" />
<img width="1599" height="899" alt="image" src="https://github.com/user-attachments/assets/f5b18735-a971-47c0-ab85-a86a7e3b391f" />




### SAMPLE OUTPUT:

<img width="767" height="727" alt="image" src="https://github.com/user-attachments/assets/078f6a97-19bc-4cdc-b75f-c19b8fb95c7b" />





RESULT:
Thus, the linear convolution of the two given sequences were performed and its result was verified.
