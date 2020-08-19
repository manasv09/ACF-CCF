# GP 503
## Assignment 01 - Computing ACF & CCF

The Correlation class below implements the following methods-

- **__init__**(algo): algo is either **acf** or **ccf** and to be provided when the Correlation object is created.

- __call__(x, tau, y): This function takes 2 parameters for algo = **acf** or 3 parameters for algo = **ccf** and a parameter tau(lag).

- **acf**(x, tau): Implemented function for calculating the acf of a time series signals by padding them first and then performing dot product for all discrete values in range of **tau**.

- **ccf**(x, y, tau): Implemented function for calculating the ccf of two distinct time series signals (need not be equal in length) by padding them first and then performing dot product for all discrete values in range of **tau**.

- **autocorrelate**(x, tau): Modified the builtin function **numpy.correlate()** to compute the Auto Correlation of a signal for discrete values in range of **tau** and store values for plotting.

- **crosscorrelate**(x, y, tau): Modified the builtin function **numpy.correlate()** to compute the Cross Correlation of two signal for discrete values in range of **tau** and store values for plotting.

- **plot**(): Plots the values of acf/ccf w.r.t values in the range of tau.


## Input format-  

1. Run the file in the terminal using `python3 assign1.py`

2. Enter **0** for providing input using a **.txt file** or, **1** for providing input in terminal.

### Terminal input format-

1. Enter three space seperated integers **least_value** **max_value** **size** for series A.

2. Enter an integer specifying the value of **tau**.

3. Enter the algo type **acf** or **ccf**.

    - If algo type **ccf**, enter three space seperated integers **least_value** **max_value** **size** for series B.

### Input file format-

Multiple inputs can be provided at once and plots of all can be viewed in a sequential manner. Sample inputs are shown below-

    0 20 10
    5
    acf
    0 100 500
    65
    ccf
    0 50 75

> Line 1 specifies the **least_value** **max_value** **size** for series A for first input. Line 2 is the value of **tau**. Line 3 is the algo type. If **acf** then first input ends here.

> Line 4 specifies the **least_value** **max_value** **size** for series A for secod input. Line 5 is the value of **tau**. Line 6 is the algo type. If **ccf** then the next line should contain **least_value** **max_value** **size** for series B.

### Results
![Plot 1](/plots/plot1.png)
![Plot 2](/plots/plot2.png)
