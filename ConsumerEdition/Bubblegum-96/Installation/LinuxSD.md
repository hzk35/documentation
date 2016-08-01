## How to flash Debian on Bubblegum-96 with SD card
---

This section show how to install an operating system to your Bubblegum-96 using the SD Card method on a Linux host computer. **This method will require an SD card with at least 4GB of storage**.

***

- **Step 1**: Download the compressed SD image and decompress it.  
- **Step 2**: Create the SD card **(>4G)**
- **Step 3**: Flash your Bubblegum-96 board
- **Step 4**: Reboot Bubblegum-96

***

###Step1. Dowload the compressed SD image and decompress it.
You need to download the compressed `sd-burn.img.gz` from:  

*Link: [https://pan.baidu.com/s/1c2Hnc3Y](https://pan.baidu.com/s/1c2Hnc3Y)  
Password:* tt5a  

Decompress it with following command:  
`$ gzip -dk sd-burn.img.gz`  

### Step 2: Create the SD card
In this step, please choose the one of two methods depending on your host PC(Linux or Windows).  

**Linux Host**

`$ cd folder`  
`# folder is where you saved the image`  
`$ lsblk`  
`# Find your SD card device. eg. /dev/sdx`  
`$ sudo dd if=sd-burn.img of=/dev/sdx bs=32M`  
`# dd img to the whole sd card. It will take about 6mins`  

### Step3: Flash your Bubblegum-96 board.  
1. Insert your SD card into Bubblegum
2. Boot from SD card:  
1 Press ADFU key for **5 seconds**  
2 Power on **without releasing ADFU key**  
3 Continue pressing ADFU key for **3 seconds**  
3. This Bubblegum will boot from SD card. The LEDs between USB2.0 and USB3.0 will be turned on after 10 seconds.  
4. The bashes will run and flash board automatically. It will take about 6mins.
5. The LEDs between USB2.0 and USB3.0 will be turned off once flashing finished.

### Step4: Reboot Bubblegum-96
Press "reset" key, and the board will reboot into Debian.