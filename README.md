# Introduction
This code is authored by Ben Barsdell. The code can be found in Google Code Archive (https://code.google.com/archive/p/dedisp)

dedisp provides a simple C interface to computing dedispersion transforms using a GPU. The interface is modelled on that of the well-known FFTW library, and uses an object-oriented approach. The user first creates a dedispersion _plan_, and then calls functions to modify or execute that plan. A full list and description of the functions provided by the library can be viewed in the API documentation below.

# Dependencies

The library requires NVIDIA's CUDA in order to access the GPU. This also imposes the constraint that the target hardware must be an NVIDIA GPU. To compile the library you must have the NVIDIA CUDA C compiler _nvcc_ in your path.

# Installation

- Modify the entries in Makefile.inc to suit your system.
- Run make.

If all goes well, the library will be built in the lib/ subdir and the header in include/ subdir. If something goes wrong, please let me know either via email or the project website.

# Debugging

The following make flag can be used to build the library in a
debug mode, which will print the location and description of errors as
they happen:

`$ make DEDISP_DEBUG=1`

# API Documentation

View the API documentation in the html/ subdir (dedisp_8h.html).

# C++ Interface

A simple C++ wrapper for the library is also provided; see src/ subdir (DedispPlan.hpp).
