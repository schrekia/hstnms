##Links providing *hosts* files

Updated `hosts` files from the following locations are always unified and included:

* Peter Lowe at [https://pgl.yoyo.org/adservers/](https://pgl.yoyo.org/adservers/), updated regularly.
  -- **DL** [https://pgl.yoyo.org/adservers/serverlist.php?hostformat=hosts&mimetype=plaintext&useip=0]()
* The [Adaway hosts file](https://adaway.org/hosts.txt), updated regularly.
  -- **DL** [https://adaway.org/hosts.txt]()
* MVPs.org Hosts file at [http://winhelp2002.mvps.org/hosts.htm](http://winhelp2002.mvps.org/hosts.htm), updated
monthly, or thereabouts.
  -- **DL** [http://winhelp2002.mvps.org/hosts.txt]()
* Dan Pollock at [http://someonewhocares.org/hosts/](http://someonewhocares.org/hosts/) updated regularly.
  -- **DL** [http://someonewhocares.org/hosts/zero/hosts]()
* Malware Domain List at [https://www.malwaredomainlist.com/](https://www.malwaredomainlist.com/), updated regularly.
  -- **DL** [https://www.malwaredomainlist.com/hostslist/hosts.txt]()
* Spotify ads [here](https://raw.githubusercontent.com/StevenBlack/hosts/master/data/SpotifyAds/hosts).
  -- **DL** [https://raw.githubusercontent.com/StevenBlack/hosts/master/data/SpotifyAds/hosts]()
* Block Windows 10 tracking.
  -- **DL** [https://raw.githubusercontent.com/WindowsLies/BlockWindows/master/hosts]()
  -- **DL** [https://raw.githubusercontent.com/tyzbit/hosts/master/data/tyzbit/hosts]()
* Cameleon ads list at [http://sysctl.org/cameleon/](http://sysctl.org/cameleon/hosts).
  -- **DL** [http://sysctl.org/cameleon/hosts]()
* Hosts-file.net ad blocking servers [https://hosts-file.net/](https://hosts-file.net/), updated regularly.
  -- **DL** [https://hosts-file.net/ad_servers.txt]()
* Ads blocking [here](https://github.com/nomadturk/vpn-adblock).
  -- **DL** [extra advertising domains](https://raw.githubusercontent.com/nomadturk/vpn-adblock/9a5c01eb1b3354388e8f4dd8450f27638b632a64/hosts-sources/Turkish/hosts)
* Large hosts file [https://hostsfile.mine.nu/](https://hostsfile.mine.nu/).
  -- **DL** [https://hostsfile.mine.nu/hosts0.txt]()
* Large list including ads, tracking, etc. domains [https://github.com/notracking/hosts-blocklists/](https://github.com/notracking/hosts-blocklists/).
  -- **DL** [https://raw.githubusercontent.com/notracking/hosts-blocklists/master/hostnames.txt]()
* Depformation hosts list.
  -- **DL** [domains list](https://raw.githubusercontent.com/vavavr00m/dephormation/0406637355b328086145871dfe67898d27425ecd/host.txt)
* Adzhosts list at [https://sourceforge.net/projects/adzhosts/](https://sourceforge.net/projects/adzhosts/).
  -- **DL** [http://netcologne.dl.sourceforge.net/project/adzhosts/0.0.0.0/HOSTS.txt]()



## Location of hosts file
To modify your current `hosts` file, look for it in the following places and modify it with a text
editor.

**Mac OS X, iOS, Android, Linux**: `/etc/hosts` folder.

**Windows**: `%SystemRoot%\system32\drivers\etc\hosts` folder.

## Reloading hosts file
Your operating system will cache DNS lookups. You can either reboot or run the following commands to
manually flush your DNS cache once the new hosts file is in place.

### Mac OS X
Open a Terminal and run:
```
sudo dscacheutil -flushcache; sudo killall -HUP mDNSResponder
```

### Linux
Open a Terminal and run with root privileges:

**Debian/Ubuntu** `sudo /etc/rc.d/init.d/nscd restart`

**Linux with systemd**: `sudo systemctl restart network.service`

**Fedora Linux**: `sudo systemctl restart NetworkManager.service`

**Arch Linux/Manjaro with Network Manager**: `sudo systemctl restart NetworkManager.service`

**Arch Linux/Manjaro with Wicd**: `sudo systemctl restart wicd.service`

**Others**: Consult [this wikipedia article](https://en.wikipedia.org/wiki/Hosts_%28file%29#Location_in_the_file_system).
