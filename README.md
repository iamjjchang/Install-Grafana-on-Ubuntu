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

