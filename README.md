# Genetic-Algorithm-Python
This python code is developed by Sreemannarayana Ikkurthi,
as a part of course notes for the course 15AES477: Multidisciplinary Design Optimization (MDO).

In support of Dr. Rajesh Senthil Kumar T.,
Assistant Professor, 

Department of Aerospace Engneering, Amrita Vishwa Vidyapeetham.
## About Genetic Algorithm
Genetic Algorithm is an optimization method, mimicing natural selection process.

A detailed explanation about the method can be found in the text book:
###### *Deb Kalyanmoy, Optimization for Engineering Design, Algorithms and Examples. (2012)*
## About Code
This code can be used to optimize an objective function of n variables and produce a contour plots of adjacent variables of all generations.

The code contains 8 important functions and 16 helping functions.

The 16 helping functions are made to help the 5 important functions as dividing tasks into smaller functions improves the efficiency of the program. 

The 8 important functions and thier usage is as follows:

### pop = ini_pop(no_bit, no_var, npop):
        Inputs:
              no_bit = No. of bits per variable
              no_var = No. of variables
              npop = Population size
        Outputs:
              pop = Binary population
        Usage: 
              This function is used to produce a set of binary population with given requirements.
### nor_pop = norm_pop(co_pop, lim):
        Inputs:
              co_pop = Binary population
              lim = Limits of variables of form [a, b]; a: lower limit, b: upper limit
        Outputs:
              nor_pop = Normalized population
        Usage: 
              This function is used to convert binary population into normalized population, normalized to given limits.
### mat_pool = rep_pop(co_pop, lim):
        Inputs:
              co_pop = Binary population
              lim = Limits of variables of form [a, b]; a: lower limit, b: upper limit
        Outputs:
              mat_pool = Mating pool
        Usage: 
              This function is used to get mating pool from the given population using roulette wheel selection.
### int_pool = crov_pop(mat_pool, cp):
        Inputs:
              mat_pool = Mating pool
              cp = Cross-over probability
        Outputs:
              int_pool = Intermediate pool
        Usage: 
              This function is used to get intermediate pool from mating pool.
### mut_pool = mut_pop(int_pop, mp):
        Inputs:
              int_pop = Intermediate pool
              mp = Mutation probability
        Outputs:
              mut_pool = Mutated pool
        Usage: 
              This function is used to get mutated pool from intermediate pool.
### cont_plot(x, y, a, b):
        Inputs:
              x = x coordinate points
              y = y coordinate points
              a = index of x variable
              b = index of y variable
        Usage: 
              For plotting contour of x and y.
### f = fun(x):
        Inputs:
              x = Variables
        Outputs:
              f = Function value
        Usage: 
              To get the value of function.
### min_point, fun_val, gen = Genetic_A(fun, no_var, var_lim, no_bit, npop, n_gen):
        Inputs:
              fun = Objective function
              no_bit = No. of bits per variable
              no_var = No. of variables
              npop = Population size
              var_lim = Limits of variables
              n_gen = No. of generations
        Outputs:
              min_point = Minima point
              fun_val = Minimum function value
              gen = Variables of all generations
        Usage: 
              To optimize objective function.
