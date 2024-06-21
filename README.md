# Computing Skills Toolkit — Basic Example

This is a fairly minimal working example which incorporates and allows building the necessary elements of the projects in this series, and can be used as a base repository for each problem set in the module.

It provides all of the necessary elements for compiling programs using the [GNU Scientific Library (GSL)](https://www.gnu.org/software/gsl/) and [gnuplot-iostream](https://github.com/dstahlke/gnuplot-iostream) (for plotting).

## Compiling

### Dependencies

 - A C++ compiler supporting the C++17 standard
 - CMake >= 3.1.0
 - [GSL](https://www.gnu.org/software/gsl/) (on Ubuntu-based distributions, this can be installed with `sudo apt install libgsl-dev`)
 - Boost components from Boost >= 1.71.0 (`sudo apt install libboost-all-dev`):
   - `iostreams`
   - `system`
   - `filesystem`

### Build Instructions

Building is fairly straightforward using CMake as the build system. However, you must make sure to clone the git repository recursively in order to retrieve all of the necessary libraries:

```bash
git clone --recursive https://github.com/CDT-Numerical-Exercises/BasicExample
cd BasicExample
mkdir build && cd build
cmake -DCMAKE_BUILD_TYPE=Release ..
make -j4
```

This will build all executables under `BasicExample/build`, and these can be run directly from there.
