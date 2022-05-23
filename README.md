# PDECharactSimulink

Solving partial differential equations (PDEs) in _Simulink_ with the method of characteristics.

## First-order quasilinear (FOQL) PDEs

Library `PDECharactLib.slx` contains the `FOQL PDE` subsystem for modeling first-order quasilinear PDEs of the form

$$w_t + v\big( t, x, w(t, \cdot)_{[0, \ell]} \big) w_x = f\big( t, x, w(t, \cdot)_{[0, \ell]} \big)$$

with initial condition $w(0, x) = w_0(x)$ ($x \in [0, \ell]$) and boundary condition $w(t, 0) = u(t)$ ($t \ge 0$). Detailed description of the method is available at https://arxiv.org/abs/1907.13419.

Examples:
* `FOQL_PDE_SimpleExample.slx`: simple example of using the `FOQL PDE` subsystem.
* `FOQL_PDE_OutputFeedback.slx`: model of a heat exchanger with output feedback control, discussed in the PDF file `FOQL_PDE_OutputFeedback.pdf`.
* `FOQL_PDE_StateFeedback.slx`: example with full-state feedback, discussed in the main paper https://arxiv.org/abs/1907.13419.
