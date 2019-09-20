# Pareto-front-data

## data generation methods

### 3D data
For DTLZ1 (i.e., the linear triangular Pareto front), the data is generated by the simplex-lattice design method. The code is from [PlatEMO](https://github.com/BIMK/PlatEMO/).

For MinusDTLZ1 (i.e., the linear inverted triuangular Pareto front), the data is obtained from DTLZ1 by transforming each point <a href="https://www.codecogs.com/eqnedit.php?latex=(f_1,f_2,f_3)" target="_blank"><img src="https://latex.codecogs.com/png.latex?(f_1,f_2,f_3)" title="(f_1,f_2,f_3)" /></a> to <a href="https://www.codecogs.com/eqnedit.php?latex=(1-f_1,1-f_2,1-f_3)" target="_blank"><img src="https://latex.codecogs.com/png.latex?(1-f_1,1-f_2,1-f_3)" title="(1-f_1,1-f_2,1-f_3)" /></a>.

For DTLZ2 (i.e., the concave triangular Pareto front), the data is obtained from DTLZ1 by transforming each point <a href="https://www.codecogs.com/eqnedit.php?latex=(f_1,f_2,f_3)" target="_blank"><img src="https://latex.codecogs.com/png.latex?(f_1,f_2,f_3)" title="(f_1,f_2,f_3)" /></a> to <a href="https://www.codecogs.com/eqnedit.php?latex=(\frac{f_1}{\sqrt{f_1^2&plus;f_2^2&plus;f_3^2}},\frac{f_2}{\sqrt{f_1^2&plus;f_2^2&plus;f_3^2}},\frac{f_3}{\sqrt{f_1^2&plus;f_2^2&plus;f_3^2}})" target="_blank"><img src="https://latex.codecogs.com/png.latex?(\frac{f_1}{\sqrt{f_1^2&plus;f_2^2&plus;f_3^2}},\frac{f_2}{\sqrt{f_1^2&plus;f_2^2&plus;f_3^2}},\frac{f_3}{\sqrt{f_1^2&plus;f_2^2&plus;f_3^2}})" title="(\frac{f_1}{\sqrt{f_1^2+f_2^2+f_3^2}},\frac{f_2}{\sqrt{f_1^2+f_2^2+f_3^2}},\frac{f_3}{\sqrt{f_1^2+f_2^2+f_3^2}})" /></a>.

For MinusDTLZ2 (i.e., the convex inverted triangular Pareto front), the data is obtained from DTLZ2 by transforming each point <a href="https://www.codecogs.com/eqnedit.php?latex=(f_1,f_2,f_3)" target="_blank"><img src="https://latex.codecogs.com/png.latex?(f_1,f_2,f_3)" title="(f_1,f_2,f_3)" /></a> to <a href="https://www.codecogs.com/eqnedit.php?latex=(1-f_1,1-f_2,1-f_3)" target="_blank"><img src="https://latex.codecogs.com/png.latex?(1-f_1,1-f_2,1-f_3)" title="(1-f_1,1-f_2,1-f_3)" /></a>.


### 5D and 10D data
For DTLZ1 (i.e., the linear triangular Pareto front), the data is generated by two parts:
- The simplex-lattice design method;
- The uniformly sampling method.

The uniformly sampling method is used to uniformly sample points on a unit hypersphere. It works as follows: First we randomly sample points <a href="https://www.codecogs.com/eqnedit.php?latex=\mathbf{x}" target="_blank"><img src="https://latex.codecogs.com/png.latex?\mathbf{x}" title="\mathbf{x}" /></a> according to the normal distribution <a href="https://www.codecogs.com/eqnedit.php?latex=\mathcal{N}_m(0,I_m)" target="_blank"><img src="https://latex.codecogs.com/png.latex?\mathcal{N}_m(0,I_m)" title="\mathcal{N}_m(0,I_m)" /></a>, then the corresponding points on the hypersphere are obtained by <a href="https://www.codecogs.com/eqnedit.php?latex=\mathbf{x}'&space;=&space;|\mathbf{x}|/\left&space;\|&space;\mathbf{x}&space;\right&space;\|_2" target="_blank"><img src="https://latex.codecogs.com/png.latex?\mathbf{x}'&space;=&space;|\mathbf{x}|/\left&space;\|&space;\mathbf{x}&space;\right&space;\|_2" title="\mathbf{x}' = |\mathbf{x}|/\left \| \mathbf{x} \right \|_2" /></a>.

Then each point <a href="https://www.codecogs.com/eqnedit.php?latex=(f_1,f_2,f_3)" target="_blank"><img src="https://latex.codecogs.com/png.latex?(f_1,f_2,f_3)" title="(f_1,f_2,f_3)" /></a> on the hypersphere is transformed to the simplex by <a href="https://www.codecogs.com/eqnedit.php?latex=(\frac{f_1}{f_1&plus;f_2&plus;f_3},\frac{f_2}{f_1&plus;f_2&plus;f_3},\frac{f_3}{f_1&plus;f_2&plus;f_3})" target="_blank"><img src="https://latex.codecogs.com/png.latex?(\frac{f_1}{f_1&plus;f_2&plus;f_3},\frac{f_2}{f_1&plus;f_2&plus;f_3},\frac{f_3}{f_1&plus;f_2&plus;f_3})" title="(\frac{f_1}{f_1+f_2+f_3},\frac{f_2}{f_1+f_2+f_3},\frac{f_3}{f_1+f_2+f_3})" /></a>.

For DTLZ2, MinusDTLZ1 and MinusDTLZ2, the data is generated from DTLZ1 in the same manner as in 3D case.

## Notice
All the Pareto fronts are in the normalized objective space, i.e., ideal point is (0,...,0) and nadir point is (1,...,1).
