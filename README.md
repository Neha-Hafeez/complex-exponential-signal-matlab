# Complex Exponential Signals

# Introduction
A complex exponential signal is an exponential signal whose samples are complex numbers (i.e., having real and imaginary components). A complex signal is made up of two real signals, one for the real component and the other for the imaginary part. A complex signal's linear processing, such as filtering with a time-invariant linear filter, relates to applying the processing to both the real and imaginary parts of the signal.

# MATLAB Implementation
```
close all;
clc;
clear all;

% Initialization
fs = 5;
ts = 1/fs;
t = 0:ts:20-ts;
c = 0.103 + 1.03j;
x = 50*exp(c*t);

% Real Part
figure;
subplot(421);
stem(t,real(x),'b','LineWidth',3);
xlabel('Time Samples');
ylabel('Real Part');
grid on;
axis tight;
set(gca, 'FontSize', 12, 'FontWeight', 'b');

% Imaginary Part
subplot(423);
stem(t,imag(x),'R','LineWidth',3);
xlabel('Time Samples');
ylabel('Imaginary Part');
grid on;
axis tight;
set(gca, 'FontSize', 12, 'FontWeight', 'b');

% Magnitude
subplot(425);
stem(t,abs(x),'K','LineWidth',3);
xlabel('Time Samples');
ylabel('Magnitude');
grid on;
axis tight;
set(gca, 'FontSize', 12, 'FontWeight', 'b');

% Phase
subplot(427);
stem(t,angle(x),'M','LineWidth',3);
xlabel('Time Samples');
ylabel('Phase');
grid on;
axis tight;
set(gca, 'FontSize', 12, 'FontWeight', 'b');

% 3D Plot
subplot(4, 2, [2, 4, 6, 8]);
plot3(t,real(x),imag(x),'r','LineWidth',5);
xlabel('Time Samples');
ylabel('Real Part');
zlabel('Imaginary Part');
title('3D Plot of Complex Exponential Function');
grid on;
axis square;
set(gca, 'FontSize', 14, 'FontWeight', 'b');

% Title
sgtitle('Complex Exponential Signal in MATLAB', 'FontSize', 20, 'FontWeight', 'b');
```

# 3-D Plotting

![image](https://user-images.githubusercontent.com/85940284/232215331-92a77ff6-617a-4360-ab78-8f9f4d95f2a2.png)

![image](https://user-images.githubusercontent.com/85940284/232215453-8c1f9dd1-8737-4b0c-94bb-c3f256777a12.png)
![image](https://user-images.githubusercontent.com/85940284/232216048-3089aa88-938b-4f5d-90ef-b40b95b4543b.png)

# APPLICATION OF COMPLEX SIGNALS TO REAL WORLD 

The application of this approach to real-world problems includes the propagation of acoustic waves relevant to jet engine design, the development of boundary-integral techniques useful for solving many problems in solid and fluid mechanics, as well as conformal geometry in imaging and shape analysis, among other things. However, complex numbers have additional features that make them more suitable for wave representation than 2D real vectors. As a result, wave equations are virtually usually stated using complex numbers.

# APPLICATIONS OF COMPLEX SIGNALS IN ENGINEERING 

Complex analysis and Fourier analysis work hand in hand in signal processing, and this has a plethora of applications, such as in communication systems (your broadband, Wi-Fi, satellite communication, image/video/audio compression, signal filtering/repair/reconstruction, and so on). Essentially, if you look for signal processing apps, you will find applications that are indirectly sophisticated analytic applications. Although most engineers would tell you that complicated analysis is not required to "get" signal processing, I have found that it is really useful in progressing from just applying the Fourier transform, etc., to a point where one fully understands what is going on. The second area of application is control theory, especially in the examination of system stability and controller design. The term "system" is used broadly here and does not always relate to an electrical system. For example, it may be used to (attempt to) explain stock market movement or chemical processes/reactions. Furthermore, control theory and, by extension, complex analysis are widely employed in robotics.

