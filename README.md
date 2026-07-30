# THIS DASHBOARD IS DEPRECATED.

It is still provided in order to support older robots, but if you're looking for the latest
Dashboard, you probably want this repository: https://github.com/MINDS-i/Dashboard

# MINDS-i Dashboard

Dashboard for communicating with and configuring MINDS-i ground and air drones.

Download the latest version as a zip in the [Releases Section][1].

Code and Software is under apache license 2.0

## Connecting your Drone

#### First time only:
 * Follow the setup instructions in the [MINDS-i Drone Library][2] repository for your drone
 * Make sure appropriate drivers are available for your telemetry radios
     *  If you are running windows, a driver installation button is available
        in the configuration menu.
        Other operating systems frequently work without modification.
 * Configure your Telemetry Radios
 
#### Each Flight:
 * Connect the telemetry radio to the computer
 * Turn on your drone
 * Press refresh in the dashboard window connection tray
 * select the appropriate serial device from the drop-down
 * press connect
 * You should start seeing telemetry from your drone arrive shortly. Waypoints
   you have already entered will be sent to the drone, and the settings stored
   onboard will be loaded so they can be changed in the telemetry window.

## Radio Configuration
 * Make sure appropriate drivers are available
 * start the dashboard and open the Configuration window
 * Connect the telemetry radio to the dashboard in the configuration window
 * Refresh, Select and connect to the telemetry radio
    Radios will come with a default of 56700 baud, but after configuration
    they will connect at 9600 baud
 * Make the changes you want, or press "Import defaults" to automatically
configure it for use with MINDS-i drones
 * Press "Save Changes", disconnect, and power cycle the telemetry radio
 * Remember to update the settings on both the sending and receiving
telemetry radios

## Switching Between Ground and Air Mode
To switch the dashboard between ground drone and air drone mode,
Open the configuration window, press "Toggle ground/air mode", and then
restart the dashboard

## Artificial Horizon
When in air mode, the artificial horizon widget can be clicked on to
open a full size window with altitude and heading overlaid on the right
and top edge respectively.

## Waypoint Targeting
When in ground mode, clicking the map will place a GPS waypoint at that
location that a connected rover will attempt to drive to.
To add a waypoint at the end of the path, click on the map.
click on an existing path's line to "break" it and add a new point inbetween.
right click on a point to delete that waypoint

## Log Files
The dashboard makes a `.log` and a `.telem` file in the log
directory each time its run.

`.log` files contain a record of
errors, warnings, and messages received from the robot while its running.

`.telem` files contain the robots telemetry data storing in CSV format
with the first column containing the timestamp that data was stored at,
and the remaining columns being each index of telemetry in order.

The frequency that received telemetry is logged can be changed in the
telemetry window, accessible from the left navigation box in the dashboard.

## Graph Instructions
Any number of Live telemetry graphs can be opened with the "Graph" button
in the navigation box. Once a graph is opened, click configure to select
which telemetry lines to graph and set their color. Drag and zoom within
the graph to change the view, or change the scales and center values in the
configuration window.

## IT setup for MINDS-i system
To configure a new computer for use with the full MINDS-i Drone system,

* Make sure the following domains are accessible
    * arduino.cc (for the library manager updates)
    * arcgisonline.com (dashboard satellite imagery)
    * thunderforest.com (dashboard map imagery)
* Install Arduino
    * Use the Arduino installer to get drivers at the same time
    * Open the library manager (in sketch->libraries->manage libraries) and download both "MINDSi" and
      "MINDS-i-Drone"
* Download the latest release of the MINDS-i Dashboard
    * Windows: Installer the driver found in the dashboard configuration window

[1]: https://github.com/MINDS-i/Dashboard/releases
[2]: https://github.com/MINDS-i/MINDS-i-Drone
