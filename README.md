# <div align="center">Applied-Linear-Controls-Project-Part-2</div>
**<div align="center">To develop an [output feedback controller](http://www.cds.caltech.edu/~murray/books/AM08/pdf/am06-outputfbk_16Sep06.pdf) and demonstrate regulation of states and outputs using the dynamic system from the Project Part 1 [system identification](https://www.mathworks.com/help/ident/gs/about-system-identification.html) methods</div>**

> **Note**: The first step for developing a state feedback or an output feedback controller is to develop a state-space model of the open loop plant, which is done in the Project Part 1.

#### How to Access the Unknown Plant function in the script:
```Matlab
  [y, u, xhat] = s20_plant(dt_ofc, time)
```

#### Tasks List:
- [x] Executing the appropriate code based on the sequential objectives below
- [x] Debugging (Comparison of [H1 Estimate](https://community.sw.siemens.com/s/article/what-is-a-frequency-response-function-frf) and [Minimum Realization](https://en.wikipedia.org/wiki/Minimal_realization) FRF)
- [x] Finding the appropriate reduced order LTI object whose FRF is in coherence with the above two

#### Objectives Achieved: 

- 



- Constructed an excitation signal for System Identification following the saturation limit for DAC (Digital-to-Analog Converter)
- Estimated the SNR (Signal to Noise Ratio) for each path of signal `u1 -> y1` and `u1 -> y2`
- Computed the Power Spectrum for responses and noise signals
- Applied H1 estimate technique to estimate the frequency response function and estimated coherence of each path
- Estimated Discrete time transfer functions for each path using `invfreqz()` function and converted it into minimum realization using `minreal()` function
- Generated a Balanced Realization using `balreal()` and plotted the [Hankel singular values](https://en.wikipedia.org/wiki/Hankel_singular_value) to help generate a reduced order LTI discrete time state space model using `modred()`
- Generated z-domain grid to plot the z-domain eigen values (poles) for each path using `zgrid()` function
- Computed and Plotted final discrete-time state space LTI object in comparison to H1 estimate


<p align="center"><img src="Excitation.jpeg"> </p>

<p align="center"><img src="Hankel.jpeg"> </p>

<p align="center"><img src="zgrid.jpeg"> </p>

<p align="center"><img src="FinalPlots.jpeg"> </p>





#### Languages Used:
- Matlab
- Latex 

#### Use of each file:
- [**Midterm_Project_Japnit_Sethi.mlx**](Midterm_Project_Japnit_Sethi.mlx) - Executable file with learly defined problem statement and approach
- [**Midterm_Project_Japnit_Sethi.pdf**](Midterm_Project_Japnit_Sethi.pdf) - Published Document for a quick check of Solutions and Code
- [**s20_plant.p**](s20_plant.p) - Plant function file that takes excitation u as input (1xN) and returns the output response y(2xN), where N is the number of samples
