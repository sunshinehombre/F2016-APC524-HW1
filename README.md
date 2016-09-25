# F2016-APC524-HW1
# Written by Jeffry Lew, jklew@princeton.edu
# September 25, 2016

Assignment 1: ODE integrator provides three methods to numerically integrate the second-order forced Duffing oscillator, whose initial conditions are x(0) = x_dot(0) = 0.

These methods include
      -Explicit Euler
      -Fourth-order Runge-Kutta
      -Second-order Adams-Bashforth

Assignment 1 requires six files to run
	   -duffing.c (Driver program to integrate the Duffing equation)
	   -euler.c (Implementation of the Euler integrator)
	   -rk4.c (Implementation of the 4th-order Runge-Kutta integrator)
	   -ab2.c (Implementation of the 2nd-order Adams-Bashforth integrator)
	   -integrator.h (Header file which all integrators implement)
	   -Makefile (Generates targets duffing_euler, duffing_ab2, and duffing_rk4)

To compile Assignment 1, ensure the above six files are in the same directory

~/Documents/APC-524/HW1-F2016/

and cd to this directory.

From the terminal, compile the code through:

$ make clean
$ make

The program should take two command-line arguments - the timestep h [sec] and the number of steps to take.

The format of the method call is: 
$ selected_integrator h steps

Example of using the explicit Euler integrator:
$ duffing_euler 0.1 100

Example of using the fourth-order Runge-Kutta integrator:
$ duffing_rk4 0.1 100

Example of using the second-order Adams-Bashforth integrator:
$ duffing_ab2 0.1 100

The above method calls will printout the time, x, and x_dot to the terminal at every integration step.