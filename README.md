# Easily install Arch linux  
This ansible playbook can easily install Arch linux  

# Before Using
- This ansible playbook only use UEFI system  
- This installation is dirty and is being improved

# Install
- Increase cowspace partition: ```mount -o remount,size=2G /run/archiso/cowspace```

- Install git and ansible: ```pacman -Sy git ansible```

- run playbook  
```
 $ git clone https://github.com/jon20/archlinux.git
 $ cd archlinux  
 $ ansible-playbook partitioning.yml  
```

- When installation over, next run playbook  
```
 $ arch-chroot /mnt /bin/bash  
 $ pacman -S git ansible  
 $ git clone https://github.com/jon20/archlinux.git
 $ cd archlinux
 $ ansible-playbook system_setting.yml
```  

- Reboot your PC  
```
 $ exit
 $ reboot
```
  