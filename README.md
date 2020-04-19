# PDECharactSimulink

Solving partial differential equations (PDEs) in _Simulink_ with the method of characteristics.

## First-order quasilinear (FOQL) PDEs

Library `PDECharactLib.slx` contains the `FOQL PDE` subsystem for modeling first-order quasilinear PDEs. Detailed description is available at https://arxiv.org/abs/1907.13419.

Examples:
* `FOQL_PDE_SimpleExample.slx`: simple example of using the `FOQL PDE` subsystem.
* `FOQL_PDE_OutputFeedback.slx`: model of a heat exchanger with output feedback control, discussed in the PDF file `FOQL_PDE_OutputFeedback.pdf`.
* `FOQL_PDE_StateFeedback.slx`: example with full-state feedback, discussed in the main paper https://arxiv.org/abs/1907.13419.
