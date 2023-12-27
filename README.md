# Investigation on Quasi-STAtic Test (IQStaT)

## Description

<p align="justify"> IQStaT is a class of software developed to investigate the results obtained from the quasi-static (or pseudo-static) test of cantilever columns. In the case of most commonly used conventional experimental setup for cantilever column the true lateral load behavior and its capacity (both yield and ultimate) cannot be captured due to the fixing arrangements of the actuator heads and their interactions with the column specimen. Therefore, the experimental data must be rectified using *IQStat1.exe* before using them directly for other purposes (e.g., calibration of any numerical model). The software considers force and displacement readings of vertical and horizontal actuators recorded during monotonic or cyclic quasi-static test in the case of a cantilever column subjected to (constant) axial loading and unidirectional lateral loading as input and it produces the corresponding rectified displacement and force values along with the capacity parameters as output following the mechanics-based approach proposed by <a href="https://doi.org/10.1061/(ASCE)ST.1943-541X.0002522">Naskar et al.</a>. </p>

## Instructions to use IQStat1
---
<p align="justify">
1. Download *IQStaT1.rar* from <a href="https://github.com/SubhadipN/IQStat/blob/main/IQStaT1.rar">here</a>.

2. Unzip *IQStaT1.rar*.

3. Find file *IQStaT1.input* within the unzipped folder, and enter numerical values (from Line 1 to Line 17) associated with different parameters (for sucessful execution of *IQStat1.exe*) as shown in that file. Representation of various geometrical parameters (from Line 1 to Line 7) for different types of quasi-static experimental arrangements is shown in the figure given below for better clarity.
<p align="center">
    <img align="center" src="https://drive.google.com/uc?export=view&id=18AEgjvi-5OX_SYTfAg_KjDnQ6nDbGKxY" alt="drawing" width="750"/>
</p>

4. Provide the filename, which includes the experimental data, at the end (i.e., Line 18) of *IQStaT1.input* file. The filename must not have any blank space.

5. Place the file (whose name is provided at the end of *IQStaT1.input* file) in the same folder where *IQStaT1.exe* resides. This file must be in 3-column format with the following values.
	>* 1st column: force readings (in kN) obtained from vertical actuator
	>* 2nd column: displacement readings (in mm) obtained from horizontal actuator
	>* 3rd column: force readings (in kN) obtained from horizontal actuator
Each row of this file corresponds to the increments of the (displacement- or force-controlled) horizontal actuator during the quasi-static experiment.

6. Run *IQStaT1.exe* (note the output filename).

7. The output file will record the rectified data following the same (3-column) format as described in Step 5. The output file will also record the computed yield values at the very end. The output file will be saved at the same folder where *IQStaT1.exe* resides. 
</p>
---

> [!NOTE]
<p align="justify">
> 1. Two sample files (*monotonic_test.dat* and *cyclic_test.dat*) including experimental data following the 3-column format (as prescribed in Step 5) are provided within *IQStaT1.rar* file as a reference for the users. Any other file with different name and different extension (other than **.dat*) can also be used for successful execution of *IQStaT1.exe* provided it contains the experimental data in the 3-column format as shown in the sample files.
> 2. Two sample output files (*rectified_monotonic_test.dat* and *rectified_cyclic_test.dat* corresponding to the files *monotonic_test.dat* and *cyclic_test.dat*, respectiely) are also provided within *IQStaT1.rar* file as a reference for the users.
</p>

## Cite as
<p align="justify"> **S. Naskar**, S. Das, H.B. Kaushik (2017) "Retrieval of True Lateral Load–Deformation Behavior of Axially Loaded Columns from Experimental Data", *Journal of Structural Engineering*, Vol. 146(3), pp. 04020007. <a href="https://doi.org/10.1061/(ASCE)ST.1943-541X.0002522">https://doi.org/10.1061/(ASCE)ST.1943-541X.0002522</a> </p>
