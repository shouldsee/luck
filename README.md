# LUCK: LUigi-based Compiling Kit 

## Overview:

Makefile is traditional and is great. But makefile can be difficult to debug, interrupt. 
In contrast, pdb module in python allows very easy high-level debugging as compared to gdb.
Since my quick search did not reveal any obvious Python alternative to gnu-make, I decided
to adapt the well-known pipeline manager [**luigi**](https://github.com/spotify/luigi) to 
check and resolve the dependency.

This is so far a personal project that helped me understood how luigi works, but if anyone
find this useful, feel free to write documentation / extension modules and make issues/PR.

## Improvements:

- Performance is not tested at all.
- Python is not the best language for writing a build system because of its poor portability.
I am using python because it is more expressive than a static yaml/json file. It would be 
great if we can write a parser in c/cpp/go to emulate a reduced version of python.
- profiling gprof
- dry run dependency graph

## install 

```bash
pip install luck@https://github.com/shouldsee/luck/tarball/master
```


## Example

adapted from ECE264

```bash
cd example-ece264-hw04.dir
luck clean
luck testall
echo [FIN]
```
