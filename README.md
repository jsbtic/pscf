# PSCF - Polymer Self-Consistent Field Theory

[![Travis][buildstatus_image_travis]][travisci]

Copyright (2002-2016) Regents of the University of Minnesota

PSCF is a Fortran 90 program for numerically solving the polymer
self-consistent field theory for periodic microstructures formed
by incompressible melts or mixtures of linear block copolymers,
linear homopolymers, and small molecule solvents.

This program is free software; you can redistribute it and/or modify
it under the terms of the GNU General Public License as published by
the Free Software Foundation. A copy of this license is included in
the LICENSE file in the top-level PSCF directory.

# Contributors

- David Morse
- Chris Tyler
- Jian Qin
- Amit Ranjan
- Raghuram Thiagarajan
- Akash Arora

# Dependencies

 PSCF depends upon the FFTW fast Fourier transform library and the
 LAPACK linear algebra library.  These packages must be installed
 before attempting to compile the program from source.

# User Documentation

A web user manual is avalaible at:

    https://pscf.readthedocs.io

Instructions for compiling the program from source, as well as various
ways to install precompiled executables, are given in the user manual.

The source files for the user manual are text files that are stored in
the doc/user-man directory. The relevant files have file extension .rst.

# Developer Documentation

A local copy of the developer API documentation, which includes
documentation for all modules, subroutines and public variables, may
be regenerated by following instructions given in the file doc/README.
The resulting .html page are installed in doc/devel-man.

# Directory Structure

    src/                          - Fortran 90 source files
    doc/                          - documentation files
    doc/user-man                  - - user manual source files
    tools/                        - Tools for processing output and source
    tools/matlab                  - - matlab scripts for visualization
    tools/python                  - - python modules
    make/                         - build directory for make

An annotated list of source files is given in the file src/SRC_FILES.
Before modifying any fortran files, see the note at the end of that
file regarding the use of preprocessor to generate some files.

# Examples

A library of examples is provided in a separate github repository,
located at https://github.com/dmorse/pscf-examples


[buildstatus_image_travis]: https://travis-ci.org/Gjacquenot/pscf.svg?branch=master
[travisci]: https://travis-ci.org/Gjacquenot/pscf