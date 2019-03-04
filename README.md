# Fexta2016
![gui](Gui.png)
##### The analyses process is done in the following steps. (1) chose the file containing the raw stiffness data  (2) input the number of bp in the dsDNA and the salt concentraion at which the dsDNA data was obtained. Chose ‘Analyze DNA’. The program will then process the calibration, display the calibration parameters and the calibrated dsDNA (blue circles in the right panel). (3) The user may input the data obtained from the same DNA to calibrate the subsequent experimental data conducted on the same DNA molecule. In this example the exonculeolysis data of T7DNAp is analyzed. The force-extension is shown in red on the left panel, and the extension-time (blue) and the force-time (green) are displayed in the right panel in blue.

Raw data acquired from UTC contains information on the positions of the stage (xs), and the laser deflection (xd) due to the bead displacement on the optical trap. Therefore, the raw data requires to be calibrated in order to obtain the absolute end-to-end distance between the tether points of the DNA molecule and to convert the laser deflection into pN. The extension-force profile of a dsDNA molecule is well-behaved in a given monovalent salt concentration352. Here the program utilized the raw data of a dsDNA molecule and the bead displacement as a function of laser deflection; information that essentially is a measure of the trap-stiffness, and the expected force-extension profile of a dsDNA in a given monovalent salt concentration, to find offsets in force and extension, and conversion factor to convert xd in A.U. to pN. The empirical force induced melting midpoint18 at a given [Na+] and the theoretical extensible worm like chain model (WLC) are the constraints used to calibrate data obtained for a dsDNA molecule.
First, the midpoint of the plateau region in the stiffness corrected dsDNA curve is determined using a heuristic algorithm. This value of laser deflection,  , corresponds to a known value of force,  . This is used to determine an offset by which xd is shifted. 
Because the calibration parameters remain the same for a given tethered DNA molecule, we use these values to calibrate the subsequent data acquired using the same DNA molecule. The software detects and separates the force-extension data, and extension-time data, and provide the user with the option to automatically save those as a text file in the same folder where the raw data is located.
