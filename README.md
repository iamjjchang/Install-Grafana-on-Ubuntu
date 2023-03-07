# Install Grafana on Ubuntu 22.04 LTS

## Installation prerequisite

Get the latest version of Grafana

[Official Grafana Download Page](https://grafana.com/grafana/download?platform=linux)


```
sudo apt-get install -y adduser libfontconfig1
```

Download Grafana for Linux 
```
wget https://dl.grafana.com/enterprise/release/grafana-enterprise_9.4.3_amd64.deb
```

Install Grafana
```
sudo dpkg -i grafana-enterprise_9.4.3_amd64.deb
```

Start Grafana
```
systemctl start grafana-server
```

Check status of Grafana
```
systemctl status grafana-server
```

Additional Plugins to install
```
grafana-cli plugins install grafana-piechart-panel
grafana-cli plugins install fifemon-graphql-datasource
grafana-cli plugins install grafana-worldmap-panel
```

## Uninstall Grafana

The parameter `remove` will remove installation files while keeping configuration data.

```
sudo apt-get remove grafana 
```

**Uninstall grafana including dependent package** \
If you would like to remove grafana and it's dependent packages which are no longer needed from Ubuntu
```
sudo apt-get remove --auto-remove grafana 
```

**Purging grafana** \
We instruct apt-get to remove configuration files
```
sudo apt-get purge grafana 
```

If you use purge options along with auto remove, will be removed everything regarding the package, It's really useful when you want to reinstall again.
```
sudo apt-get purge --auto-remove grafana 
```