## GeSe calculation

1. The harmonic coupling plot (energy vs P_i-<P_j>)cannot be reproduced using the provided coupling coefficient `D=8.0904`. The 2D lattice have 4 nearest neighbor, which means:
```
E=4*D/2*(P_i-<P_j>)^2
```
But the plot actually show:
```
E=8*D/2*(P_i-<P_j>)^2
```
two times higher than the provided coupling coefficient.

![FIG.1](./fig/FIG1.png)

2. Despite the difference between the the coupling plot and provided coupling coefficient, using mpiPyMC, I am able to plot the phase transition identical to the paper and get same T_c for FE to turn PE.

![FIG.2](./fig/FIG2.png)

3. Using two times the provided coupling coefficient `D`, the transition temperature is around 350K.

![FIG.3](./fig/FIG3.png)

## Parameters
| NAME                   | DATA                                       |
|:----------------------:|:------------------------------------------:|
| `nt`                   | 18                                         |
| `N`                    | 30                                         |
| `eqSteps`              | 8000                                       |
| `mcSteps`              | 4000                                       |
| `A_data` `B_data` `C_data` `D_data`| -15.261, 1.8389, 1.7137, 8.0904|
| `ps`                   | 1.59                                       |
| `T`                    | 0.01, 400                                  |
