# MATLAB Assignment: Z-Transform and One-Sample Delay

Part 1

Question 1

The term 1 represents x[0] = 1.
The term 2z^-1 represents x[1] = 2.
The term z^-2 represents x[2] = 1.

Question 2

The Z-transform of the delayed signal is:

Xd(z) = z^-1 + 2z^-2 + z^-3

or equivalently:

Xd(z) = z^-1 X(z)

Question 3

Delaying the signal by one sample shifts all samples one position to the right. In the Z-transform domain, this multiplies X(z) by z^-1.

Part 2

Question 4

Using y[n] = 0.5x[n] + 0.5x[n−1]:

y[0] = 0.5
y[1] = 1.5
y[2] = 1.5
y[3] = 0.5

The MATLAB output was:

[0.5 1.5 1.5 0.5]

which matches the manual calculations.

Question 5

The vector b = [0.5 0.5] contains the coefficients of H(z).
The first coefficient (0.5) corresponds to the current sample x[n].
The second coefficient (0.5) corresponds to the delayed sample x[n−1].

Therefore:

H(z) = 0.5 + 0.5z^-1

Question 6

The system was changed to:

H(z) = 0.8 + 0.2z^-1

by changing:

b = [0.8 0.2];

The new output samples are:

[0.8 1.8 1.2 0.2]

The current input sample x[n] has more influence on the output because its coefficient is 0.8, while the previous sample x[n−1] has a coefficient of 0.2.