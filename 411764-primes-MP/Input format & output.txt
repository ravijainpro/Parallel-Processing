A C++ code which counts the number of primes between 1 and N, using OpenMP to carry out the calculation in parallel. For each integer I, it checks whether any smaller J evenly divides it. The total amount of work for a given N is thus roughly proportional to 1/2*N^2.

In the BASH shell, the program could be run with 2 threads using the commands:
	1>	export OMP_NUM_THREADS=2
	2>	g++ -c -Wall -fopenmp prime_openmp.cpp
	3> 	g++ -fopenmp prime_openmp.o
	4>	./a.out



=================Output======================

(base) ravijain@ravijain-HP-Pavilion-Laptop-15-cc1xx:~/Desktop/openMP/Prime$ ./a.out 

PRIME_OPENMP
  C++/OpenMP version

  Number of processors available = 8
  Number of threads =              2

TEST01
  Call PRIME_NUMBER to count the primes from 1 to N.

         N        Pi          Time

         1         0     0.000186855
         2         1       7.483e-06
         4         2     5.44199e-06
         8         4     5.87601e-06
        16         6     6.05201e-06
        32        11       5.861e-06
        64        18       1.007e-05
       128        31      2.4259e-05
       256        54      8.1105e-05
       512        97     0.000261008
      1024       172     0.000903265
      2048       309      0.00331418
      4096       564       0.0132808
      8192      1028       0.0321918
     16384      1900       0.0611634
     32768      3512        0.172317
     65536      6542        0.599941
    131072     12251         2.05724

TEST01
  Call PRIME_NUMBER to count the primes from 1 to N.

         N        Pi          Time

         5         3     2.31601e-06
        50        15       1.668e-06
       500        95      5.8827e-05
      5000       669       0.0040472
     50000      5133        0.320499
    500000     41538         27.2001

PRIME_OPENMP
  Normal end of execution.

