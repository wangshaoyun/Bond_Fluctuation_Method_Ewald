![Schmetical Diagram](https://github.com/wangshaoyun/Bond_Fluctuation_Method_Ewald/blob/master/Fig1.jpeg "Simulation System")
# Bond_Fluctuation_Method_SPME
## About this program
1. This is a program used to simulate weak polyelectrolytes(PE) brushes with salts by Kremer's bond fluctuation method [1,4].
2. PE brushes can be linear or star. 
3. 6*6 chains are grafted on a plate, and each chain includes 100 monomers. In addition, each 5 monomers with 1 charged monomer so charge fraction is 1/5. Same quantities counterions of PE brushes are added in the system.
3. Interaction only includes Coulomb potential and Metropolis algorithm is used to update position.
4. For Coulomb interaction, Ewald summation is used [3]. Because best computational complexity is O(N^(3/2)) which is little large so that only 3000 particles can be simulated without parallel computation. 
7. Constant pH titration algorithm is used to simulate the titration process.
8. Short part potential is calculated by pure cell lists algorithm with doubly linked lists.
>[1] David P. Landau, Kurt Binder. "An Guide to Monte-Carlo Simulation in Stastical Physics." 3rd ed, Cambridge Unversity Press, Cambridge UK, 2009.  
>[2] K. Bernacki, B. Hetenyi, B. J. Berne. "Multiple "Time Step" Monte Carlo Simulations: Application to charged systems with Ewald Summation." *Journal of Chemical Physics*, **121** (1), pp.44-50, 2004.  
>[3] Frenkel D, Klein M, Parrrinello M. "Understanding Molecular Simulation: From Algorithm to Applications". 2nd ed. Singapore: Elsevier Pte Ltd, 2002.  
>[4] I. Carmesin, Kurt. Kremer. "The Bond Fluctuation Method: A New Effective Algorithm for the Dynamics of Polymers in All Spatial Dimensions.", *Macromolecules*, **21** (9), pp. 2819-2823, 1988. 

## About Parameter Files 
+ energy_data.txt: It is a parameter file which includes Bjerrum length, external electric field
+ system_data.txt: It is a parameter file which includes system, time, brushes parameter.  

## Compiling files
1. Determine the parameters such as box size, brush chians, time step and so on.
2. Set the parameters in energy_data.txt and system_data.txt
3. Open terminal and enter the current file content
4. To compile the files:
```
$ make
```
  
5. To execute the files:
```
$ ./main &
```







