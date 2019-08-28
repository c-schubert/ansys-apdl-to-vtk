# ansys-apdl-to-vtk
APDL Script to write elemental or nodal results from ANSYS Mechanical APDL to an unstructured VTK file. Script is a modified version taken from [Pastebin-Link](https://pastebin.com/gyJHKTeJ) (an explanation is given in [this Stackoverflow discussion](https://stackoverflow.com/questions/41722822/how-to-read-ansys-data-files-in-paraview)). 
I have modified the script to besser fit my needs and also to work for elemental result exports. Please make sure to run
```
sed -i -e 's/ \{2,\}/ /g' -e 's/^ //g' -e 's/\r$//g' -e 's/ $//g' ansys_res_out.vtk
```
under Linux (or an equivalent command in Windows) to make the generated vtk file readable for ParaView. This is necessary due to the limited writing capabilities of APDL.
