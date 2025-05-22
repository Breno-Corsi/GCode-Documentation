# G-Code and M-Code Documentation

This repository contains comprehensive documentation for G-Code and M-Code commands used in CNC programming. G-Code is primarily used for controlling CNC machines, while MCode is used for miscellaneous functions. This documentation aims to provide clear explanations and examples for each command to assist users in understanding and utilizing them effectively.

**Warning:** This documentation is currently valid only for lathe machines. Please ensure to verify compatibility with your specific CNC machine before use. The commands and their behavior may vary depending on your machine's configuration and capabilities.

## G-Code Table

| Gcode | Function      | Explanation                                         | Example                     | Modal |
|-------|---------------|-----------------------------------------------------|-----------------------------|-------|
| G00   | Motion        | Move in a straight line at rapid speed.            | G00 X10 Y10 Z5             | Yes   |
| G01   | Motion        | Move in a straight line at last commanded feedrate. | G01 X10 Y10 F100           | Yes   |
| G02   | Motion        | Clockwise circular arc at feedrate.                 | G02 X10 Y10 I5 J0 F100     | Yes   |
| G03   | Motion        | Counter-clockwise circular arc at feedrate.         | G03 X10 Y10 I-5 J0 F100    | Yes   |
| G04   | Motion        | Dwell: Stop for a specified time.                   | G04 P1000 (1 second)       | No    |
| G09   | Motion        | Exact stop check.                                   | G09                         | No    |
| G10   | Compensation  | Programmable parameter input.                        | G10 L2 P1 X10              | No    |
| G17   | Coordinate    | Select X-Y plane.                                  | G17                         | Yes   |
| G18   | Coordinate    | Select X-Z plane.                                  | G18                         | Yes   |
| G19   | Coordinate    | Select Y-Z plane.                                  | G19                         | Yes   |
| G20   | Coordinate    | Program coordinates are in inches.                 | G20                         | Yes   |
| G21   | Coordinate    | Program coordinates are in mm.                     | G21                         | Yes   |
| G27   | Motion        | Reference point return check.                       | G27                         | No    |
| G28   | Motion        | Return to home position.                            | G28                         | No    |
| G29   | Motion        | Return from the reference position.                 | G29                         | No    |
| G30   | Motion        | Return to the 2nd, 3rd, and 4th reference point.   | G30                         | No    |
| G32   | Canned        | Constant lead threading.                            | G32                         | Yes   |
| G40   | Compensation  | Tool cutter compensation off.                       | G40                         | Yes   |
| G41   | Compensation  | Tool cutter compensation left.                      | G41                         | Yes   |
| G42   | Compensation  | Tool cutter compensation right.                     | G42                         | Yes   |
| G43   | Compensation  | Apply tool length compensation (plus).              | G43 H01                     | Yes   |
| G44   | Compensation  | Apply tool length compensation (minus).             | G44 H01                     | Yes   |
| G49   | Compensation  | Tool length compensation cancel.                    | G49                         | No    |
| G50   | Compensation  | Reset all scale factors to 1.0.                     | G50                         | No    |
| G51   | Compensation  | Turn on scale factors.                              | G51 S2                      | Yes   |
| G52   | Coordinate    | Local workshift for all coordinate systems.         | G52 X10 Y10 Z5              | Yes   |
| G53   | Coordinate    | Machine coordinate system.                          | G53                         | Yes   |
| G54   | Coordinate    | Work coordinate system (1st Workpiece).            | G54                         | Yes   |
| G55   | Coordinate    | Work coordinate system (2nd Workpiece).            | G55                         | Yes   |
| G56   | Coordinate    | Work coordinate system (3rd Workpiece).            | G56                         | Yes   |
| G57   | Coordinate    | Work coordinate system (4th Workpiece).            | G57                         | Yes   |
| G58   | Coordinate    | Work coordinate system (5th Workpiece).            | G58                         | Yes   |
| G59   | Coordinate    | Work coordinate system (6th Workpiece).            | G59                         | Yes   |
| G61   | Other         | Exact stop check mode.                              | G61                         | No    |
| G62   | Other         | Automatic corner override.                          | G62                         | Yes   |
| G63   | Other         | Tapping mode.                                      | G63                         | Yes   |
| G64   | Other         | Best speed path.                                   | G64                         | Yes   |
| G65   | Other         | Custom macro simple call.                          | G65 P1000                   | No    |
| G70   | Canned        | Finish Turning Cycle.                              | G70                         | Yes   |
| G71   | Canned        | Rough Turning Cycle.                               | G71                         | Yes   |
| G72   | Canned        | Rough Facing Cycle.                                | G72                         | Yes   |
| G73   | Canned        | Pattern Repeating Cycle.                           | G73                         | Yes   |
| G74   | Canned        | Peck drilling cycle or tapping cycle.             | G74 X10 Y10 Z-5 R1 F100    | Yes   |
| G75   | Canned        | Grooving Cycle.                                    | G75 X10 Z-5 R1 F100        | Yes   |
| G76   | Canned        | Threading Cycle.                                   | G76 P100 Q10 R1            | Yes   |
| G77   | Canned        | Back boring cycle.                                 | G77 X10 Z-5 R1 F100        | Yes   |
| G78   | Canned        | Boring cycle with dwell.                           | G78 X10 Z-5 R1 P100        | Yes   |
| G79   | Canned        | Canned cycle cancel.                               | G79                         | No    |
| G80   | Canned        | Cancel canned cycle.                               | G80                         | Yes   |
| G81   | Canned        | Simple drilling cycle.                             | G81 Z-5 R1 F100            | Yes   |
| G82   | Canned        | Drilling cycle with dwell.                         | G82 Z-5 R1 P100 F100       | Yes   |
| G83   | Canned        | Peck drilling cycle.                               | G83 Z-10 R1 Q2 F100        | Yes   |
| G84   | Canned        | Tapping cycle.                                     | G84 Z-5 R1 F100            | Yes   |
| G85   | Canned        | Boring cycle with feed in and rapid out.          | G85 Z-5 R1 F100            | Yes   |
| G86   | Canned        | Boring cycle, spindle stop, rapid out.            | G86 Z-5 R1                 | Yes   |
| G87   | Canned        | Back boring cycle.                                 | G87 Z-5 R1                 | Yes   |
| G88   | Canned        | Tapping cycle with manual retraction.              | G88 Z-5 R1 F100            | Yes   |
| G89   | Canned        | Boring cycle with dwell.                           | G89 Z-5 R1 P100            | Yes   |
| G90   | Coordinate    | Absolute programming of XYZ.                       | G90                         | Yes   |
| G91   | Coordinate    | Incremental programming of XYZ.                    | G91                         | Yes   |
| G92   | Coordinate    | Thread cutting cycle or set position.              | G92 X0 Y0                  | No    |
| G93   | Other         | Inverse time feed rate.                            | G93                         | Yes   |
| G94   | Other         | Feed rate per minute.                              | G94                         | Yes   |
| G95   | Other         | Feed rate per revolution.                           | G95                         | Yes   |
| G96   | Motion        | Constant surface speed ON.                         | G96 S200                   | Yes   |
| G97   | Motion        | Cancel constant surface speed.                     | G97                         | No    |
| G98   | Canned        | Return to initial level in canned cycles.          | G98                         | Yes   |
| G99   | Canned        | Return to R level in canned cycles.                | G99                         | Yes   |


