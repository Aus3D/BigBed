**Please note that BigBed is still in development and is not ready for use - we're in the testing phase right now, and should be ready to go shortly. Thanks for your patience!**

# Aus3D BigBed

BigBed is an open-source PCB heated-bed for RepRap 3D printers. It is based on [earlier PCB heated bed designs](http://reprap.org/wiki/PCB_Heatbed), but incorporates several key improvements. It features many of the same design choices from the popular MK2, MK2b and MK3 open-source heated beds, and should feel quite familiar to anyone who has used one of those designs before.

# Key Features
## Edge Temperature Correction 
Both E3D and Prusa Printers have announced new heated beds that make use of variable trace width to 'regulate' the amount of heat generated by different regions of the heated bed. This allows the outer edges of the PCB to maintain a much closer temperature to the centre, whereas with previous designs there was often a non-trivial temperature difference.

Unfortunately, at the time of writing, neither option is open source, and both can only be obtained as part of their respective 3D printer kits. While it is likely that both companies will release open-source designs at some point in the future (due to their strong history of contributing to the RepRap community), this means there is no readily available option at present for those building their own printers, or looking to upgrade machines they already have.

## SMD Thermistor
Most PCB heated beds require a separate wired thermistor to be attached to the bed in order to monitor the temperature. The BigBed features pads for an 0603 SMD thermistor, and pins near the power connectors through which it can be wired. This should make wiring easier and removes the need to secure an external thermistor to the bed (which is usually done using Kapton tape).

## Pluggable Connectors
The previous designs (MK2 et. al) require the user to directly solder the power wires to the heated bed. While this works fine for power transmission, the inability to disconnect the wires easily can be annoying in some situations (maintenance, cable-management, etc.).

To address this, the BigBed takes a cue from E3D's Varipower bed and adds pins for suitable Molex connectors that can be used to carry both power and the thermistor signal back to the printers' control board. Molex Micro-Fit connectors were chosen due to their small-footprint, good mechanical strength (to resist cable strain on moving beds) and relatively high current-carrying capacity.

The BigBed has room for two of these connectors, where one connects the board in a 12V configuration and the other in a 24V configuration. We have cables available that match with these connectors and provide suitable plugs for most control boards on the other end.

We don't want to exclude anyone though, so the large pads used for directly soldering wires on earlier PCB heated beds are still present - feel free to directly attach wires if that's the best solution for your printer.

![Connectors](https://raw.githubusercontent.com/Aus3D/BigBed/master/Images/Connectors.png "Connectors")
## Big!
BigBed isn't the biggest bed out there - and yes, we know, "But it's called BigBed!". 

BigBed has a print area of 240x240mm, which is intended to be a healthy improvement over it's predecessor's 200x200mm print areas. Larger sizes become difficult to heat without stressing 12V power supplies, or overheating the control board's MOSFET. Additionally, larger sizes start to become unwieldly for printers that use a moving print-bed (including i3-based printers, etc.), due to the increased mass of the bed - resulting in either decreased print speed or lower-quality prints. 

BigBed's size was selected to provide an optimum between print volume, electronics compatibility, and print quality.

#Dimensions and Mounting
![Dimensions](https://raw.githubusercontent.com/Aus3D/BigBed/master/Images/Composite%20Drawing%20Small.png "Dimensions")

#Where to Buy
Once we've got the design thoroughly tested and are happy that everything is working smoothly, we'll have these boards up for sale on the [Aus3D](http://aus3d.com.au/) website.

# Open Source
In the spirit of the RepRap project, BigBed is fully open source - files to manufacture or modify a board of your own are included in this repository. BigBed is licensed under a GPLv3 license, and anyone is free to modify it, manufacture it, sell it - as long as you share your modifications under the same license, we're good!





