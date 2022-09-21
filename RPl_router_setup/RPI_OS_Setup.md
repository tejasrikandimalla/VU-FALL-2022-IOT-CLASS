Prerequisites Hardware:
Laptop 
Router 
Raspberry Pi B model
32GB SD card along with card reader

STEP 1:
Download the file extractor 7-zip using  https://www.7-zip.org for windows.
Download the SD card writer balenaEtcher using https://www.balena.io/etcher/

STEP 2:

EXTRACT THE DietPi Disk IMAGE:
1.	Download the Diet Pi Disc image using the link https://dietpi.com/downloads/images/DietPi_RPi-ARMv8-Bullseye.7z
2.	Then extract the DietPi bulleye (DietPi_RPi-ARMv8-Bullseye.7z) image using the file extractor 7-Zip.

FLASHING:
1.	Insert the SD Card to the laptop using Card reader.
2.	Next Open the balenaetcher.
3.	Select the dietpi image using the from the file button.
4.	Select Target card (SD card).
5.	Click Flash button.
6.	Wait until the validation is completed and a success of flash is popped up.
7.	Close balenaEtcher


![FLASH](https://user-images.githubusercontent.com/112652553/191414311-8341e124-49e2-4119-aeeb-ac77a3c1ceda.png)


CONFIGURATION:
1.	Open the SD Card drive in file explorer 
2.	Copy the dietpi.txt and dietpi-wifi.txt files to temporary folder for future use.
3.	Edit the configuration of dietpi-wifi.txt file with Wi-Fi credentials of router
                 aWIFI_SSID[0]=''
                 aWIFI_KEY[0]=''

4.	Edit the configuration of dietpi.txt file with below provide variables
              AUTO_SETUP_LOCALE=en_US.UTF-8
              AUTO_SETUP_KEYBOARD_LAYOUT=us
              AUTO_SETUP_TIMEZONE=America/New_York
              AUTO_SETUP_NET_ETHERNET_ENABLED=0
              AUTO_SETUP_NET_WIFI_ENABLED=1
              AUTO_SETUP_NET_WIFI_COUNTRY_CODE=US
              AUTO_SETUP_DHCP_TO_STATIC=1
              AUTO_SETUP_NET_HOSTNAME=DietPi_{YOUR_INITIALS}
              AUTO_SETUP_HEADLESS=1
              AUTO_SETUP_AUTOSTART_TARGET_INDEX=1
              SURVEY_OPTED_IN=0
              CONFIG_SERIAL_CONSOLE_ENABLE=1

5.	Save the diepi.txt and dietpi-wifi.txt files to save the changes made
6.	Eject the SD card

RASPBERRY Pi SETUP:
1.	Insert the SD Card into the raspberry pi and power the pi
2.	Wait until the flashing green light is stopped.
3.	Open the client section of the router admin website and copy the IP address of DietPi

CONFIGURATION OF DietPi:
1.	Open command prompt and enter the following commands
               ssh root@copiedIPAddress
               password: dietpi
2.	Next the default password is changed to user provided password 

 ![dietpi](https://user-images.githubusercontent.com/112652553/191415375-d7ba88e9-e52a-43a6-a03f-7882ddd93b99.png)
 
3.	The command prompt directs to Dietpi module.

![dietpi_install](https://user-images.githubusercontent.com/112652553/191415596-6c1357bb-2dff-4f80-9e12-6be0976d89f2.png)
