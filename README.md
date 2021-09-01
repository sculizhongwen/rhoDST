![enter image description here](https://user-images.githubusercontent.com/30440239/129488825-eb1f5388-fe71-45bf-9f60-6a9d69466836.jpg)

# rhoDST
This repository provides a density based solver **rhoDST** for steady and unsteady simulation of high speed compressible flows over aeronautical vehicles. The proposed solver **rhoDST** has been developed based on  foam-extend 4.1  libraries for the fully-coupled solution of governing equations on highly skewed unstructured meshes. 

![BG1](https://user-images.githubusercontent.com/30440239/131627275-4d343da5-bcdc-4502-8275-a7f8de4ea75a.jpg)
 

# Features

 - Continuity, momentum and energy equations are implicity coupled in a single matrix.  The corresponding matrix can be solved using block-matrix solvers such as GMRES, BICG and multigrid methods. 
 - Local time stepping is used for the fast convergence to the steady-state solution. 
 - Shock-discontinuities can be captured using Kurganov, AUSM, AUSM+, AUSM+up, HLL, HLLC and HLLCP shock-capturing methods. 
 - Modifications of SpalartAllamaras turbulence model are incorporated to the turbulence libraries. Simpler Rotation-Curvature and Spalart-Shur rotation/curvature correction are implemented to account for rotation and curvature effects.  Negative Spalart-Allmaras is implemented to resolve numerical issues near the interface between turbulent and irrotational regions. 
 - Characteristic far-field boundary conditions are used at the outer boundaries for subsonic, transonic and supersonic freestream flows. 
 
# Installation Guide
The dependencies for the solver **rhoDST** are the same as for foam-extend-4.1 and by installing foam-extend-4.1 all dependencies would be satisfies. Before compiling the solver **rhoDST**, environment variables must be set for foam-extend-4.1.

```bash
cd $WM_PROJECT_USER_DIR
git clone https://github.com/DSTECHNO/rhoDST rhoDST
cd rhoDST
./Allwmake
```


# Developers

Ender Demirel, PhD

Aras Dogan


