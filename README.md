# Spin Dissipative Molecular Dynamics by Magnetic Microwaves #

## Microwave sintering experiments and its theory

We mark that microwave magnetic field to heat metal oxide of magnetite 
which is above the Curie temperatre 585 Celsius to 1300 Celsius.
Microwave sintering was tested by experiments and good quarity irons were created 
(R. Roy et. al., Nature, 1999), Ref.1.  

Later, theory and numerical simulation were used to identify unpaired 3d 
electron spins of Fe(3+) and Fe(2+) irons to increase much above the Curie 
temperature (M. Tanaka et al., Phys. Rev. B, 2009), Ref.2. The recent 
simulations using Fortran 2003/2008 and MPICH4 with the updated code 
reproduce the same result of magnetic magnetite sintering.

## Simulation procedures and our theory

Electron spins of Fe(3+), Fe(2+) and O(2-) in cubic cells

Magnetic microwaves of giga-Hertz frequency that is 2.5 GHz

Metropolis criterion is used to accept/reject in the MC cycle

Dissipation spin molecular dynamics simulation is executed in the MD cycle.

  > Execution of a few 1,000,000 steps (1 GHz range) for $ Delta t= 0.001 $ ps

Microwave magnetic heating by numerical simulation reaches 1,300 Celsius for 
metal oxide magnetite. 
The peak of the time derivative dU_sys/dt corresponds to the Curie temperatre 
of 858 K (585 C) with the sinusoidal magnetic field Bz= 5,000 gauss, the 
constant magnetic field B_z0= 2x10^4 gauss, and the initial temperture 200 K.
The total energy U_sys and the time derivative dU_sys/dt in sai124a.pdf 
are shown for these temperatures, as the proof of our theory of 
microwave magnetic sintering, Ref. 2. Recent simulations with Fortran 2003/2008
and MPICH4, with the code update, are the same result of microwave magnetic sintering. 


## Numerical code, parameters and files

1) @spin_SMD7a.f03: Dissipative spin molecular dynamics. An odd number of processors
in the z direction is required for your choice. Read the simulation code and parameters
for details !!

2) param_spinRL7.h: Parameters 

 > number of processors (nodes), total cells of irons and oxygens (odd numbers such as 5x5x5 nodes),
p3m resolution
  
3) SAI107_config.START1: Configuration file

 > physical run time, lattice sizes, number of cells, exchange integrals for Fe and O,
  period of microwave magnetic field, temperature, Curie temprature, etc.
  About 1,000,000 steps are required !

4) Magnetite in a cubic lattice: magnetite8.xyz for initialization of 
the a,b,c cell


## References

1. R. Roy, D. Agrawal, J. Cheng, and S. Gedevanishvili, Full sintering of powdered-metal bodies
in a magnetic field, Nature, 399, 668 (1999).

2. M. Tanaka, H. Kono, and K. Maruyama, Selective heating mechanism of magnetic
metal oxides by a microwave magnetic field, Phys. Rev. B, 79, 104420 (2009).

