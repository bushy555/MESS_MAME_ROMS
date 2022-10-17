# MESS_MAME_ROMS
MESS and MAME ROMs - VZ200, VZ300, Microbee, Aquarius.

mbee.zip      - Microbee

Microbee: plonk this zip file, as it is, uncompressed, into the ROMS directory of mess/mame. Mess/mame will read directly from the zip file.




roms.all.zip  - VZ200 / VZ300 / Aquarius

VZ and Aquarius: Extract this zip file into the ROMS directory. Leave the .ZIP files as they are. Mess/mame will read directly from the zip file.


Got sick of loosing URL's for these ROMs, so dumped them here for my future reference.
I physically own all of these machines, so this one liner disclaimer hopefully can avoid any and all copyright issues should someone have a go at me.
I can't help it if others find this repositry.




Ensure that within the .ini file, the rom path is set correctly.
For older versions of MESS, eg  (v1.49 from 2009-2011 era that works extremely well and is easy to use) Find, download and use the extra front end startup utility called MESSUI.EXE


Mess emulation for the VZ Dribble
-----------------------------------
MAME is the biggest and largest combination of emulators on this planet. All rolled up into one 
heck of a single platform. Juergen Buchmueller and Dirk Best were both members of the VZ Yahoogroups
list in the early years, and wrote the VZ emulator within MESS/MAME. 
Disk drive and serial terminal emulation works. 



http://www.mamedev.org				MAME			
			
https://messui.1emulation.com/			Downloads.

https://messui.1emulation.com/howto.html	How to. Website still alive Feb 2022.

https://docs.mamedev.org/usingmame/index.html	Basic MAME Usage and Configuration

http://www.youtube.com/watch?v=0kIcY2f7f_A	fx.vz running on MESS (Youtube)

https://www.planetemu.net/roms/mess-roms	Download ROMS from here.




2. Quick Setup overview
=======================

1. Find and download MESS.

2. Install to C:\MESS

3. Command prompt, Go to drive letter, CD \MESS

4. MESS -CC		(creates MESS.INI)

5. Create c:\mess\ini 

6. move mess.ini to c:\mess\ini

7. create sub directory 	c:\mess\roms

8. create sub directory 	c:\mess\ini

9. edit c:\mess\ini
	    	readconfig 		1
	    	writeconfig 	1
	    	inipath 		ini
	    	menu 		1
	    	filter 		0
	    	hlsl_enable 	0
	    	rompath             c:\mess\roms

9. Find these files

     		vtechv20.u09
		
     	 	vtechv20.u10
		
		vtechv20.u12
		
      		vtechv20.lo
		
      		vtechv20.hi
		
      		vtechv20.rom
		

10. ZIP up  vtechv20.u09 and vtechv20.u10 and rename ZIP file to: LASER210.ZIP

    ZIP up  vtechv20.u12 and rename ZIP file to: LASER310.ZIP
    
    ZIP up  vtechv20.lo and vtechv20.hi and rename ZIP file to: VZ200.ZIP
    
    ZIP up  vtechv20.rom and rename ZIP file to: VZ300.ZIP
    

11. MOVE ZIP files to c:\mess\roms

12. From command prompt within c:\mess , type :  	MESS LASER310
	Screen should come up. Type in 'ok', and the VZ screen should then come up.
    From c:\mess should be able to run MESSGUI.EXE and run any of the listed VZ/Laser systems.

13. MESS File Manager and Settings PRESS :

      Press :  <SCROLL LOCK> then <TAB>

      Down-arrow down to SNAPSHOT. Go looking for a .VZ file.





Try directly loading from the command line:    	MESS.EXE VZ300 -dump <file>.vz	

ie:	MESS.EXE VZ300 -dump hoppy.vz

Or use the builtin file manager:		MESS.EXE VZ300


then press ScrLock to disable full keyboard emulation, press Tab and select
the File Manager, then load hoppy.vz into the Snapshot slot.



4. More info
============

* MENU KEY WHEN IN EMULATOR : SCROLL / NUM LOCK

* Press F5, this will scan your roms so that MESSUI will know which systems can be run.

* Click on View, Customize fields... - you can choose which columns to display in the list of systems

* Click on View, and make sure the first 5 choices are ticked/checked.

* Click on View, Show Pictures and choose which things you would like to see on the righthand side.

* Click on Options, Directories and for each item in the list, choose where it is located. The list is somewhat daunting, so for now do nothing, it can be fine-tuned later.

* Click on Options, Background Image... - navigate to a folder containing PNG files, then choose a nice-looking one.

* Now, the system list might be hard to read, so click on Options, System List Font, and choose another colour. Note this changes ALL text in MESSUI.

* Click on Options, System List Clone Color - if you want clones to be another colour, choose it here. You can't choose a different font.

* Click on Options, Default System Options - this should be the same as you had set up in MESS.INI earlier, but you can change it here. It only applies to systems you have never run.

* Now, exit MESSUI so we can save our settings. If MESSUI crashes, any changed settings are lost. 






5. Words from Dirk Best.
========================
MESS can be confusing to use, it's the price we have to pay to support a few thousand 
systems and run on many different operating systems.

Some tips:

First time you run MESS, start it with "mess.exe -cc", this creates the mess.ini main 
config file. I like to edit it and disable fullscreen for example.

Some keys:

- ScrLock: Disables or enables full keyboard mode. In full keyboard mode, all
   keys are grabbed and sent to the emulated system (so you can't even exit the
   emulator with ESC). In partial keyboard mode, the UI keys respond as normal.
- F12: Screenshot
- F11: Display current emulation speed and framerate
- F10: Toggle throttle, if you don't want to wait for something to load (great for tapes)
- Tab: Open builtin menu, to load files or configure the emulator

Starting a system from the command line with the -listmedia switch will
display the files it accepts. For vz300:


d:\workspace\mame>mess64.exe vz300 -listmedia
 SYSTEM      MEDIA NAME (brief)   IMAGE FILE EXTENSIONS SUPPORTED
 
----------  --------------------  ------------------------------------


vz300        printer     (prin)     .prn

             snapshot    (dump)     .vz
	     
             cassette    (cass)     .wav  .cas
	     
             cartridge   (cart)     .rom
	     
             floppydisk1 (flop1)    .dsk
	     
             floppydisk2 (flop2)    .dsk
	     


So you can use "-dump file.vz" to load it.


-ramsize ram_value'', where //ram_value// can assume one of the following values 

  2k - standard model
  
  18k - with 16K memory expansion
  
  66k (default) - with 64K memory expansion
  
  4098k - with 4MB memory expansion

MESS Debuger 				mess.exe vz300 -debug			(type help)


Loading a file from command line	mess.exe vz300 -dump FX.VZ

Using the builtin file manager		mess.exe vz300

						Press <ScrLock> to disable full keyboard emulation.
						
						Press <TAB>
						
						Select the File Manager and then load FX.VZ into the Snapshot slot.
						

Dumping to AVI video file		mess.exe vz300 -dump FX.VZ -aviwrite fx.avi

						

6. Running MAME on Linux - Command line example

===============================================

mame laser210 -mem laser_64k -video soft -ui_active -bp ~/.mame/roms -resolution0 1280x720 -aspect 1000:750 -skip_gameinfo -nowindow -dump thejungle.vz 






