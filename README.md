# Ubuntu Virtual Machine - UTM Lab on MacOS

This project document my **home lab setup** of Ubuntu running inside a virtual machine on MacOS using [UTM](https://mac.getutm.appmac.). 
The main goal of this lab is to practice Linux system administration and IT support tasks, and showcase my technocal skills in a practical way. 

---
##Screenshots
| Task | Screenshot |
|------|-----------|
|Checking hostname|[Show hostname](images/hostname.png)|
|Checking OS information|[Show OS Info](images/os_info.png)|
|Creating new user|[Creating new user step](images/new_user.png)|
|Permission setting|[Set permissions for a new file](images/user_permission.png)|
|Checking all network interfaces and IP adresses|[Show IP network information](images/ip_a.png)|
|Checking routing table|[Show routing table](images/ip_route.png)|
|Installing Interactive system monitor|[Htop installing steps](images/htop.png)|
|Testing htop|[Running htop in terminal](images/ran_htop.png)|
|Apache2 installation|[Apache2 installing step](images/apache2.png)|
|Testing Apache2 in browser|[Running Apache2 in browser](images/apache2_test.png)|

---

## Lab Setup
- **Host machine:** macOS (MacBook Pro 16Gb M2)
- **Virtualisation tool:** UTM
- **Guest OS:** Ubuntu 25.04 ARM64 bit Arcitecture
- **Allocated resources:** 4Gb RAM, 4 Cores CPU, 30Gb Storage


---

## Tasks Completed

- Updated and upgrated packages:
```bash
sudo apt update && sudo apt upgrade -y
```

- Created and managed permission for a new user:
```bash
sudo adduser simon_it_dep
su - simon_it_dep
mkdir ~/firstdir
cd firstdir
touch firstfile.txt
sudo chmod 744 firstfile.txt
```

- Check Networking
```bash
ip a
ip route
ping -c 5 google.com
```

- Installed and ran a package and service
```bash
sudo apt install htop -y
htop
sudo apt install apache2 -y
sudo systemctl status apache2
```

- Installed and configured Git and VS code
```bash
sudo snap install code --classic #didn't work for this arcitecture so i downloaded directly the package from the site
wget https:..update.code.visualstudio.com/latest/linux-deb-arm64/stable -O vscode-arm64.deb
sudo install apt install ./vscode-arm64.deb
rm vscode-arm64.deb
mkdir ~/ubuntu_vm
cd ~/ubuntu_vm
touch README.md
code .
```

- Documented everything and pushed to my Git Repository 
```bash
git add.
git commit -m 'Initial commit: Ubuntu VM lab'
git branch -M main
git remote add origin https://github.com/zhuzumA/ubuntu_vm.git
git push -u origin main
```
