# HTPublic
## This is the contents of the autostart file needed for HT Kiosks

OS of April 2020, Ver 10, Buster,  

To build Micro SD card, =>8GB, class 10, from blank install:

1. On a computer install the program RaspberryPi Imager from the RaspberryPi web site.

2. Run Imager to install the full 32bit Raspian OS onto a MicroSD, then

3. Insert MicroSD into RaspberryPi and power it up. (If it reboots during the initialization phase and does not display, wait 5 minutes and reboot) (Remove and insert power connector)

4. Follow directions on the screen to prepare the RaspberryPi system, setting location, WiFi (Might take a minute to connect) and update software (takes time). 

Upper and lower case matters.

5. Copy Instructions to RaspberryPi
a. Open a Terminal window on top left Launch Task bar
b. Enter the following: the $ sign is shown in the Terminal window, you enter everything after the $
i. $ git clone https://github.com/gsrobin99/HTPublic

c. Using File Manager on top left Launch Task bar
i. View, show hidden files visible
ii. Open folder HTPublic
iii. Open file HT_Kiosk_Instruc_V(n).txt

6. Create Folders
a. Using File Manager 
i. In .config  create      folder lxsession
ii. In lxsession create  folder LXDE-pi
iii. In LXDE-pi create new file      autostart 
iv. Open autostart using a text editor, right click on autostart
v. Copy autostart text below to file autostart 

@xscreensaver -no-splash
@~/.config/lxsession/LXDE-pi/autostart
@lxpanel --profile LXDE-pi
@pcmanfm --desktop --profile LXDE-pi
@point -rpi
@midori -e Fullscreen -a https://www.buildinglink.com 

7. Install programs on RaspberryPi
Follow instructions in the text and copy/paste commands as an aide to accuracy
a. Using the Terminal window: copy from text to terminal window, in editor Select text then Copy text, in Terminal window hold the CTRL + Shift + v keys to paste
b. $ sudo apt install xscreensaver  -y
c. $ sudo apt install midori  -y
d. $ sudo crontab -e  (Use nano editor), 
e. To cause RaspberryPi to Reboot @2am: Enter at $ without quotes
" * 2 * * * sudo /sbin/reboot now"
f. Ctrl O  to write file, Enter to say yes, ctrl x to exit

8. Reboot

a. Open Upper left Raspberry icon, select Logout at bottom of menu, then in window in center of screen select REBOOT

9. Setup Midori Browser to display BuildingLink screens
a. Move pointer to icon in upper right of browser screen which will reveal itself when the mouse pointer gets close. 
b. Click on icon that reduces screen to part of the display. 

b. The display should be Login screen, Login to BuildingLink with username and password below. Check box to remember username and password

9. Insert Preferences:

a. Upper left click on Raspberry icon, which drops a Menu  choose Preferences Raspberry Pi: 
i. Check wait for network and in interfaces check VNC then OK
b. click on Raspberry icon choose Screensaver in Mode choose disable, then Close

10. 
a. In upper right, left click on network icon, choose WiFi off,   Right click on network icon, choose Wireless & Wired Network Settings, eth0 and define ip address (10.1.10.n) to make it a static address. Get n from list below
b. Reboot and l
c. Once running, To switch to not full screen click icon in upper right of browser which will reveal itself when the mouse pointer gets close. To switch to full screen click on icon with arrows pointing to corners.

23 November 2020


