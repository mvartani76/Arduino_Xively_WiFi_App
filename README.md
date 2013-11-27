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

char ssid[] = "YOUR_SSID";    //  your network SSID (name) <br>
char pass[] = "YOUR PASSWD";  // your network password (use for WPA, or use as key for WEP)<br>
int keyIndex = 0;             // your network key Index number (needed only for WEP)<br>
 <br>
// Your Xively key to let you upload data<br>
char xivelyKey[] = "YOUR XIVELY KEY";<br>

//your xively feed ID<br>
"#define xivelyFeed YOUR_XIVELY_FEED_ID<br>
<br>
Plus you need to ensure that the channel names are consistent between the Arduino code and Xively.<br>
//datastreams<br>
char sensorID[] = "LIGHT_SENSOR_CHANNEL";<br>
char ledID[] = "LED_CHANNEL";<br>

The code is currently configured for WPA WiFi access.<br>
This is configured in line 78 of the code.<br>
<b>For WEP -</b> status = WiFi.begin(ssid, keyIndex, pass);<br>
<b>For WPA -</b> status = WiFi.begin(ssid,pass);<br>


