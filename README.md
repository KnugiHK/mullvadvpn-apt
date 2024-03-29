# mullvadvpn-apt
# The repository is moved to https://github.com/GHaaAPT/mullvadvpn-apt
Unofficial APT repository for [MullvadVPN](https://github.com/mullvad/mullvadvpn-app) that will check for updates regularly

EZ update your Mullvad VPN Debian/Ubuntu client

I do this for myself, but if you want to use it, feel free to audit this repo first and you are strongly recommended to do so.

# Install as APT repo manually
```shell
sudo apt remove mullvad-vpn # if you installed the vpn client through deb file already, uninstall first.
```
```shell
wget -qO- https://ghaaapt.github.io/mullvadvpn-apt/mullvad-vpn-archive-keyring.asc | gpg --dearmor | sudo tee /usr/share/keyrings/mullvad-vpn-archive-keyring.gpg > /dev/null
```
```shell
echo 'deb [arch=amd64 signed-by=/usr/share/keyrings/mullvad-vpn-archive-keyring.gpg] https://ghaaapt.github.io/mullvadvpn-apt/ stable main' | sudo tee /etc/apt/sources.list.d/mullvad-vpn.list
```
```shell
sudo apt update && sudo apt install mullvad-vpn -y
```

# Install as APT repo automatically
```shell
wget -q https://ghaaapt.github.io/mullvadvpn-apt/install_mullvad_vpn.sh && sudo bash ./install_mullvad_vpn.sh
```

# Checksum
1b707891bfae82e918b42547dc71c8e37bb79fd1b4757e96c98500dd7fec67ea  pool/main/m/mullvad-vpn/mullvad-vpn_2022.5_amd64.deb

# Copyright
The Mullvad VPN installer (deb file) is re-distributed in GPLv3
