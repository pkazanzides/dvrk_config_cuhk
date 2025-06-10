dVRK configuration files for CUHK
=================================

Since there are multiple systems at CUHK, the configuration files are
organized in sub-directories.

* cuhk-daVinci: this is the full da Vinci system, with setup joints, currently located in the MRC.

* cuhk-dVRK: this is a dVRK system, currently located at Prince of Wales Hospital (PWH).

The cuhk-daVinci system was updated to dVRK software version 2.3.0, and the configuration files
were updated in June 2025. At that time, it was discovered that the MTM serial numbers
were 73298 (MTML) and 28002 (MTMR) instead of 41878 (MTML) and 31519 (MTMR). The CAL files for
73298 and 28002, originally in the cuhk-dVRK subdirectory, were copied to the cuhk-daVinci
subdirectory. It is possible that 41878 and 31519 are with the dVRK, but this has not been
verified. It is also possible that there is no surgeon console with the dVRK.

The Version 5 XML files for 73298 and 28002 were created by running the config generator with
the original CAL files, and then updating the motor current calibration by copying the values from
the previous XML files. The MTML board ids were changed from the defaults of 0,1 to 4,5 to match the
CUHK hardware setup. Then, the potentiometer scale calibration was performed. The potentiometer offsets
were left at their default values (based on the CAL files). The potentiometer distance tolerance for MTMR
axes 4 and 5 was changed from the default value of 5.0 to 20.0 to match the previous versions of the
files; without this change, the robot would not home.

The Version 5 XML files for the prior MTMs (41878 and 31519) and for PSM1 (28124), PSM2 (33281) and ECM
(29738) were created at CUHK by manually updating the Rev 3 files.
