Copyright (C) 2018-2019, Advanced Realtime Tracking GmbH


License
-------

This library is distributed under the BSD 3-clause License. 
You can modify the sources and/or include them into own software (for details see 
'license.txt').


Purpose of DTrackSDK
--------------------

A set of functions to provide an interface to DTrack tracking systems.
The functions receive and process DTrack measurement data packets (UDP; ASCII),
and send/exchange DTrack2/DTrack3 command strings (UDP/TCP; ASCII).


How to receive and process DTrack tracking data
-----------------------------------------------

DTrack uses Ethernet (UDP/IP datagrams) to send measurement data to other
applications. It uses an ASCII data format.
In its most simple operating mode DTrackSDK is just receiving and processing these data. In
this case DTrackSDK just needs to know the port number where the data are arriving; all necessary
settings have to be done manually in the DTrack frontend software.

DTrack2/DTrack3 also provides a way to control the tracking system through a command interface via
ethernet. DTrack2/DTrack3 uses ASCII command strings which are sent via a TCP/IP connection.

The formats and all other necessary definitions are described in
'DTrack2 User Manual: Technical Appendix' or 'DTrack3 Programmer's Guide'.


Sample source codes for an own interface
----------------------------------------

The sample source code files show how to use the DTrackSDK:

  Listening:           pure listening for measurement data
  ListeningMulticast:  multicast listening for measurement data
  Communicating:       additional controlling the tracking system through remote commands
  TactileFlystick:     controlling a tactile feedback device using a Flystick


Source Documentation
--------------------

Please refer to the Javadoc located at ./doc/index.html
  

Development with DTrackSDK
--------------------------

In order to use this mavenized version of [the original SDK](https://github.com/ar-tracking/DTrackSDK-Java) in your project, add the
jitpack repository to the repositories section of your `pom.xml`:

```xml
<repositories>
  <repository>
    <id>jitpack.io</id>
    <url>https://jitpack.io</url>
  </repository>
</repositories>
```

After, you can add a dependency on the package as:

```xml
<dependency>
  <groupId>graphics.scenery</groupId>
  <artifactId>art-dtrack-sdk</artifactId>
  <version>2.6.0</version>
</dependency>
```

Alternatively, any commit hash (such as 18b4a12) can be used in the
`<version>` tag. For more information how to this package with other package
managers, see [the documentation at jitpack.io](https://jitpack.io#scenerygraphics/art-dtrack-sdk)


Company details
---------------

Advanced Realtime Tracking GmbH
Am Oeferl 6
D-82362 Weilheim
Germany

http://www.ar-tracking.de/

