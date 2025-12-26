# [J Cal](github.com/LafeLabs/jcal)

The data in the folder [jpa-nopump-scan2-s1p/](jpa-nopump-scan2-s1p/) is from the dilution refrigerator run in the SD dil fridge in room 2138 in building 1 at NIST Boulder in September of 2025, specifially from [September 24, 2025](https://github.com/lafefspietz/MM4250_dil_fridge_september_2025/tree/main/data092425-base).  

 - [jpa-model.html](jpa-model.html)
 - [data folder](../MM4250_dil_fridge_september_2025-main/)
 - [planet jupyter](http://localhost:8888/tree/jcal)
 - [edit-web-files.html](edit-web-files.html)
 - [edit-markdown-files.html](edit-markdown-files.html)
 - [read-markdown-latex-files.html](read-markdown-latex-files.html)
 - [index.html](index.html)

$$
L_J = \frac{\Phi_0}{2\pi I_C}   
$$

$$
L = \frac{L_J}{\cos{\phi}}
$$
$$
\phi = 2\pi\frac{\Phi}{\Phi_0}
$$
$$
\Phi_0 = \frac{h}{2e} \approx 2.07\times 10^{-15} \textrm{ Wb}
$$


Plan: browser front end inputs set flux bias, Ljmin, L0, C0, Cin, coax length, and puts them all into control.json.  coax-jpa.ipynb then takes control.json and creates a one port scikit-rf network object, saves phase and magnitude(which is always 1 in this simplified model) as s11.json, which is passed back to the web page which displays the plotted angle as a function of frequency.  At the same time, real data are plotted for calibrated values of flux in units of phi0 which match the value of the simulation.  We will use this to approach building a model of the system, and eventually using the a fit to a model as the basis of a measurement of various components of the measurement system(launch, coax, connectors).  

We will repeat all of this for a stub on a tee for use in a 2 port cal. We will also repeat all this with the waveguide qubit based power standard.  

All of this will become a paper on the measurement of the JPA with the calibrated switches and modeling of it, as well as the calibration at the plane of the JPA and finally using that to measure the gain of the JPA with a cal.  

Then we will use the qubit cal to calibrate some useful qubit circuit in a standard qubit comparison experiment.  

We want to use the qubit ecal to measure amplifiers. Also look into using nonlinearity of JPA and equations of SQUID to calibrate the power in real watts. Could the JPA be its own noise calibrator by way of a power measurement?  How predictable is that physics?

Finally, this project will involve creating a white paper on how frictionless replication of calibrations can accelerate hardware development cycles across the quantum information technology industry.

 - [jpa-model.html](jpa-model.html)
 - [edit-web-files.html](edit-web-files.html)
 - [qrcode.html](qrcode.html)
 - [graphics/](graphics/)
 - [http://localhost/jcal/](http://localhost/jcal/)
 

![](qrcode.png)

![](graphics/jpa-coax.svg)

Calibration of radio frequency circuits using Josephson Junctions.

