Arduino_Xively_WiFi_App
=======================

Arduino App that interfaces with Xively

This tutorial helps the user get the Arduino Xively App up and running.
This tutorial is base off the the tutorial from the Xively site, https://xively.com/dev/tutorials/arduino_wi-fi/.

Set Up Xively Account
=====================
See Xively tutorial section, <b>Setup New Xively:</b>

Git the Code
============
Git the Code from GitHub
<ol>
<li><b>Arduino Xively Library -</b> https://github.com/mvartani76/Arduino_Xively
<li><b>Arduino Xively Http Client Library -</b> https://github.com/mvartani76/Arduino_Xively_HttpClient
<li><b>Arduino Xively WiFi App -</b> https://github.com/mvartani76/Arduino_Xively_WiFi_App
</ol>

Install Xively Arduino Libraries
================================
In order to get this app to correctly work with Xively, you will need to install the following two libraries.
<ol>
<li>Arduino_Xively
<li>Arduino_Xively_HttpClient
</ol>
These libraries should be placed under the Arduino folder @ <b>\YourPath\Arduino\libraries\ </b>. For example, on my PC, the libraries would be placed under @ <b>C:\Program Files (x86)\Arduino\libraries\ </b>.

Run the Code
============
Before running the code, make sure you update the following information:

char ssid[] = "YOUR_SSID";    //  your network SSID (name) 
char pass[] = "YOUR PASSWD";  // your network password (use for WPA, or use as key for WEP)
int keyIndex = 0;             // your network key Index number (needed only for WEP)
 
// Your Xively key to let you upload data
char xivelyKey[] = "YOUR XIVELY KEY";

//your xively feed ID
#define xivelyFeed YOUR_XIVELY_FEED_ID


Plus you need to ensure that the channel names are consistent between the Arduino code and Xively.
//datastreams
char sensorID[] = "LIGHT_SENSOR_CHANNEL";
char ledID[] = "LED_CHANNEL";

The code is currently configured for WPA WiFi access.
