# HiGGS Calibration Survey

## About

Survey by the [HiGGS](https://github.com/wevbarker/HiGGS) package of Poisson brackets between primary and secondary constraints for 192 modified gravity theories with curvature and torsion.

See [HiGGS README.md](https://github.com/wevbarker/HiGGS/README.md) and references therein for all details, conventions, notation and motivation.

## Installation
1. Make sure you have [installed HiGGS](https://github.com/wevbarker/HiGGS).
2. Download the survey: 
	```bash, git
	git clone https://github.com/wevbarker/HiGGS-calibration-survey
	cd HiGGS-calibration-survey
	tar -xzvf svy.tar.gz
	```
3. Place the `./svy` directory in the working directory of your Mathematica notebook.

## Quickstart 

The theory files `./svy/simple_spin_*.thr.mx` contain all the physics. Everything under `./svy/node-*` pertains to clocking.

The `.thr.mx` theory files use a conventions in which _vanishing_ multiplier couplings (convention is `A` for "alpha" couplings and `B` for "beta" couplings) are appended to the file name, but only if they are not constrained by default.

Open a fresh notebook in the same directory as `svy` and run:
```wolfram
$Path~AppendTo~NotebookDirectory[];
Needs["xAct`HiGGS`"];
BuildHiGGS[];
```
You should end up in a HiGGS environment. To view the constraint and bracket structure of a given theory, such as the minimal spin-parity 1<sup>+</sup> case with all (surveyed) multipliers active, try
```wolfram
ViewTheory["simple_spin_1p_","Literature"->True,"PPM"->True,"Velocities"->False];
```
