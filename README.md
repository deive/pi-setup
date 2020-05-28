# pi-setup
Raspberry Pi Raspbian headless setup automation script.

My automation for creating headless setups on Ubuntu for Raspbian (including Lite).
```
git clone git@github.com:deive/pi-setup.git
cd pi-setup
chmod +x pi-setup
./pi-setup
```
This requires root access (and will ask for it)

I have commented some of the script so please read before running!
1. Enable SSH
2. Enable and bind WiFi (with encrypted passphrase)
3. Set hostname
4. Update pi user password (with encryption)

You can use a config file for the values, instead of the interactive shell:
```
mv pi_setup.config.example pi_setup.config
nano pi_setup.config
```
