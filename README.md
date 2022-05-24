# HiGGS Calibration Survey

## About

Survey by the [HiGGS](https://github.com/wevbarker/HiGGS) package of Poisson brackets between primary and secondary constraints for 192 modified gravity theories with curvature and torsion.

See [HiGGS README.md](https://github.com/wevbarker/HiGGS/README.md) and references therein for

## Installation
1. Make sure you have [installed xAct](http://www.xact.es/download.html).
2. Download HiGGS:
	```bash, git
	git clone https://github.com/wevbarker/HiGGS-calibration-survey
	cd HiGGS
	tar -xzvf svy.tar.gz
	```
3. Place the `./svy` directory in the working directory of your Mathematica notebook

## Quickstart 

The package loads just like any other part of xAct, just open a fresh notebook and run:
```wolfram
$Path~AppendTo~NotebookDirectory[];
Needs["xAct`HiGGS`"];
BuildHiGGS[];
```
This loads the package (i.e. the names of the functions provided), along with its dependencies in the xAct bundle. However it does _not_ load the physics. To construct the HiGGS environment, one must run:
```wolfram
ViewTheory["simple_spin_1p_","Literature"->True,"PPM"->True,"Velocities"->False];
```
