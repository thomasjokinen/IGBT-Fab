## Synopsis

This project was to design an IGBT for fabrication. Fabrication steps were collaborated on and created.  These files are the fab steps of the silicon ('Athena' Folder) and testing of the device ('Atlas' Folder).  Hand Calculations are in the 'IGBT Calculations' Excel file.  The IGBT is a bit rough with all the restrictions in place. These designs were then implements and created inside a cleanroom.  CMOS devices were also built on the substrate.  If I find the files I'll upload my Half-Adder and other CMOS devices created for this substrate.

## Motivation

This project was created to learn about the fab process and gain experience in the clean room.

![Alt text](http://files.1337upload.net/Device_Post_Nplus-9cc9f3.png "Half-Adder after n+ implantation")
This is a picture of the substrate while it was being designed.  This is the Half-Adder created with 5 NOR gates, with PMOS on the left and NMOS on the right. 

## Installation

Requires Silvaco TCAD to run, specifically Athena and Atlas.  Drop a .in file into deckbuild and run

Q: 	What are with all the .in files?

A: 	So since we have a range of initial concentrations there are files for the highest init conc and lowest init conc.

	The files with "highC" have the high concentration as you could guess  
	The files with "lowC"  have the low  concentration
	"LG" for the athena files means Low quality Grid, (LG) for short

	The Atlas files also have the highC and lowC versions.  
	The VcSweeps should be ran first.  The Vc sweeps create the electrodes for the runs while the Gate sweeps DO NOT.

------------------------------------------------------------------------------

	SO HERE'S A DIAGRAM OF WHAT TO RUN IN WHAT ORDER IF YOU DON'T FEEL LIKE READING ABOVE

------------------------------------------------------------------------------

=> FOR HIGH INITIAL CONCENTRATION

	IGBT_Prelim_highC.in OR IGBT_Prelim_highC_LG.in

			 ||
		    \  /
			 \/

	IGBT_ATLAS_Prelim_VcSweep_highC.in

			 ||
		    \  /
			 \/

	IGBT_ATLAS_Prelim_GateSweep_highC.in


------------------------------------------------------------------------------

=> FOR LOW INITIAL CONCENTRATION

	IGBT_Prelim_lowC.in OR IGBT_Prelim_lowC_LG.in

			 ||
		    \  /
			 \/

	IGBT_ATLAS_Prelim_VcSweep_LowC.in

			 ||
		    \  /
			 \/

	IGBT_ATLAS_Prelim_GateSweep_LowC.in


------------------------------------------------------------------------------

Thanks for reading,
Thomas


