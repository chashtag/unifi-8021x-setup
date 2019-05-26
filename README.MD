# Unifi files for WAN networks requiring 802.1x
- config/wpa_supplicant.conf: Sample wpa_supplicant config file
- etc/init.d/wpa_supplicant: Service file
- var/lib/unifi/sites/\<your site name\>/config.gateway.json: Gateway interface override

--- 
deb file comes from
https://community.ubnt.com/ubnt/attachments/ubnt/EdgeMAX/235525/1/wpasupplicant_2.6-21~bpo9+1_mips.deb.tar.gz

Before installing add the required repos to the USG to fulfill dependencies
```
configure
set system package repository wheezy components 'main contrib non-free' 
set system package repository wheezy distribution wheezy 
set system package repository wheezy url http://archive.debian.org/debian
commit; save
sudo apt-get update
```
