Given the continuous-time (CT) signal:

\[ x(t) = 5 \cos(8 \pi t) \]

the signal is sampled 8 times starting at \( t = 0 \) with a sampling period \( T_s = 0.05 \) seconds. Let's find the sampled values and compute the Discrete Fourier Transform (DFT).

### Sampling the Signal
The sample times are given by:

\[ t_n = nT_s = 0.05n \, \text{for } n = 0, 1, \ldots, 7 \]

Thus, the sampled values of \( t \) are:

\[ t_n = \{0, 0.05, 0.1, 0.15, 0.2, 0.25, 0.3, 0.35 \} \]

### Compute the Sampled Signal

Given \( x(t) = 5 \cos(8 \pi t) \), we can compute the sampled values as follows:

\[
\begin{align*}
x(0) &= 5 \cos(8 \pi \cdot 0) = 5 \\
x(0.05) &= 5 \cos(8 \pi \cdot 0.05) = 5 \cos(0.4 \pi) = 5 (-1) = -5 \\
x(0.1) &= 5 \cos(8 \pi \cdot 0.1) = 5 \cos(0.8 \pi) = 5 (1) = 5 \\
x(0.15) &= 5 \cos(8 \pi \cdot 0.15) = 5 \cos(1.2 \pi) = 5 (-1) = -5 \\
x(0.2) &= 5 \cos(8 \pi \cdot 0.2) = 5 \cos(1.6 \pi) = 5 (1) = 5 \\
x(0.25) &= 5 \cos(8 \pi \cdot 0.25) = 5 \cos(2 \pi) = 5 (1) = 5 \\
x(0.3) &= 5 \cos(8 \pi \cdot 0.3) = 5 \cos(2.4 \pi) = 5 (-1) = -5 \\
x(0.35) &= 5 \cos(8 \pi \cdot 0.35) = 5 \cos(2.8 \pi) = 5 (1) = 5 
\end{align*}
\]

Therefore, the sampled signal \( x[n] \) is:

\[ x[n] = \{5, -5, 5, -5, 5, -5, 5, -5 \} \]

### Compute the DFT

The DFT \( X[k] \) of the sequence \( x[n] \) is given by:

\[ X[k] = \sum_{n=0}^{7} x[n] e^{-j\frac{2 \pi}{8} kn} \]

We need to determine \( X[2] \):

\[ X[2] = \sum_{n=0}^{7} x[n] e^{-j \frac{2 \pi}{8} 2 n} \]

Simplify the exponential term:

\[ e^{-j \frac{2 \pi}{8} 2 n} = e^{-j \frac{\pi}{2} n} \]

The values of \( e^{-j \frac{\pi}{2} n} \) for \( n = 0, 1, 2, 3, 4, 5, 6, 7 \) are:

\[ 1, -j, -1, j, 1, -j, -1, j \]

Using these, we can express \( X[2] \) as follows:

\[
X[2] = 5(1) + (-5)(-j) + 5(-1) + (-5)j + 5(1) + (-5)(-j) + 5(-1) + (-5)j
\]

Simplifying term by term:

\[
X[2] = 5 - 5j - 5 + 5j + 5 - 5j - 5 + 5j
\]

Group the real and imaginary parts:

\[
X[2] = (5 - 5 + 5 - 5 + 5 - 5 + 5 - 5) + (- 5j + 5j - 5j + 5j - 5j + 5j - 5j + 5j)
\]
\[
X[2] = 0 + 0j = 0
\]

### DFT Magnitude

Since \( X[2] = 0 \), the magnitude of the frequency component \( X[2] \) is:

\[ |X[2]| = 0.000 \]

So, the magnitude of the frequency component \( X[2] \) is \(0.000\) when rounded to three decimal places.
