![Logo](admin/robonect.png)
ioBroker.robonect
=============

**Tests:** Linux/Mac: [![Build Status](https://travis-ci.org/braindead1/ioBroker.robonect.svg?branch=master)](https://travis-ci.org/braindead1/ioBroker.robonect)
Windows: [![Build status](https://ci.appveyor.com/api/projects/status/yl79oamamifjvqrq?svg=true)](https://ci.appveyor.com/project/braindead1/iobroker-robonect)

This is an ioBroker adapter for your Robonect HX enabled lawn mower. It have been tested with a Gardena R70Li.

## Settings
* It is required to enter the IP address of the Robonect module. In case username and password are set, they are required, too.
* ioBroker.robonect polls data at different intervals: By default status information is polled every 60 seconds (1 minute) and other information is polled every 900 seconds (15 minutes).
* For every API request it is possible to choose the polling interval (status or info) or don't poll at all.

## Control
### Mode
The mode of the lawn mower can be controlled by changing robonect.0.status.mode. Possible modes are "Auto", "Home", "Manual", "End of day" and "Job" (not fully implemented at the moment).

### Extensions
It is possible to control the extensions GPIO 1, GPIO 2, OUT 1 and OUT 2 of the Robonect module. Requirement is that the mode of the extension is configured as "API" via the Robonect Web-UI. If for example LEDs are connected to OUT1, it is possible to switch them on in the night and off in the morning by setting Robonect.0.extension.out1.status to "true" or "false".

## Changelog
### 0.0.3
* (braindead1) support of Admin3

### 0.0.2
* (braindead1) updated to work with Robonect HX version 1.0 Beta2

### 0.0.1
* (StefSign) initial commit

## License
The MIT License (MIT)

Copyright (c) 2017 StefSign <hufnagl@hotmail.com>

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in
all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
THE SOFTWARE.