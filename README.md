# CoreDNS container

Repo to store my coredns compose file<br>
Used at my tests labs

# Previous Steps

In Ubuntu 18.04, we need to disable the "local" dns resolver

Check the 53 port are listening
````bash
lsof -i :53
````
````bash
echo "DNS=1.1.1.1" >> /etc/systemd/resolved.conf
echo "DNSStubListener=no" >> /etc/systemd/resolved.conf
````
We need to reboot the instance
````bash
reboot
````
Re-check that the 53 port are not listening
````bash
lsof -i :53
````

# Configfiles

At `Corefile` we can indicate the DNS forwarding and the domains DNS records files.

The *.db file have all the DNS records for the desired domain

# License

<img src="./img/by-sa.png">

This work is under [Creative Commons Attribution-ShareAlike 4.0 International License](http://creativecommons.org/licenses/by-sa/4.0/).

Please read the [LICENSE](LICENSE) file for more details.
