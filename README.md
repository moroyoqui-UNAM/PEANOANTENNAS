This is an application to obtain resonance frequencies and VSWR of Peano antennas, they are FASS (space-filling, self-avoiding, and self-similar) type 
with a trace length of S. 
 

Antenna characteristics:
iterations  1 ,2 or 3 \n
lateral size L from 0.001m  to 0.1m
made of metal 
air substrate 
width of  0.25mm, 0.5mm  and 1.0 mm 
feeding point at 1/8S , 7/16S ,5/16S y 1/2S   

Download  &  use 

The application consists of a single file written in Python 3.7 which must be executed from the command line. 


Command line parameters.

p	properties (vswr,resonance)
g	generate the mesh.
a	calculates antenna characteristics


vswr   calculates the center frequency with  VSWR < 2
r		calculates the resonance frequency 
g		generates antenna geometry in a file .m  for processing in MATLAB 
 
i:  antenna iteration (1,2,3)
F:  frequency[MHz](300MHz-3000MHz)
d:  antenna width [mm](0.25,0.5,1.0)
L:  lateral size [m](0.001m-0.1m)
feed:  feeding point [0.125,0.1875,0.4375,0.5]
 

Example

Calculate the resonant frequencies of a Peano antenna with a lateral size L=0.025m,  width d=0.25mm, an iteration i=2 with feed point at 1/8S (0.125S)

python peanoantena.py -p -r -i 2 -L 0.025 -d 0.5 -feed 0.125

Calculate the center frequencies with VSWR <2 of a Peano antenna with a lateral size L=0.033m, width d=0.25mm, an iteration i=3 with feed point at 7/16S (0.4375)

python peanoantena.py -p -vswr -i 3 -L 0.033 -d 0.25 -feed 0.4375

Calculate the properties of an iteration antenna i=1, feed point at 5/16S (0.1875) and resonant frequency F=2200MHz.

python peanoantena.py -a -r -i 1 -feed 0.1875 -F 2200

Calculate the properties of the iteration antenna i=2 with the feed point at 1/2S (0.5) and center frequency with VSWR<2 at 2800MHz.

python peanoantena.py -a -vswr -i 2 -feed 0.5 -F 2800

