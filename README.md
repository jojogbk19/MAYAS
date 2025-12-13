jogbk19/jojogbk19** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile
Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ... 
- 😄 Pronouns: ...
- ⚡ Fun fact: ...

Install Visual Studio Code (RHEL / CentOS / Fedora — dnf)

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

Notes:
- The above instructions target RHEL/CentOS/Fedora systems using dnf. If you use openSUSE (zypper) or Debian/Ubuntu (apt) let me know and I will update the instructions accordingly.
