**Mojahedabdo/MOja-MoRaL-** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ... 
- 😄 Pronouns: ...
- ⚡ Fun fact: ...

## Install Visual Studio Code

Below are official install instructions for Visual Studio Code on common Linux distributions. Follow the section for your distribution.

### RHEL / CentOS / Fedora (dnf)

```bash
sudo rpm --import https://packages.microsoft.com/keys/microsoft.asc
sudo sh -c 'cat > /etc/yum.repos.d/vscode.repo <<EOF
[code]
name=Visual Studio Code
baseurl=https://packages.microsoft.com/yumrepos/vscode
enabled=1
gpgcheck=1
gpgkey=https://packages.microsoft.com/keys/microsoft.asc
EOF'
sudo dnf check-update
sudo dnf install -y code
```

### Debian / Ubuntu (apt)

```bash
# Import the Microsoft GPG key and add the repository
wget -qO- https://packages.microsoft.com/keys/microsoft.asc | gpg --dearmor > packages.microsoft.gpg
sudo install -o root -g root -m 644 packages.microsoft.gpg /usr/share/keyrings/
sudo sh -c 'echo "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/packages.microsoft.gpg] https://packages.microsoft.com/ubuntu/ $(lsb_release -cs) main" > /etc/apt/sources.list.d/vscode.list'

# Update and install
sudo apt update
sudo apt install -y code

# Cleanup
rm packages.microsoft.gpg
```

Notes: if gpg is not available on the machine, install gnupg (sudo apt install -y gnupg) first.

### openSUSE (zypper)

```bash
sudo rpm --import https://packages.microsoft.com/keys/microsoft.asc
sudo zypper addrepo --check --name 'vscode' https://packages.microsoft.com/yumrepos/vscode vscode
sudo zypper refresh
sudo zypper install -y code
```

Notes:
- The RHEL/CentOS/Fedora instructions use dnf. The Debian/Ubuntu instructions use apt. The openSUSE instructions use zypper.
- If you want additions (Flatpak/Snap, or instructions for older distro releases), tell me which target and I will update the README.
