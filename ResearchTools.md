# Research Tools

## Basic Skills

### GitHub
- Learn basic [GitHub skills](https://guides.github.com/activities/hello-world/) from an excellent tutorial : fork, pull, merge

### Unix/Linux

### LaTeX/LyX

1. [LaTeX - Introductory Playlist](https://www.youtube.com/playlist?list=PLSnC4a32tFDpvPrKNEpu1VYQ5PR55QXy0) by E.P. Blair

2. [LyX - Introductory Playlist](https://www.youtube.com/playlist?list=PLSnC4a32tFDrVdmLsQVkAwY5TtOvj83FU) by E.P. Blair


## Advanced Skills

### MATLAB

1. [Intro to MATLAB Booklet](https://github.com/enriquepacis/MATLABIntro) by E.P. Blair

2. [Intro to Object-oriented Programming in MATLAB](https://github.com/enriquepacis/MATLAB_OOP_booklet) by E.P. Blair

### Mathematica

1. [Intro to Mathematica](https://www.youtube.com/watch?v=IQBT29jXLGg&list=PLSnC4a32tFDqBNVkr_1BfIPTXQreWExOu) playlist by E.P. Blair

### Python

## Density Functional Theory - Software

### Atomic Simulation Environment (ASE)

Why ASE? ASE is a Python front end for chemical calculation platforms such as VASP, Quantum ESPRESSO, NWChem, GAMESS, and many others that can make life much easier.
1. Simplicity. Many DFT platforms require complex text input files, and they output user-unfriendly text output files. ASE can manage the input and output files, and it has many well-developed algorithms for importing or creating complex atomic structures.
2. Power. DFT calculations can be supercharged by ASE's Python interface, which allows iteration and visualization. Additionally, ASE can add checkpointing to calculations.

Some *excellent* ASE resources:
1. [ASE Documentation](https://wiki.fysik.dtu.dk/ase/).

2. Install ASE from [GitHub](https://gitlab.com/ase/ase), or, better yet, after you have Python 3 installed on a UNIX/Linux system, use
```bash
$ pip3 install ase
```

If you're not an administrator on a high-performance computing cluster, you may have to ask them to install ASE, or you might get away with installing it only for yourself by typing
```bash
$ pip3 install --user ase
```

3. Read John Kitchin's [book on DFT Calculations using ASE](https://github.com/jkitchin/dft-book). This book uses ASE as a front-end for VASP, but it has a great section on making crystals and molecules using ASE, which is VASP-independent.

4. The [Espresso-ASE](https://wiki.fysik.dtu.dk/ase/ase/calculators/espresso.html) interface documentation. This *includes a tutorial on calculating band structure diagrams*.

5. [*The* paper](https://iopscience.iop.org/article/10.1088/1361-648X/aa680e) on ASE. This is ASE canon right here.

6. Tutorial: [Calculating the Formation Energies of Charged Defects](https://wiki.fysik.dtu.dk/gpaw/tutorials/defects/defects.html). This is a *very rich* ASE example, and it includes supercells, defects, and fairly complex calculations in ASE (with a GPAW calculator). It also has lots of great theoretical background on defect formation energies.

### Theory

Some introductory texts I've found helpful:
1. C. Cramer, [Essentials of Computational Chemistry: Theories and Models (Second Edition)](https://www.amazon.com/Essentials-Computational-Chemistry-Theories-Models/dp/0470091827), John Wiley & Sons, Hoboken NJ (2004)

On my reading list:
1. Szabo and Ostlund, [Modern Quantum Chemistry: Introduction to Advanced Electronic Structure Theory (First Revised Edition)](https://www.amazon.com/Modern-Quantum-Chemistry-Introduction-Electronic/dp/0486691861), Dover (1996)

