# LC-Linkous/JTAGenum
---
WARNING: This is not the original JTAGenum! This is a FORKED branch for personal notes and documentation.

Find the original repository at https://github.com/cyphunk/JTAGenum 

Find the original Wiki at https://github.com/cyphunk/JTAGenum/wiki 



## Table of Contents
* [About JTAGenum](#about-jtagenum)
   * [Changes in This Fork](change-in-this-fork)
   * [JTAGenum Links](jtagenum-links)
      * [Original Project](original-project)
      * [This Project Repository](this-project-repository)
      * [Select Media Publications](select-media-publications)
   * [Authors and Code Branches](authors-and-code-branches)
   * [Similar Tools and Branches](similar-tools-and-branches)
      * [Commercial Tools](commercial-tools)
      * [JTAGenum Project Expansion and Branches](jtagenum-project-expansion-and-branches)
      * [Related Projects](related-projects)
* [What is JTAG?](what-is-jtag)
* [Hardware](hardware)
   * [Tested Hardware](tested-hardware)
   * [Choosing Hardware](choosing-hardware)
* [JTAGenum Usage](jtagenum-usage)
   * [Arduino](arduino)
   * [Raspberry Pi](raspberry-pi)
* [References](references)



## About JTAGenum
---

JTAGenum is an open source Arduino ``JTAGenum.ino`` or Raspberry Pi``JTAGenum.sh`` (experimental) scanner. This code was built with three primary goals:
   1. Given a large set of pins on a device determine which are JTAG lines
   2. Enumerate the Instruction Register to find undocumented functionality
   3. be easy to build and apply

JTAGenum is a more Arduino'y fork of [Arduinull](https://github.com/zoobab/arduinull) by Sébastien Bourdeauducq (lekernel), which is inspired by Benedikt Heinz's [JTAG scanner](https://elinux.org/JTAG_Finder). 

JTAGenum also includes instruction scanning functionality best described by [Felix Domke (tmbinc)](https://github.com/tmbinc) in his [26c3 paper](http://events.ccc.de/congress/2009/Fahrplan/attachments/1435_JTAG.pdf). The initial version of this branch was built for personal research and while working on various projects at [Recurity Labs](https://recurity-labs.com/).

For questions about the original project, please refer to the [original repository](https://github.com/cyphunk/JTAGenum) and [wiki](https://github.com/cyphunk/JTAGenum/wiki) for the author's preferred contact availability.  




### Changes in This Fork
---

* README update
   * Formatting updates for easier reference additions
   * Links to a modified wiki with some quick-start and troubleshooting
   * Links to other similar projects as they're found
* Wiki Update
   * The linked wiki is based on [cypunk's JTAGenum wiki](https://github.com/cyphunk/JTAGenum/wiki), but focuses more on experimental notes
* Citations and references
   * Additional collected materials, IEEE format default

### JTAGenum Links
---


#### Original Project
| Description | Author | Link |
|----------|----------|----------|
| Original Project      | [cyphunk](http://github.com/cyphunk/)| [JTAGenum](https://github.com/cyphunk/JTAGenum) |
| Original Project Wiki | [cyphunk](http://github.com/cyphunk/)| [JTAGenum Wiki](http://github.com/cyphunk/JTAGenum/wiki) |
| Embedded Analysis Wiki| [Embedded Analysis](https://github.com/cyphunk/JTAGenum/wiki/Embedded-Analysis) |
| JTAGenum Blog Post    | [cyphunk, deadhacker.com](deadhacker.com)| [2010 JTAGenum blog post]http://deadhacker.com/2010/02/03/jtag-enumeration/|  
| JTAGenum Video Tutorial|[cyphunk](http://github.com/cyphunk/)|["Ghetto Tools for Embedded Analysis REcon 2011"](https://www.youtube.com/watch?v=ZmBfahwV3ss)|


#### This Project Repository
| Description | Location | Author  | Link |
|----------|----------|----------|---------|
| Forked Repository  | Git Repo | [LC-Linkous](https://github.com/LC-Linkous) |[LC-Linkous/JTAGenum](https://github.com/LC-Linkous/JTAGenum) |
| Forked Project Wiki| Wiki     |                                             |                                                              |     
|        |      |                                      |                                                              |   

#### Select Media Publications

|  Medium     | Title    |  Author  |  Link    |
|-------------|----------|----------|----------|
| Paper       | Blackbox JTAG Reverse Engineering  | [Felix Domke (tmbinc)](https://github.com/tmbinc)        |   http://events.ccc.de/congress/2009/Fahrplan/attachments/1435_JTAG.pdf       |
| Presentation|          |          |          |
|----------|          |          |          |
|----------|          |          |          |
To reduce broken links to online material, select references have been included in the 'media' directory of this repository. 


### Authors and Code Branches
---


|  Authors |   Link to Code                              |             Notes            |
|----------|---------------------------------------------|------------------------------|
|  cyphunk | http://github.com/cyphunk/JTAGenum/         |  ongoing, root repo          |
|  jal2    | http://github.com/jal2/JTAGenum/            |  no recent updates           |
|  zoobab  | http://hackerspace.be/JTAG_pinout_detector  |  redirected to 404, hsbxl.be |
|  z1Y2x   | https://github.com/z1Y2x/JTAGenum/          |  no recent updates           |



### Similar Tools and Branches
---

NOTE: This is not an endorsement of any tool, or guarantee of how well they work. This section is for completeness of resources, but it is far from exhaustive. 



#### Commercial Tools
|   Name       |        Description             |           Link                      |
|----------------|----------------------------------------------------------------------|--------------------------------------------------|
|  JTAGulator    | (joegrands) purpose built hardware with improvements and added voltage range  |  http://www.grandideastudio.com/jtagulator/      |
|  Tigard        |  open source FT2232H-based, multi-protocol, multi-voltage tool for hardware hacking          | https://www.crowdsupply.com/securinghw/tigard       |
| GreatFET One/Azalea  |  open-source, next-gen goodFET. JTAG ability is contradicted in documentation/tutorials| https://greatfet.readthedocs.io/en/latest/        |
|  GoodFET       |  open-source JTAG adapter, loosely based upon the TI MSP430 FET UIF and EZ430U boards        | https://goodfet.sourceforge.net/       |
| EasyJtag, EasyJtag Plus |  universal service tool for phone boot and chip firmware repair, data recovery, and digital forensics         |   https://easy-jtag.com/ , https://z3x-team.com/products/easy-jtag-plus-activation/|
|   JTAGfinder   |  30 I/O commercial JTAG finder       |  https://www.jtagfinder.com/   |
| MiracleBox | listed on main repository, but might be a dead/discontinued product c. October 2024 | |




#### JTAGenum Project Expansion and Branches
|   Author       |                            Description                               |                     Link                         |
|----------------|----------------------------------------------------------------------|--------------------------------------------------|
|  gremwell      | RaspberryPi GoLang rewrite + improvements, JTAGulator Mix      |  https://github.com/gremwell/go-jtagenum         |
|                |          |          |
|                |          |          |




#### Related Projects
|   Author       |        Description                                     |                     Link                             |
|----------------|--------------------------------------------------------|------------------------------------------------------|
|  szymonh       | arduino based SWD finder                               | https://github.com/szymonh/SWDscan                   |
|  szymonh       | arduino based with logic similar to jtagulator         | https://github.com/szymonh/JTAGscan                  |
|  dxa4481       | 1.8-5v voltage shifting shield                         | https://github.com/dxa4481/inputProtectionShield     |   
|  dipusone      | fork of dxa4481's shield                               | https://github.com/dipusone/inputShieldProtection    |


## What is JTAG?
--- 
## A bit about JTAG
================

Basic understanding of how JTAG works will be helpful when using
JTAGenum. There are 4 lines/pins: TDO=output, TDI=input, TCK=clock,
TMS=state machine control.  Say you want to read the ID of the chip.
First you would send the IDCODE instruction to the instruction
register (IR). The JTAG controller then places the actual id code
value of the chip in a data register which you could then read out.
You would think that it would be enough to have one input line going
to the IR and one output coming from the DR but JTAG also supports
writing to the DR. As apposed to adding another input line specific
to the DR instead JTAG works by moving the input and output lines
between IR and DR. The TMS line is used to switch TDI/TDO to IR
when you want to place an instruction and back to DR when you want
to read or write data. With all operations, be it state change (TMS)
reading (TDI) or writing (TDO), the clock line must be cycled once
(TCK) for every bit or change. This was a brutal and drastic
simplification but with that understood reading the Usage section
should be comprehensible.

For a more detailed discussion of JTAG see 
https://github.com/cyphunk/JTAGenum/wiki



## Hardware
---

### Tested Hardware

NOTE: add WIKI links and some pics for the full breakdown

JTAGenum has been tested on the following hardware:

* RaspberryPi (3.3V) with mixed results
* standard Arduino (5V)
* Arduino on Teensy (3.3V) (http://www.pjrc.com/teensy/index.html)
* Arduino on Texas Instruments Tiva C / Stellaris (3.3V) (https://github.com/cyphunk/JTAGenum/issues/4)
* Arduino on STM32 Bluepill board (3.3V) (https://wiki.stm32duino.com/index.php?title=Blue_Pill and http://www.zoobab.com/bluepill-arduinoide)

When picking your micro-controller platform consider two issues: 

1. How many pins do you want to check on your target. 
2. what voltage level does your target device require.  

Concerning voltage RaspberryPi's I/O operate at 3.3v, many Arduinos 
work at 5 volts. Some are switchable but even those that are not could 
be modified. Alternatively voltage shifting Arduino shields or 
voltage shifting gadgets can be used. See the Voltage Shifting Appendix 
discussion on the Embedded Analysis wiki for more details.
https://github.com/cyphunk/JTAGenum/wiki/Embedded-Analysis#Voltage_Shifting

When connecting the micro-controller to the pins of your target one
thing to be aware of is possible cross-talk between wires. The 
loopback check function in JTAGenum cab help you determine which wires
may produce cross talk. 

### Choosing Hardware




## JTAGenum Usage
---

### Arduino



### Raspberry Pi





For use on **Raspberry Pi** use and consult the ``JTAGenum.sh``. The 
Raspberry Pi pins being used for scanning should be specified inside the script
file. This script is experimental and only provides the functions for finding JTAG. 
To use the script should be *sourc'ed* on the console the user should execute
the desired scan. See the comments in the header of the script for further details.

For use on a **Arduino** the ``JTAGenum.ino`` sketch is loaded. The Arduino pins 
being used for scanning should first be specified at the top of the sketch. This
is all that is required for basic JTAG scanning functionality. Once the 
correct JTAG pins on the target have been determined they can be specified in 
the script and along with the defining the proper IR_LENGTH the user can then
execute the search for hidden instructions or print the boundary scan register.

Before loading the sketch first define the pins[] and pinnames[] arrays. After
loadin the sketch open a serial console at baud of 115200 to access the 
user interface.  Sending a h to the console will print usage information that 
describes each function. Each function is enacted by sending the defined one 
character code:

**v > verbose**

Toggles verbose output. At times verbose might present too much
information or without it too little.

**l > loopback check**

Find loopback pairs that will generate false-positives for other
tests. After running you should remove any loopback pairs from your
pins[]/pinnames[]. Looback pairs are found by sending a predetermined
pattern[] to all possible pins while checking all pins for matching
output.  Because the JTAG clock (TCK) and state (TMS) pins are NOT
being stimulated the input/output pairs where the pattern is found
represent loopbacks. NOTE: you should probably run this once with
and without internal pull-up resistors set (r) to avoid problems
of cross-talk which is discussed in detail later.

**s > scan**

This routine is used to check all possible pins and find JTAG  clock,
state, input and output pins lines (TCK,TMS,TDI,TDO). This is done
by setting the JTAG state (TMS) into Shift_IR mode and then sending
pattern[] to TDI and checking for it on TDO while clocking TCK.
This check is run for every possible pin combination and it is
important that you remove loopback pins before running. While this
scan is meant to determine all of the JTAG pins required it is
possible that the  TMS pin found is incorrect.  This depends on if
the target uses the bypass register by default (described later).
If an IDCODE register is present then bypass mode is not the default
and you can assume that the pin this scan defines as TMS is correct.
Otherwise, only the TCK, TDI and TDO pins can be determined.  NOTE:
run with pull-ups on (r) as any cross-talk might result in
false-positives.

**y > brute force IR search**

This will set the instruction register (IR) to all possible values
and check the output. This can be used to find undocumented
instructions and examine their results via the data register (DR).
To run this scan you should have already determined the 4 JTAG pins
and define pins[] as such: [0]=TCK [1]=TMS [2]=TDO [3]=TDI.  NOTE:
run with pull-ups on (r) as any cross-talk might result in
false-positives.

**x > boundary scan**

This will return the state of all the pins on the target.  Actually
it is not just the pins but the contents of the scan/sample register.
This should be a rather large register and is defined in the code
by SCAN_LEN+100. You can check your targets documentation and specify
this or just leave it as a large number (currently 1800). To run
this scan you should have already determined the 4 JTAG pins and
define pins[] as such: [0]=TCK [1]=TMS [2]=TDO [3]=TDI.  NOTE: run
with pull-ups on (r) as any cross-talk might result in false-positives.

**i > idcode scan**

The JTAG standards specify that if an idcode register is present
it should be set as the default data register (DR) and attached to
output (TDO) by default. Meaning, regardless of the state of the
JTAG chip (set with TMS line) and regardless of input being sent
to the chip (TDI) by clocking the chip (TCK) it should return the
contents of the idcode to the output (TDO). Hence, this routine
iterates through all possible TCK,TDO pairs of pins and prints the
output when it changes (we assume an idcode will not be all 0s or
1s). You should examine the documentation of your target(s) to see
if the idcode matches. NOTE: run with pull-ups on (r) as any
cross-talk might result in false-positives.

**b > shift_bypass**

Broken atm (need to add TCK enumeration). The JTAG standards specify
that if and idcode register is NOT present on the chip then the
bypass register (length of 1) should be the default DR. Essentially
this means what is sent to the input (TDI) should come out on the
output (TDI) with a one clock delay (TCK). It is important that you
remove loopbacks before running this test otherwise the loopback
pins will look like valid JTAG lines. NOTE: run with pull-ups on
(r) as any cross-talk might result in false-positives.

**r > set pull-up resistors & cross-talk**

If like me the cables you use to connect between JTAGenum to your
targets are flimsy or uninsulated you might run into issues of
cross-talk whereby when one pin is transmitting a nearby pin picks
up the transmission even though they are not connected. To avoid
this you can turn on the internal pull-up resistors which will force
the pin to a default state. If for some reason you continue to have
sporadic issues run the following in sequence to check if the problem
is the cable, target or other:

1. Disconnect the cables between your target and JTAGenum. Disconnected them
   entirely from JTAGenum as well.

2. Run a loopback check (l) with pull-ups off. In this state the pins are in
   open mode and might fluctuate.  Youll notice that as you move the
   microcontroller around, turn lights on and off or move other devices close
   to or away from it that the results change.

3. Turn on pull-ups (r) and run the test again. The results should now be
   consistent. If they arent, then let me know.

4. Now attach your cables to JTAGenum but not the target. Run steps 2 and 3
   again. Step 2 will give you a feel for how much inconsistency the cable may
   add. If the loopback check results in actual pattern matches then your cable
   has cross-talk. Step 3 should still result in a consistent state of either
   all high (1s) or all low (0s) and if it doesnt then your cross-talk issues
   are such that all JTAGenum tests are going to be buggy at best. Feel free to
   give me an email and I will happily try to help solve the problem.



## References

Original JTAGenum Project:
* Find the original repository at https://github.com/cyphunk/JTAGenum 
* Find the original Wiki at https://github.com/cyphunk/JTAGenum/wiki 
* JTAGenum is a more Arduino-based fork of [Arduinull](https://github.com/zoobab/arduinull) by Sébastien Bourdeauducq (lekernel)
   * Arduinull was inspired by Benedikt Heinz's [JTAG scanner](https://elinux.org/JTAG_Finder), at https://elinux.org/JTAG_Finder
   * Arduinull is hosted on github by zoobab, which may or may not be an account/person linked to lekernel
   * Some original code/notes for Arduinull:
      * https://web.archive.org/web/20110127112909/http://lekernel.net/blog/?p=319
      * https://web.archive.org/web/20110127112909/http://lekernel.net/blog/wp-content/uploads/2009/06/arduinulltar.bz2
* JTAGenum also includes instruction scanning functionality best described by [Felix Domke (tmbinc)](https://github.com/tmbinc) in his [26c3 paper](http://events.ccc.de/congress/2009/Fahrplan/attachments/1435_JTAG.pdf). The initial version of this branch was built for personal research and while working on various projects at [Recurity Labs](https://recurity-labs.com/).


LC-Linkous Forked Repository:
* 
