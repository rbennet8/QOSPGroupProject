MATLAB Code for QOSP
Spring 23

Robert Bennet
Katie Geary
Maxwell Lee
Arian Sohrabi
Joshua Stapleton

This MATLAB code serves as a proof of concept for our mathematical model modification. This code is split out into multiple files for the different functions available, however only the Main.mlx file needs to be run, 
as it calls all other functions and files as required. The data.mlx file is our storage of expected data values. Since we expect the effects of frequency to saturate at some point, the curve we are expecting from our
experimental results should be a roughly sigmoidal shape. We therefore assume some rough parameters to get the expected shape, which we then provide the least squares regression (lsqcurvefit) to return the parameters 
to fit that function. In the scenario which we were acting on this research proposal, instead of this theoretical data, we would be feeding in experimental data for the lsqcurvefit() function which would return the 
parameters based on the experimental data. In the event that our experimental data is not returned to be sigmoidal, we would then adjust the equation used for the lsqcurvefit() as needed to match our outcome and 
continue from there. 

There are two options for the subsequent application of this. Prior to running the model itself and solving the ODE's, the gamma value needs to be calculated as demonstrated in example 1 and example 2. Gamma can either
be picked based on an input value where the corresponding function finds the closest matching value and returns the frequency which produces that value as well as the value itself, which would be useful for our AIM 2, 
where we plan to use this output for in vivo validation. The other option is to use the more exploratory function where you input your frequency which you want to investigate, and the regression will provide the expected
permeability at that frequency. This provides researchers with a numerical method to investigate the effects of varying FU parameters before performing an in vivo or even in vitro study.

The end result is that the ODE's we have modified are then solved using the gamma value either produced or selected through frequency input to provide the expected curve for cell number over time.


THANKS!