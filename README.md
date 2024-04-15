# penrose
Generate a piece of the Penrose tiling using [N. G. de Bruijn's pentagrid method](https://www.math.brown.edu/reschwar/M272/pentagrid.pdf). A _pentagrid_ is made up of five copies of a regularly spaced grid of parallel lines where each new copy is rotated by a 5-fold rotation ($\frac{2\pi}{5}$ radians) relative to the one that came before it. The crux of this method is to find all points of intersection between the lines of the multigrid. Each intersection corresponds to a tile. Further algebraic manipulation gives the type and orientation of the tile. The details of the method, and the proof that it works, is in De Bruijn's manuscript linked above. Here, I've provided a quick practical overview of how to use this repository to generate a Penrose tiling. 

## Quickstart

The main workhorse is the class `Pentagrid` which takes one required argument: `gammas`, a list of five real numbers. In order for the generated tiling to be a Penrose tiling, the five real numbers must sum to zero. If they don't, we get a  _generalized Penrose tiling_. I'll come back to these later, but for now, let's assume that the five real numbers some to zero.  

The particular section of the Penrose tiling that will be generated depends on what these numbers are. 


