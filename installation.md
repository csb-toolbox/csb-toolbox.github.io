System Requirements
-------------------

CSB is distributed as a pure python package, which renders it cross-platform.
Installation is therefore a very trivial task. The source code is also kept
compatible across Python versions, so we guarantee that every official release
package will work on both Python 2 and 3 without any change. We test all nightly
builds against Python versions 2.7 and 3.6, but technically CSB should run on 
Python 2.6 and all subsequent versions except probably 3.0.


User Installation
-----------------

Install ``csb`` from PyPi:

    $ pip install csb

``pip`` will take care of all necessary dependencies. However, on Windows this might
fail. If this is the case, install ``numpy`` and ``scipy`` manually and rerun the pip
installation shown above. The easiest way to get ``numpy`` and ``scipy`` on Windows is 
to get them from [this site](http://www.lfd.uci.edu/~gohlke/pythonlibs/). Or if
you are using Anaconda:

    $ conda install numpy scipy
    $ pip install csb


Developer Installation
----------------------

ABOUT DEPENDENCIES

CSB depends on 2 very well-known and readily available python packages:

* [numpy](https://pypi.python.org/pypi/numpy) - required
* [scipy](https://pypi.python.org/pypi/scipy) - required
* [matplotlib](https://pypi.python.org/pypi/matplotlib) and 
  [wxPython](https://pypi.python.org/pypi/wxPython) - optional, needed only 
  if you want to use ``csb.io.plots``

``epydoc`` is required to build the API documentation.


INSTALLATION

First get the source code from github::

    $ git clone https://github.com/csb-toolbox/CSB.git
    $ cd CSB

Then install the project in editable mode::

    $ pip install --editable .[dev]

``pip`` will take care of all runtime and development dependencies and make the source
code location importable. No need to modify your ``$PYTHONPATH``.

If dependencies cannot be resolved on your system - this is often the case on
Windows - the best way to go from here is to install Anaconda. Then use the conda
package manager to install all missing packages:

    $ conda install --file requirements.txt
    $ pip install --editable .[dev]



Testing
-------

Running the CSB test suite may be useful in order to check if your installation works.
All CSB tests are executed with the ``csb.test.Console``. A typical way to run the 
console is:

    $ csb-test "csb.test.cases.*"


