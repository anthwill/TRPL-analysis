# TRPL-analysis
These programs help to analyze the slope of Time-Resolved Photoluminescence data and produce a minority carrier lifetime. I created this code to expediate the process of acquiring minority carrier lifetime of optoelectronics I have been working with.

The data was collected through the use of the Horiba Fluorolog-3 machine. For this machine, the format is typically a .txt file, which can be imported easily into this program and saved as a DataFrame. If TRPL data is in other formats, there may be slight changes that need to be made to the import code to ensure smooth processing.

I have made a Python program to find TRPL minority carrier lifetimes with extensive direction for using the program. This was aimed to help out those less familiar with the conventions of this code and the nuances of my own programming style. 

There is also a version of the same program with less explanation, making it much more streamlined and limiting the scrolling.

Currently, this code is equipped to fit a single-exponential decay well, with little user input required to produce results. Multi-exponential curves can also be fit, though with the way this code works, there will be some user analysis of the curve to determine the approximate shift from one decay to another. 

To do this, you can look at the Log plot of the data with a single-exponential decay fit overtop. While this fit is much too rough to be an accurate approximation, we can use it to approximate each decay, shifting the slope a bit steeper or a bit shallower than the fit straight line. By also declaring the y-intercept of each slope, the program can accurately find the slope of each decay.
