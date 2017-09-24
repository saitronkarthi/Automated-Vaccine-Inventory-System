# Automated-Vaccine-Inventory-System
Hardware:
1.	Raspberry pi 2
2.	Edimax  wifi dongle
3.	DYMO Digital Postal Scale / Shipping Scale, 10-pound (USB)
4.	AWS Tide dash button
5.	CC2650 STK TI SensorTag
6.	CC-DEVPACK-DEBUG-SimpleLink SensorTag Debugger DevPack
Connections:
1.	Dymo scale connected to Raspberry Pi USB port.
Software setup:
1.	Raspberry pi 2
In sudo nano /etc/rc.local insert the start up scripts so that it runs on boot up.
sudo python /home/pi/usbscaleMC1.py &
sudo python /home/pi/aws-V1-dashbutton.py &
sudo python /home/pi/emailsms-weightlog.py &
sudo python /home/pi/emailsms-dashbutton.py &

2.	In aws RDS create the tables & store procedure objects
3.	In aws ec2 host the application
4.	The sensortag is programmed to broadcast the aws ec2 url.
5.	Code composer studio IDE for programming the SensorTag 
6.	The SensorTag BLE project is to be modified as Sensortag.c file attached in this project


