# Security-Analysis

Download Wireshark version 4.04, I have a Mac, so I downloaded macOS Intel 64-bit.dmg. I did try macOS Arm 64-bit.dmg but it did not work, so be sure to download the correct version for your device.

Packet Capture: 
When you open Wireshark, there are a bunch of interfaces, you don't need any privileged administrator access to capture live network data so 
just choose the WiFi interface. Immediately, Wireshark will start capturing data and you can click the red square on the top left to stop the capture. 
To resume click the shark tail icon and a pop up will come up and ask if you'd like to save the packet capture, this is entirely up to you but, 
in this instance I did not; so, I clicked 'continue without saving'. This is how you start and stop packet captures.

Create Columns:
For security analysis you want to have specific information on your Wireshark dashboard. What you can currently see is the packet number time source destination protocol length and extra info. This is good but not good enough for an analysis, from a security standpoint when you want to analyse you want to see the source IP and the destination port.
If you navigate to the User Datagram Protocol header you will see source port right click on source ports and click and apply it as a column. You will then see a source port column you can drag the column source port next to source to tidy up your Wireshark interface.
Another way to add a column is by right clicking anywhere and choosing column preferences you can click the + to add a column, name the column ‘dst_prt’ Click the drop down on number and select Destination Port. Drag your new column next to destination.
The time display on Wireshark is not the best so, click on view, click time display format then click UTC date and time of day.

<img width="1425" alt="Screenshot 2023-03-22 at 02 55 19" src="https://user-images.githubusercontent.com/105232776/227067895-370a5dfa-7edb-4060-b9a0-449ab0ef4c69.png">
<img width="819" alt="Screenshot 2023-03-22 at 02 57 34" src="https://user-images.githubusercontent.com/105232776/227067902-ba522b08-8e37-4dc0-95a6-1e233a9ed9f6.png">
<img width="817" alt="Screenshot 2023-03-22 at 02 59 16" src="https://user-images.githubusercontent.com/105232776/227067913-bd7daf86-a35f-4477-847b-2a61247fa3d4.png">
<img width="389" alt="Screenshot 2023-03-22 at 03 03 46" src="https://user-images.githubusercontent.com/105232776/227067922-a98fb28a-9ee7-482c-b6e8-e80ab1f21ee2.png">
<img width="262" alt="Screenshot 2023-03-23 at 00 40 58" src="https://user-images.githubusercontent.com/105232776/227069810-797c9695-5597-4cb5-b396-2a61ed0737f9.png">



Filtering Packets:

<img width="185" alt="Screenshot 2023-03-23 at 00 20 51" src="https://user-images.githubusercontent.com/105232776/227068010-fbe0a2bf-7cfa-4616-bb41-cf4f4972fa8f.png">
<img width="330" alt="Screenshot 2023-03-23 at 00 16 54" src="https://user-images.githubusercontent.com/105232776/227068001-50f5aebb-b782-46ec-9cee-4a0362b580a2.png">
<img width="319" alt="Screenshot 2023-03-23 at 00 32 21" src="https://user-images.githubusercontent.com/105232776/227068844-6bd5bd74-0bc6-4175-9707-ca28589a32f6.png">
<img width="313" alt="Screenshot 2023-03-23 at 00 35 12" src="https://user-images.githubusercontent.com/105232776/227069127-8b440d0d-9a68-4250-8e71-97d6ba9e96e2.png">
<img width="916" alt="Screenshot 2023-03-23 at 00 39 33" src="https://user-images.githubusercontent.com/105232776/227069629-6782336d-2309-4de0-8d7e-c3e3e61f57ad.png">




Nmap - Network Scanning
I tried to install Nmap on Ubuntu however I did not have the administrator privileges to run the $ sudo command. I ended up deleting my Ubuntu VM on VirtualBox and redownloading it to give me administrator privileges. However, this still did not work. I had to type into Terminal
1)	 $ su -i 

Which then opened the root file and I typed this in: 

2)	# usermod -aG sudo (username)

Type in your username without brackets!

3)	# reboot
4)	$ sudo -i
This finally gave me user privileges to install Nmap by running this command

$ sudo apt install nmap

Terminal will prompt you for password then begin downloading Nmap

<img width="699" alt="Screenshot 2023-03-31 at 09 59 27" src="https://user-images.githubusercontent.com/105232776/229292018-496aa2c6-faf3-4b9d-b242-351b13432f70.png">

<img width="922" alt="Screenshot 2023-03-31 at 09 59 14" src="https://user-images.githubusercontent.com/105232776/229292026-4ab51221-7cff-44fb-8b36-2d7d9b1cb0a2.png">

<img width="697" alt="Screenshot 2023-03-31 at 10 00 01" src="https://user-images.githubusercontent.com/105232776/229292043-378fa637-ba57-41ca-87c3-09395bf0dae0.png">




