
# N3BKV Station Control

Welcome to the N3BKV Station Control Node-RED project.  

These flows are used to monitor and control a remote Amateur Radio station. The station has an 20-15-10 beam, 40 meter 4 Square and 80/40 diplole antennas.

Feel free to play with them and provide any feedback you might have. 

# Screenshots

![HF](https://i.postimg.cc/7hjD2HDx/Screenshot-2025-05-06-at-7-52-12-AM.png)

![Environmental](https://i.postimg.cc/h4kz7xsR/Screenshot-2025-05-06-at-9-52-34-AM.png)

![DX Cluster](https://i.postimg.cc/9fMmvwzg/Screenshot-2025-05-06-at-2-11-15-PM.png)

![Grafana](https://i.postimg.cc/Y9LpSc61/Screenshot-2025-05-06-at-2-11-35-PM.png)

![Ham Shack Hotline](https://i.postimg.cc/W1pTkqmp/Screenshot-2025-05-06-at-2-12-01-PM.png)

![Master Status](https://i.postimg.cc/PxDjjWHy/Screenshot-2025-05-06-at-2-14-20-PM.png)

![Master Status Graphs](https://i.postimg.cc/9QfHM5Vr/Screenshot-2025-05-06-at-2-16-09-PM.png)

![Sat Control](https://i.postimg.cc/fTB112XZ/Screenshot-2025-05-06-at-2-18-45-PM.png)

![Sat WX Pictures](https://i.postimg.cc/JhBgDRF4/Screenshot-2025-05-06-at-2-19-18-PM.png)

![WX Station](https://i.postimg.cc/GtzSwt4z/Screenshot-2025-05-06-at-2-19-29-PM.png)
# Equipment Supported

Node-RED (4.08) is running on 2x Win10 computers, one primary (folder - Computer 1) and the second just for HF amp control by the amplifer (folder - Computer 2). Just install Node-RED on each and then import the flows to the respective computer from each folder.

The station consists of the following equipment and control devices:

Arduino - controlling the 4 Square

ControlByWeb WebRelay Devices (X-WR-1R12-1I24-I, X-WR-4R3-I Quad LS, DAQ x-320, X-WR-4R3-I Quad LS, X-WR-4R3-E, X408, X410) using Modbus for communication

CSN Technologies S.A.T.

Digital Loggers Web Power Switch Pro

Elecraft KPA500 Amp

Flex 6700

Hygain Rotor (HF)

HeimVision HM241 Security System

Icom 9700

Tempest WX Station

Yaesu G-5500 Rotor (Satellite)
 
# Node-RED Configuration

You'll need to make the following changes to your settings.js file in your ~\.node-red directory

 /** Context Storage
     * The following property can be used to enable context storage. The configuration
     * provided here will enable file-based context that flushes to disk every 30 seconds.
     * Refer to the documentation for further options: https://nodered.org/docs/api/context/
     */
    //contextStorage: {
    //    default: {
    //        module:"localfilesystem"
    //    },
    //},
    
## Node-RED UI Configuration

Make sure your Node-RED UI settings are as follows:

Site

1x1 Widget Size - 48 x 48
Widget Spacing - 6 x 6
Group Padding - 0 x 0
Group Spacing - 6 x 6

Theme

Light

# Node-RED Dependencies

The following Node-RED modules need to be installed for the flows to function correctly.

node-red-contrib-buffer-parser - 3.2.2

node-red-contrib-discord-advanced - 3.6

node-red-contrib-flexradio - 1.2.3

node-red-contrib-fs - 1.4.1

node-red-contrib-http-request - 0.1.14

node-red-contrib-image-tools - 2.1.1

node-red-contrib-influxdb - 0.7.0

node-red-contrib-latch - 1.0.0-a

node-red-contrib-modbus - 5.41.0

node-red-contrib-msg-resend - 1.0.0

node-red-contrib-simple-gate - 0.5.2

node-red-contrib-startup-trigger - 0.1.0

node-red-contrib-streamdeck-ws - 1.1.0

node-red-contrib-string - 1.0.0

node-red-contrib-telnet-client - 1.0.4

node-red-contrib-ui-button_state - 0.2.2

node-red-contrib-ui-level - 0.1.46

node-red-contrib-ui-svg - 2.3.3

node-red-contrib-web-worldmap - 5.0.8

node-red-dashboard - 3.6.5

node-red-node-email - 3.0.2

node-red-node-openweathermap - 1.0.1

node-red-node-ping - 0.3.3

node-red-node-serialport - 2.0.2

node-red-node-smooth - 0.1.2

node-red-node-ui-iframe - 0.2.1

node-red-node-ui-table - 0.4.4

# Other Dependencies

You will need to install an Influx DB server if you want to use Grafana and an Mqtt server to communicate between the main and rotor computers.


# Node-RED Fixes

After loading the flows, you might get an errors that says "The workspace contains some nodes that are not properly configured" This is normal can can be fixed by opening each one of the listed nodes and then clicking "Done".  There will also be red triangles on each one in the Node-RED editor.


# Special Thanks/Flows and Programs Incorporated

AA0Z 

DJ2VA

Ham Shack Dashboard - N2NXX

K5MAP

K6HN

KA5LUG

KB8CR

LA9VKA

SM6AFV

WA9WUD

WO2X

W8BE

