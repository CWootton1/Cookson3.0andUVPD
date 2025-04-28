These pulse programs files can be copy-pasted into the pulse program folder in the FTMS control directory:

These "single file" pulse program versions are designed to stay in the list and loaded when needed from the FTMS/MRMS control software GUI. This is done by going to XXX -> XXX -> select pulse program. while in stop mode. 
The pulse program is then compiled and used on next tune/acquisition.
they do not need to be copy/pasted into a directory every time they are needed like older/different "2 file" pulse programs. 

The pulse program set is needed as when running PCD or ADD mode a different pulse program instance is loaded. 
Please ensure to have all 3 files included in the pulse program list otherwise the software will crash when moving to certain acquisition modes.

The pulse program is a simplistic trigger program. it includes an additional event just prior to ion excitation in the ICR cell. 
To be clear this means all other cell processes will happen before this event. including in cell isolations and/or MS/MS events
the trigger is included in the "excitation" block and just fires before the ion excite pulse
it is a single pulse event for a duration defined by "D25" in the parameter control tab.
if 0.1 is set in D25 then a 0.1second/100ms "high" (5V) pulse will occur in the next scan once compiled.
the trigger will be produced at the AUX interface above the ESI source and so is easily interfaced with. 
Pin # 35 on the D-Sub connector will pulse high/low according to the instrument timing sequence

NOTE - THIS IS A NANOBAY+PARACELL PULSE PROGRAM ONLY.
If you need a pulse program for an infinity cell - this is included separately
if you need an updated NEO pulse program - these are not yet included.
do not attempt to use pulse programs designed for different hardware. 

LASER NOTE - please be aware that as soon as the pulse program is loaded and the instrument moves to tune/acquire - THE LASER WILL BEGIN TO FIRE AND CONTINUE TO DO SO. 
please check pulsing/triggering without laser hardware connected beforehand via oscilloscope etc. 
Such programs and setups are only to be used by laser qualified people, etc. 
no responsibility, liability, etc bared by the author or any institution. these programs are here for reference in connection with previous results obtained on hardware and setups that may be different to yours.
Any person(s) using the programs are entirely responsible for their use and downstream effects - especially regarding other equipment such as lasers or peripherals.
these are simply reference text files.