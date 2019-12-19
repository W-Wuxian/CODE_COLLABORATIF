# CODE_COLLABORATIF
AUTHORS: François Barbe & Victor Lederer

ENSEMBLE DES CODES POUR LE PROJET DE CODE COLLABORATIF

gfortran -Wall  -pg -g -O0 main.f90 -o run
gprof -l run gmon.out  > analysis.txt

voir les analysis* des repertoires pour retrouver les résultats du rapport:
lien du rapport : https://www.overleaf.com/read/xhjvgjtdtbdm

C0 CODE NON OPTIMISE    --> NO_OPT.zip
C1 VARIABLES OPTIMISEES --> VAR_OPT.zip
C2 C1+BOX-MULLER IF     --> BOX_MULLER_FORME1.zip UNCOMMENT IF COMMENT STEP
C3 C1+BOX-MULLER STEP   --> BOX_MULLER_FORME1.zip

gfortran -Wall  -pg -g -O3 -mavx2 main.f90 -o run
C5 C3+UNROLL-JAM        --> BOX_MULLER_UNROLL.zip

Voir rapport pour compilation
C7 C5+OPENMP-SIMD ifort --> C7_PLAFRIM.zip

Nous avons pas rajouté le .zip des versions des codes qui n'apportent rien à l'optimisation
efficace comme par exemple la version polaire de box-muller qui est en terme de temps de
calcul moins efficace que celle de boxe-muller forme1.