## M-Code Table
| Mcode | Function                     | Explanation                                         | Example                     |
|-------|------------------------------|-----------------------------------------------------|-----------------------------|
| M00   | Program Control              | Program Stop (non-optional).                        | M00                         |
| M01   | Program Control              | Optional Stop: Operator Selected to Enable.         | M01                         |
| M02   | Program Control              | End of Program.                                     | M02                         |
| M03   | Spindle Control              | Spindle ON (CW Rotation).                           | M03 S1000                  |
| M04   | Spindle Control              | Spindle ON (CCW Rotation).                          | M04 S1000                  |
| M05   | Spindle Control              | Spindle Stop.                                       | M05                         |
| M06   | Tool Management              | Tool Change.                                        | M06 T01                    |
| M07   | Coolant Control              | Mist Coolant ON.                                    | M07                         |
| M08   | Coolant Control              | Flood Coolant ON.                                   | M08                         |
| M09   | Coolant Control              | Coolant OFF.                                       | M09                         |
| M13   | Spindle and Coolant Control  | Spindle ON (CW Rotation) + Coolant ON.             | M13 S1000                  |
| M14   | Spindle and Coolant Control  | Spindle ON (CCW Rotation) + Coolant ON.            | M14 S1000                  |
| M30   | Program Control              | End of Program, Rewind and Reset Modes.            | M30                         |
| M97   | Subprogram Control           | Haas-Style Subprogram Call.                         | M97 P1000                  |
| M98   | Subprogram Control           | Subprogram Call.                                    | M98 P1000                  |
| M99   | Subprogram Control           | Return from Subprogram.                             | M99                         |

## Contributing

Contributions to this documentation are welcome! If you have additional commands, corrections, or improvements, please feel free to submit a pull request.

## Acknowledgments

Thanks to the CNC community for their contributions and support in developing this documentation. Special thanks to [CNC Cookbook](https://www.cnccookbook.com/) for providing valuable resources and references that helped shape this documentation. Your input helps make CNC programming more accessible to everyone!
