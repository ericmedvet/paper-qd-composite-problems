# Quality-Diversity in Problems with Composite Solutions: a Case Study on Body-Brain Robot Optimization
Code repository for the paper "Quality-Diversity in Problems with Composite Solutions: a Case Study on Body-Brain Robot Optimization"

This repository contains two files which can be used to re-run all the experiments described in the paper.
The execution requires to install and use [JGEA](https://github.com/ericmedvet/jgea), in particular the version [2.7.0](https://github.com/ericmedvet/jgea/releases/tag/v2.7.0).

Once you have installed it, you can execute the experiments as follows.
For the experiment concerning the *reaching* task:
```shell
java -jar io.github.ericmedvet.jgea.experimenter/target/jgea.experimenter-2.7.0-jar-with-dependencies.jar -nr 4 -nt 16 -f reaching.txt
```
where `-nr 4` means that 4 evolutionary runs will be executed concurrently and `-nt 16` means that 16 threads will be used.
Adjust the last value (`-nt`) to match the number of cores of your machine (or the one you want to actually use).
For the *covering* task:
```shell
java -jar io.github.ericmedvet.jgea.experimenter/target/jgea.experimenter-2.7.0-jar-with-dependencies.jar -nr 4 -nt 16 -f covering.txt
```

The outcome will be a folder (with subfolders) containing videos, plots, `.csv` files, basically a superset of the ones shown in the paper.
Consider that each one of the two executions takes, on a modern machine with 36 cores, some days to complete.

