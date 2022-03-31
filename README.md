# roger-skyline-1

## Mandatory Part

### V.2 VM Part
- My choice for the Virtual Machine's Linux OS is **Debian** as it was used in the previous project [init](https://github.com/peetuskytta/init)
- Hypervisor: VirtualBox
- Debian --> [debian-11.2.0-amd64-netinst.iso](https://www.debian.org/download) (direct download)

#### VM specs:
✅ A disk size of 8 GB.

✅ Have at least one 4.2 GB partition which I chose *primary* and mounted on `/` and 4.4 GB partition as *logical* mounted on `/home`

✅ Packages up to date and installed to meet the demands of the project. Use the command below:
  
```
apt-get update -y && apt-get upgrade -y
```

I want to have sudo and vim so I installed them with the command below:
```
apt install vim && apt install sudo
```

### V.3 Network and Security Part
For the network on your VM, here are the steps to achieve:
- [ ] You must create a non-root user to connect to the machine and work.
- [ ] Use sudo, with this user, to be able to perform operation requiring special rights.
- [ ] We don’t want you to use the DHCP service of your machine. You’ve got to configure it to have a static IP and a Netmask in \30.
- [ ] You have to change the default port of the SSH service by the one of your choice. SSH access HAS TO be done with publickeys. SSH root access SHOULD NOT be allowed directly, but with a user who can be root.
- [ ] You have to set the rules of your firewall on your server only with the services used outside the VM.
- [ ] You have to set a DOS (Denial Of Service Attack) protection on your open ports of your VM.
- [ ] You have to set a protection against scans on your VM’s open ports.
- [ ] Stop the services you don’t need for this project.
- [ ] Create a script that updates all the sources of package, then your packages and which logs the whole in a file named /var/log/update_script.log. Create a scheduled task for this script once a week at 4AM and every time the machine reboots.
- [ ] Make a script to monitor changes of the /etc/crontab file and sends an email to root if it has been modified. Create a scheduled script task every day at midnight.

