# Time Warped Edit Distance

This is a python wrapper for Marteau's implementation of his 2009 paper introducing TWED (slightly modified and provided here). TWED is probably the current most accurate distance metric for timeseries data.

Follow the example build string to produce a shared library loadable in python2. Adjust as needed.

The module can then be loaded directly like so:

```
import twed
import numpy
seq1 = numpy.array([[1.0], [2.1], [3.2], [4.3], [5.4]]).astype('float64')
seq2 = numpy.array([[9.8], [7.6], [6.5], [4.3], [2.1]]).astype('float64')
ts1 = numpy.array([1., 2., 3., 4., 5.]).astype('float64')
ts2 = ts1.copy()
twed.twed(seq1, seq2, ts1, ts2)
```

So long as the shared library produced is in the `PYTHONPATH`.

I'm uploading this in case it can be useful to someone, but this isn't exactly a well-structured project with maintenance goals.

TODO:
* properly design build instructions
* properly package this
