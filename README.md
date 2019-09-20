# Pareto-front-data

## data generation methods

### 3D data
For DTLZ1 (i.e., the linear triangular Pareto front), the data is generated by the simplex-lattice design method. The code is from [PlatEMO](https://github.com/BIMK/PlatEMO/).

For MinusDTLZ1 (i.e., the linear inverted triuangular Pareto front), the data is obtained from DTLZ1 by transforming each point <a href="https://www.codecogs.com/eqnedit.php?latex=$(f_1,f_2,f_3)$" target="_blank"><img src="https://latex.codecogs.com/pdf.latex?$(f_1,f_2,f_3)$" title="$(f_1,f_2,f_3)$" /></a> to $(1-f_1,1-f_2,1-f_3)$.

For DTLZ2 (i.e., the concave triangular Pareto front), the data is obtained from DTLZ1 by transforming each point $(f_1,f_2,f_3)$ to $(\frac{f_1}{\sqrt{f_1^2+f_2^2+f_3^2}},\frac{f_2}{\sqrt{f_1^2+f_2^2+f_3^2}},\frac{f_3}{\sqrt{f_1^2+f_2^2+f_3^2}})$..

For MinusDTLZ2 (i.e., the convex inverted triangular Pareto front), the data is obtained from DTLZ2 by transforming each point $(f_1,f_2,f_3)$ to $(1-f_1,1-f_2,1-f_3)$.


### 5D and 10D data
For DTLZ1 (i.e., the linear triangular Pareto front), the data is generated by two parts:
- The simplex-lattice design method;
- The uniformly sampling method.

The uniformly sampling method is used to uniformly sample points on a unit hypersphere. It works as follows: First we randomly sample points $\mathbf{x}$ according to the normal distribution $\mathcal{N}_m(0,I_m)$, then the corresponding points on the hypersphere are obtained by $\mathbf{x}' = |\mathbf{x}|/\left \| \mathbf{x} \right \|_2$.

## Notice
All the Pareto fronts are in the normalized objective space, i.e., ideal point is $(0,...,0)$ and nadir point is $(1,...,1)$.
