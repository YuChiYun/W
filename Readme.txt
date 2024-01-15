Goals
* Write Protection
    - a feature that prevents data from being written
* This can be issued by
    - the user (to protect important information)
    - firmware automatically (to protect the NAND chip from over-written).
* Write protection is typically implemented through:
    - hardware-based write protection switches or locks
    - software-based write protection settings that can be configured through the SSD's firmware.

Requirement
* To implement your own software-based write protection
* Which can be issued through UART command
    - protectEnable and protectDisable
* When the protect status is on ( protectEnable )
    - the SCSI write command should NOT change the data inside SSD NAND chip
* When the protect status is off ( protectDisable )
    - the SCSI write command can change the data