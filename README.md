# ML_Proj
CryoTankBCSim

Title: CFD Extraction of Heat Flux Distribution on Vapor Phase from the Tank Wall 

For NASA’s future space missions, a key technology is the long-term storage of cryogenics in 
outer space. Due to heat leaks into the cryogenic propellant tanks, the liquid hydrogen vaporizes 
and pressurizes the tank [1]. Due to large density variation of the vapor phase, thermal stratification 
occurs. Thermal stratification in cryogenic propellant tanks present unique challenges to the 
modeling and simulation of heat transfer from wall to vapor phase. Currently, cryogenic propellant 
self-pressurization is a key phenomenon to simulate for long term cryogenic propellant storage
[2,3]. However, current experiments cannot directly measure and quantify the boundary conditions 
of the fluids. Instead, we have temperature of the fluid at different elevations for the thermal 
stratification. It is of interest to determine the heat flux distribution from the wall to the vapor 
phase for simulation benchmarking purposes. Reduced order models (ROMs) were developed to 
provide closures for nodal models such as heat transfer from ullage to interface and liquid to 
interface through steady state simulations [4,5]. Similarly, we can apply the same technique to 
generate data for a machine learning model to determine heat flux distribution for an insulated 
cryogenic propellant tank.

Currently, a suitable dataset containing fluid temperatures at different elevations was obtained 
from NASA for a MHTB tank experiment. The wall heat flux at the outer wall is uniform but at 
the inner wall it is difficult to quantify due to the thermal stratification of vapor phase and the high 
conductivity of the metal wall relative to the vapor phase. There is currently a lack of correlations 
to quantify the heat flux distribution on the vapor dome. It is of interest to obtain reduced order 
models through FEM simulation approach to generate good amounts of data. One way is to test 
different heat flux distributions and the target would be the temperature profile with respect to 
elevation. Through generating different models with distributions, the heat flux at various 
elevations can be quantified and studied to obtain a distribution for a reduced order model (ROM).
Currently, we propose to use an artificial neural network (ANN) or deep neural network (DNN) to 
learn from dataset. The model will be trained on the generated data acquired through FEM 
simulations. At last, the model will be evaluated by implementation in a nodal code to compare 
results with experimental data. The primary impact of this project is to provide higher fidelity 
boundary conditions as compared to an approximate boundary condition which hinders the model 
development effort for cryogenic propellant thermal and fluid analysis.
