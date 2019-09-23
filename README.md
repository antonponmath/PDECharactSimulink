# PDECharactSimulink

Solving partial differential equations (PDEs) in _Simulink_ with the method of characteristics. Detailed description: https://arxiv.org/abs/1907.13419.

The library `PDECharactLib.slx` contains the `FOQL PDE` subsystem for modeling first-order quasilinear PDEs.

## First-order quasilinear (FOQL) PDE solver

The file `FOQL_PDE_Solver_SimpleExample.slx` contains a simple example of using the `FOQL PDE` subsystem to simulate the PDE dynamics

> ![equation](https://latex.codecogs.com/gif.latex?%5Cbegin%7Balign*%7D%20%26%5Cfrac%7B%5Cpartial%20w%28t%2C%20x%29%7D%7B%5Cpartial%20t%7D%20&plus;%20%28x%20&plus;%201.1%20&plus;%20%5Csin%20t%29%20%5Cfrac%7B%5Cpartial%20w%28t%2C%20x%29%7D%7B%5Cpartial%20x%7D%20%3D%20-w%28t%2C%20x%29%2C%20%5C%5C%20%26%5Ctext%7BInitial%20state%3A%20%7D%20w%280%2C%20x%29%20%3D%201%20-%20x%5E2%2C%20%5C%3A%20x%20%5Cin%20%5B0%2C%201%5D%2C%20%5C%5C%20%26%5Ctext%7BBoundary%20condition%3A%20%7D%20w%28t%2C%200%29%20%3D%20%5Cbegin%7Bcases%7D%201%20&plus;%20%5Ccos%5Ctfrac%7B%5Cpi%20t%7D%7B2%7D%2C%20%26%20t%20%3C%2016%2C%20%5C%5C%200%2C%20%26%20t%20%5Cgeq%2016%2C%20%5Cend%7Bcases%7D%20%5C%5C%20%26%5Ctext%7BOutput%3A%20%7D%20y%28t%29%20%3D%20w%28t%2C%201%29.%20%5Cend%7Balign*%7D)

In general, the `FOQL PDE` subsystem can handle systems of this sort:

> ![equation](https://latex.codecogs.com/gif.latex?%5Cbegin%7Balign*%7D%20%26%5Cfrac%7B%5Cpartial%20w%28t%2C%20x%29%7D%7B%5Cpartial%20t%7D%20&plus;%20v%20%5Cbig%28%20t%2C%20x%2C%20w%28t%2C%20%5Ccdot%29%7C_%7B%5B0%2C%20%5Cell%5D%7D%2C%20%5Cdots%20%5Cbig%29%20%5Cfrac%7B%5Cpartial%20w%28t%2C%20x%29%7D%7B%5Cpartial%20x%7D%20%3D%20f%20%5Cbig%28%20t%2C%20x%2C%20w%28t%2C%20%5Ccdot%29%7C_%7B%5B0%2C%20%5Cell%5D%7D%2C%20%5Cdots%20%5Cbig%29%2C%20%5C%5C%20%26%5Ctext%7BInitial%20state%3A%20%7D%20w%280%2C%20x%29%20%3D%20w_0%28x%29%2C%20%5C%3A%20x%20%5Cin%20%5B0%2C%20%5Cell%5D%2C%20%5C%5C%20%26%5Ctext%7BBoundary%20condition%3A%20%7D%20w%28t%2C%200%29%20%3D%20u%20%5Cbig%28%20t%2C%20%5Cdots%20%5Cbig%29.%20%5Cend%7Balign*%7D)

Ellipsis in the arguments of the equation terms denotes, e.g., possible feedback through other dynamical systems, etc.
