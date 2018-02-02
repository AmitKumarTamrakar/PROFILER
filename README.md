# PROFILER 1D Decomposition [v2.0]

This repository contains the code Profiler, a Python program for decomposing galaxy light profiles in 1D

#COMPATIBILITY:

Tested on Mac OSX Yosemite and Linux Ubuntu 14.04, 16.04 LTE

#REQUIREMENTS:

1. Pre-installed Python distribution (Ureka - which contains PyRAF - is good: http://ssb.stsci.edu/ureka/). Python 2.7 recommended, Python 3 not tested but may have incompatibilities.

2. The Python library lmfit version 0.8.3 (https://pypi.python.org/pypi/lmfit OR if pip is available, then in the terminal $> pip install lmfit==0.8.3)

3. A LaTeX distribution, necessary for generating the figures (the special fonts are required). Note, the code fits and generates logfile with results without this, but does not make the plots.

#RECOMMENDED INSTALLATION

1. Extract the profiler2.0 directory from the .tar archive in a desired location
2. Edit the .bashrc (or .cshrc) file to contain the line:
  alias profiler='python path/to/profiler2.0/profiler.py' (if using bash terminal)
  alias profiler python path/to/profiler2.0/profiler.py   (if using cshell)
3. In the terminal, type "$> source ~/.bashrc" for bash or "$> source ~/.cshrc" for cshell

#USE

If an alias is created as above, then from the terminal, in any directory, typing "$> profiler" will launch the GUI. The input should be an ASCII file located in the working directory (wherever Profiler was launched from), and should have either the format generated by IRAF Ellipse, IRAF Isofit (http://adsabs.harvard.edu/abs/2015ApJ...810..120C) or a 2-column file (isophote semi-major axis and INTENS).

Attached to the release is a step-by-step tutorial providing an example galaxy decomposition.

For details on the use of the code to decompose galaxy profiles, please refer to the accompanying paper (Ciambur 2016, arXiv:1607.08620/PASA 33, 62;  or at http://adsabs.harvard.edu/abs/2016PASA...33...62C).

#N.B. 

It is recommended to start fitting without the PSF convolution (i.e., set its FWHM to 0). This is done very quickly and the result can be used to update the guesstimate parameter values. Then the fit can be run WITH the PSF convolution to get the exact solution.

#ACKNOWLEDGEMENT

If PROFILER was useful for your research, please provide an acknowledgement by citing the above paper.

Thank you! Happy decomposing!
