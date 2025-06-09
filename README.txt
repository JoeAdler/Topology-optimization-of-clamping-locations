#Topology Optimization of Fixture Clamping Locations for Machining Processes

##Author: Joé ADLER


The goal of this work is to optimize the clamping locations on a workpiece mesh during a given machine process. This is done by formulating the problem as a topology optimization problem for which the clamping points are modeled using bar elements. Design variables are the normalized densities of these bar elements. A SIMP formulation is used for the Young's modulus. This work contains:

* 'inputs.py': code responsible for managing the inputs to the program (workpiece mesh, fixed nodes, machining loads, etc.)
* 'elementary.py': code responsible for defining the elementary stiffness and mass matrices (tetrahedral and bar elements)
* 'assembly.py': code responsible for assembling the structural matrices and applying BCs
* 'reduction.py': code responsible for applying Guyan-Irons reduction method to the structural matrices
* 'sensitivity.py': code responsible for determining the sensitivities of the objective and constraint functions
* 'display.py': code responsible for displaying the FE mesh, the solutions, etc.
* 'validation.py': code used to validate the finite element code
* 'optimization_scipy.py': code responsible for optimizing the clamping locations using scipy.optimize.minimize (SLSQP method)
* 'optimize_MMA.py': code responsible for optimizing the clamping locations using the Method of Moving Asymptote's (MMA) by employing 'mmapy' module (by Deetman 2024)
* 'others.py': code responsible for plotting some of the figures in the report (not all of them)


##References:

- Svanberg, K. (1987). The Method of Moving Asymptotes – A new method for structural optimization. International Journal 
for Numerical Methods in Engineering 24, 359-373. [doi:10.1002/nme.1620240207](https://onlinelibrary.wiley.com/doi/abs/10.1002/nme.1620240207)
 - Svanberg, K. (n.d.). MMA and GCMMA – two methods for nonlinear optimization. Retrieved August 3, 2017 from  
https://people.kth.se/~krille/mmagcmma.pdf


##Requirements:
-------------
matplotlib
numpy
scipy
time
mmapy

