# Infinity Node Bootstrap
In case you need to quickly sync the blockchain of your Infinity Node or linux wallet, follow the steps below:

```bash
# stop infinity node
sudo systemctl stop sinovate.service

# install unzip package
sudo apt update && sudo apt install unzip

# remove old files and folders
rm -rf ~/.sin/{blocks,chainstate,debug.log,mnpayments.dat,mncache.dat,banlist.dat,peers.dat,netfulfilled.dat,governance.dat,fee_estimates.dat}

# download bootstrap archive
# please check the latest version available at github replacing the bootstrap URL from the command below:
# https://github.com/SINOVATEblockchain/SIN-core/releases/latest
wget -O ~/bootstrap.zip https://github.com/SINOVATEblockchain/SIN-core/releases/download/ec78b3b/bootstrap.02.01.2020.zip

# unzip the bootstrap archive
unzip ~/bootstrap.zip

# move bootstrap files
mv -t ~/.sin ~/bootstrap/blocks ~/bootstrap/chainstate

# remove unnecessary files
rm -rf ~/{bootstrap,bootstrap.zip}

# reboot infinitynode
sudo reboot
```
