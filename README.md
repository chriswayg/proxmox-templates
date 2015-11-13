# Proxmox LXC templates
Proxmox LXC Templates using DAB

### Create a minimal Debian Jessie Container Template:

Install DAB:

```
apt-get install dab
```

Clone the git repository:
```
git clone https://github.com/chriswayg/proxmox-templates.git
cd proxmox-templates/debian-8.2-minimal-64/
```

Create the template and cleanup the directory:
```
make
make clean
```

Shorten the name and move template into place (if using local storage):
```
mv debian-8.0-debian-8.2-minimal_8.2-1_amd64.tar.gz debian-8.2-minimal_8.2-1_amd64.tar.gz
mv debian-8.2-minimal_8.2-1_amd64.tar.gz /var/lib/vz/template/cache/
```

Then create a container based on this template in the Proxmox GUI or using `pct create `.

### References
- [Proxmox Linux Container](https://pve.proxmox.com/wiki/Linux_Container)
- [Proxmox Debian Appliance Builder](https://pve.proxmox.com/wiki/Debian_Appliance_Builder)
- [Proxmox Build your first DAB Appliance Template](https://pve.proxmox.com/wiki/Build_your_first_DAB_Appliance_Template)
- [Git Repo of Proxmox Templates](https://git.proxmox.com/?p=dab-pve-appliances.git;a=summary)
