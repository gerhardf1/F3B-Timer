# F3BTimer
The App "F3BTimer" is running on Android mobilephones and acts as a simple Timer for the [piCAMTracker](https://github.com/barney-NG/piCAMTracker).
Starting with V0.5 the piCAMTracker sends UDP broadcasts when it is powered and in case a "Turn" is detected.
The App receives the UDP broadcasts and handles a F3B Speed run.

# F3FTimerRemoteSwitch
The App [F3FTimerRemoteSwitch](https://github.com/gerhardf1/F3F-Timer/tree/master/F3FTimerRemoteSwitch) is running on Android mobilephones and can be used instead of piCAMTracker to manually produce "Turn" signals on Base A or B.

# News
* 2024-06-01: added some informations in case of range problems
* 2024-01-14: V0.1 released

# Prerequisite:

* piCAMTracker and the mobilephone has to be in the same IP network.
* The simplest solution is to use the mobilephone as a hotspot and connect both piCAMTracker to it.
* Be sure that the following lines are included in config.json:
  * "IPUDPBEEP": "255.255.255.255",
  * "accessPoint": false,

# Usage:

* First of all the App "F3BTimer" has to be started.
* It shows the own IP address.
* After pressing button "Connect" it waits for Base A.
* Now piCAMTracker of Base A should be powered or button "Connect" should be pressed on App "F3BTimerRemoteSwitch"
* After booting the App will show the IP address of Base A.
* Now piCAMTracker of Base B should be powered or button "Connect" shoud be pressed on App "F3BTimerRemoteSwitch".
* After booting the App "F3BTimer" will show the IP address of Base B and is now ready for start (the IP addresses are stored and you have to do this procedure only at the first connection).
* you can select between 2 modes:
  * F3B-Speed: 4 laps are measured
  * beeper: at every Turn signal the beeper is activated, no time measurement.

* To start the Timer the button "Start" has to be pressed once.
* Now the App is ready for Turn signals from Base A and B.
* After 4 laps the flight time will be announced and recorded.
* The next run will start automatically.
* With pressing button "Reset" the time and counters will be resetted.
* With pressing button "List Rounds" the time for the last rounds are shown.

# range problems
In case of having range problems the the following items can be used:
* using a WiFi access point as a hotspot, e.g. Mikrotik wAP, which has several advantages
  * is suitable for outdoor use
  * can be powered by a 3s or 4s LiPo battery
* using a Raspberry Pi with an external WiFi antenna:
  * informations how to update the Pi can be found [here](https://geeks-r-us.de/2019/08/31/wlan-bluetooth-upgrade-fuer-den-rpi-4/)
  * already updated Pi can be bought [here](https://geeks-r-us.de/produkt/raspberry-pi-4-mit-u-fl-buchse/)
