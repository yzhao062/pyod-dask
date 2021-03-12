Dask on PyOD (PyOD-Dask)
========================

As the most popular outlier detection toolbox, `PyOD <https://github.com/yzhao062/pyod>`_
has been widely used in academia and industry for detecting outliers/anomalies.

One pending issue of PyOD is it is built with native Python along with
numpy, scipy, and scikit-learn, more importantly **joblib**
(`documentation <https://joblib.readthedocs.io/en/latest/>`_),
which does not scale nicely in distributed environment, e.g., a cluster of
machines.

To fix this, we designed this embarrassingly extension of PyOD based on
`Dask <https://dask.org/>`_, one of the leading distributed framework for data analytics.
Without fully redesigning PyOD, we leverage Dask as the backend of Joblib-enabled
programs, **brining 2-10 times faster calculation on the same machine**.
See (`this article <https://ml.dask.org/joblib.html>`_) for details.

PyOD-Dask is featured for:

* **Same API as PyOD** but **much faster**!
* May scale seamlessly to a cluster of machines (to be verified).


----


Important Notes
^^^^^^^^^^^^^^^

1. Different PyOD models may show different degree of acceleration effect.

2. It is under development. **Please star/follow and come back for latest progress**.

PyOD vs. PyOD-Dask
^^^^^^^^^^^^^^^^^^

Table to fill

===================  ================  ============  ============  ============  ============  ==============
Algorithm            Dataset           # Samples     # Dims        PyOO          PyOD-Dask     Times Faster
===================  ================  ============  ===========   ============  ============  ==============
kNN
LOF
===================  ================  ============  ===========   ============  ============  ==============

