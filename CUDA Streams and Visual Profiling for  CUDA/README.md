
CUDA Streams and Visual Profiling for CUDA

Accelerating and Optimizing an N-Body Simulator

An [n-body](https://en.wikipedia.org/wiki/N-body_problem) simulator predicts the individual motions of a group of objects interacting with each other gravitationally. [01-nbody.cu](../edit/09-nbody/01-nbody.cu) contains a simple, though working, n-body simulator for bodies moving through 3 dimensional space. The application can be passed a command line argument to affect how many bodies are in the system.

In its current CPU-only form, working on 4096 bodies, this application is able to calculate about 30 million interactions between bodies in the system per second. Your task is to:

- GPU accelerate the program, retaining the correctness of the simulation
- Work iteratively to optimize the simulator so that it calculates over 30 billion interactions per second while working on 4096 bodies `(2<<11)`
- Work iteratively to optimize the simulator so that it calculates over 325 billion interactions per second while working on ~65,000 bodies `(2<<15)`
