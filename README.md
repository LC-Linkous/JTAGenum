# LC-Linkous/JTAGenum
---
WARNING: This is not the original JTAGenum! This is a FORKED branch for personal notes and documentation.

Find the original repository at https://github.com/cyphunk/JTAGenum 

Find the original Wiki at https://github.com/cyphunk/JTAGenum/wiki 

Find this repository Wiki: https://github.com/LC-Linkous/JTAGenum/wiki and [This Project Repository](#this-project-repository)

## Table of Contents
* [About JTAGenum](#about-jtagenum)
   * [Changes in this Fork](#hanges-in-this-fork)
   * [JTAGenum Links](#jtagenum-links)
      * [Original Project](#original-project)
      * [This Project Repository](#this-project-repository)
      * [Select Media Publications](#select-media-publications)
   * [Authors and Code Branches](#authors-and-code-branches)
   * [Similar Tools and Branches](#similar-tools-and-branches)
      * [Commercial Tools](#commercial-tools)
      * [JTAGenum Project Expansion and Branches](#jtagenum-project-expansion-and-branches)
      * [Related Projects](#related-projects)
* [JTAG](#jtag)
   * [What is JTAG?](#what-is-jtag)
   * [How JTAG Works](#how-jtag-works)
   * [Identifying JTAG](#identifying-jtag)
* [Hardware](#hardware)
   * [Tested Hardware](#tested-hardware)
   * [Choosing Hardware](#choosing-hardware)
* [JTAGenum Usage](#jtagenum-usage)
   * [Arduino](#arduino)
   * [Raspberry Pi](#raspberry-pi)
* [References](#references)



## About JTAGenum
---

JTAGenum is an open source Arduino ``JTAGenum.ino`` or Raspberry Pi``JTAGenum.sh`` (experimental) scanner. This code was built with three primary goals:
   1. Given a large set of pins on a device determine which are JTAG lines
   2. Enumerate the Instruction Register to find undocumented functionality
   3. be easy to build and apply

JTAGenum is a more Arduino'y fork of [Arduinull](https://github.com/zoobab/arduinull) by Sébastien Bourdeauducq (lekernel), which is inspired by Benedikt Heinz's [JTAG scanner](https://elinux.org/JTAG_Finder). 

JTAGenum also includes instruction scanning functionality best described by [Felix Domke (tmbinc)](https://github.com/tmbinc) in his [26c3 paper](http://events.ccc.de/congress/2009/Fahrplan/attachments/1435_JTAG.pdf). The initial version of this branch was built for personal research and while working on various projects at [Recurity Labs](https://recurity-labs.com/).

For questions about the original project, please refer to the [original repository](https://github.com/cyphunk/JTAGenum) and [wiki](https://github.com/cyphunk/JTAGenum/wiki) for the author's preferred contact availability.  




### Changes in this Fork
---

This repository takes a "starting from scratch" approach to JTAG and JTAGenum. The linked Wiki has updated documentation, more examples, and 
explanations of the 'why' for making hardware choices. That said, there are many external links and tutorials that have been incorporated.


* README update
   * Formatting updates for easier reference additions
   * Links to a modified wiki with some quick-start and troubleshooting
   * Links to other similar projects as they're found
* Wiki Update
   * The linked wiki is based on [cypunk's JTAGenum wiki](https://github.com/cyphunk/JTAGenum/wiki), but focuses more on experimental notes
   * JTAG basics, hardware basics, wiring examples
   * Some "what's next" discussion
* Citations and references
   * Additional collected materials, presentations, and publications
* Additional files
   * the **media** directory has select public presentations, and images used in this README and wiki tutorials



### JTAGenum Links
---


#### Original Project
| Description | Author | Link |
|----------|----------|----------|
| Original Project       | [cyphunk](http://github.com/cyphunk/)    | [JTAGenum](https://github.com/cyphunk/JTAGenum) |
| Original Project Wiki  | [cyphunk](http://github.com/cyphunk/)    | [JTAGenum Wiki](http://github.com/cyphunk/JTAGenum/wiki) |
| Embedded Analysis Wiki | [cyphunk](http://github.com/cyphunk/)    | [Embedded Analysis](https://github.com/cyphunk/JTAGenum/wiki/Embedded-Analysis) |
| JTAGenum Blog Post     | [cyphunk, deadhacker.com](deadhacker.com)| [2010 JTAGenum blog post](http://deadhacker.com/2010/02/03/jtag-enumeration/)|  
| JTAGenum Video Tutorial|[cyphunk](http://github.com/cyphunk/)     | ["Ghetto Tools for Embedded Analysis REcon 2011"](https://www.youtube.com/watch?v=ZmBfahwV3ss)|


#### This Project Repository
| Description | Location | Author  | Link |
|----------|----------|----------|---------|
| Forked Repository  | Git Repo | [LC-Linkous](https://github.com/LC-Linkous) |[LC-Linkous/JTAGenum](https://github.com/LC-Linkous/JTAGenum) |
| Forked Project Wiki| Wiki     | [LC-Linkous](https://github.com/LC-Linkous) |[LC-Linkous/JTAGenum/wiki](https://github.com/LC-Linkous/JTAGenum/wiki)                                                             |     



Detailed Wiki Information:
|       Sub/Page              |                                      Link                                        | 
|-----------------------------|----------------------------------------------------------------------------------|
| Main Wiki Intro             |  https://github.com/LC-Linkous/JTAGenum/wiki                                     |
| JTAGenum                    |                                                                                  |
| What is JTAG?               |  https://github.com/LC-Linkous/JTAGenum/wiki/JTAG#what-is-jtag                   |
| How JTAG Works              |  https://github.com/LC-Linkous/JTAGenum/wiki/JTAG#how-jtag-works                 |
| Identifying JTAG            |  https://github.com/LC-Linkous/JTAGenum/wiki/JTAG#identifying-jtag               |
| Interfacing with JTAG       |  https://github.com/LC-Linkous/JTAGenum/wiki/JTAG#interfacing                    |
| Selecting Hardware          |  https://github.com/LC-Linkous/JTAGenum/wiki/Selecting-Hardware                  |
| Wiring up the Arduino       |                                                                                  |
| Selecting Target Hardware   |                                                                                  |



#### Select Media Publications

|      Medium     | Title    |  Author  |  Link    |
|-----------------|----------|----------|----------|
| Paper           | Blackbox JTAG Reverse Engineering  | [Felix Domke (tmbinc)](https://github.com/tmbinc)        |   http://events.ccc.de/congress/2009/Fahrplan/attachments/1435_JTAG.pdf       |
| Book Chapter    | JTAG Debugging and Exploitation. In: The IoT Hacker's Handbook. | A. Gupta | https://doi.org/10.1007/978-1-4842-4300-8_6   |

To reduce broken links to online material, select references have been included in the 'media' directory of this repository. 


### Authors and Code Branches
---

Original Authors:
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



## JTAG
--- 

For detailed explanations and examples, visit the assorted Wiki articles:


Original JTAGenum Wiki: https://github.com/cyphunk/JTAGenum/wiki 


This repository wiki: https://github.com/LC-Linkous/JTAGenum/wiki/JTAG 



### What is JTAG?

JTAG, which stands for Joint Test Action Group, is a standard (IEEE 1149.1) employed for testing and debugging electronic circuits,
 especially integrated circuits (ICs). It allows access to the internal components of a chip via a serial interface. Typically, 
 JTAG utilizes several specific pins (like TCK, TMS, TDI, and TDO) to control and communicate with the device being tested.

The JTAG interface connects to an on-chip Test Access Port (TAP), which is a type of state machine used to access the set of 
registers related to chip logic and device capabilities. 


JTAG has several usages:

**Device Programming:**
   * JTAG is widely used to program devices like microcontrollers, FPGAs, and CPLDs. During the manufacturing process, 
   firmware or configuration data can be loaded directly onto the chip via the JTAG interface. This is particularly 
   useful for ensuring that devices are ready to operate immediately after production.

**Verification:** 
   * After programming, JTAG helps verify that the correct data has been loaded onto the device. This verification 
   process ensures that the firmware or configuration matches the intended design, helping to catch any errors that 
   might have occurred during programming.

**In-System Testing:**
   * JTAG allows for in-system testing of the programmed device without needing to remove it from the circuit board. 
   This capability is essential for ensuring that the device functions correctly within the context of the entire system.

**Production Efficiency:**
   * By enabling automated testing and programming, JTAG reduces the time and labor required in production. This efficiency 
   can lead to higher throughput and lower manufacturing costs.

**Field Updates:**
   * JTAG can also facilitate firmware updates in the field, allowing manufacturers to fix bugs or enhance functionality 
   after devices have been deployed. This is particularly important in industries where devices must remain operational 
   without significant downtime.

**Boundary Scan Testing:**
   * In addition to programming and verification, JTAG supports boundary scan testing, which helps identify faults in
    connections between chips and other components on a circuit board. This capability is vital for ensuring quality 
    in high-density PCB designs.


### How JTAG Works

Some basic understanding of what JTAG is and how it works is helpful when using JTAGenum. The 
[wiki page on JTAG](https://github.com/LC-Linkous/JTAGenum/wiki/JTAG) covers JTAG and its 
applications in detail. However, what's included in this README is enough to get started.

The following is a useful overview of the process from the original project repo:

>
>  Say you want to read the ID of the chip.
>
>   First, you would send the IDCODE instruction to the instruction
>   register (IR). The JTAG controller then places the actual id code
>   value of the chip in a data register (DR) which you could then read out.
>   You would think that it would be enough to have one input line going
>   to the IR and one output coming from the DR but JTAG also supports
>   writing to the DR. As apposed to adding another input line specific
>   to the DR instead JTAG works by moving the input and output lines
>   between IR and DR. The TMS line is used to switch TDI/TDO to IR
>   when you want to place an instruction and back to DR when you want
>   to read or write data. With all operations, be it state change (TMS)
>   reading (TDI) or writing (TDO), the clock line must be cycled once
>   (TCK) for every bit or change. This was a brutal and drastic
>   simplification but with that understood reading the Usage section
>   should be comprehensible.


For a more detailed explanation, JTAG works through a standardized interface that allows for 
communication with a target device via a set of dedicated signals. There are 5 core JTAG signals 
(and associated pins), though they may be included in connectors with 5 - 20 pins depending on 
the chosen debug connector of teh board designer. For any suspected JTAG, make sure to refer 
to the standard for that pinout configuration. 

The five JTAG interface signals are as follows:

   * **TCK (Test Clock):** Provides the timing for the JTAG operations. It's a clock signal used to synchronize data transfers.
   * **TMS (Test Mode Select):** Controls the state machine of the JTAG interface, determining the next state based on its value.
   * **TDI (Test Data In):** The input for data that is sent to the device.
   * **TDO (Test Data Out):** The output for data that is sent from the device back to the debugger or programmer.
   * **TRST (optional):** An optional reset signal for the JTAG state machine.

Of these five interface signals, TCK, TMS, and TRST are connected to the TAP controller. This TAP controller manages the
finite state machine (FSM) that transitions between different states based on the values of TMS and TCK. The main states include:

   * **Test-Logic Reset:** Initializes the JTAG state machine.
   * **Run-Test/Idle:** The default state where the device operates normally.
   * **Select-DR-Scan:** Selects the data register for scanning operations.
   * **Select-IR-Scan:** Selects the instruction register for scanning operations.

More detail of these states and registers are avilable on the Wiki. For the purposes of entry-level exploration, 
keep in mind that two of the registers that exist are:

   * **Instruction Register (IR):** Contains instructions that define operations (like EXTEST, BYPASS, or SAMPLE).
   * **Data Register (DR):** Holds the actual data being tested or debugged. JTAG can manipulate this data through 
   boundary scan or other methods.


When the instruction register is selected, one of the states in this instruction mode allows users to send in 
instructions through the TDI pin. The following are an example of instructions that can be used to get information from a chip:

   * **IDCODE:** Outputs an identification code stored in a data register
   * **USERCODE:** Outputs an identification code stored in a data register, this is a user-programmable ID
   * **ECIDCODE:** Outputs an identification code stored in a data register, this is the electronic chip identification  

For other instructions, which may cause state changes or resets, refer to the Wiki or official documentation. Running commands 
without considertation to your current state or what the commands do may damage your device under test.


### Identifying JTAG

* TODO: add in a few images




## Hardware
---

### Tested Hardware

NOTE: Oct. 22, 2024. Specific Raspberry Pi and Arduino boards are in the process of being added to keep up to date with the variety that exists now.

JTAGenum has been tested on the following hardware:

* RaspberryPi (3.3V) with mixed results
* standard Arduino (5V)
* Arduino on Teensy (3.3V) (http://www.pjrc.com/teensy/index.html)
* Arduino on Texas Instruments Tiva C / Stellaris (3.3V) (https://github.com/cyphunk/JTAGenum/issues/4)
* Arduino on STM32 Bluepill board (3.3V) (https://wiki.stm32duino.com/index.php?title=Blue_Pill and http://www.zoobab.com/bluepill-arduinoide)


|        Brand        |       Model/Version      | Input Voltage | Output Voltage Options | GPIO Logic Voltage | Datasheet |
|---------------------|--------------------------|---------------| -----------------------|--------------------|-----------|   
|     |        |        |        |        |
|     |        |        |        |        |
|     |        |        |        |        |
|     |        |        |        |        |
|     |        |        |        |        |



### Choosing Hardware

When choosing hardware for JTAGenum, refer to the [Selecting Hardware Wiki page](https://github.com/LC-Linkous/JTAGenum/wiki/Selecting-Hardware) for detailed information.

When picking your micro-controller platform consider two issues: 

1. How many pins do you want to check on your target. 
2. what voltage level does your target device require.  


**Reguarding issue 1:**
Arduino and Raspberry Pi now offer a broad variety of devices with a broad variety of pins.


The following table is an example of avilable devices, but is in no means exhaustive:
|        Brand        |       Model/Version      | Num. Pins | Input V. | Output V. Options | GPIO Logic V. | Datasheet |
|---------------------|--------------------------|-----------|----------| ------------------|---------------|-----------|   
| .    |        |        |        |        |        |        |
|   .  |        |        |        |        |        |        | 
|  .   |        |        |        |        |        |        |
|  .   |        |        |        |        |        |        |
|  .   |        |        |        |        |        |        |



**Reguarding issue 2:**
* Many device chips operate at 3.3V, so the voltage for any such interfaces should be at 3.3V
   * Some chips may operate at votlages as low as 1.7V, or as high as 5V, so refer to the datasheet for that chip if you are unsure
* GPIO operating voltages tend to be 3.3 V for Arduino and Raspberry Pi devices
   * Pins operating at 3.3V are not always 5V tolerant, and sending a 5V signal to those pins may damage the board


NOTE: INCORPORATING THE FOLLOWING WITH THE UPDATE

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




## JTAGenum Usage
---
SECTION IN PROGRESS 

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


This Repository:
* The supporting project Wiki: https://github.com/LC-Linkous/JTAGenum/wiki/

* Media Citations (ongoing collection):
   * Gupta, A. (2019). JTAG Debugging and Exploitation. In: The IoT Hacker's Handbook. Apress, Berkeley, CA. https://doi.org/10.1007/978-1-4842-4300-8_6
      * https://github.com/practical-iot-hacking 

* JTAG references:
   * https://en.wikipedia.org/wiki/JTAG 
   * https://www.allaboutcircuits.com/technical-articles/jtag-test-access-port-tap-state-machine/
   * https://www.allaboutcircuits.com/technical-articles/introduction-to-jtag-test-access-port-tap/
   * https://www.intel.com/content/www/us/en/docs/programmable/683705/20-3/design-example-tap-controller-state-machine.html
   * https://developer.arm.com/documentation/ddi0192/a/debug-interface/scan-chains-and-jtag-interface/the-jtag-state-machine 
   * https://www.xjtag.com/about-jtag/jtag-a-technical-overview/ 
   * https://www.asset-intertech.com/wp-content/uploads/2022/08/IEEE-1149.1-JTAG-and-Boundary-Scan-Tutorial-Second-Edition.pdf
   * https://www.intel.com/content/www/us/en/docs/programmable/683210/current/jtag-instructions.html 
   * https://openocd.org/doc-release/html/JTAG-Commands.html 

 