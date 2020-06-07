# pi-setup
Raspberry Pi Raspbian headless setup automation script.

My automation for creating headless setups on Ubuntu for Raspbian (including Lite).
```
git clone git@github.com:deive/pi-setup.git
cd pi-setup
chmod +x pi-setup
./pi-setup
```
I have commented some of the script so please read before running! This requires root access (and will ask for it).

Features:
1. Enable SSH
2. Enable and bind WiFi (with encrypted passphrase)
    - On desktop first run wizard, you can skip the WiFi section as the pi is already connected
    - On Lite, the startup wizard doesn't run, so the WiFi continues to be blocked by rfkill (even though the country is set). You will need to run `rfkill unblock wlan` and then reboot.
3. Set hostname
4. Update pi user password (with encryption)
    - On desktop first run wizard, you can just click next with an empty password as this is already updated.
5. Set fixed IP for ethernet
6. Setup Bridging from internal ethernet clients to external WiFi (with dnsmasq)

You can use a config file for the values, instead of the interactive shell:
```
mv pi_setup.config.example pi_setup.config
nano pi_setup.config
```
