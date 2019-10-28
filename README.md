# vSAN Excel Calc

vSAN Excel Calculator is a macro-enabled Excel spreadsheet created to perform VMware vSAN (Virtual SAN) cluster sizing.

An official sizer is available at https://vsansizer.vmware.com, but vSAN Excel Calc takes a different approach aimed at optimizing hardware configuration.

Main difference comes from the initial assumption made to perform calculation.
- Official sizer uses predefined node CPU and Memory settings to calculate storage configuration and amount of nodes. This approach can result in extra nodes being added to satisfy CPU/RAM requirements.
- vSAN Excel Calc performs calculations to recommend minimum Memory configuration and optimal CPU selection to match resource requirements.

In the present tool, sizing is only based on capacity. Storage IOPS performance is not considered in calculation due to the unability to predict which hardware devices will be used (models, technologies and generation).

## Disclaimer
This spreadsheet is given as is and doesn't pretend to provide a better output than the official sizer.
Intention is only to help in determining a good hardware configuration to get a valid cluster sizing.

Before making a purchase or sending a quote, you are encouraged to check calculation using the official vSAN sizer.

The author of the spreadsheet makes no warranties regarding any information provided and disclaims liability for potential prejudice resulting from its usage.

## How to use it
Please refer to the [help guide](https://github.com/jrmclx/vsancalc/blob/master/vSAN%20Calc%20Guide.pdf) to understand how to use the tool.
A proper markdown user guide will be created later.

## Mac Users
The spreadsheet has not been tested on Office for Mac.

This tool uses VBA code, developed and tested on Windows platform. While efforts were made in maximising portability on Mac platform, some features may be dependent on Windows libraries (like update checking process) and objects specific to VBA for Windows.

Cluster calculation does not depend on VBA code and should not be impacted. However, some settings may not be accessible in the GUI when running on a Mac. Event-based automatic value adjustments may also fail and will require manual fixing.
