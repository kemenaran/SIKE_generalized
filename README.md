# SIKE_generalized

Supersingular isogeny graph key exchange, using prime numbers (2,3) as in the spec, or any odd prime, as in the paper from Costello and Hisil.

### Run instruction

Contains a makefile.
To run the protocole, type

$ make

$./Main

To run the protocole with the profiler, use "makefile_with_profiling" instead.

By default, the protocole is run with parameters from specification, with prime of size 503. To run any other parameters, just uncomment the right set in the Main.c file.

### Content

Header.h with declarations.

fp.c to initialize, handle and clear elements in fp2.

curve_point.c to initialize, handle and clear curve and points.

montgomery.c contains methods for Montgomery's arithmetic.

isogeny.c contains methods to compute images from curves and points by 2, 3, or any odd degree isogeny.

pk_sk_param.c  contains methods to initialize, set and clear public parameters, private key and public key, including key generation and key exchange.

Main.c contains wrappers for key generation and key exchange, and a set of tests to run the protocole.

Makefile for a neat compiling.

Rapport_Mathilde.pdf contains a short summary of mathematical background around isogeny graphs, a description of the key exchange protocol, some optimization technics, and a more detailled explaination from the code, as well as performances comparisons. And very nice graphics.

### Strategies

Being processed in branch strategy.
