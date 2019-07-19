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

Note: at this time, our interface between Python 3.7.2 and ASE and QE 6.3 is not working well. Possible solutions:
- Try Python 3.6 instead
- Use [GPAW](https://wiki.fysik.dtu.dk/gpaw/index.html) instead

5. [*The* paper](https://iopscience.iop.org/article/10.1088/1361-648X/aa680e) on ASE. This is ASE canon right here.

6. Tutorial: [Calculating the Formation Energies of Charged Defects](https://wiki.fysik.dtu.dk/gpaw/tutorials/defects/defects.html). This is a *very rich* ASE example, and it includes supercells, defects, and fairly complex calculations in ASE (with a GPAW calculator). It also has lots of great theoretical background on defect formation energies.

### GPAW

This appears to be an excellent, open-source, Python-based DFT calculator. It is built as a Python calculator for the ASE, so the GPAW-ASE integration is natural, and compatibility issues as in the ASE-ESPRESSO interface should be non-existent.

1. There are many great GPAW tutorials available:

- Calculate band structure diagrams ([GPAW tutorial](https://wiki.fysik.dtu.dk/gpaw/exercises/band_structure/bands.html))
- Structural relaxation ([GPAW tutorial](https://wiki.fysik.dtu.dk/gpaw/tutorials/H2/optimization.html))
- Calculate formation energies ([GPAW tutorial](https://wiki.fysik.dtu.dk/gpaw/tutorials/defects/defects.html), including defects, electrostatic correction terms, and chemical potentials)
- Calculating band-gap corrections ([GPAW tutorial](https://wiki.fysik.dtu.dk/gpaw/exercises/gw/gw.html))
- More on building supercells ([ASE tutorial](https://wiki.fysik.dtu.dk/ase/tutorials/defects/defects.html), [VASP Blog by Dr. P. Larsson](https://www.nsc.liu.se/~pla/blog/2013/02/26/vaspsupercells/))
  
#### GPAW Setup

GPAW requires some setup on Kodiak.
1. Download the pseudopotentials. This is done as follows
- On Kodiak, navigate to a place where you want to install the GPAW data files.
- If you haven't already put ```module load python/3.7.2``` into your ```.bashrc``` file, load that module in the command line after the prompt ($), like this:
```bash
module load python/3.7.2
```
- Now, install the GPAW data using this command:
```bash
gpaw install-data
```
- Make note of the path to your installation data. For me, the installation created a folder ```gpaw-setups-0.9.20000```. Specifically, this is
  ```
  /ion/home/blaire/materials/gpaw/gpaw-setups-0.9.20000
  ```
and this can be referenced more simply using the ```~``` shortcut for my personal space ```/ion/home/blaire```

2. Add lines to your ```.bashrc``` file which creates some environment variables:
```bash
export GPAW_SETUP_PATH=~/materials/gpaw/gpaw-setups-0.9.20000
export OMP_NUM_THREADS=1
```
For more information on this, see the [GPAW installation instructions](https://wiki.fysik.dtu.dk/gpaw/install.html) (especially the "Environment Varibles" section)

### Quantum ESPRESSO

1. Tutorials
  a. [Getting Started (Shanghai 2013)](https://www.quantum-espresso.org/resources/tutorials/shanghai-2013) - this tutorial has a great [Getting Started](https://www.quantum-espresso.org/resources/tutorials/shanghai-2013/getting-started/lecture1.pdf) lecture which gives a nice outline of the SCF process and an input file description. Also included are instructions on the exercises (note: the exercise code, I believe, comes with the QE software in the form of bash scripts which write input files and run calculations).
2. Documentation
   - The [pw.x input file description](https://www.quantum-espresso.org/Doc/INPUT_PW.html) - a very useful reference with information on all the inputs to *pw.x*
3. Pseudopotentials
   - The [Pseudopotential library](https://www.quantum-espresso.org/pseudopotentials) - find and download pseudopotentials here.


## Theory

### Textbooks

Some introductory texts I've found helpful:
1. C. Cramer, [Essentials of Computational Chemistry: Theories and Models (Second Edition)](https://www.amazon.com/Essentials-Computational-Chemistry-Theories-Models/dp/0470091827), John Wiley & Sons, Hoboken NJ (2004)

On my reading list:
1. Szabo and Ostlund, [Modern Quantum Chemistry: Introduction to Advanced Electronic Structure Theory (First Revised Edition)](https://www.amazon.com/Modern-Quantum-Chemistry-Introduction-Electronic/dp/0486691861), Dover (1996)


### Writing
Technical writing is one of the most important parts of our work as researchers. No matter how stunning the results, novel research will not matter to anyone unless it is clearly and insightfully communicated. This means making difficult concepts as clear as possible and laying out arguments and derivations in an organized manner. It also means not simply presenting data to the readers, but also giving them a clear and compelling interpretation. Here are some quick tips on writing papers:

0. Have a clear concept of the story you're trying to tell. Even technical writing tells a story: it has a context, poses a problem, and identifies a solution.

1. Write in the following order, which may seem counterintuitive, but can be quite helpful:
- Start with the figures. Then add captions to each figure. When ordered, figures and captions will provide the structure of the manuscript. It will then be fleshed out with words.
- When writing:
  - Write the \it[Results] section first.
  - Next, write the \it[Background] section. Having already written the results up, you can now provide only the background information necessary to convey the desired results: nothing more, and nothing less.
  - Finally, write the introduction and the conclusion. The introduction should provide the context and tell the reader why this paper is significant. The conclusion should emphasize the take-aways from the manuscript.
  - A \it[Discussion] section could be included that provides some analysis or synthesis of the results that is at a level that is not quite at the level of broad, concise overview provided by the conclusion.
 
2. Be clear and purposeful.
 - Each figure, paragraph, and sentence should have a purpose in the narrative.
 - Each paragraph should have a topic sentence that provides that states the theme of its paragraph. Typically, this will be the first sentence. Supporting sentences will follow this and elaborate on the paragraph's topic by providing additional detail or information.
 
3. Be concise.
 - Avoid using too many words or run-on sentences. Run-on sentences may often be broken up into shorter sentences.
 - Active verbs typically provide clarity and conciseness. Passive verbs involve the some form of the verb "to be" (was, is, are, will be) and another verb. To make a passive verb active, eliminate the "to be" and simply use the other verb.
   - Passive example: "B is shown by A."
   - Active example: "A shows B."
   
4. Good figures are very important, because if used well, they can clearly convey your result. On the other hand, poorly-crafted figures can confuse the readers or mislead them. Here are some tips for figures.
 - Make sure that text and legends are legible. Avoid using figure text much smaller than the text in the manuscript.
 - A good caption begins with a sentence that tells the reader (clearly) what the figure means. Additional details can be provided after this opening sentence.

