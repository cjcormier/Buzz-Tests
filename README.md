# Overview

This is a simple repository for several tests using [argos3](https://github.com/ilpincy/argos3), [Buzz](https://github.com/MISTLab/Buzz) and the [argos3 khepera plugin](https://github.com/ilpincy/argos3-kheperaiv). Before running these tests, make sure argos3, Buzz and the argos3 khepera plugin are installed in that order (see links above). 

# Tests

Currently there are two tests:

* Crash
* Debug

## Crash
Currently attempting to select a robot in the qt-opengl visualizer in argos3 using shift-click crashes argos on systems using intel integrated graphics. Crash demonstrates the ability to select robots in argos3 using a software select in the Buzz debuger. Hopefully this can help determine the cause of the crash.

### Compile & Run
In the project root

```
bzzc crash.bzz
argos3 -c crash.argos
```

### Tests
All crash tests should be run on intel integrated graphics. 

#### Standard Selection
* Launch the argos3 crash experiment.
* Shift-click a robot in the main argos3 window.
* Argos3 should now crash. 

#### Buzz Selection
* Launch the argos3 crash experiment.
* Click the play button in the main argos3 window.
* In the Buzz Debugger, select the robot.
* The robot should now be selected.

## Debug
Debug is a minimal example showing that despite running with the same setup, khepera robots will not display the debug information above themselves, but footbots will

### Compile & Run
In the project root

```
bzzc debug.bzz
argos3 -c debug.argos
```

### Tests

#### Debug
* Launch the argos3 crash experiment.
* Click the play button in the main argos3 window.
* The footbot robots should have debug information displayed above them, while kheperas will not.
