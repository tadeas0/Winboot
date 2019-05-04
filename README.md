# winboot
useful for dual boot setups

**Winboot** is a shell script that reboots directly into Windows from your Linux session, without having to select it from the grub menu. *For all those times you forget to do it and your grub timer runs out.*

Installation:
-
          1. Open up a terminal 
          
          2. Run the following commands:
                    
                    git clone https://github.com/semiismaili/Winboot.git
                    
                    cd Winboot
                    
                    chmod 755 winboot
                    
                    ./winboot -install
                    

Configuration Notes:
-
Winboot needs a little configuration change in /etc/default/grub to work:


    Step 1: Edit the grub configuration file by running: sudo gedit /etc/default/grub

    Step 2: Change the GRUB_DEFAULT parameter so it says GRUB_DEFAULT="saved" then save&exit

Disclaimer: 
-
  Winboot assumes Windows is the second entry on your grub menu (entry number 1, counting from 0), 
 if your setup is different, please run:
                             
           sudo winboot -set <your_windows_entry_number>

Usage:
-
          winboot (reboots to windows)
          
          winboot -h (brings this screen)
          
          winboot -update (updates to latest version from repository)
          
          winboot -install (initial one-time only installation)
          
          



