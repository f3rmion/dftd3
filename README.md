# Extensions to the *dftd3* program

Some *dftd3* (see [*JCP* **132**, 154104 (2010)](https://dx.doi.org/10.1063/1.3382344) and [*JCC* **32**, 1456 (2011)](https://dx.doi.org/10.1002/jcc.21759) for details) extensions. This version of dftd3 is able to fix coordination numbers (CNs) for simple energy calls within molecular and periodic energy calculations.

This is easily possible by running

```bash
dftd3 coord -func pbe -bj -fixcn
```

Please note that one has to write a "fixcns" file beforehand, which is defined as follows:

```bash
1 2.3  
2 3.4
15 0.9
158 1.0
```

Within this example the CN-values for atoms 1, 2, 15, and 158 are constrained to values of CN<sub>1</sub>=2.3, CN<sub>2</sub>=3.4, CN<sub>15</sub>=0.9, and CN<sub>158</sub>=1.0 for some random molecule. 
