The folders in this directory correspond to the cases used for the calculation of the interfacial/surface tension (gamma) and the thermal conductivity and viscosity (kappa and mu).

For the calculation of the thermal conductivity and viscosity, we a simulation box with periodic boundary conditions all around. The liquid fills up the entire simulation box. An initial NPT simulation is performed to resize the simulation box in order to obtain the correct pressure. Then an NVT simulation is performed to obtain the properties. 

For the interfacial tension between benzene and water we follow a similar approach. Now the two liquids are stratified within the simulation box. Again an NPT and NVT run is used to control the pressure and temperature

For the calculation of the surface tension (i.e. water/benzene with vacuum), we follow a similar approach. However, the liquid only fills up half of the simulation box, and the other half remains empty, obtaining a free surface. We also don't run an NPT simulation, as that would simply rezise the simulation box. T

Notes
------
1. We only show the calculation of the properties at pressure 1 Bar and temperature 275K. These can easily be changed in the run.in.nve file in the nvt fix command (applies to all quantities, gamma, kappa and mu) and the npt fix command (doesn't apply to gamma) 
2. The initial microstate can be changed by changing the random seed in the velocity command at the end of the system.in.settings file
3. These runs are relatively short compared to the cases of the droplet migration