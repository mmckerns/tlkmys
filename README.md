mystic: a brief introduction
=============================

The `mystic` framework enables the solving of difficult optimization problems through three major innovations: (1) plug-and-play component-based optimization algorithms, (2) the ability to dynamically construct and apply generalzed trnasforms, `K`, where `x' = K(x)`, and (3) workflows providing asynchronous execution and statefulness.

These features, in conjunction with supporting packages `pathos`, `pyina`, and `klepto`, can provide massively-parallel scalable workflows for quickly solving optimization problems in complex nonlinear spaces. `mystic` can be used to simplify non-convex optimization problems by transforming away nonlinearities through user-built kernel transforms

This talk demonstrates using `mystic` for machine learning with automated dimensional-reduction, using embarrasingly parallel solver ensembles to find an accurate interpolated surrogate for a nonlinear surface, and the determination of worst-case bounds on expectation value of an objective function under uncertainty.


In this talk, I'll introduce mystic, a python package for nonconvex optimization, machine learning, and uncertainty quantification. mystic provides a simple interface to configuring and solving difficult constrained optimization problems.

First, I'll demonstrate how mystic provides a scipy.optimize-like interface to solving optimization problems. Then, I'll show how mystic solvers can be configured to include things like callback functions, parameter monitors, and constraints solvers. Constraint solvers can be thought of providing a mapping or transform into a simpler coordinate space. Next, I'll show mystic's expanded (class) interface, which allows more granular customization. Then, I'll discuss the use of penalty functions and constraints, showing how both type of transforms can be used to enforce information within the optimization problem. Then, I'll demonstrate how mystic provides asynchronous execution, solver restarts, saved state, and automated dimensional reduction.  I'll then demonstrate using a parallel ensemble of solvers for customizable machine learning, interpolation, and uncertainty quantification.  I inlude a brief interlude on using pathos, pyina, and klepto, which can be used to augment mystic for large-scale parallel computing and database interaction.

The audience should gain an understanding of how to use mystic to augment their data analytics and modeling.



Content
---------

All talk content can be obtained from this repository either with
`git, or by downloading the repository content as a zip file.  If you use
git, you can clone this repostory with::

    $ git clone https://github.com/mmckerns/tlkmys.git


or, download and unzip the zipfile.



Requirements
--------------

To be able to run the examples, demos, and exercises in this talk,
the following packages must be installed::

    numpy >= 1.15.2,
    matplotlib >= 2.2.2,
    sklearn >= 0.20.0,
    dill >= 0.2.9,
    pyina >= 0.2.1,
    pathos >= 0.2.6,
    klepto >= 0.1.6,
    mystic >= 0.3.6


Installation
--------------

All packages can be installed with `pip`::

    >$ pip install setuptools
    >$ pip install numpy
    >$ pip install matplotlib
    >$ pip install sklearn
    >$ pip install pyina
    >$ pip install pathos
    >$ pip install klepto
    >$ pip install mystic


The `pip` installs of `numpy`, `matplotlib`, and `sklearn` often fail.
A more stable choice for installing these three packages is to use a
scientific python distribution such as `canopy` or `anaconda`.

