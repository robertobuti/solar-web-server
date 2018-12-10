Solar inverter web server, (Danfoss),  PvOutput client

This project is finalized to realize a simple web server where check the energy production from solar plant system, based on Danfoss inverter.
Web page can be cusotmized as you like, but space & resource are limited, i suggest html white page with text only.
A client for PVoutput storic data collector is provided, like protocol for inverter.
Software is designed for 3 inverters connected by RS485 , wifi connection is provided and based on PIC processor.

Use Microchip Mplab IDE to compile the project and ICD for debug, some personalizations are necessary like :
WiFi access info, patch wifi.h
Dyndns account must be provided (main.c)
Pvoutput account , generic TCPclient.c (actually manage two clients)
Danfoss.c , here youy need to patch inverter ID on RS485, unfortunatly these information is not signed on inverter, you need to discover by yourself with debug. In Danfoss.c is provided a routine to discover the id from a message from your inverter, connect just one inverter at time and run this routine, then with debug discover the iD and use it in source code .

Remmber the source manage 3 inverters, you need to adapt the code for different inverter number.

Most document on Stack for wifi & tcp are provided from Microchip web site
used wifi module:
https://www.microchip.com/wwwproducts/en/MRF24WN0MA and use with it any dev kit you like, just RS485 interface  driver need to be added, or simply use fly port by open picus and add the RS485 interface.
http://wiki.openpicus.com/index.php/Flyport_WiFi

PvOutput service.
https://www.pvoutput.org/list.jsp?userid=1930


> Written with [StackEdit](https://stackedit.io/).