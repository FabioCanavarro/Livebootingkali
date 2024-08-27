# Livebootingkali
liveboot kali for beginner


Getting started
requirement
1. A usb with minimum 8 gb memory card
2. a computer
3. Internet connection



1. Get balena ethcer at https://www.balena.io/etcher
or
1. Get rufus on https://rufus.ie/
3. go to https://www.kali.org/get-kali/#kali-live to get the live boot image of kali
![image](https://github.com/user-attachments/assets/e279d51d-bf17-421d-97f7-cad5a06cda90)

Live boot everything
1. Use any vpn and download Free download manager, since it is a torrent
2. download the torrent
3. open rufus or balena ethcer
4. select the iso and the usb you want to liveboot in
5. Press start and wait for it to finish
   ![image](https://github.com/user-attachments/assets/69d45d50-b672-4262-afbd-0e81346b31ac)

# i used BalenaEtcher
6. restart your laptop and go to bios(hold f2 for Asus laptop)
7. go to advanced option and security and disable secure boot
8. go to the homepage and change the position of window and the usb
9. save changes and exit
10. Enjoy

How to exit?
1. restart
2. go to bios
3. change position of usb and windows
easier
1. restart, before it starts back pull out the usb



PERSISTENCE
1. go to live boot with persistence, press enter
2. go to terminal
3. make a variable to make things easier
   `usb=/dev/wrapper #(change the wrapper)
   sudo fdisk $usb <<< $(printf "n\np\n\n\n\nw")
   sudo mkfs.ext4 -L persistence ${usb}3    #change to ext3 if error
   sudo mkdir -p /mnt/my_usb
   sudo mount ${usb}3 /mnt/my_usb
   echo "/ union" | sudo tee /mnt/my_usb/persistence.conf
   sudo umount ${usb}3`
4. make a text document
5. restart
6. check if its there



