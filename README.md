# CODE_COLLABORATIF
ENSEMBLE DES CODES POUR LE PROJET DE CODE COLLABORATIF

!gprof -l run gmon.out  > analysis.txt

!gfortran -Wall  -pg -g -O0 main.f90 -o run
C0 CODE NON OPTIMISE
C1 VARIABLES OPTIMISEES
C2 C1+BOX-MULLER IF
C3 C1+BOX-MULLER STEP

gfortran -Wall  -pg -g -O3 -mavx2 main.f90 -o run
C5 C3+UNROLL-JAM

Voir rapport pour compilation
C7 C5+OPENMP-SIMD ifort

